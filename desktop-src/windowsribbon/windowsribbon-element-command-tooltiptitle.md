---
title: Свойство Command. Тултиптитле
description: Представляет заголовок подсказки.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Лента Windows для свойства Command. Тултиптитле
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492510"
---
# <a name="commandtooltiptitle-property"></a>Свойство Command. Тултиптитле

Представляет заголовок подсказки.

## <a name="usage"></a>Использование

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
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
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.

**Command. тултиптитле** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.

> [!Note]  
> Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.

 

Максимальная длина не ограничена.

Если для **Command. тултиптитле** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .

> [!Note]  
> Если **Command. тултиптитле** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .

 

**Command. тултиптитле** поддерживает только выравнивание по левому краю.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. тултиптитле** .


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[UI \_ PKEY \_ тултиптитле](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





