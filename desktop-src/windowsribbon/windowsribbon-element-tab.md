---
title: Элемент Tab
description: Представляет базовую или контекстную вкладку.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- элемент вкладки Windows лента
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64f5bffb6a81a1efd112c3f52f5d1276f893e9cfb059a5f240a6c8c73b990c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441644"
---
# <a name="tab-element"></a>Элемент Tab

Представляет [базовую](windowsribbon-controls-tab.md) или [контекстную](windowsribbon-controls-tabgroup.md) вкладку.

## <a name="usage"></a>Использование

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
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
<td><strong>аппликатионмодес</strong><br/></td>
<td>xs:string<br/></td>
<td>нет<br/></td>
<td>Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.<br/> Пробелы допустимы и пропускаются.<br/> Максимальная длина: 250 символов. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                         | Описание                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [**Группа**](windowsribbon-element-group.md)<br/>                         | Может происходить один или несколько раз<br/> <br/> |
| [**TAB. Скалингполици**](windowsribbon-element-tab-scalingpolicy.md)<br/> | Может выполняться не более одного раза<br/> <br/>      |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                             |
|---------------------------------------------------------------------|
| [**Лента. вкладки**](windowsribbon-element-ribbon-tabs.md)<br/> |
| [**Группа вкладок**](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a>Remarks

Обязательный.

Должен быть хотя бы один раз для каждого элемента [**Ribbon. Табуляторы**](windowsribbon-element-ribbon-tabs.md) или [**табграуп**](windowsribbon-element-tabgroup.md) .

**Вкладка** поддерживает [режимы приложений](ribbon-applicationmodes.md).

Если для элемента **Tab** имеется [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) , то в **скалингполици. идеалсизес** требуется запись для каждого элемента [**группы**](windowsribbon-element-group.md) и его идеальный размер.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **вкладки** .

В этом разделе кода показаны объявления команд **вкладки** для вкладки " **Главная** ".


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



В этом разделе кода показаны объявления элементов управления **вкладки** .


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a>Сведения об элементе

- **минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: нет



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления табуляции](windowsribbon-controls-tab.md)
</dt> <dt>

[Элемент управления группы вкладок](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[**сетмодес**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

