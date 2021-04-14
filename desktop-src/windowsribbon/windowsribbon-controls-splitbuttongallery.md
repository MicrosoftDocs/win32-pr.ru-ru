---
title: Коллекция разделенных кнопок
description: Коллекция разворачивающихся кнопок — это составной элемент управления, который содержит основную кнопку, предоставляющую один элемент или команду по умолчанию, и вспомогательную кнопку, которая при нажатии отображает остальную часть элемента или коллекции команд в взаимно исключающем раскрывающемся списке.
ms.assetid: c0fcfe72-d2e9-465d-941a-b3832b36b8c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1865949c1b6f3e274b01d0b4e454dc42e619c2c0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104413928"
---
# <a name="split-button-gallery"></a>Коллекция разделенных кнопок

Коллекция разворачивающихся кнопок — это составной элемент управления, который содержит основную кнопку, предоставляющую один элемент или команду по умолчанию, и вспомогательную кнопку, которая при нажатии отображает остальную часть элемента или коллекции команд в взаимно исключающем раскрывающемся списке.

-   [Подробные сведения](#details)
-   [Свойства коллекции разделенных кнопок](#split-button-gallery-properties)
-   [См. также](#related-topics)

## <a name="details"></a>Сведения

Этот элемент управления полезен для предоставления тесно связанных элементов в случаях, когда доступно очевидное по умолчанию, а отдельные элементы могут быть представлены изображением, текстом или обоими.

На следующем снимке экрана показана коллекция кнопок разделения ленты в Microsoft Paint.

![снимок экрана элемента управления сплитбуттонгаллери на ленте Microsoft Paint.](images/controls/splitbuttongallery.png)

## <a name="split-button-gallery-properties"></a>Свойства коллекции разделенных кнопок

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления коллекции разворачивающихся кнопок.

Как правило, свойство коллекции разделенных кнопок обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления коллекции "разворачивающаяся кнопка".



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ключ свойства</th>
<th>Примечания</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(допустимо только для коллекции элементов)<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.
<blockquote>
[!Note]<br />
Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Может обновляться только через недействительность.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Сплитбуттонгаллери, элемент разметки**](windowsribbon-element-splitbuttongallery.md)
</dt> <dt>

[Работа с коллекциями](ribbon-controls-galleries.md)
</dt> <dt>

[Пример коллекции](windowsribbon-gallerysample.md)
</dt> </dl>

