<p align="center">
  <img width="320" height="320" src="https://github.com/g00dvin/continent-faq/blob/master/res/logo.png">
</p>

# АПКШ Континент
> Так или иначе, но тебе повезло и ты нашел этот документ. Тут мы постараемся рассказать тебе о том, что поможет тебе в дальнейшем не страдать, а получать удовольствие при использовании АПКШ Континент.

Оглавление:
[Версии программного обеспечения][1]


## Версии программного обеспечения
[1] На текущий момент актуальной является версия АПКШ Континент 3.7.7.

|Версия|Статус|Последний сертифицированный билд|
| --- | --- | --- |
| 3.5 | EOL | 3.5.74.0 |
| 3.6 | EOL | 3.6.90.4 |
| **3.7** | **Текущая** | **3.7.7.671** |
| 3.9 | Сертификация | 3.9.2880 |
| 4 | В разработке | Не зафиксировано |

## Аппаратные платформы
| Модель | Шасси | Поддерживаемые версии ПО |
|--- | --- | --- |
| IPC10 | S088| 3.7, 3.9 |
| IPC10 | LN010A | 3.7, 3.9, 4 |
| IPC10 | S185 | 3.9, 4 |
| IPC25 | GA630 | 3.5, 3.6 |
| IPC25 | 9830 | 3.5, 3.6 |
| IPC25 | 92D9 | 3.6, 3.7, 3.9 |
| IPC25 | S115 | 3.7, 3.9, 4* |
| IPC50 | LN010C | 3.9, 4 |
| IPC100 | G560 | 3.5, 3.6 |
| IPC100 | 92E3 | 3.6, 3.7, 3.9 |
| IPC100 | S102 | 3.6, 3.7, 3.9, 4* |
| IPC400 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC400 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC500 | LN015B | 3.7, 3.9, 4 |
| IPC500F | LN015C | 3.9, 4 |
| IPC600 | DV030A | 3.9, 4 |
| IPC800F | DV030B | 3.9, 4 |
| IPC1000 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1000F | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1000F2 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1010 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1000 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC1000F | S021 | 3.6, 3.7, 3.9, 4* |
| IPC1000F2 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC1000 | DV031A | 3.9, 4 |
| IPC1000F | DV031B | 3.9, 4 |
| IPC1000F2 | DV031C | 3.9, 4 |
| IPC3000F | S021 | 3.6, 3.7, 3.9, 4* |
| IPC3034 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC3034F | S021 | 3.6, 3.7, 3.9, 4* |
| IPC3000F | LN021 | 3.9, 4 |
| IPC3000FC | LN021A | 3.9, 4 |
| IPC3000NF2 | LN021E | 3.9, 4 |
| IPC3034F | LN021C | 3.9, 4 |
| IPC3000 | LN021D | 3.9, 4 |
| IPC5000FC | S145 | 3.9, 4 |

*\* требуется приобретение комплекта модернизации RAM и HDD, подробности уточнять у вендора.*

## Инсталляция ПО
АПКШ Континент, в случае его приобретения, поставляется с предустановленной, на производстве Кода Безопасности, текущей тиражируемой версией ПО. В некоторых случая может потребоваться переустановка ПО (понижение или повышение версии, восстановление работоспособности, установка отладочной версии по и т.д.).

### Инсталляция на аппаратную платформу
При инсталляции ПО на аппаратную платформу используются два источника инсталляции:
* CD-диск (входит в комплекте поставки оборудования)
* USB Flash drive (так же входит в состав поставки)

