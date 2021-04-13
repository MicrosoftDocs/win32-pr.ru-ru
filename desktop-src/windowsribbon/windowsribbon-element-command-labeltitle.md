---
title: Свойство Command. Лабелтитле
description: Представляет заголовок метки.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Лента Windows для свойства Command. Лабелтитле
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535075"
---
# <a name="commandlabeltitle-property"></a>Свойство Command. Лабелтитле

Представляет заголовок метки.

## <a name="usage"></a>Использование

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
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

**Command. лабелтитле** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.

> [!Note]  
> Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.

 

Максимальная длина не ограничена.

Если для **Command. лабелтитле** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .

> [!Note]  
> Если **Command. лабелтитле** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .

 

**Command. лабелтитле** поддерживает только выравнивание по левому краю.

Если команда предоставляется через пункт меню, а значение **Command. лабелтитле** или [ \_ \_ подпись PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md) содержит букву, предшествующую амперсанду, как показано в следующем примере, эта буква рассматривается как KeyTip и сочетание клавиш для этой команды в инфраструктуре Ribbon.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Чтобы отобразить знак амперсанда в метке, необходимо экранировать Специальный символ с двойным амперсандом ( `&&` ), как показано в следующем примере.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. лабелтитле** .


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

[\_Метка PKEY пользовательского интерфейса \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





