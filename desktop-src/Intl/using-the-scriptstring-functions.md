---
description: Для приложения, которое работает с неформатированным текстом, Uniscribe предоставляет \* функции скриптстринг.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Использование функций Скриптстринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6685af7dad2c9e1b8d0cf460d526155f967a9105e1b107047afb99c18a5124f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389410"
---
# <a name="using-the-scriptstring-functions"></a>Использование функций Скриптстринг

Для приложения, которое работает с неформатированным текстом, Uniscribe предоставляет функции **скриптстринг \** _. Эти функции похожи на [_ *ExtTextOut* *](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)и [**жеттекстекстент**](/cpp/mfc/reference/cdc-class#gettextextent), но они обеспечивают полную поддержку сложных скриптов, включая размещение курсора. Эти функции похожи на другие функции Uniscribe, но адаптированы к более простым требованиям обработки обычного текста.

В следующей таблице описаны функции **скриптстринг \*** и любые аналоги в других функциях Uniscribe.



<table>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>скриптстринганалисе</strong></a></td>
<td>Анализирует обычный текст. Эта функция соответствует следующим функциям:<br/> <dl><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>скриптитемизе</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>скриптшапе</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>скриптплаце</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>скриптбреак</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>скриптжеткмап</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>скриптжустифи</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>скриптлайаут</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>скриптстрингкптокс</strong></a></td>
<td>Получает координату x для позиции символа. Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>скрипткптокс</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>скриптстрингфри</strong></a></td>
<td>Освобождает структуру <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>скриптстрингжетлогикалвидсс</strong></a></td>
<td>Преобразует визуальные значения ширины в логические. Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>скриптжетлогикалвидсс</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>скриптстрингжетордер</strong></a></td>
<td>Карты позиции глифов символов аналогичным образом для <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">жетчарактерплацемент</a>, только для устаревшего использования. Эта функция плохо работает с скриптами, которые создают более одного глифа для каждой кодовой точки.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>скриптстрингаут</strong></a></td>
<td>Отображает обычный текст. Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>скрипттекстаут</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></td>
<td>Возвращает указатель на длину обрезанной простой текстовой строки.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></td>
<td>Возвращает указатель на буфер логических атрибутов для проанализированной простой текстовой строки.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></td>
<td>Возвращает указатель на размер (ширину и высоту) для проанализированной простой текстовой строки.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>скриптстрингвалидате</strong></a></td>
<td>Определяет последовательности кодовых точек, недопустимые в данном скрипте. Эта функция отличается от <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>скриптжеткмап</strong></a>, которая идентифицирует кодовые точки, отсутствующие в шрифте.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>скриптстрингкстокп</strong></a></td>
<td>Преобразует координату x в символьную точку. Эта функция соответствует <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>скрипткстокп</strong></a>.</td>
</tr>
</tbody>
</table>

Чтобы отобразить только обычный текст без каких бы то ни было изменений, приложение должно вызвать [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**скриптстрингаут**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), а затем [**скриптстрингфри**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree). Другие функции используются для изменения обычного текста перед отображением.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
