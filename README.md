# SI_2025_lab2_233131
Teodora Spasikj 233131

![graf](images/graff.png)

За овој код цикломатската комплексност изнесува 9 т.е претставува број на региони.Вкупниот број го добив со следната формула број на ребра - број на јазлии+2

![C0](images/C0.png)

C0 - test case-ови

Ќе ни бидат потребни минимум 6 test cases-ови имајќи за цел секоја линија да биде опфатена

Тest case 1 - allItems е null па затоа ќе се фрли исклучок: "allItems list can't be null!"

Тest case 2 - item.name е null исто и тука ќе се фрли исклучок: "Invalid item!"

Теst case 3 - Условот item.getPrice() > 300 || getDiscount() > 0 || getQuantity() > 10, и discount > 0, sum = -30 + 500*(1-0.2)*20 = -30 + 8000 = 7970

Теst case 4 - Немаат важност условот if(...), и discount = 0

Теst case 5 - cardNumber има карактер (а треба број), "Invalid"

![Multiple](images/Multiple.png)

Multiple Condition за if (item.getPrice() > 300 || item.getDiscount() > 0 || item.getQuantity() > 10)

За следниот услов во кој што има логички оператор OR, во сите три случаи ќе биде TRUE освен во едниот случај каде што ќе биде FALSE

![kod](images/kod.png)

Test case 1:

FTX - item.Price=100; item.Discount=-1; item.Quantity=8; за овие три услови ќе врати false.

Test case2:

FFF - item.Price=100; item.Discount=2; item.Quantity=8; за условот се прави проверка на вториот дел од условот т.е дали item.getDiscount() > 0. Ако е исполнет целиот услов ќе врати true, па за третиот дел item.getQuantity() > 10 нема да се провери (поради кратко спојување на логичкиот оператор OR).

Test case 3:

FFT - item.Price=400; item.Discount=2; item.Quantity=8; за првиот дел item.getPrice() > 300 ќе врати false потоа се проверува и вториот услов item.getDiscount() > 0 и тоа враќа false и на крај ќе го проверуваме и третиот услов item.getQuantity() > 10 и тука целиот услов поминува бидејќи враќа true.

Test case 4:

ТXX - item.Price=100; item.Discound=-1; item.Quantity=15; во првата проверка условот if враќа false потоа го проверуваме вториот и тој ќе врати false па се проверува и третиот каде што и тој враќа false и заради тоа целиот услов паѓа.

