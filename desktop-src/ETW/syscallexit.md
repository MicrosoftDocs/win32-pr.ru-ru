---
description: Этот класс является классом типа события для событий выхода из системного вызова. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Класс Сискаллексит
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985697"
---
# <a name="syscallexit-class"></a>Класс Сискаллексит

Этот класс является классом типа события для событий выхода из системного вызова.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Участники

Класс **сискаллексит** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **сискаллексит** имеет следующие свойства.

<dl> <dt>

**сискаллнтстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Format ("x")
</dt> </dl>

Код состояния, возвращенный системным вызовом NT.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




