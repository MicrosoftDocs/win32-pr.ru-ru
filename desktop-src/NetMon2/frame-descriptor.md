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
ms.openlocfilehash: 1e675c07eae46096878e7c0aa71b53ba5bf22194e82ad8cc5aa5b6070d7e27e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938575"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




