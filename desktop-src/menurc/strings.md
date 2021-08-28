---
title: строк
description: В этом разделе обсуждаются строковые функции.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- ресурсы, строки
- строки;
- строковые функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3799c151b828dba1d687068da6f7f5924aded09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478900"
---
# <a name="strings"></a>Строки

В этом разделе описываются строковые функции и объясняется, как использовать их в приложениях.

### <a name="in-this-section"></a>В этом разделе



| Имя                                     | Описание                                             |
|------------------------------------------|---------------------------------------------------------|
| [Сведения о строках](about-strings.md)       | Описывает строковые функции.<br/>              |
| [О Стрсафе. h](strsafe-ovw.md)       | Описывает строковые функции в Стрсафе. h.<br/> |
| [Ссылка на строку](string-reference.md) | Содержит справочник по API.<br/>                  |



 

### <a name="string-functions"></a>Строковые функции




| Имя | Описание | 
|------|-------------|
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>чарловер</strong></a> | Преобразует строку символов или один символ в нижний регистр. Если операнд является символьной строкой, функция преобразует символы на месте. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>чарловербуфф</strong></a> | Преобразует символы верхнего регистра в буфере в символы нижнего регистра. Функция преобразует символы на месте. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>чарнекст</strong></a> | Извлекает указатель на следующий символ в строке. Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>чарнекстекса</strong></a> | Получает указатель на следующий символ в строке. Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>чарпрев</strong></a> | Извлекает указатель на предшествующий символ в строке. Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>чарпревекса</strong></a> | Получает указатель на предшествующий символ в строке. Эта функция может выполнять обработку строк, состоящих из однобайтовых символов или из одного или нескольких байтов.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>чартуем</strong></a> | Преобразует строку в набор символов, определяемый изготовителем оборудования.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>чартуембуфф</strong></a> | Преобразует указанное число символов в строке в набор символов, определенный изготовителем оборудования.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>чаруппер</strong></a> | Преобразует строку символов или один символ в верхний регистр. Если операнд является символьной строкой, функция преобразует символы на месте. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>чаруппербуфф</strong></a> | Преобразует символы нижнего регистра в буфере в символы верхнего регистра. Функция преобразует символы на месте. <br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a> | Сравнивает две символьные строки, используя заданный языковой стандарт.<blockquote>[!Note]<br />Для совместимости с Юникодом используйте <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>компарестринжекс</strong></a> или версию <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>API CompareString</strong></a>с поддержкой Юникода.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>компарестринжекс</strong></a> | Сравнивает два строки Юникода (расширенных символов) с использованием указанного языкового стандарта.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a> | Карты одну строку в другую, выполняя указанный параметр преобразования. <br /> | 
| <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>жетстрингтипеа</strong></a> | Извлекает сведения о символьном типе для символов в указанной исходной строке. Для каждого символа в строке функция задает один или несколько битов в соответствующем 16-разрядном элементе выходного массива. Каждый бит определяет заданный символьный тип, например, является ли символ буквой, цифрой или ни одной.<br /> | 
| <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>жетстрингтипикс</strong></a> | Извлекает сведения о символьном типе для символов в указанной исходной строке. Для каждого символа в строке функция задает один или несколько битов в соответствующем 16-разрядном элементе выходного массива. Каждый бит определяет заданный символьный тип, например, является ли символ буквой, цифрой или ни одной. <br /> В отличие от его близких родственников <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>жетстрингтипеа</strong></a> и <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>жетстрингтипев</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>жетстрингтипикси</strong></a> работают со стандартным поведением с помощью параметра <strong>#define Unicode</strong> . Это рекомендуемая функция.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>жетстрингтипев</strong></a> | Извлекает сведения о символьном типе для символов в указанной исходной строке. Для каждого символа в строке функция задает один или несколько битов в соответствующем 16-разрядном элементе выходного массива. Каждый бит определяет заданный символьный тип, например, является ли символ буквой, цифрой или ни одной.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>исчаралфа</strong></a> | Определяет, является ли символ буквенно-знакомым. Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>исчаралфанумерик</strong></a> | Определяет, является ли символ алфавитным или цифровым символом. Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>исчарловер</strong></a> | Определяет, является ли символ строчным. Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>исчаруппер</strong></a> | Определяет, является ли символ прописным. Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>лоадстринг</strong></a> | Загружает строковый ресурс из исполняемого файла, связанного с указанным модулем, копирует строку в буфер и добавляет завершающий нуль-символ.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>лстркат</strong></a> | Добавляет одну строку в другую.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>лстркмп</strong></a> | Сравнивает две символьные строки. При сравнении учитывается регистр.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>лстркмпи</strong></a> | Сравнивает две символьные строки. Сравнение выполняется без учета регистра.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>лстркпи</strong></a> | Копирует строку в буфер.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>лстркпин</strong></a> | Копирует указанное число символов из исходной строки в буфер. <br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a> | Определяет длину указанной строки (не включая завершающий нуль-символ).<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>оемточар</strong></a> | Преобразует строку из кодировки, определенной изготовителем оборудования, в строку в кодировке ANSI или в расширенных символах.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>оемточарбуфф</strong></a> | Преобразует указанное число символов в строке из набора, заданного изготовителем оборудования, в строку в кодировке ANSI или в расширенных символах.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>вспринтф</strong></a> | Записывает форматированные данные в указанный буфер.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>ввспринтф</strong></a> | Записывает форматированные данные в указанный буфер с помощью указателя на список аргументов.<br /> | 




 

