# input() funsiyası

input() funksiyası məlumatın girişi cihazından (əsasən bu klavyatura olur) məlumatı almaq üçün funksiyadır. Default olaraq məlumatları string tipində alır. Aşağıdakı nümunəyə baxaq

```
yas = input("Neçə yaşınız var? ")
print("Sizin " + yas + " yaşınız var!")


"""
Ekrana çıxan yazı

Neçə yaşınız var? 18
Sizin 18 yaşınız var!
"""
```

Yuxarıdakı kod parçası işə düşdükdə istifadəçidən bir şey daxil etməsini gözləyir. Bundan sonra isə istifadəçinin daxil etdiyi stringi cümlənin içində print edir.

Əgər istifadəçinin daxil etdiyi məlumatla bağlı bir hesablama etmək lazım olacaqsa, yuxarıdakı formada istifadəçidən məlumatı olmaq xətaya səbəb ola bilər. Çünki hesablamalarla bağlı bir çox işlərdə integer və float tipindən istifadə olunur və bu tiplər string ilə arithmetic operaor-lar vasitəsilə işləyə bilmirlər. Bunun həll yolu istifadəçidən məlumatı aldıqdan dərhal sonra onu müvafiq data tipinə çevirməkdir.

```python
bölünən = int(input("Bölünəni daxil edin: "))
bölən = int(input("Böləni daxil edin: "))
qismət = str(int(bölünən/bölən))

print("Cavab: " + qismət)

'''
Ekrana çıxan nəticə

Bölünəni daxil edin: 18
Böləni daxil edin: 3
Cavab: 6
'''
```

Yuxarıdakı misalda bölən və bölünən üzərində hesablama aparılacağına görə onları string yox integer tipində yadda saxlamaq lazım idi. Buna görə birinci və ikinci sətirlərdə `int()` ilə type casting etmişəm. üçüncü sətirdə isə bölmə əməliyyatı həmişə float tipində rəqəm qaytardığına görə, cavabın 6.0 kimi yox 6 kimi görsənməsini istəmişəm. Buna görə birinci növbədə bölməni integerə çevirmişəm int() vasitəsilə, bundan sonra isə, `str()` ilə integeri stringə çevirməyimin səbəbi 5-ci sətirdəki concatination əməliyyatı olub. integer olaraq qalsaydı 'integer və string concationate ola bilmir' xətası verəcəkdi.

