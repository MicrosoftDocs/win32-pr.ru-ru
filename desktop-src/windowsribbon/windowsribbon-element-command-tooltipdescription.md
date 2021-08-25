---
title: Свойство Command. Тултипдескриптион
description: Представляет описание подсказки.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- свойство Command. тултипдескриптион, Windows лента
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dd356ae3bcfa5949e8469240330a3a09a11f01b5a919ed02f4eb55683fbc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933214"
---
# <a name="commandtooltipdescription-property"></a>Свойство Command. Тултипдескриптион

Представляет описание подсказки.

## <a name="usage"></a>Использование

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
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

**Command. тултипдескриптион** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.

> [!Note]  
> Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.

 

Максимальная длина не ограничена.

Если для **Command. тултипдескриптион** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .

> [!Note]  
> Если **Command. тултипдескриптион** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .

 

**Command. тултипдескриптион** поддерживает только выравнивание по левому краю.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. тултипдескриптион** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[UI \_ PKEY \_ тултипдескриптион](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





