---
description: Подмножество Юникода битовых полей (Усбс) используется в структурах ФОНТСИГНАТУРЕ и ЛОКАЛЕСИГНАТУРЕ.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Битовых полей подмножества Юникода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f0fa4791e62f397e62a99a78d41dbcdc67c55299a650b1bc78bea685205399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787994"
---
# <a name="unicode-subset-bitfields"></a>Битовых полей подмножества Юникода

Подмножество Юникода битовых полей (Усбс) используется в структурах [**фонтсигнатуре**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) и [**локалесигнатуре**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Поддиапазон Юникода</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>Базовая латиница</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>Дополнительная латиница 1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>Расширенная латиница-A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>Расширенная латиница-B</td>
</tr>
<tr class="odd">
<td rowspan="3">4 $ {REMOVE} $<br />
</td>
<td>0250 - 02AF</td>
<td>Расширения IPA</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>Фонетические расширения</td>

</tr>
<tr class="odd">
<td>1D80 - 1DBF</td>
<td>Дополнение к фонетическим расширениям</td>

</tr>
<tr class="even">
<td rowspan="2">5 $ {REMOVE} $<br />
</td>
<td>02B0 - 02FF</td>
<td>Буквы модификаторов расстояний</td>
</tr>
<tr class="odd">
<td>A700 - A71F</td>
<td>Буквы тоновых модификаторов</td>

</tr>
<tr class="even">
<td rowspan="2">6 $ {REMOVE} $<br />
</td>
<td>0300 - 036F</td>
<td>Сочетание диакритических знаков</td>
</tr>
<tr class="odd">
<td>1DC0 - 1DFF</td>
<td>Дополняющие диакритические знаки</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>Греческий и Коптский</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2C80 - 2CFF</td>
<td>Коптский</td>
</tr>
<tr class="even">
<td rowspan="4">9 $ {REMOVE} $<br />
</td>
<td>0400 - 04FF</td>
<td>Кириллица</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>Дополнение для кириллицы</td>

</tr>
<tr class="even">
<td>2DE0 - 2DFF</td>
<td>Кириллица, расширенная — A</td>

</tr>
<tr class="odd">
<td>A640 - A69F</td>
<td>Кириллица, расширенная — B</td>

</tr>
<tr class="even">
<td>10</td>
<td>0530 - 058F</td>
<td>Армянский</td>
</tr>
<tr class="odd">
<td>11</td>
<td>0590 - 05FF</td>
<td>Иврит</td>
</tr>
<tr class="even">
<td>12</td>
<td>A500 - A63F</td>
<td>Ваи</td>
</tr>
<tr class="odd">
<td rowspan="2">13 $ {REMOVE} $<br />
</td>
<td>0600 - 06FF</td>
<td>Арабский</td>
</tr>
<tr class="even">
<td>0750-077F</td>
<td>Дополнение для арабского языка</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07C0 - 07FF</td>
<td>Блок</td>
</tr>
<tr class="even">
<td>15</td>
<td>0900 - 097F</td>
<td>Девангари</td>
</tr>
<tr class="odd">
<td>16</td>
<td>0980 - 09FF</td>
<td>Бенгальский</td>
</tr>
<tr class="even">
<td>17</td>
<td>0A00 - 0A7F</td>
<td>Гурмукхи</td>
</tr>
<tr class="odd">
<td>18</td>
<td>0A80 - 0AFF</td>
<td>Гуджарати</td>
</tr>
<tr class="even">
<td>19</td>
<td>0B00 - 0B7F</td>
<td>Ория</td>
</tr>
<tr class="odd">
<td>20</td>
<td>0B80 - 0BFF</td>
<td>Тамильский</td>
</tr>
<tr class="even">
<td>21</td>
<td>0C00 - 0C7F</td>
<td>Телугу</td>
</tr>
<tr class="odd">
<td>22</td>
<td>0C80 - 0CFF</td>
<td>Каннада</td>
</tr>
<tr class="even">
<td>23</td>
<td>0D00 - 0D7F</td>
<td>Малаялам</td>
</tr>
<tr class="odd">
<td>24</td>
<td>0E00 - 0E7F</td>
<td>Тайский</td>
</tr>
<tr class="even">
<td>25</td>
<td>0E80 - 0EFF</td>
<td>Лаосский</td>
</tr>
<tr class="odd">
<td rowspan="2">26 $ {REMOVE} $<br />
</td>
<td>10A0 - 10FF</td>
<td>Грузинский</td>
</tr>
<tr class="even">
<td>2D00 - 2D2F</td>
<td>Дополнительный грузинский</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1B00 - 1B7F</td>
<td>Балийский</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>Знаки хангыль</td>
</tr>
<tr class="odd">
<td rowspan="3">29 $ {REMOVE} $<br />
</td>
<td>1E00 - 1EFF</td>
<td>Расширенная латиница дополнительно</td>
</tr>
<tr class="even">
<td>2C60 - 2C7F</td>
<td>Латиница Extended-C</td>

</tr>
<tr class="odd">
<td>A720 - A7FF</td>
<td>Расширенная латиница-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>Греческий расширенный</td>
</tr>
<tr class="odd">
<td rowspan="2">31 $ {REMOVE} $<br />
</td>
<td>2000 - 206F</td>
<td>Общие знаки препинания</td>
</tr>
<tr class="even">
<td>2E00 - 2E7F</td>
<td>Дополнительные знаки препинания</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>Надстрочные и подстрочные индексы</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>Символы валют</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>Сочетание диакритических знаков для символов</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>Буквоподобных символы</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>Числовые формы</td>
</tr>
<tr class="even">
<td rowspan="4">37 $ {REMOVE} $<br />
</td>
<td>2190 - 21FF</td>
<td>Стрелки</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>Дополнительные стрелки</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>Дополнительные стрелки — B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>Различные символы и стрелки</td>

</tr>
<tr class="even">
<td rowspan="4">38 $ {REMOVE} $<br />
</td>
<td>2200 - 22FF</td>
<td>Математические операторы</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>Различные математические символы — A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>Различные математические символы — B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>Дополнительные математические операторы</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>Прочие технические</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>Управление рисунками</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>Оптическое распознавание символов</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>Вложенные буквенно-цифровые символы</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>Рисование Box</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Блочные элементы</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>Геометрические фигуры</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>Прочие символы</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Dingbats</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>ККЯ — символы и пунктуация</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>Хирагана</td>
</tr>
<tr class="odd">
<td rowspan="2">50 $ {REMOVE} $<br />
</td>
<td>30A0 - 30FF</td>
<td>Катакана</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>Фонетические расширения катакана</td>

</tr>
<tr class="odd">
<td rowspan="2">51 $ {REMOVE} $<br />
</td>
<td>3100 - 312F</td>
<td>Бопомофо</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>Расширенный бопомофо</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>Знаки совместимости хангыль</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 - A87F</td>
<td>Блок-PA</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>Вложенные символы CJK и месяцы</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>ККЯ — совместимость</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>Слоги хангыль</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800-DFFF</td>
<td>Не плоскость 0. Обратите внимание, что установка этого бита подразумевает наличие по крайней мере одной дополнительной кодовой точки за пределами основной многоязычной плоскости (BMP), поддерживаемой этим шрифтом. См. Дополнительные сведения о <a href="surrogates-and-supplementary-characters.md">суррогатах и добавочных символах</a>.</td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900-1091F</td>
<td>Финикийский алфавит</td>
</tr>
<tr class="even">
<td rowspan="7">59 $ {REMOVE} $<br />
</td>
<td>2E80 - 2EFF</td>
<td>Дополнительные радикалы CJK</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>Радикалы кандзи</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>Идеографические символы описания</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>Канбуна</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>ККЯ — унифицированные иероглифы, расширение A</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>ККЯ — унифицированные иероглифы</td>

</tr>
<tr class="even">
<td>20000-2A6DF</td>
<td>ККЯ — унифицированные иероглифы, расширение B</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>Область закрытого использования</td>
</tr>
<tr class="even">
<td rowspan="3">61 $ {REMOVE} $<br />
</td>
<td>31C0 - 31EF</td>
<td>ККЯ — штрихи</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>ККЯ — иероглифы совместимости</td>

</tr>
<tr class="even">
<td>2F800 - 2FA1F</td>
<td>ККЯ — дополнительные иероглифы совместимости</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>Формы представления по алфавиту</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>Формы для арабского представления — A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>Объединение половинных делений</td>
</tr>
<tr class="even">
<td rowspan="2">65 $ {REMOVE} $<br />
</td>
<td>FE10 - FE1F</td>
<td>Вертикальные формы</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>ККЯ — формы совместимости</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>Варианты малых форм</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>Формы для арабского представления — B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>Формы с шириной в полуширинные и в виде ширины</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>Блок</td>
</tr>
<tr class="even">
<td>70</td>
<td>0F00 - 0FFF</td>
<td>Тибетский</td>
</tr>
<tr class="odd">
<td>71</td>
<td>0700 - 074F</td>
<td>Сирийский</td>
</tr>
<tr class="even">
<td>72</td>
<td>0780 - 07BF</td>
<td>мальдивский</td>
</tr>
<tr class="odd">
<td>73</td>
<td>0D80 - 0DFF</td>
<td>Сингальский</td>
</tr>
<tr class="even">
<td>74</td>
<td>1000 - 109F</td>
<td>Мьянма</td>
</tr>
<tr class="odd">
<td rowspan="3">75 $ {REMOVE} $<br />
</td>
<td>1200 - 137F</td>
<td>Эфиопского</td>
</tr>
<tr class="even">
<td>1380-139F</td>
<td>Дополнение эфиопского</td>

</tr>
<tr class="odd">
<td>2D80 - 2DDF</td>
<td>Эфиопского Расширенная</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>Чероки</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>Унифицированное канадское письмо слогового письма</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>Блок</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>руник</td>
</tr>
<tr class="even">
<td rowspan="2">80 $ {REMOVE} $<br />
</td>
<td>1780 - 17FF</td>
<td>Кхмерский</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>Кхмерский символ</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>Монгольский</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>Шаблоны Брайля</td>
</tr>
<tr class="even">
<td rowspan="2">83 $ {REMOVE} $<br />
</td>
<td>A000 - A48F</td>
<td>Ий — слоги</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Радикалы в Yi</td>

</tr>
<tr class="even">
<td rowspan="4">84 $ {REMOVE} $<br />
</td>
<td>1700 - 171F</td>
<td>Тагальский</td>
</tr>
<tr class="odd">
<td>1720 - 173F</td>
<td>Блок</td>

</tr>
<tr class="even">
<td>1740 - 175F</td>
<td>Бухид</td>

</tr>
<tr class="odd">
<td>1760 - 177F</td>
<td>Тагбануа</td>

</tr>
<tr class="even">
<td>85</td>
<td>10300-1032F</td>
<td>Старый курсив</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330-1034F</td>
<td>Arial</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400-1044F</td>
<td>Дезерет</td>
</tr>
<tr class="odd">
<td rowspan="3">88 $ {REMOVE} $<br />
</td>
<td>1D000 - 1D0FF</td>
<td>Бизантине Музыкальные символы</td>
</tr>
<tr class="even">
<td>1D100 - 1D1FF</td>
<td>Музыкальные символы</td>

</tr>
<tr class="odd">
<td>1D200 - 1D24F</td>
<td>Античного греческая музыкальная нотация</td>

</tr>
<tr class="even">
<td>89</td>
<td>1D400 - 1D7FF</td>
<td>Математические буквенно-цифровые символы</td>
</tr>
<tr class="odd">
<td rowspan="2">90 $ {REMOVE} $<br />
</td>
<td>FF000-FFFF</td>
<td>Частное использование (плоскость 15)</td>
</tr>
<tr class="even">
<td>100000-10FFFD</td>
<td>Частное использование (плоскость 16)</td>

</tr>
<tr class="odd">
<td rowspan="2">91 $ {REMOVE} $<br />
</td>
<td>FE00 - FE0F</td>
<td>Селекторы вариантов</td>
</tr>
<tr class="even">
<td>E0100 - E01EF</td>
<td>Дополнение селекторов вариантов</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 - E007F</td>
<td>Теги</td>
</tr>
<tr class="even">
<td>93</td>
<td>1900 - 194F</td>
<td>Лимбу</td>
</tr>
<tr class="odd">
<td>94</td>
<td>1950 - 197F</td>
<td>Тай Le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980-19DF</td>
<td>Новая письменность тай-лю</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1A00 - 1A1F</td>
<td>Бугийский</td>
</tr>
<tr class="even">
<td>97</td>
<td>2C00 - 2C5F</td>
<td>глаголитик</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30 - 2D7F</td>
<td>Тифинаг</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>Символы ижинг Цзин</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 - A82F</td>
<td>Силоти нагри</td>
</tr>
<tr class="even">
<td rowspan="3">101 $ {REMOVE} $<br />
</td>
<td>10000-1007F</td>
<td>Линейная B — слоговая</td>
</tr>
<tr class="odd">
<td>10080-100FF</td>
<td>Линейная B Идеограмс</td>

</tr>
<tr class="even">
<td>10100-1013F</td>
<td>Эгейский университет числа</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140-1018F</td>
<td>Античного Греческий номер</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380-1039F</td>
<td>Угаритский</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103A0 - 103DF</td>
<td>Старый Персидский</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450-1047F</td>
<td>шавиан</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480-104AF</td>
<td>османя</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800-1083F</td>
<td>Циприотская слоговая</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10A00 - 10A5F</td>
<td>кхарошси</td>
</tr>
<tr class="even">
<td>109</td>
<td>1D300 - 1D35F</td>
<td>Символы Тай Ксуан Цзин Чань</td>
</tr>
<tr class="odd">
<td rowspan="2">110 $ {REMOVE} $<br />
</td>
<td>12000-123FF</td>
<td>кунеиформ</td>
</tr>
<tr class="even">
<td>12400-1247F</td>
<td>Кунеиформ цифры и пунктуация</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1D360 - 1D37F</td>
<td>Подсчет чисел</td>
</tr>
<tr class="even">
<td>112</td>
<td>1B80 - 1BBF</td>
<td>Сунданская письменность</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1C00 - 1C4F</td>
<td>Лепча</td>
</tr>
<tr class="even">
<td>114</td>
<td>1C50 - 1C7F</td>
<td>Письменность ол-чики</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 - A8DF</td>
<td>Саураштра</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900 - A92F</td>
<td>Письменность кайях-ли</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 - A95F</td>
<td>Реджангский</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 - AA5F</td>
<td>Чамская письменность</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190-101CF</td>
<td>Античного символы</td>
</tr>
<tr class="even">
<td>120</td>
<td>101D0 - 101FF</td>
<td>Фаистос диск</td>
</tr>
<tr class="odd">
<td rowspan="3">121 $ {REMOVE} $<br />
</td>
<td>10280-1029F</td>
<td>Ликийский</td>
</tr>
<tr class="even">
<td>102A0 - 102DF</td>
<td>Карийский</td>

</tr>
<tr class="odd">
<td>10920-1093F</td>
<td>Лидийский</td>

</tr>
<tr class="even">
<td rowspan="2">122 $ {REMOVE} $<br />
</td>
<td>1F000 - 1F02F</td>
<td>Плитки в маджонг</td>
</tr>
<tr class="odd">
<td>1F030 - 1F09F</td>
<td>Плитки Domino</td>

</tr>
<tr class="even">
<td>123</td>

<td><strong>Windows 2000 и более поздних версий:</strong> Ход выполнения макета, горизонтальный справа налево</td>
</tr>
<tr class="odd">
<td>124</td>

<td><strong>Windows 2000 и более поздних версий:</strong> Ход выполнения макета, по вертикали перед горизонтальным</td>
</tr>
<tr class="even">
<td>125</td>

<td><strong>Windows 2000 и более поздних версий:</strong> Ход выполнения макета, Вертикальный снизу вверх</td>
</tr>
<tr class="odd">
<td>126-127</td>

<td>Зарезервировано для внутреннего использования процессом</td>
</tr>
</tbody>
</table>



 

 

 



