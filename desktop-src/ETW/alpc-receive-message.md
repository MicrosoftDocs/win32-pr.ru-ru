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
ms.openlocfilehash: 98a565ea445ddd803ce217abca3993c2561d464829635bbb1a546824f27c3b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070364"
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

## <a name="members"></a>Члены

Класс **\_ \_ сообщений ALPC получит** следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




