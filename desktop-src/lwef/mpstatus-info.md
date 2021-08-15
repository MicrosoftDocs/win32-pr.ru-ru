---
title: Структура MPSTATUS_INFO (Мпклиент. h)
description: Сведения о состоянии для диспетчера защиты от вредоносных программ.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO структуры устаревшие функции среды Windows
- функции PMPSTATUS_INFO Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: 8cb93bd15fe05955c9e8d87828d4b94b08e3d577659c629b52b3f908cb045ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883305"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
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

 

 





