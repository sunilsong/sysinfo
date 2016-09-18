#!/bin/bash
ctim=$(date | awk '{print $4}')
cdat=$(date +%D)
hstnm=$(hostname)
uptim=$(uptime -p | sed 's/up//' | sed 's/hour/hr/' | sed 's/minutes/mins/')
ttlmem=$(free -h | grep Mem | awk '{print $2}')
fremem=$(free -h | grep Mem | awk '{print $7}')
cpufree=$(mpstat | grep all | awk '{print $13}')
ttlusrs=$(cat /etc/passwd | wc -l)
dskusa=$(df -h | grep /dev/sda1 | awk '{print $5}')

echo "-----------------------------------------------------------------"
echo "*************************# SYSTEM REPORT #***********************"
echo "-----------------------------------------------------------------"
echo "-----------------------------------------------------------------"
echo "Date: $cdat          Time: $ctim          System: $hstnm         " 
echo "-----------------------------------------------------------------"
echo "Uptime:$uptim  Memory Free: $fremem/$ttlmem  CPU Free: $cpufree % "
echo "-----------------------------------------------------------------"
echo "Total Users:$ttlusrs              Total Disk Usage: $dskusa" 
echo "-----------------------------------------------------------------"
echo "-----------------------*# END OF REPORT #*-----------------------"
echo "-----------------------------------------------------------------"
