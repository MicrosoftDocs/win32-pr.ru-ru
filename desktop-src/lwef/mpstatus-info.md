---
title: Структура MPSTATUS_INFO (Мпклиент. h)
description: Сведения о состоянии для диспетчера защиты от вредоносных программ.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO структуры устаревшие функции среды Windows
- Функции PMPSTATUS_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801247"
---
# <a name="mpstatus_info-structure"></a>\_Структура сведений о мпстатус

Сведения о состоянии для диспетчера защиты от вредоносных программ.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**продуктстатус**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Общее состояние продукта. Это сочетание битовых флагов из [**\_ флага мпстатус**](mpstatus-flag.md).

</dd> <dt>

**ласткуиккскан**
</dt> <dd>

Тип: **[ **мпскан \_ результат**](mpscan-result.md)**

</dd> <dd>

Результаты последней проверки с помощью диспетчера защиты от вредоносных программ. См. [**мпскан \_ result**](mpscan-result.md).

</dd> <dt>

**ластфуллскан**
</dt> <dd>

Тип: **[ **мпскан \_ результат**](mpscan-result.md)**

</dd> <dd>

Результаты последней полной проверки с помощью диспетчера защиты от вредоносных программ. См. [**мпскан \_ result**](mpscan-result.md).

</dd> <dt>

**среатстатс**
</dt> <dd>

Тип: **[ **мпсреат \_ stats**](mpthreat-stats.md)**

</dd> <dd>

Статистика активных угроз. См. [**мпсреат \_ stats**](mpthreat-stats.md).

</dd> <dt>

**среатстате**
</dt> <dd>

Тип: **[**мпсреат \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ угроза \_ stat \_ Max \_ Value + 1\]**

</dd> <dd>

Дополнительные данные статистики угроз, например число угроз. См. [**мпсреат \_ stats \_ Data**](mpthreat-stats-data.md).

</dd> <dt>

**Компонент**
</dt> <dd>

Тип: **[**мпкомпонент \_ Status**](mpcomponent-status.md) \[ мпкомпонент \_ MaxValue + 1\]**

</dd> <dd>

Массив состояний для нескольких компонентов. Используйте значение из перечисления [**мпкомпонент \_ ID**](mpcomponent-id.md) в качестве индекса в массиве.

</dd> <dt>

**продуктекспиратионтиме**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Метка времени истечения срока действия продукта в формате UNC. Это допустимо, только если задано состояние истечения срока действия.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_идентификатор мпкомпонент**](mpcomponent-id.md)
</dt> <dt>

[**\_состояние мпкомпонент**](mpcomponent-status.md)
</dt> <dt>

[**МПСКАН \_ результат**](mpscan-result.md)
</dt> <dt>

[**\_флаг мпстатус**](mpstatus-flag.md)
</dt> <dt>

[**\_Статистика мпсреат**](mpthreat-stats.md)
</dt> <dt>

[**\_данные статистики \_ мпсреат**](mpthreat-stats-data.md)
</dt> </dl>

 

 





