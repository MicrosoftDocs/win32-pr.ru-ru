---
title: Средство выбора цвета Drop-Down
description: Платформа Windows Ribbon предоставляет специализированный элемент управления "Выбор цвета" Drop-Down, который предоставляет разнообразные параметры цвета с помощью кнопки разделения и настраиваемого выбора раскрывающегося цвета.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443665"
---
# <a name="drop-down-color-picker"></a>Средство выбора цвета Drop-Down

Платформа Windows Ribbon предоставляет специализированный элемент управления "Выбор цвета" Drop-Down, который предоставляет разнообразные параметры цвета с помощью кнопки разделения и настраиваемого выбора раскрывающегося цвета.

-   [Введение](#introduction)
-   [разметку](#markup)
-   [Код](#code)
    -   [Свойства](#properties)
    -   [Обработчики команд](#command-handlers)
-   [Связанные темы](#related-topics)

## <a name="introduction"></a>Введение

Имитируя внешний вид и функциональность средства выбора цвета Microsoft Office, платформа Ribbon может использовать оба преимущества, а также обеспечивать согласованность и знание широкого спектра приложений.

## <a name="markup"></a>разметку

Как и все элементы управления Ribbon, палитра Drop-Down цвета легко реализуется и настраивается с помощью разметки. Платформа предоставляет ряд атрибутов элементов для средства выбора цвета Drop-Down для предоставления различных уровней функциональности. В следующей таблице перечислены атрибуты палитры цветов Drop-Down.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>колортемплате</td>
<td>Шаблоны макета, указывающие тип Drop-Down палитры.<br/> Существует три шаблона, каждый из которых задает макет элемента управления и значения по умолчанию для связанных атрибутов и ключей свойств. <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>чипсизе</td>
<td>Размер каждой цветовой микросхемы (или образца).<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>Столбцы</td>
<td>Число столбцов цветовой микросхемы (или образцов).<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>Имя связанного объявления команды. <br/></td>
</tr>
<tr class="odd">
<td>исаутоматикколорбуттонвисибле</td>
<td>Отображает (или скрывает) <strong>автоматическую</strong> кнопку.<br/> Допустим, только если <em>колортемплате</em> имеет значение <code>ThemeColors</code> или <code>StandardColors</code> .<br/></td>
</tr>
<tr class="even">
<td>исноколорбуттонвисибле</td>
<td>Отображает (или скрывает) кнопку <strong>без цвета</strong> .<br/> Допустимо для всех значений <em>колортемплате</em> .<br/></td>
</tr>
<tr class="odd">
<td>рецентколоргридровс</td>
<td>Число строк цветовой микросхемы (или образца) в области " <strong>Последние цвета</strong> ".<br/> Допустимо, только если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .<br/></td>
</tr>
<tr class="even">
<td>стандардколоргридровс</td>
<td>Число строк цветовой микросхемы (или образца) в области <strong>Стандартные цвета</strong> .<br/></td>
</tr>
<tr class="odd">
<td>семеколоргридровс</td>
<td>Число строк цветовой микросхемы (или образца) в области <strong>цвета темы</strong> .<br/> Допустимо, только если <em>колортемплате</em> имеет значение <code>ThemeColors</code> .<br/></td>
</tr>
</tbody>
</table>



 

На следующих снимках экрана показаны макеты палитры Drop-Down по умолчанию для трех цветовых шаблонов.



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ снимок экрана новой строки для \] ![ элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение "семеколорс". ](images/markup/colortemplate.themedcolors.1.png) \[ новой строки\] | `standardcolors`: \[ снимок экрана новой строки для \] ![ элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение "стандардколорс". ](images/markup/colortemplate.standardcolors.3.png) \[ новой строки\] | `highlightcolors`: \[ снимок экрана новой строки для \] ![ элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение "хигхлигхтколорс".](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

Базовая разметка, необходимая для каждого типа средства выбора цвета Drop-Down, показана в следующих примерах:

> [!Note]  
> Палитра Drop-Down Color — это допустимый элемент управления ["Кнопка"](windowsribbon-controls-button.md) в шаблоне [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .

 


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a>Код

В качестве специализированного элемента управления, поддерживающего настройку, любая реализация средства выбора цвета Drop-Down, которая использует преимущества этих возможностей, требует специального кода приложения для управления свойствами и обработки всех команд, выдаваемых элементом управления.

### <a name="properties"></a>Свойства

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "Выбор цвета" Drop-Down.

Как правило, свойство выбора цвета для Drop-Down обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления "Выбор цвета" Drop-Down.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Ключ свойства</th>
<th>Описание</th>
<th>Примечания</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Определяет метку для кнопки <strong>автоматического</strong> цвета.<br/> Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> или <code>StandardColors</code> .<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Определяет выбранное значение цвета как <a href="/windows/win32/gdi/colorref">COLORREF</a>.<br/> Допустимо только в том случае, если <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> имеет значение <code>UI_SWATCHCOLORTYPE_RGB</code> .<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Определяет выбранный тип цвета.<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Определяет возможность элемента управления реагировать на взаимодействие с пользователем.<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Определяет символьную строку для метки элемента управления.<br/></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Определяет крупное изображение высокой контрастности, отображаемое для элемента управления.<br/></td>
<td>Может обновляться только через недействительность.<br/> Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Определяет крупное изображение, отображаемое для элемента управления.<br/></td>
<td>Может обновляться только через недействительность.<br/> Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Определяет метку для кнопки " <strong>другие цвета</strong> ".<br/> Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> или <code>StandardColors</code> .<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Определяет метку для кнопки <strong>без цвета</strong> .<br/> Допустимо для всех значений <em>колортемплате</em> .<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Определяет метку для категории " <strong>Последние цвета</strong> ".<br/> Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> . Это единственный шаблон, содержащий помеченные категории.<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Определяет небольшое изображение с высокой контрастностью, отображаемое для элемента управления.<br/></td>
<td>Может обновляться только через недействительность.<br/> Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Определяет небольшое изображение, отображаемое для элемента управления.<br/></td>
<td>Может обновляться только через недействительность.<br/> Дополнительные сведения о форматах изображений см. в разделе <a href="windowsribbon-imageformats.md">указание ресурсов изображения ленты</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Определяет массив значений <a href="/windows/win32/gdi/colorref">COLORREF</a> для образцов палитры цветов Drop-Down.<br/> Каждый Drop-Down палитра цветов <em>колортемплате</em> содержит <code>StandardColors</code> сетку. <br/>
<blockquote>
[!Note]<br />
Отобразятся значения <a href="/windows/win32/gdi/colorref">COLORREF</a> из начальных <em>столбцов</em> <em>стандардколоргридровс</em> x массива. Если массив определяет меньше цветов, чем число <code>StandardColors</code> образцов, объявленных в разметке, для недостающих микросхем отображаются пустые пробелы.
</blockquote>
<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Определяет метку для категории " <strong>Стандартные цвета</strong> ".<br/> Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> . Это единственный шаблон, содержащий помеченные категории.<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Определяет строковый массив всплывающих подсказок палитры цветов для <code>StandardColors</code> сетки.<br/> Каждый Drop-Down палитра цветов <em>колортемплате</em> содержит <code>StandardColors</code> сетку. <br/>
<blockquote>
[!Note]<br />
Используются только подсказки, необходимые для метки цветовых палитр, отображаемых в <code>StandardColors</code> сетке. Если указано меньшее количество меток, чем число образцов в <code>StandardColors</code> сетке, для образцов ремаинининг предоставляется значение по умолчанию.
</blockquote>
<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Определяет массив значений <a href="/windows/win32/gdi/colorref">COLORREF</a> для образцов палитры цветов Drop-Down.<br/> Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Отобразятся значения <a href="/windows/win32/gdi/colorref">COLORREF</a> из начальных <em>столбцов</em> <em>семеколоргридровс</em> x массива. Если массив определяет меньше цветов, чем число <code>ThemeColors</code> образцов, объявленных в разметке, для недостающих микросхем отображаются пустые пробелы.
</blockquote>
<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Определяет строковый массив всплывающих подсказок палитры цветов для <code>ThemeColors</code> сетки.<br/> Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Используются только подсказки, необходимые для метки цветовых палитр, отображаемых в <code>ThemeColors</code> сетке. Если указано меньшее количество меток, чем число образцов в <code>ThemeColors</code> сетке, для образцов ремаинининг предоставляется значение по умолчанию.
</blockquote>
<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Определяет метку для категории <strong>цветов темы</strong> .<br/> Допустим только в том случае, если <em>колортемплате</em> имеет значение <code>ThemeColors</code> . Это единственный шаблон, содержащий помеченные категории.<br/></td>
<td>Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Определяет строку символов для описания подсказки, связанной с <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.<br/></td>
<td>Может обновляться только через недействительность.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Определяет строку символов для всплывающей подсказки команды.<br/></td>
<td>Может обновляться только через недействительность.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Обработчики команд

Метод [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) используется для настройки палитры Drop-Down цветом с помощью перечисленных выше ключей свойств. В следующем примере показано, как задать образцы цветов для палитры Drop-Down цвета на основе предпочтения пользовательского стиля или сетки пользовательских образцов, объявленной в разметке.


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



В следующем примере демонстрируется реализация метода [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) , который предоставляет цвет образца палитры Drop-Down цветов для приложения ленты.


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Библиотека элементов управления платформы Windows ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Дропдовнколорпиккер, элемент разметки**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md)
</dt> <dt>

[Пример Дропдовнколорпиккер](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

