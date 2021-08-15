---
title: Структура MPCALLBACK_DATA (Мпклиент. h)
description: Данные, передаваемые функции обратного вызова.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA структуры устаревшие функции среды Windows
- функции PMPCALLBACK_DATA Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1eb129101c341485a1e6b5763a0325cbf586a6e51e5e2875b4465696c39df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883656"
---
# <a name="mpcallback_data-structure"></a>\_Структура данных мпкаллбакк

Данные, передаваемые функции обратного вызова.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**Уведомление**
</dt> <dd>

Тип: **[ **мпнотифи**](mpnotify.md)**

</dd> <dd>

Изменить уведомление на отчет.

</dd> <dt>

**Состав**
</dt> <dd>

Тип: **HRESULT**

</dd> <dd>

Код ошибки в случае внутреннего сбоя.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Текущая отметка времени.

</dd> <dt>

**Type**
</dt> <dd>

Тип: **[ **мпкаллбакк \_ тип**](mpcallback-type.md)**

</dd> <dd>

Специальный тип данных обратного вызова.

</dd> <dt>

**Данные**
</dt> <dd>

Специальные данные обратного вызова. Указатель на соответствующую структуру зависит от значения **типа**.

<dl> <dt>

**пстатусдата**
</dt> <dd>

Тип: **пмпстатус \_ Data** .

</dd> <dd>

При **вводе**  ==  **\_ состояния мпкаллбакк**. См. [**мпстатус \_ Data**](mpstatus-data.md).

</dd> <dt>

**пскандата**
</dt> <dd>

Тип: **пмпскан \_ Data** .

</dd> <dd>

При   ==  **\_ проверке типа мпкаллбакк**. См. [**мпскан \_ Data**](mpscan-data.md).

</dd> <dt>

**пклеандата**
</dt> <dd>

Тип: **пмпклеан \_ Data** .

</dd> <dd>

При **вводе типа**  ==  **мпкаллбакк \_ Clean**. См. [**мпклеан \_ Data**](mpclean-data.md).

</dd> <dt>

**ппречеккдата**
</dt> <dd>

Тип: **пмпклеан. \_ Проверка \_ данных**

</dd> <dd>

При   ==  **\_ проверке типа мпкаллбакк**. См. раздел [**мпклеан \_ recheck \_ Data**](mpclean-precheck-data.md).

</dd> <dt>

**псреатдата**
</dt> <dd>

Тип: **пмпсреат \_ Data** .

</dd> <dd>

При **типе**  ==  **мпкаллбакк \_ THREAT**. См. [**мпсреат \_ Data**](mpthreat-data.md).

</dd> <dt>

**псигупдатедата**
</dt> <dd>

Тип: **пмпсигупдате \_ Data** .

</dd> <dd>

При **типе**  ==  **мпкаллбакк \_ сигупдате**. См. [**мпсигупдате \_ Data**](mpsigupdate-data.md).

</dd> <dt>

**псампледата**
</dt> <dd>

Тип: **пмпсампле \_ Data** .

</dd> <dd>

При **вводе**  ==  **\_ образца Type мпкаллбакк**. См. [**мпсампле \_ Data**](mpsample-data.md).

</dd> <dt>

**пресерведдата**
</dt> <dd>

Тип: **пмпресервед \_ Data** .

</dd> <dd>

Если **тип**  ==  **мпкаллбакк \_ зарезервирован**. См. [**мпресервед \_ Data**](mpreserved-data.md).

</dd> <dt>

**пконфигуратиондата**
</dt> <dd>

Тип: **пмпконфигуратион \_ Data** .

</dd> <dd>

При   ==  **\_ \_ уведомлении о конфигурации типа мпкаллбакк**. См. [**мпконфигуратион \_ Data**](mpconfiguration-data.md).

</dd> <dt>

**пфастпасдата**
</dt> <dd>

Тип: **пмпфастпас \_ Data** .

</dd> <dd>

При **типе**  ==  **мпкаллбакк \_ фастпас**. См. [**мпфастпас \_ Data**](mpfastpath-data.md).

</dd> <dt>

**пекспиратиондата**
</dt> <dd>

Тип: **пмпекспиратион \_ Data** .

</dd> <dd>

При **вводе**  ==  **мпкаллбакк \_ \_ срока действия продукта**. См. [**мпекспиратион \_ Data**](mpexpiration-data.md).

</dd> <dt>

**пнисприватедата**
</dt> <dd>

Тип: **пмпнис \_ Private \_ Data**

</dd> <dd>

Если **введите**  ==  **мпкаллбакк \_ NIS \_ Private**. См. раздел [**мпнис \_ Private \_ Data**](mpnis-private-data.md).

</dd> <dt>

**феалсдата**
</dt> <dd>

Тип: **пмфеалс \_ Data** .

</dd> <dd>

При **типе**  ==  **\_ работоспособности мпкаллбакк**. См. [**мфеалс \_ Data**](mphealth-data.md).

</dd> <dt>

**пендофлифедата**
</dt> <dd>

Тип: **пмпендофлифе \_ Data** .

</dd> <dd>

При **типе**  ==  **мпкаллбакк \_ ендофлифе**. См. [**мпендофлифе \_ Data**](mpendoflife-data.md).

</dd> <dt>

**пмалваретоастдата**
</dt> <dd>

Тип: **пмпмалваретоаст \_ Data** .

</dd> <dd>

При **типе**  ==  **мпкаллбакк \_ малваретоаст**. См. [**мпмалваретоаст \_ Data**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип мпкаллбакк**](mpcallback-type.md)
</dt> <dt>

[**\_данные мпклеан**](mpclean-data.md)
</dt> <dt>

[**МПКЛЕАН \_ предпроверить \_ данные**](mpclean-precheck-data.md)
</dt> <dt>

[**\_данные мпконфигуратион**](mpconfiguration-data.md)
</dt> <dt>

[**\_данные мпендофлифе**](mpendoflife-data.md)
</dt> <dt>

[**\_данные мпекспиратион**](mpexpiration-data.md)
</dt> <dt>

[**\_данные мпфастпас**](mpfastpath-data.md)
</dt> <dt>

[**\_данные мфеалс**](mphealth-data.md)
</dt> <dt>

[**\_данные мпмалваретоаст**](mpmalwaretoast-data.md)
</dt> <dt>

[**МПНИС \_ закрытые \_ данные**](mpnis-private-data.md)
</dt> <dt>

[**мпнотифи**](mpnotify.md)
</dt> <dt>

[**\_данные мпресервед**](mpreserved-data.md)
</dt> <dt>

[**\_данные мпсампле**](mpsample-data.md)
</dt> <dt>

[**\_данные мпскан**](mpscan-data.md)
</dt> <dt>

[**\_данные мпсигупдате**](mpsigupdate-data.md)
</dt> <dt>

[**\_данные мпстатус**](mpstatus-data.md)
</dt> <dt>

[**\_данные мпсреат**](mpthreat-data.md)
</dt> </dl>

 

 





