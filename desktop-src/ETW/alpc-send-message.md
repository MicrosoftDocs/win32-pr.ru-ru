---
description: Этот класс является классом типа событий для ALPC "Отправка сообщения о событиях". Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: Класс ALPC_Send_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154854"
---
# <a name="alpc_send_message-class"></a>ALPC. \_ Отправка \_ класса сообщения

Этот класс является классом типа событий для ALPC "Отправка сообщения о событиях".

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Участники

Класс **\_ \_ сообщения ALPC Send** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ сообщения ALPC Send** имеет следующие свойства.

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



 

 




