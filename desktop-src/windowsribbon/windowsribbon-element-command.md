---
title: Command, элемент
description: Представляет определение команды.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Лента Windows для командных элементов
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443485"
---
# <a name="command-element"></a>Command, элемент

Представляет определение команды.

## <a name="usage"></a>Использование

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Комментарий</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Используется для добавления аннотации в элемент Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> Максимальная длина: 250 символов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs: Поситивеинтежер Union xs: String<br/></td>
<td>Нет<br/></td>
<td>Уникальный идентификатор ресурса. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Объединение xs: Поситивеинтежер и xs: String)<br/> </dt> <dd> Целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем. <br/> Максимальная длина — 10 символов, включая необязательные нули в начале. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Keytip</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Строка, представляющая сочетание клавиш для элемента Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>лабелдескриптион</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Строка, представляющая текст, отображаемый в элементе Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>лабелтитле</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Строка, представляющая текст, отображаемый в элементе Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Имя</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из буквы или символа подчеркивания, за которой следует любая последовательность цифр, букв или знаков подчеркивания.<br/> Максимальная длина: 100 символов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Символ</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из буквы или символа подчеркивания, за которой следует любая последовательность цифр, букв или знаков подчеркивания.<br/> Максимальная длина: 100 символов.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>тултипдескриптион</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Строка, представляющая текст, отображаемый в элементе Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>тултиптитле</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Строка, представляющая текст, отображаемый в элементе Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                     | Описание                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Command. комментарий**](windowsribbon-element-command-comment.md)<br/>                                 | Может выполняться не более одного раза<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Может выполняться не более одного раза<br/> <br/> |
| [**Command. keytip**](windowsribbon-element-command-keytip.md)<br/>                                   | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Лабелдескриптион**](windowsribbon-element-command-labeldescription.md)<br/>               | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Лабелтитле**](windowsribbon-element-command-labeltitle.md)<br/>                           | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Ларжехигхконтрастимажес**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Ларжеимажес**](windowsribbon-element-command-largeimages.md)<br/>                         | Может выполняться не более одного раза<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Смаллхигхконтрастимажес**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Смаллимажес**](windowsribbon-element-command-smallimages.md)<br/>                         | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Может выполняться не более одного раза<br/> <br/> |
| [**Command. Тултиптитле**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Может происходить один или несколько раз для каждого элемента [**Application. Commands**](windowsribbon-element-application-commands.md) .

Дочерние элементы элемента **Command** могут происходить в любом порядке.

Как правило, ресурсы команды объявляются в разметке ленты, но их также можно задать во время выполнения с помощью вызова [**сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). Например, можно задать свойство [UI \_ PKEY \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md) для команды вместо объявления значения в разметке с помощью элемента [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .

В случаях, когда свойства команды, такие как метки и изображения, не могут быть заданы с помощью [**сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , их можно сделать недействительными при вызове [**инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand). После недействительности платформа запрашивает в ведущем приложении сведения о ресурсе.

> [!Note]  
> Невозможно восстановить ресурс из таблицы ресурсов разметки после того, как она стала недействительной.

 

В файл заголовка разметки ленты добавляется определение команды для каждой **команды** , объявленной в разметке.

Значение *KeyTip* выступает в качестве сочетания клавиш для команды, если эта команда не предоставлена через пункт меню. В этом случае платформа игнорирует значение *KeyTip* и вместо этого использует символ, предшествующий амперсанду, как указано в *лабелтитле* или [ \_ \_ метке PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md). Если амперсанд не указан с помощью *лабелтитле* или \_ метки PKEY пользовательского интерфейса \_ , keytip или сочетание клавиш не предоставляются.

## <a name="examples"></a>Примеры

В следующем примере показан манифест элементов **команды** для вкладки " **Главная** ".


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a>Сведения об элементе

* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



 