Самый распространенный способ - это установка через USB Flash drive. В этом случае на носитель необходимо записать образ USB Flash drive из комплекта поставки, образы находятся на CD-диске в директории Setup\Continent\FLASH\IMAGES, имеют расширение .flash и записываются на USB Flash drive при помощи таких утилит как dd (Linux), [Win32DiskImager](https://sourceforge.net/projects/win32diskimager/), [Rufus](https://rufus.ie/ru_RU.html) (Windows). По факту каждый образ это raw image жесткого диска с двумя разделами, первый раздел FAT размером 8 МБ предназначен для сохранения ключей администратора ЦУС или же конфигурации и ключей КШ, второй раздел UFS (FreeBSD) содержит необходимые для установки ПО файлы. Созданный таким образом USB Flash drive будет являться загрузочным устройством и позволит произвести установку ПО на аппаратную платформу АПКШ.

Каждый образ установочного ПО содержит требуемый функционал для конкретной реализации ПО:

* arm_release.flash - АРМ ГК (Генерации Ключей)
* cgw.aserv_release.flash - КШ-СД
* cgw_release.flash - КШ
* csw_release.flash - КК
* ids_release.flash - ДА
* ncc.aserv_release.flash - ЦУС-СД
* ncc_release.flash - ЦУС

#### Соболь
При перезаливке ПО на аппаратную платформу АПМДЗ "Соболь" будет выдавать предупреждение о том, что изменился загрузочный диск, на запрос о изменении загрузочного диска следует ответить "НЕТ", в ином случае Соболь при загрузке уже с диска опять выдаст это предупреждение. Так же после перезаливки ПО сбрасится настройка "Время автоматического входа в систему", следует установить этот параметр в значение, отличное от 0, иначе устройство будет требовать предъявление iButton при каждой загрузке. Пункт "Время автоматического входа в систему" может быть недоступен для редактирования, в этом случае необходимо создать пользователя AUTOLOAD в меню управления пользователям АПМДЗ "Соболь". 

### Инсталляция ПО на виртуальную машину
Для того, чтобы установить ПО Континент на виртуальную машину используется специальный ISO-образ, который содержит в инсталляционных файлах все возможные компоненты комплекса (ЦУС, КШ, КК, ДА, ЦУС-СД, КШ-СД, АРМ ГК). Основное отличие данного ISO-образа это эмуляция Соболя, по факту же данный образ может использоваться для установки на x86-совместимое аппаратное обеспечение, но стоит понимать, что в этом случае мы никогда не получим формальное соответствие формуляру (актуально для версии 3.7 и ниже). 
При установке на виртуальную платформу необходимо выбирать гостевую систему FreeBSD (32 bit) ниже 10 версии.

Для оптимизации потребления ресурсов гипервизора рекомендуется использовать следующие параметры в файле /boot/loader.rc:

* set hint.p4tcc.0.disabled=1
* set hint.acpi_throttle.0.disabled=1
* set hint.apic.0.clock=0
* set kern.hz=50

Начиная с версии 3.9 для установки на реальную платформу и на гипервизор используется один установочный диск, который самостоятельно определяет в каком режиме он будет работать.

## Строка инициализации
Строка инициализации используется для создания устройства в ПУ ЦУС, это способ сообщить ПУ ЦУС идентификационный номер устройства, а так же количество и тип сетевых интерфейсов. При ошибке в строке инициализации в дальнейшем будет невозможно загрузить конфигурацию на устройство, так что стоит быть предельно внимательным при ее вводе.
Строка инициализации для оборудования, поставляемого производителем приведена в Паспорте, так же строку инициализации можно увидеть при инсталляции ПО (строка инициализации появляется после ввода идентификатора устройства, в некоторых случая строка инициализации может уйти за границы экрана, в этом случае необходимо нажать Scroll Lock и прокрутить экран вверх при помощи клавиш с указателями).

> Следует быть внимательным, при установке на виртуальную машину, поскольку в некоторых гипервизорах могут использоваться различные типы интерфейсов, к примеру в VirtualBox используются интерфейсы le. Так же стоит обратить внимание, если количество интерфейсов в строке инициализации отличается от фактического количества интерфейсов на аппаратной платформе, это может быть признаком выхода интерфейса из строя, и как следствие ОС не может его обнаружить.

Строка инициализации имеет четкий формат, например 000027103igb0*02BDigb1*02BDigb2*02BDffff где:

* 0000 - признак начала строки инициализации
* 2710 - HEX-представление идентификатора устройства, в данном случае идентификатор устройства равен 10000
* 3 - количество сетевых интерфейсов устройства, далее и до конца строки идет перечисление интерфейсов и их режимов работы
* igb0*02BD - наименование сетевого интерфейса, как его определяет операционная система и его режим работы (скорость, дуплекс), для каждого типа интерфейсов * предусмотренны свои режимы
* ffff - признак окончания строки инициализации

Интерфейсы и режим работы:
* em0 (медь) - 02BD
* igb (оптика) - 3001
* igb (медь) - 02BD
* ix (оптика 10G) - 0001
* ixl (оптика криптоускоритель) - 2E801

