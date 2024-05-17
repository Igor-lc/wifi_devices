import pywifi
from pywifi import const

# Створення профілю
profile = pywifi.Profile()
profile.ssid = 'pycharm 5 GHz'
profile.auth = const.AUTH_ALG_OPEN
profile.akm.append(const.AKM_TYPE_WPA2PSK)
profile.cipher = const.CIPHER_TYPE_CCMP
profile.key = 'wifipass'

# Ініціалізація інтерфейсу
wifi = pywifi.PyWiFi()
iface = wifi.interfaces()[0]

# Видалення попереднього профілю, якщо він існує
iface.remove_all_network_profiles()

# Додавання нового профілю
tmp_profile = iface.add_network_profile(profile)
