import re

def normalize_space(teks):
    """
    Menghapus spasi berlebih dalam sebuah string dan menggantinya dengan satu spasi.

    Args:
        teks (str): String yang akan dinormalisasi spasinya.

    Returns:
        str: String dengan spasi normal.
    """
    # Menggunakan regular expression untuk mengganti satu atau lebih spasi dengan satu spasi
    return re.sub(r'\s+', ' ', teks).strip()

# Contoh penggunaan
teks_input = "saya  tidak   suka    memancing ikan  "
teks_normal = normalize_space(teks_input)
print(f"Teks sebelum normalisasi: '{teks_input}'")
print(f"Teks setelah normalisasi: '{teks_normal}'")

teks_lain = input("Masukkan teks dengan spasi berlebih: ")
teks_normal_lain = normalize_space(teks_lain)
print(f"Teks setelah normalisasi: '{teks_normal_lain}'")
