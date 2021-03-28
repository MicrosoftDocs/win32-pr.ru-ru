---
description: Для шрифтов и текста используются следующие функции.
ms.assetid: 69c04ed7-52da-4cb6-9fd2-f2a8c044df8b
title: Функции шрифтов и текста (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a4dd6f000356dfb0e52c34fadef81bd6e8843e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544495"
---
# <a name="font-and-text-functions-windows-gdi"></a>Функции шрифтов и текста (Windows GDI)

Для шрифтов и текста используются следующие функции.



| Функция                                                   | Описание                                                                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**аддфонтмемресаурцеекс**](/windows/desktop/api/Wingdi/nf-wingdi-addfontmemresourceex)       | Добавляет внедренный шрифт в таблицу системных шрифтов.                                                                      |
| [**аддфонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)                 | Добавляет ресурс шрифта в таблицу системных шрифтов.                                                                       |
| [**аддфонтресаурцеекс**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)             | Добавляет закрытый или не перечислимый шрифт в таблицу системных шрифтов.                                                      |
| [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)                           | Создает логический шрифт.                                                                                              |
| [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)           | Создает логический шрифт из структуры.                                                                             |
| [**креатефонтиндиректекс**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa)       | Создает логический шрифт из структуры.                                                                             |
| [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)                               | Рисует форматированный текст в прямоугольнике.                                                                                 |
| [**дравтекстекс**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)                           | Рисует форматированный текст в прямоугольнике.                                                                                   |
| [**енумфонтфамекспрок**](/previous-versions//dd162618(v=vs.85))             | Функция дефинедкаллбакк приложения, используемая с [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) для обработки шрифтов. |
| [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa)           | Перечисляет все шрифты в системе с определенными характеристиками.                                                     |
| [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)                           | Рисует строку символов.                                                                                            |
| [**жетаспектратиофилтерекс**](/windows/desktop/api/Wingdi/nf-wingdi-getaspectratiofilterex)   | Возвращает параметр для фильтра пропорций.                                                                        |
| [**жетчарабквидсс**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)               | Возвращает ширину последовательных символов из шрифта TrueType.                                                    |
| [**жетчарабквидссфлоат**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata)     | Возвращает ширину последовательных символов от текущего шрифта.                                                     |
| [**жетчарабквидсси**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsi)             | Возвращает ширину последовательных индексов глифов или из массива индексов глифов из шрифта TrueType.               |
| [**жетчарактерплацемент**](/windows/desktop/api/Wingdi/nf-wingdi-getcharacterplacementa)     | Возвращает сведения о символьной строке.                                                                           |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)                   | Возвращает ширину последовательных символов от текущего шрифта.                                                     |
| [**жетчарвидсфлоат**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata)             | Возвращает дробную ширину последовательных символов от текущего шрифта.                                          |
| [**жетчарвидси**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthi)                     | Возвращает ширину последовательных индексов глифов или массив индексов глифов из текущего шрифта.                     |
| [**жетфонтдата**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)                         | Возвращает данные метрики для шрифта TrueType.                                                                                |
| [**жетфонтлангуажеинфо**](/windows/desktop/api/Wingdi/nf-wingdi-getfontlanguageinfo)         | Возвращает сведения о выбранном шрифте для контекста вывода.                                                   |
| [**жетфонтуникодеранжес**](/windows/desktop/api/Wingdi/nf-wingdi-getfontunicoderanges)       | Указывает, какие символы Юникода поддерживаются шрифтом.                                                              |
| [**жетглифиндицес**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphindicesa)                 | Преобразует строку в массив индексов глифов.                                                                  |
| [**жетглифаутлине**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea)                 | Возвращает контур или точечный рисунок для символа в шрифте TrueType.                                                     |
| [**жеткернингпаирс**](/windows/desktop/api/WinGdi/nf-wingdi-getkerningpairsa)                 | Возвращает пары символов кернинга для шрифта.                                                                         |
| [**жетаутлинетекстметрикс**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)     | Возвращает метрики текста для шрифтов TrueType.                                                                                |
| [**жетрастеризеркапс**](/windows/desktop/api/Wingdi/nf-wingdi-getrasterizercaps)             | Указывает, установлены ли шрифты TrueType.                                                                          |
| [**жеттаббедтекстекстент**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)         | Вычисление ширины и высоты символьной строки, включая символы табуляции.                                                 |
| [**жеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)                       | Возвращает параметр выравнивания текста для контекста устройства.                                                                |
| [**жеттекстчарактерекстра**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)     | Возвращает текущий интервал между символами для контекста устройства.                                                        |
| [**жеттекстколор**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)                       | Возвращает цвет текста для контекста устройства.                                                                            |
| [**жеттекстекстентекспоинт**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa)       | Возвращает количество символов в строке, которые будут помещаться в пробел.                                              |
| [**жеттекстекстентекспоинти**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointi)     | Возвращает число индексов глифов, которые будут помещаться в пробел.                                                       |
| [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)       | Вычисление ширины и высоты строки текста.                                                                   |
| [**жеттекстекстентпоинти**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpointi)         | Вычисление ширины и высоты массива индексов глифов.                                                          |
| [**жеттекстфаце**](/windows/desktop/api/Wingdi/nf-wingdi-gettextfacea)                         | Возвращает имя шрифта, выбранного в контексте устройства.                                                    |
| [**жеттекстметрикс**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)                   | Заполняет буфер метриками для шрифта.                                                                          |
| [**Текст**](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)                         | Рисует несколько строк, используя цвета шрифта и текста в контексте устройства.                                            |
| [**ремовефонтмемресаурцеекс**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex) | Удаляет шрифт, источник которого был внедрен в документ из таблицы системных шрифтов.                                   |
| [**ремовефонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)           | Удаляет шрифты из файла из таблицы системных шрифтов.                                                              |
| [**ремовефонтресаурцеекс**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)       | Удаляет закрытый или не перечислимый шрифт из таблицы системных шрифтов.                                                 |
| [**сетмапперфлагс**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)                   | Изменяет алгоритм, используемый для отображения логических шрифтов в физических шрифтах.                                                    |
| [**сеттексталигн**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)                       | Задает флаги выравнивания текста для контекста устройства.                                                                  |
| [**сеттекстчарактерекстра**](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)     | Задает межзнаковый интервал.                                                                                     |
| [**сеттекстколор**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)                       | Задает цвет текста для контекста устройства.                                                                            |
| [**сеттекстжустификатион**](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)       | Указывает объем пространства, который система должна добавить к символам разрыва в строке.                             |
| [**таббедтекстаут**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)                     | Записывает строку символов в месте, расширяя вкладки до указанных значений.                                         |
| [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)                                 | Записывает строку символов в месте расположения.                                                                             |



 

## <a name="obsolete-functions"></a>Устаревшие функции

Эти функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Windows.

-   [**креатескалаблефонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-createscalablefontresourcea)
-   [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)
-   [**енумфонтфампрок**](/previous-versions//dd162621(v=vs.85))
-   [**енумфонтс**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa)
-   [**енумфонтспрок**](/previous-versions//dd162623(v=vs.85))
-   [**жетчарвидс**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidtha)
-   [**жеттекстекстентпоинт**](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa)

 

 
