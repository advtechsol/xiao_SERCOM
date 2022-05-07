# xiao_SERCOM
SERCOM

// Serial2 pin and pad definitions (in Arduino files Variant.h & Variant.cpp)  
#define PIN_SERIAL2_RX       (5u)               // Pin description number for PIO_SERCOM on D12  
#define PIN_SERIAL2_TX       (4u)               // Pin description number for PIO_SERCOM on D10  
#define PAD_SERIAL2_TX       (UART_TX_PAD_0)      // SERCOM pad 2 (SC1PAD2)  
#define PAD_SERIAL2_RX       (SERCOM_RX_PAD_1)    // SERCOM pad 3 (SC1PAD3)  
// Instantiate the Serial2 class  
Uart Serial2(&sercom2, PIN_SERIAL2_RX, PIN_SERIAL2_TX, PAD_SERIAL2_RX, PAD_SERIAL2_TX);  

void SERCOM2_Handler()  
{  
Serial2.IrqHandler();  
}  
