---
description: Этот класс является классом типа событий для событий окончания ожидания ALPC. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: Класс ALPC_Unwait
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542767"
---
# <a name="alpc_unwait-class"></a>Класс "ALPC — \_ Ожидание"

Этот класс является классом типа событий для событий окончания ожидания ALPC.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a>Участники

Класс **\_ неожиданий в ALPC** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **с \_ неожиданием «ALPC** » имеет следующие свойства.

<dl> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние из операции ожидания.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




