---
title: Свойство String. Content
description: Представляет содержимое строкового ресурса.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Лента Windows свойства String. Content
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701035"
---
# <a name="stringcontent-property"></a>Свойство String. Content

Представляет содержимое строкового ресурса.

## <a name="usage"></a>Использование

``` syntax
<String.Content/>
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

Этот элемент содержит значение типа *xs: String*. Значение ограничено строкой, состоящей из любой последовательности символов, включая пробелы и символы разрыва строки.

Максимальная длина не ограничена.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **String. Content** .


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



 

 





