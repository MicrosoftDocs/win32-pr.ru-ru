---
description: Структура ПРОТОКОЛИНФО описывает протокол.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Структура ПРОТОКОЛИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674084"
---
# <a name="protocolinfo-structure"></a>Структура ПРОТОКОЛИНФО

Структура **протоколинфо** описывает протокол.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**протоколид**
</dt> <dd>

Назначенный системой идентификатор протокола для указанного сеанса выполнения.

</dd> <dt>

**пропертидатабасе**
</dt> <dd>

База данных свойств указанного протокола.

</dd> <dt>

**ProtocolName**
</dt> <dd>

Сокращенное имя протокола.

</dd> <dt>

**HelpFile**
</dt> <dd>

Необязательное имя файла справки, связанное с протоколом.

</dd> <dt>

**Комментарий**
</dt> <dd>

Комментарий, описывающий протокол.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




