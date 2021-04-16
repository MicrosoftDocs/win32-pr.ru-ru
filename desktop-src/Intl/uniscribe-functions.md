---
description: В этом разделе описываются функции для оформления и для обработки сложных скриптов.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Функции Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f623c8da04f985f88d091f8e9e2b4cb724c0801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651204"
---
# <a name="uniscribe-functions"></a>Функции Uniscribe

В этом разделе описываются функции для оформления и для обработки сложных скриптов.



| Функция                                                               | Описание                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**скриптапплидигитсубститутион**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Применяет указанные параметры подстановки цифр к заданному элементу управления скрипта и структурам состояния скрипта.                                                                    |
| [**скриптапплилогикалвидс**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Принимает массив предварительных значений ширины для выполнения и создает массив скорректированных значений ширины предварительных глифов.                                                                               |
| [**скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Получает сведения для определения разрывов строк.                                                                                                                                |
| [**скрипткачежесеигхт**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Извлекает высоту текущего кэшированного шрифта.                                                                                                                                |
| [**скрипткптокс**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Создает смещение x от левого конца или ведущего края выполнения в начале или в конце логического кластера логических символов.                                          |
| [**скриптфрикаче**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Освобождает кэш скрипта.                                                                                                                                                             |
| [**скриптжеткмап**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Получает индексы символов Юникода в строке в соответствии с таблицей TrueType кмап или стандартной таблицей кмап, реализованной для шрифтов старого стиля.         |
| [**скриптжетфонталтернатеглифс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Извлекает список альтернативных глифов для указанного символа, доступ к которому можно получить с помощью указанной функции OpenType.                                                         |
| [**скриптжетфонтфеатуретагс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Извлекает список типографских функций для определенной системы записи для обработки OpenType.                                                                                  |
| [**скриптжетфонтлангуажетагс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Извлекает список тегов языка, доступных для указанного элемента, и поддерживается указанным тегом скрипта для обработки OpenType.                                  |
| [**скриптжетфонтпропертиес**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Извлекает из кэша шрифтов сведения о специальных глифах, используемых шрифтом.                                                                                                   |
| [**скриптжетфонтскрипттагс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Извлекает список скриптов, доступных в шрифте для обработки OpenType.                                                                                                        |
| [**скриптжетглифабквидс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Возвращает ширину ABC для данного глифа.                                                                                                                                         |
| [**скриптжетлогикалвидсс**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Преобразует ширину глифа для определенного шрифта в логические значения ширины.                                                                                                        |
| [**скриптжетпропертиес**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Извлекает сведения о текущих скриптах.                                                                                                                                  |
| [**скриптискомплекс**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Определяет, требует ли строка Юникода обработку сложных скриптов.                                                                                                           |
| [**скриптитемизе**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Разбивает строку Юникода на отдельные фигурные элементы.                                                                                                                        |
| [**скриптитемизеопентипе**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Разбивает строку Юникода на отдельные фигурные элементы и предоставляет массив тегов функций для каждого фигурного элемента для обработки OpenType.                                  |
| [**скриптжустифи**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Создает таблицу предварительных ширины, чтобы разрешить обоснование текста при передаче функции [**скрипттекстаут**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) .                                                   |
| [**скриптлайаут**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Преобразует массив уровней выполнения при внедрении в карту с отображением визуального элемента в логическое и (или) с логического на визуальное расположение.                                                               |
| [**скриптплаце**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Формирует ширину глифа и сведения о двухфазной смещении из выходных данных [**скриптшапе**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).                                                       |
| [**скриптплацеопентипе**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Создает глифы и визуальные атрибуты для выполнения Юникода с информацией OpenType из выходных данных [**скриптшапеопентипе**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**скриптпоситионсинглеглиф**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Размещает один глиф с одной коррекцией, используя заданную функцию, указанную в шрифте для обработки OpenType.                                                         |
| [**скриптрекорддигитсубститутион**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Считывает собственные параметры подстановки цифр и цифр в многоязыковой поддержке (NLS) и записывает их в структуру [**сценария \_ дигитсубституте**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) . |
| [**скриптшапе**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Создает глифы и визуальные атрибуты для выполнения Юникода.                                                                                                                         |
| [**скриптшапеопентипе**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Создает глифы и визуальные атрибуты для выполнения Юникода с информацией OpenType.                                                                                               |
| [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Анализирует обычную текстовую строку.                                                                                                                                                     |
| [**скриптстрингкптокс**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Получает координату x для начального или конечного края позиции символа.                                                                                              |
| [**скриптстрингфри**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Освобождает структуру [**\_ \_ анализа строки скрипта**](script-string-analysis.md) .                                                                                                     |
| [**скриптстрингжетлогикалвидсс**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Преобразует визуальные значения ширины в логические.                                                                                                                                       |
| [**скриптстрингжетордер**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Создает массив, который сопоставляет исходное расположение символа с позицией глифа.                                                                                                    |
| [**скриптстрингаут**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Отображает строку, созданную при предыдущем вызове [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) , и при необходимости добавляет выделение.                                               |
| [**Скриптстринг \_ пкаутчарс**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Возвращает указатель на длину строки после обрезки.                                                                                                                       |
| [**Скриптстринг \_ плогаттр**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Возвращает указатель на буфер логических атрибутов для анализируемой строки.                                                                                                          |
| [**Скриптстринг \_ псизе**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Возвращает указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) для анализируемой строки.                                                                                                     |
| [**скриптстрингвалидате**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Проверяет структуру [**\_ \_ анализа строк сценария**](script-string-analysis.md) на наличие недопустимых последовательностей.                                                                              |
| [**скриптстрингкстокп**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Преобразует координату x в символьную точку.                                                                                                                                 |
| [**скриптсубститутесинглеглиф**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Включает подстановку одного глифа с одной альтернативной формой того же глифа для обработки OpenType.                                                                         |
| [**скрипттекстаут**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Отображает текст для указанной фигуры скрипта и сведения о размещении.                                                                                                               |
| [**скрипткстокп**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Формирует начальный или конечный края логического кластера символов из смещения x для выполнения.                                                                                 |



 

 

 
