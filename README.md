# python3
# a quick & basic way to change your mac address
# more advance python programs coming soon! 
import subprocess

interface = input ("interface > ")
new_mac = input("new MAC > ")


print("[+] Changing MAC address for " + interface + " to " + new_mac )

subprocess.call(["ifconfig " + interface + " down ", shell=True)
subprocess.call(["ifconfig " + interface + " hw ether " + new_mac, shell=True)
subprocess.call(["ifconfig " + interface + " up ", shell=True)
