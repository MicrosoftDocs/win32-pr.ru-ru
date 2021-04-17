---
title: Структура TSMF_SUPPORT_NODEDATA_IN
description: Используется в \_ данных поддержки тсмф \_ \_ в структуре для хранения сведений о поддерживаемых форматах мультимедиа.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_NODEDATA_IN службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681918"
---
# <a name="tsmf_support_nodedata_in-structure"></a>\_Нодедата поддержки \_ тсмф \_ в структуре

Используется в [**\_ данных поддержки тсмф \_ \_ в**](tsmf-support-data-in.md) структуре для хранения сведений о поддерживаемых форматах мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a>Члены

<dl> <dt>

**byteCount**
</dt> <dd>

Размер структуры в байтах.

</dd> <dt>

**nodeId**
</dt> <dd>

Узел.

</dd> <dt>

**нуммедиатипес**
</dt> <dd>

Число структур формата мультимедиа.

</dd> <dt>

**...**
</dt> <dd>

Переменное число структур, определяющих форматы аудио-или видеоклипа. **Форматтипе** может иметь **Формат \_ Вавеформатекс** для аудио или **формата \_ мфвидеоформат** для видео.

Дополнительные сведения об этой структуре см. в разделе [TS \_ AM \_ Media \_ Type Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>         |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**ТСМФ \_ Поддержка \_ данных \_ в**](tsmf-support-data-in.md)
</dt> </dl>

 

