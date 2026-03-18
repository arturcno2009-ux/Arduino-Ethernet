# Arduino-Ethernet
Rede de internet entre o reteador  e o arduino
/**
Arduino Etnhernet
 @author Artur correia 
*/

// As linhas abaixo usam as bliotecas do modulo Ethernet
// Obs: Este modulo usa os pinos 4,10,11,12, e 13
#include <SPI.h>
#include <Ethernet.h>

// Gerar o mac ADORESS (https://ssl.crox.net/arduinomac)
byte mac(6) = { 0x90, 0xA2, 0xDA, 0x1d, 0x99, 0xFF};

// Instanciar o servidor
EthernetServer server(80); //80 porta http

void setup() {
 Serial.begin(9600);
 // A linha abaixo configura a placa de rede como DHCP
 Ethernet.begin(mac);
 // A linha abaixo inicia o servidor 
server.begin();
// Exibir as configuraçoes da rede 
Serial.println("Arduino Ethernet Sheield")
Serial.print("IP: ");
Serial.println(Ethernet.localIP)(); //exibir a mascara de rede 
Serial.print("Gateway: ")
Serial.print(Ethernt.gatawaIP)(); //exibir a gatewayv a rede 
Serial.print("DNS: ");
Serial.println(Ethernet.dnsServerIP)(); //exiibir o DNS
}

void loop() {
 

}
