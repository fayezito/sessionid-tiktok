
import requests, random, string

print("""

██╗  ██╗███╗   ██╗ ██████╗███████╗

╚██╗██╔╝████╗  ██║██╔════╝██╔════╝

 ╚███╔╝ ██╔██╗ ██║██║     █████╗

 ██╔██╗ ██║╚██╗██║██║     ██╔══╝

██╔╝ ██╗██║ ╚████║╚██████╗███████╗

╚═╝  ╚═╝╚═╝  ╚═══╝ ╚═════╝╚══════╝

              Instagram: @xnce / @ro1c\n""")

def login():

    email = input("[ + ] email: ")

    password = input("[ + ] password: ")

    time = requests.get("https://showcase.api.linx.twenty57.net/UnixTime/tounix?date=now").text

    url = f"https://api2.musical.ly/passport/user/login/?ts={time}&js_sdk_version=&app_type=normal&app_language=en&manifest_version_code=2018110525&_rticket=1636181409652&iid=7027345096371570437&channel=googleplay&language=en&fp=&device_type=ART-L29&resolution=720*1491&openudid=5da894062bfc39fa&update_version_code=2018110525&sys_region=GB&os_api=29&is_my_cn=0&timezone_name=Asia%2FAmman&dpi=320&carrier_region=JO&ac=wifi&device_id=7019232418121516549&pass-route=1&mcc_mnc=41601&timezone_offset=7200&os_version=10&version_code=900&carrier_region_v2=416&app_name=musical_ly&ab_version=9.0.0&version_name=9.0.0&device_brand=HUAWEI&ssmix=a&pass-region=1&build_number=9.0.0&device_platform=android&region=US&aid=1233&as=a1363288c09a2185760077&cp=25a0106c0361885ce1Wm_q&mas=014adde638f54037b6a282163a9b14b394ecec0c0c6cecac1c8c4c"

    head = {

        "Host": "api2.musical.ly",

        "Connection": "keep-alive", 

        "Content-Length": "0",

        "Accept-Encoding": 'gzip',

        "User-Agent": 'com.zhiliaoapp.musically/2018110525 (Linux; U; Android 10; en_GB; ART-L29; Build/HUAWEIART-L29; Cronet/58.0.2991.0)'

    }

    data = {"email": email, "password": password, "mix_mode": "0"}

    req = requests.post(url, headers=head, data=data)

    #print(req.text)

    if "has_password" in req.text:

        print(f"[ + ] {req.cookies.get('sessionid')} ",end="")

        input()

        exit()

    else:

        print(f"[ - ] {req.text} ", end="")

        input()

        exit()

login()
