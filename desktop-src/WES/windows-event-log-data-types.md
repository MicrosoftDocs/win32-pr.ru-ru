---
title: Типы данных журнала событий Windows (Виневт. h)
description: Журнал событий Windows определяет следующие типы данных
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802189"
---
# <a name="windows-event-log-data-types"></a>Типы данных журнала событий Windows

Журнал событий Windows определяет следующие типы данных:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_обработчик evt**
</dt> <dd>

Маркер объекта журнала событий Windows.

</dd> <dt>

**ПЕВТ, \_ обработчик**
</dt> <dd>

Указатель на маркер объекта журнала событий Windows.

</dd> <dt>

**\_ \_ \_ маркер свойства массива объектов \_ evt**
</dt> <dd>

Маркер массива объектов журнала событий Windows.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виневт. h</dt> </dl> |



 

 





