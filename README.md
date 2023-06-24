
1)

def sahenitap(a, h):
    s = (a*h)/2
    print(s)
sahenitap(5,6)

2)

def tekrari_sil(soz):
    result = []
    for i in range(len(soz)):
        if soz[i] == soz[i-1]:
            continue
        else:
            result.append(soz[i])
    tekrarsiz_soz= ''.join(result)
    print(tekrarsiz_soz)
tekrari_sil('ZZZZZEEEEEEEYYYYYYNEBBBBBB')

3)

def yoxla(eded):
    reqemler = ['1','2','3','4','5','6','7','8','9']
    olmayan = []
    for reqem in reqemler:
        if reqem in eded:
            continue
        else:
            olmayan.append(reqem)
    olmayan_ededler = ','.join(olmayan)

    print('Ededin icinde ', olmayan_ededler, 'reqemleri yoxdur')

yoxla('16379427')


4)

def nomre_qiymeti(nomre):
    qiymet= 60
    emsal = 0
    if nomre[:2]== '90':
        emsal += 3
    if nomre[3]== nomre[4]:
        emsal+= 4
    if nomre[6] == nomre[7] == nomre[8]:
        emsal+= 5
    if nomre[6] == nomre[8] != nomre[7]:
        emsal+=4
    son_qiymet = int(emsal)*qiymet
    print(son_qiymet)

nomre_qiymeti('90-MZ-505')


5)


def ceme_bolunur(eded):
    reqemler_cemi = 0
    for reqem in str(eded):
        reqemler_cemi += int(reqem)
    if eded % reqemler_cemi == 0:
        print('Beli, ', eded, 'ededi' ,reqemler_cemi, 'reqemine qaliqsiz bolunur')
    else:
        print('xeyr, ', eded, 'ededi', reqemler_cemi, 'reqemine qaliqsiz bolunmur')

ceme_bolunur(238)


6)



7)

bolunenler = []
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        bolunenler.append(i)

print(bolunenler)

8)

eded = int(input('eded daxil edin: '))
ededler = []
for i in range(eded):
    if i % 2 == 0:
        ededler.append(i)

print(len(ededler))

9)

list = [2,2,4,3,6,9,6,1,5,1]
for i in list:
    if i > 3:
        list.remove(i)

print(list)

10)

qazanclar = [136,151,125,119,146,133,118,106,138,136,127,101]

min_qazanc = min(qazanclar)

max_qazanc = max(qazanclar)

min_qazanc_ay = qazanclar.index(min_qazanc)+1
max_qazanc_ay = qazanclar.index(max_qazanc)+1

print('Mehsulu', min_qazanc_ay, 'ayinda alib, ', max_qazanc_ay, 'ayinda satsaq daha cox qazanc elde ederik.')
