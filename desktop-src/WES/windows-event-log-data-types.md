---
title: Windows Типы данных журнала событий (Виневт. h)
description: Windows В журнале событий определены следующие типы данных
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c309dd52471bd501aa2668220d39882ab8de7e1c23a646084364659df4ae4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619994"
---
# <a name="windows-event-log-data-types"></a>Windows Типы данных журнала событий

Windows В журнале событий определены следующие типы данных:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_обработчик evt**
</dt> <dd>

обработчик для Windows объекта журнала событий.

</dd> <dt>

**ПЕВТ, \_ обработчик**
</dt> <dd>

указатель на маркер объекта журнала событий Windows.

</dd> <dt>

**\_ \_ \_ маркер свойства массива объектов \_ evt**
</dt> <dd>

маркер массива Windows объектов журнала событий.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виневт. h</dt> </dl> |



 

 





