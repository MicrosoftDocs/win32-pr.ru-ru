---
description: '\_Структура дескрипторов кадров предоставляет описательные сведения о необработанных кадрах.'
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Структура FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673197"
---
# <a name="frame_descriptor-structure"></a>\_Структура дескриптора кадра

Структура **\_ дескрипторов кадров** предоставляет описательные сведения о необработанных кадрах.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a>Члены

<dl> <dt>

**фрамепоинтер**
</dt> <dd>

Указатель на данные кадра.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Системное время в микросекундах при записи кадра. Это время обычно используется для определения интервала между временем записи двух кадров.

</dd> <dt>

**фрамеленгс**
</dt> <dd>

Длина кадра.

</dd> <dt>

**нбитесаваил**
</dt> <dd>

Фактическая длина кадра скопирована.

</dd> <dt>

**ETYPE**
</dt> <dd>

Имя etype.

</dd> <dt>

**Протокола**
</dt> <dd>

Значение SAP.

</dd> <dt>

**ловпротокол**
</dt> <dd>

Индекс найденного протокола.

</dd> <dt>

**ловпротоколоффсет**
</dt> <dd>

Смещение к данным протокола, полученным от **ловпротокол**.

</dd> <dt>

**хигхпорт**
</dt> <dd>

Порт высокого протокола, определенный в **ловпротокол**.

</dd> <dt>

**хигхпротоколоффсет**
</dt> <dd>

Смещение к данным протокола, полученным от **хигхпорт**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




