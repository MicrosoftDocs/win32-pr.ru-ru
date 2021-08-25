---
title: Command.Id, свойство
description: Представляет уникальный идентификатор для команды.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- лента Windows свойства Command.Id
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c542cbf4103c6063a177990d454a45e5f937745720c7c0a7bc5c60c4c1047e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931622"
---
# <a name="commandid-property"></a>Command.Id, свойство

Представляет уникальный идентификатор для команды.

## <a name="usage"></a>Использование

``` syntax
<Command.Id/>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                     |
|-------------------------------------------------------------|
| [**Команда**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.

Идентификатор связан с определением команды в файле заголовка ленты, например `#define cmdSave 25003 /* Save */` .

Этот элемент содержит значение из объединения типов *xs: поситивеинтежер* и *xs: String* , ограничивающее целочисленное значение от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном виде включительно.

Максимальная длина — 10 символов, включая необязательные нули в начале.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command.ID** .


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
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



 

 





