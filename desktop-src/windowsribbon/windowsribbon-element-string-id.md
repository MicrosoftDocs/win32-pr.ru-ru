---
title: String.Id, свойство
description: Представляет уникальный идентификатор строкового ресурса.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- лента Windows свойства String.Id
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f9c1af4ba32982ce52ba470f6b3d1996abe11c81bdd520a4e50203adb56093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441654"
---
# <a name="stringid-property"></a>String.Id, свойство

Представляет уникальный идентификатор строкового ресурса.

## <a name="usage"></a>Использование

``` syntax
<String.Id/>
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

Значение для **String.ID** должно быть уникальным.

Идентификатор связан с определением строки в файле заголовка ленты, например `#define strSave 59999` .

Этот элемент содержит значение из объединения типов *xs: поситивеинтежер* и *xs: String*. Значение ограничивается целым числом от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.

Максимальная длина — 10 символов с необязательными нулями в начале.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **String.ID** .


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



 

 





