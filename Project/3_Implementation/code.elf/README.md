
#define F_CPU 8000000UL

#include <avr/io.h>

#include <avr/interrupt.h>

#include <util/delay.h>

#include "4bit_lcdlib.h"

volatile uint8_t Direction = 0; 



void ADC_init()

{

	DDRA=0X00;
	
	ADCSRA=0X87;
	
	ADMUX=0X40;
	
}

ISR(INT0_vect)

{

	Direction=~Direction;
	
	_delay_ms(100);
	
}

int adc_read(int channel)

{

	ADMUX=0x40|(channel & 0x07);
	
	ADCSRA|=(1<<ADSC);
	
	while((ADCSRA & ADIF)==0);
	
	ADCSRA|=(1<<ADIF);
	
	return ADCW;
	
}

int main(void)

{

	LCD_Init();
	
	unsigned int x=0,y=0;
	
	DDRC=0x03;
	
	DDRB|=(1<<3);
	
	DDRD&=~(1<<2);
	
	GICR = 0X40;
	
	MCUCR=(1<<ISC00)|(1<<ISC01);
	
	sei();
	
	ADC_init();
	
	TCNT0=0;
	
	TCCR0=(1<<WGM00)|(1<<WGM01)|(1<<CS01)|(1<<CS00)|(1<<COM01);
	
	lcd_gotoxy(1,1);
	
	LCD_String("Speed Detector:");
	
	lcd_gotoxy(1,2);
	
    while(1)
    
    {
    
		LCD_String("Speed= ");
		
		if(Direction!=0)
		
		{
		
			PORTC=0x01;
			
		}
		
		else
		
		{
		
			PORTC=0x02;
			
        //TODO:: Please write your application code 
	
		}
		
		x=adc_read(0);
		
		OCR0=(adc_read(0));
		
		lcd_display_int(x/10);
		
		LCD_String("Km/hr");
		
		_delay_ms(500);
		
		LCD_Clear();
		
		lcd_gotoxy(1,1);
		
		y=x/10;
		
		if(y>60)
		
		{
		
			LCD_String("Speed > 60");
			
			lcd_gotoxy(1,2);
			
			LCD_String("Reduce Speed");
			
			_delay_ms(2000);
			
		}
		
		LCD_Clear();
		
    }
    
}

