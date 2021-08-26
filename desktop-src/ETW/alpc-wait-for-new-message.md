---
description: Этот класс является классом типа событий для ALPC ожидание новых событий сообщения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: Класс ALPC_Wait_For_New_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67b3e52e59345eea95db7485e0764f31f88669241159ffc857d46cf230a5e8b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901554"
---
# <a name="alpc_wait_for_new_message-class"></a>ALPC. \_ Ожидание \_ \_ нового \_ класса сообщений

Этот класс является классом типа событий для ALPC ожидание новых событий сообщения.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a>Члены

В **ALPC \_ Ожидание \_ \_ нового класса \_ сообщений** входят следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

В **ALPC \_ Ожидание \_ \_ нового класса \_ сообщений** имеются следующие свойства.

<dl> <dt>

**иссерверпорт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли порт портом сервера.

</dd> <dt>

**портнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, содержащая имя порта, в котором находится ожидание ALPC.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




