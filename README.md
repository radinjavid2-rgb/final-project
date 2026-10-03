# final-project
پروژه نهایی

#____________________________________________________________________________________________________________________________________________________________________#

#_______final_project____1____#

import random

SAGHF = 10   # bishtarin meghdar
KAF = 0      # kamtarin meghdar

shadi_pet = [10]
energy_pet = [10]
gorosnegy = [10]

kar1 = "hich kari nakardim"
kar2 = "bia baziiii konimm"
kar3 = "bezar bekhabammmm"
kar4 = "bemm ghaza beedeeee"
khastehha = [("1", kar1), ("2", kar2), ("3", kar3), ("4", kar4)]

print("be bazi (hico pet hamishe mahbob) khosh omadid")
esm = input("esm pet-et chie? ").strip()

while True:
    shoro = input("aya mikhahid bazi ra shoro konid: 1.are  2.na ")
    match shoro:
        case "2":
            break
        case "1":
            print("bazi shoro shod!  <3")
        case _:
            print("faghat 1 ya 2 bezan")
            continue


    shadi_pet[0] = energy_pet[0] = gorosnegy[0] = 10
    nobat = 0

    while True:
        nobat += 1

    
        khast = None
        if random.random() < 0.4:
            khast, matn = random.choice(khastehha)
            print(f"{esm}: {matn}")

        javab = input("chi kar konim? 1.hichi 2.bazi 3.khab 4.ghaza 5.navazesh 6.vaziat 0.khoruj: ")

        match javab:
            case "0":
                break
            case "1":
                energy_pet[0] -= 1
                shadi_pet[0] -= 1
                gorosnegy[0] -= 1
                print(kar1)
            case "2":
                shadi_pet[0] += 2
                energy_pet[0] -= 2
                gorosnegy[0] -= 1
                print(f"{esm} shad shoooodd. vali gorosnehhh")
            case "3":
                energy_pet[0] += 3
                gorosnegy[0] -= 1
                print(f"{esm} khabid!")
            case "4":
                shadi_pet[0] += 2
                energy_pet[0] += 2
                gorosnegy[0] += 3
                print(f"{esm} ghaza khord")
            case "5":
                shadi_pet[0] += 1
                print(f"{esm} khoshhal shod, ghor ghor mikone!")
            case "6":
                print(f"{esm} -> shadi: {shadi_pet[0]} | energy: {energy_pet[0]} | sir: {gorosnegy[0]}")
                nobat -= 1
                continue
            case _:
                print("gozine-ye na-motabar")
                nobat -= 1
                continue

        if javab == khast:
            shadi_pet[0] += 1
            print(f"{esm}: mersiii, hamin ro mikhastam! <3 (shadi +1)")

    
        if random.random() < 0.2:
            e = random.choice(["ghaza", "shad", "khaste"])
            if e == "ghaza":
                gorosnegy[0] += 2
                print(f"{esm} ye ghaza rooye zamin peida kard! (sir +2)")
            elif e == "shad":
                shadi_pet[0] += 2
                print(f"{esm} be khodi khodash khandid! (shadi +2)")
            else:
                energy_pet[0] -= 1
                print(f"{esm} yeho khaste shod... (energy -1)")

    
        shadi_pet[0] = max(KAF, min(shadi_pet[0], SAGHF))
        energy_pet[0] = max(KAF, min(energy_pet[0], SAGHF))
        gorosnegy[0] = max(KAF, min(gorosnegy[0], SAGHF))

        print(f"{esm} -> shadi: {shadi_pet[0]} | energy: {energy_pet[0]} | sir: {gorosnegy[0]}")

       
        if shadi_pet[0] <= 0 or energy_pet[0] <= 0:
            if shadi_pet[0] <= 0:
                print(f"{esm} az bi-hoselegi morad... :(")
            if energy_pet[0] <= 0:
                print(f"{esm} az bi-enerjii morad... :(")
            print(f"R.I.P {esm}")
            break

        if gorosnegy[0] <= 0:
            print(f"{esm} az gorosnegi morad... :(")
            print(f"R.I.P {esm}")
            break

    print(f"emtiaz-e shoma: {nobat} nobat {esm} ra zende negah dashti!")
    
    
#____________________________________________________________________________

#_______final_project____1____#

factor_foroshgah = []

while True:
    menu = input("1 mive foroshi   2 exit   :")
    match menu:
        case "1":
            mive_ha = input("1 moz  2 sib  3 porteghal   4 narengi     5.ananas      6.hendone        7.hollo       8.karboze    9.exit : ")
            match mive_ha:
                case "1":
                    num_moz = int(input("num of order: "))
                    price_moz = num_moz * 50
                    price_moz_tax = price_moz * 1.1
                    print("gheymat", price_moz_tax)

                    if price_moz_tax >= 500:
                        takhfif = price_moz_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_moz_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_moz_tax)
                        continue

                case "2":
                    num_sib = int(input("num of order: "))
                    price_sib = num_sib * 40
                    price_sib_tax = price_sib * 1.1
                    print("gheymat", price_sib_tax)

                    if price_sib_tax >= 500:
                        takhfif = price_sib_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_sib_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_sib_tax)
                        continue

                case "3":
                    num_porteghal = int(input("num of order: "))
                    price_porteghal = num_porteghal * 40
                    price_porteghal_tax = price_porteghal * 1.1
                    print("gheymat", price_porteghal_tax)

                    if price_porteghal_tax >= 500:
                        takhfif = price_porteghal_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_porteghal_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_porteghal_tax)
                        continue

                case "4":
                    num_narengi = int(input("num of order: "))
                    price_narengi = num_narengi * 45
                    price_narengi_tax = price_narengi * 1.1
                    print("gheymat", price_narengi_tax)

                    if price_narengi_tax >= 500:
                        takhfif = price_narengi_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_narengi_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_narengi_tax)
                        continue

                case "5":
                    num_ananas = int(input("num of order: "))
                    price_ananas = num_ananas * 230
                    price_ananas_tax = price_ananas * 1.1
                    print("gheymat", price_ananas_tax)

                    if price_ananas_tax >= 500:
                        takhfif = price_ananas_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_ananas_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_ananas_tax)
                        continue

                case "6":
                    num_hendone = int(input("num of order: "))
                    price_hendone = num_hendone * 100
                    price_hendone_tax = price_hendone * 1.1
                    print("gheymat", price_hendone_tax)

                    if price_hendone_tax >= 500:
                        takhfif = price_hendone_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_hendone_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_hendone_tax)
                        continue

                case "7":
                    num_hollo = int(input("num of order: "))
                    price_hollo = num_hollo * 70
                    price_hollo_tax = price_hollo * 1.1
                    print("gheymat", price_hollo_tax)

                    if price_hollo_tax >= 500:
                        takhfif = price_hollo_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_hollo_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_hollo_tax)
                        continue

                case "8":
                    num_karboze = int(input("num of order: "))
                    price_karboze = num_karboze * 100
                    price_karboze_tax = price_karboze * 1.1
                    print("gheymat", price_karboze_tax)

                    if price_karboze_tax >= 500:
                        takhfif = price_karboze_tax * 0.05
                        print("takhfif shoma", takhfif)
                        takhfif_bad_az_hesab = price_karboze_tax - takhfif
                        factor_foroshgah.append(takhfif_bad_az_hesab)
                        print(factor_foroshgah)
                        break
                    else:
                        factor_foroshgah.append(price_karboze_tax)
                        continue

                case "9":
                    continue
