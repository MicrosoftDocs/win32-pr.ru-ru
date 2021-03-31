---
title: Элемент Application
description: Представляет элемент верхнего уровня в спецификации разметки платформы Windows Ribbon.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Лента Windows для элементов приложения
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797185"
---
# <a name="application-element"></a>Элемент Application

Представляет элемент верхнего уровня в спецификации разметки платформы Windows Ribbon.

## <a name="usage"></a>Использование

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>Атрибуты



| attribute            | Тип                 | Обязательно       | Описание                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Да<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> Универсальный код ресурса (URI) для привязки пространства имен разметки ленты. <br/> </dd> </dl> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                               | Описание                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> | Может выполняться не более одного раза<br/> <br/>  |
| [**Application. views**](windowsribbon-element-application-views.md)<br/>       | Должно выполняться только один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы

Нет родительских элементов.

## <a name="remarks"></a>Комментарии

Обязательный.

Должен выполняться ровно один раз в качестве контейнера для всей разметки ленты.

Дочерние элементы элемента **Application** должны находиться в указанном порядке:

1.  [**Application. Commands**](windowsribbon-element-application-commands.md)
2.  [**Application. views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Примеры

В следующем примере показано объявление элемента **приложения** .


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>Сведения об элементе



|                                     |           |
|-------------------------------------|-----------|
| Минимальная поддерживаемая система<br/> | Windows 7 |
| Может быть пустым                        | Нет        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объявление команд и элементов управления с разметкой ленты](windowsribbon-schema.md)
</dt> </dl>

 

 





