---
title: Свойство String. Symbol
description: Представляет имя строкового ресурса.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- свойство String. Symbol Windows лента
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6c071461fcdeb5f2bbbdbb15fce0f3f6e6031edddf4bd18e034416ba8c49e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706866"
---
# <a name="stringsymbol-property"></a>Свойство String. Symbol

Представляет имя строкового ресурса.

## <a name="usage"></a>Использование

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                   |
|-----------------------------------------------------------|
| [**Строка**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**строки**](windowsribbon-element-string.md) .

Символ связан с определением строки в файле заголовка ленты, например `#define strSave 59999` .

Этот элемент содержит значение типа *xs: String*. Значение ограничивается строкой, состоящей из буквы или символа подчеркивания, за которой следует любая последовательность букв, цифр или знаков подчеркивания.

Максимальная длина — 100 символов.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **String. Symbol** .


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



 

 





