# qrcode-generator
#This is basically a qr code generator.

import qrcode
import pyfiglet
from os import system ,name
from time import sleep
def curent_working_dir():
	if name == 'nt':
		_ = system('cd')
	else:
		_ = system('pwd')
def tool_code():
    print("")
    print("")
    things=str(input("Enter (URL/Text/) : "))
    img=qrcode.make(things)
    name=str(input("Enter name of file : "))
    print("QRCODE_GENERATING PLEASE WAIT.....")
    sleep(5)
    img.save(name)
    print("Done...")
    sleep(3)
    print(" ")
    print(" ")
    print("Your file is saved in the following path")


def banner_for_qr():
    print("   =====================================================================================")
    ascii_banner = pyfiglet.figlet_format("      QR_GENERATOR")
    
    print(ascii_banner)
    print("                                      Aurthor---->Sajawal Khan Sadozai")
    print("   =====================================================================================")
def clear():
	if name == 'nt':
		_ = system('cls')
	else:
		_ = system('clear')
sleep(5)
clear()
print("QRCODE STARTING PLEASE WAIT....")
sleep(5)
clear()
banner_for_qr()
tool_code()
print("=======================")
curent_working_dir()
print("=======================")
