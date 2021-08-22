---
description: Свойство ReadyState извлекает значение свойства ReadyState объекта Мсвебдвд.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Свойство ReadyState (ОЦидл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: 029798e66d8ed69dc18bbb23dafc8b047d770f1bc91ac1b86ca7bdb09963c2e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072788"
---
# <a name="readystate-property"></a>Свойство ReadyState

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ReadyState`Свойство получает значение свойства readyState объекта **мсвебдвд** .

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее параметр ReadyState элемента управления.



| Код возврата | Описание                                               |
|-------------|-----------------------------------------------------------|
| 0           | Состояние инициализации по умолчанию.                             |
| 1           | Объект загружает свойства.                         |
| 2           | Объект инициализирован.                              |
| 3           | Объект является интерактивным, но не все его данные доступны. |
| 4           | Объект получил все свои данные.                         |



 

## <a name="remarks"></a>Remarks

Это свойство доступно только для чтения и не имеет значения по умолчанию.

Любой объект, внедренный в веб-страницу, предоставляет `ReadyState` свойство.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>ОЦидл. h</dt> </dl> |



 

 




