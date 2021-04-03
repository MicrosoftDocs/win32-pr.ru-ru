---
title: String.Id, свойство
description: Представляет уникальный идентификатор строкового ресурса.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Лента Windows для свойства String.Id
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137194"
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



## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 





