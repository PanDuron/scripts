#!/bin/bash
while :
do 
clear
echo -en "\e[96m"
figlet +++ Buscar
echo -en "\e[97m"
figlet HostFree +++
echo ""
echo -en "\e[96mCreate By: ┣━━PanDuron-Pr1nce.€x€-F@br1x━━┫"
echo ""
echo ""
echo ""
echo -en "\e[91m[ 1 ]\e[97m••••••••\e[96mBuscar HostFree"
echo ""
echo ""
echo -en "\e[92m[ 2 ]\e[96m••••••••\e[95mESCANEAR PUERTOS"
echo ""
echo ""
echo -en "\e[95m[ 3 ]\e[93m••••••••\e[94mIP GEOLOCALIZACION"
echo ""
echo ""
echo -en "\e[97m[ 4 ]\e[92m••••••••\e[93mCHECKEAR ESTATUS DEL HOST"
echo ""
echo ""
echo -en "\e[92m[ 5 ]\e[95m••••••••\e[91mINFORMACION DE SCRIPT"
echo ""
echo ""
echo -en "\e[91m[ 0 ]\e[94m••••••••\e[97mSALIR DEL SCRIPT"
echo ""
echo ""
echo -en -n "\e[96mSELECIONE SU OPCION : "
read opcion
case $opcion in
1)clear
echo -en "\e[97m"
figlet BUSCADOR
echo -en "\e[96m"
figlet DE HOST
echo -en -n "\e[95mINGRESE EL HOST : "
echo -en "\e[96m"
read host
echo ""
sleep 2
echo -en "\e[92mBUSCANDO HOSTS...."
sleep 2
echo ""
echo ""
sleep 2
echo -en "\e[96mLISTO :D!"
echo ""
echo ""
curl http://api.hackertarget.com/hostsearch/?q=$host
sleep 2
echo ""
echo ""
echo -en "\e[91mPRESIONE ENTER PARA CONTINUAR"
read foo
;;
2)clear
echo -en "\e[97m"
figlet ESCANEAR
echo -en "\e[96m"
figlet PUERTOS
echo -en -n "\e[95mINGRESE SU HOST : "
echo -en "\e[96m"
read host
echo ""
sleep 2
echo -en "\e[92mESCANEANDO PUERTOS DEL HOST..."
echo ""
sleep 2
echo ""
echo -en "\e[96mLISTO :D!"
echo ""
echo ""
curl http://api.hackertarget.com/nmap/?q=$host
sleep 2
echo ""
sleep 2
echo -en "\e[91mPRESIONE ENTER PARA CONTINUAR"
read foo
;;
3)clear
echo -en "\e[97m"
figlet CHECKEAR
echo -en "\e[96m"
figlet GEO IP
echo -en -n "\e[95mINGRESE EL IP/HOST : "
echo -en "\e[96m"
read host
echo ""
sleep 2
echo -en "\e[92mBUSCANDO GEOLOCALIZACION DEL HOST...."
echo ""
echo ""
sleep 2
echo -en "\e[96mLISTO :D!"
echo ""
echo ""
curl http://api.hackertarget.com/geoip/?q=$host
sleep 2
echo ""
echo ""
echo -en "\e[91mPRESIONE ENTER PARA CONTINUAR"
read foo
;;
4)clear
echo -en "\e[97m"
figlet ESTATUS
echo -en "\e[96m"
figlet DEL HOST
echo -en -n "\e[95mINGRESE SU HOST : "
echo -en "\e[96m"
read host
echo ""
sleep 2
echo -en "\e[92mCOMPROBANDO ESTATUS DEL HOST INGRESADO...."
echo ""
sleep 2
echo ""
echo -en "\e[96mLISTO :D!"
echo ""
echo ""
curl http://api.hackertarget.com/httpheaders/?q=$host
sleep 2
echo ""
echo -en "\e[91mPRESIONE ENTER PARA CONTINUAR"
read foo
;;
5)clear
echo -en "\e[96m"
figlet CREDITOS
echo ""
echo -en "\e[95mLEYENDO...."
echo ""
echo ""
sleep 2
echo -en "\e[96mLISTO :D!"
echo ""
echo ""
sleep 2
cat creditos.txt
echo ""
echo -en "\e[91mPRESIONE ENTER PARA CONTINUAR"
read foo
;;
0)clear
echo -en "\e[96m"
figlet EXIT....
echo ""
echo -en "\e[95mCERRANDO EL SCRIPT...."
echo ""
echo ""
sleep 2
echo -en "\e[92mESPERE...."
echo ""
echo ""
sleep 2
echo -en "\e[96mLISTO :D!"
sleep 2
clear
echo -en "\e[97m"
ls
exit 0
;;
*)clear
echo -en "\e[96m"
figlet UPS....
echo ""
echo -en "\e[95mCOMANDO INVALIDO :("
echo ""
echo ""
sleep 2
echo -en "\e[92mREINICIANDO SCRIPT...."
echo ""
echo ""
sleep 2
echo -en "\e[96mLISTO :D"
sleep 2
bash host.sh
;;
esac
done
echo -en "\e[97m"
