---
description: Указывает тип изменения состояния службы для мониторинга и создания отчетов.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Перечисление SC_EVENT_TYPE (Винсвкп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664463"
---
# <a name="sc_event_type-enumeration"></a>\_ \_ Перечисление типов событий SC

Указывает тип изменения состояния службы для мониторинга и создания отчетов.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_ \_ изменение базы данных событий SC \_**
</dt> <dd>

Служба была добавлена или удалена. Параметр *хсервице* функции [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md) должен быть обработчиком SCM.

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_ \_ изменение свойства события \_ SC**
</dt> <dd>

Одно или несколько свойств службы были обновлены. Параметр *хсервице* функции [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md) должен быть маркером службы.

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_ \_ изменение состояния события \_ SC**
</dt> <dd>

Состояние службы изменилось. Параметр *хсервице* функции [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md) должен быть маркером службы.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винсвкп. h</dt> </dl> |



 

 




