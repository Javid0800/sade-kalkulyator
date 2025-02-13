# sade-kalkulyator
def toplama(a, b):
    return a + b

def cixma(a, b):
    return a - b

def vurma(a, b):
    return a * b

def bolme(a, b):
    if b == 0:
        return "Sıfıra bölmə mümkün deyil"
    return a / b

def kalkulyator():
    print("\n--- Sadə Kalkulyator ---")
    print("1. Toplama")
    print("2. Çıxma")
    print("3. Vurma")
    print("4. Bölmə")
    print("5. Çıxış")
    
    secim = input("Seçiminizi edin (1-5): ")

    if secim == '5':
        print("Proqramdan çıxılır...")
        return
    
    try:
        a = float(input("Birinci rəqəmi daxil edin: "))
        b = float(input("İkinci rəqəmi daxil edin: "))
    except ValueError:
        print("Yanlış rəqəm daxil etdiniz. Yenidən cəhd edin.")
        return kalkulyator()
    
    if secim == '1':
        print(f"Nəticə: {toplama(a, b)}")
    elif secim == '2':
        print(f"Nəticə: {cixma(a, b)}")
    elif secim == '3':
        print(f"Nəticə: {vurma(a, b)}")
    elif secim == '4':
        print(f"Nəticə: {bolme(a, b)}")
    else:
        print("Yanlış seçim etdiniz.")
    
    kalkulyator()

if __name__ == "__main__":
    kalkulyator()