### <a name="strsafe-functions"></a>Функции стрсафе



| Имя                                             | Описание                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**стрингкбкат**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Сцепляет одну строку с другой строкой.<br/>                                            |
| [**стрингкбкатекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Сцепляет одну строку с другой строкой.<br/>                                            |
| [**стрингкбкатн**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Сцепляет указанное число байтов из одной строки в другую.<br/>         |
| [**стрингкбкатнекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Сцепляет указанное число байтов из одной строки в другую.<br/>         |
| [**стрингкбкопи**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Копирует одну строку в другую.<br/>                                                         |
| [**стрингкбкопекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Копирует одну строку в другую.<br/>                                                         |
| [**стрингкбкопин**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Копирует указанное число байтов из одной строки в другую.<br/>                      |
| [**стрингкбкопинекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Копирует указанное число байтов из одной строки в другую.<br/>                      |
| [**стрингкбжетс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").<br/>  |
| [**стрингкбжетсекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").<br/>  |
| [**стрингкбленгс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Определяет, превышает ли строка указанную длину в байтах.<br/>                   |
| [**стрингкбпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Записывает форматированные данные в указанную строку.<br/>                                        |
| [**стрингкбпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Записывает форматированные данные в указанную строку.<br/>                                        |
| [**стрингкбвпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Записывает форматированные данные в указанную строку, используя указатель на список аргументов.<br/> |
| [**стрингкбвпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Записывает форматированные данные в указанную строку, используя указатель на список аргументов.<br/> |
| [**стрингкчкат**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Сцепляет одну строку с другой строкой.<br/>                                            |
| [**стрингкчкатекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Сцепляет одну строку с другой строкой.<br/>                                            |
| [**стрингкчкатн**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Сцепляет указанное количество символов из одной строки в другую.<br/>    |
| [**стрингкчкатнекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Сцепляет указанное количество символов из одной строки в другую.<br/>    |
| [**стрингкчкопи**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Копирует одну строку в другую.<br/>                                                         |
| [**стрингкчкопекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Копирует одну строку в другую.<br/>                                                         |
| [**стрингкчкопин**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Копирует указанное число символов из одной строки в другую.<br/>                 |
| [**стрингкчкопинекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Копирует указанное число символов из одной строки в другую.<br/>                 |
| [**стрингкчжетс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").<br/>  |
| [**стрингкчжетсекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Получает одну строку текста из stdin, вплоть до символа новой строки (" \\ n").<br/>  |
| [**стрингкчленгс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Определяет, превышает ли строка указанную длину в символах.<br/>              |
| [**стрингкчпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Записывает форматированные данные в указанную строку.<br/>                                        |
| [**стрингкчпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Записывает форматированные данные в указанную строку.<br/>                                        |
| [**стрингкчвпринтф**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Записывает форматированные данные в указанную строку, используя указатель на список аргументов.<br/> |
| [**стрингкчвпринтфекс**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Записывает форматированные данные в указанную строку, используя указатель на список аргументов.<br/> |



 

 

