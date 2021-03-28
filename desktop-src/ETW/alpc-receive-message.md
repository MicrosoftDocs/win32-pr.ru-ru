---
description: Этот класс является классом типа события для ALPC получения сообщений о событиях. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: Класс ALPC_Receive_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984533"
---
# <a name="alpc_receive_message-class"></a>ALPC \_ , \_ класс сообщения

Этот класс является классом типа события для ALPC получения сообщений о событиях.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Участники

Класс **\_ \_ сообщений ALPC получит** следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ сообщений о получении в ALPC** имеет следующие свойства.

<dl> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор сообщения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




