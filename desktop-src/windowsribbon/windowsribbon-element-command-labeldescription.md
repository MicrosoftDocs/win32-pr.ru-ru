---
title: Свойство Command. Лабелдескриптион
description: Представляет описание метки.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- свойство Command. лабелдескриптион, Windows лента
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9051b4f645744416f290906559e054405726f36f9616e8f38f3cfbae357137dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964213"
---
# <a name="commandlabeldescription-property"></a>Свойство Command. Лабелдескриптион

Представляет описание метки.

## <a name="usage"></a>Использование

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                   | Описание                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Строка**](windowsribbon-element-string.md)<br/> | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                     |
|-------------------------------------------------------------|
| [**Команда**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.

**Command. лабелдескриптион** может содержать значение *типа xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.

> [!Note]  
> Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.

 

Максимальная длина не ограничена.

Если для **Command. лабелдескриптион** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .

> [!Note]  
> Если **Command. лабелдескриптион** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .

 

**Command. лабелдескриптион** поддерживает только выравнивание по левому краю.

## <a name="examples"></a>Примеры

В следующем примере показан манифест команд буфера обмена с различными объявлениями **Command. лабелдескриптион** .


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[UI \_ PKEY \_ лабелдескриптион](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





