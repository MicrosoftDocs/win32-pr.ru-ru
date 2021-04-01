---
title: Структура MPSCAN_RESULT (Мпклиент. h)
description: Результаты проверки.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT структуры устаревшие функции среды Windows
- Функции PMPSCAN_RESULT указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262225"
---
# <a name="mpscan_result-structure"></a>\_Структура результата мпскан

Результаты проверки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a>Члены

<dl> <dt>

**ScanType**
</dt> <dd>

Тип: **[ **мпскан \_ тип**](mpscan-type.md)**

</dd> <dd>

Тип проверки. См. раздел [**\_ тип мпскан**](mpscan-type.md).

</dd> <dt>

**Источник**
</dt> <dd>

Тип: **[ **мпсаурце**](mpsource.md)**

</dd> <dd>

Источник сканирования, например инициированный пользователем или системой. См. [**мпсаурце**](mpsource.md).

</dd> <dt>

**скангуид**
</dt> <dd>

Тип: **GUID**

</dd> <dd>

Идентификатор проверки.

</dd> <dt>

**StartTime**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Время начала проверки.

</dd> <dt>

**EndTime**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Время окончания проверки.

</dd> <dt>

**среатстатс**
</dt> <dd>

Тип: **[ **мпсреат \_ stats**](mpthreat-stats.md)**

</dd> <dd>

Статистика, связанная с угрозами. См. [**мпсреат \_ stats**](mpthreat-stats.md).

</dd> <dt>

**ресаурцестатс**
</dt> <dd>

Тип: **[ **мпресаурце \_ stats**](mpresource-stats.md)**

</dd> <dd>

Статистика, связанная с ресурсами. См. [**мпресаурце \_ stats**](mpresource-stats.md).

</dd> <dt>

**Версия сигнатуры**
</dt> <dd>

Тип: **улонглонг**

</dd> <dd>

Версия подписи, используемой для проверки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Статистика мпресаурце**](mpresource-stats.md)
</dt> <dt>

[**\_тип мпскан**](mpscan-type.md)
</dt> <dt>

[**мпсаурце**](mpsource.md)
</dt> <dt>

[**\_Статистика мпсреат**](mpthreat-stats.md)
</dt> </dl>

 

 





