---
title: Константы состояния задания печати ADSI (Адсстс. h)
description: Для указания состояния задания печати используются следующие константы со свойством Иадспринтжобоператионс. status.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989101"
---
# <a name="adsi-print-job-status-constants"></a>Константы состояния задания печати ADSI

Для указания состояния задания печати используются следующие константы со свойством [**иадспринтжобоператионс. status**](iadsprintjoboperations-property-methods.md) .

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**\_Задание ADS \_ приостановлено**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Задание печати приостановлено.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_Ошибка задания \_ ADS**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Произошла ошибка.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_Удаление задания \_ ADS**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Удаляется задание печати.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_очередь заданий \_ ADS**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Задание печати помещается в очередь.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_печать задания \_ ADS**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Печатается задание печати.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**\_ \_ автономное задание AD**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Принтер отключен.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_Документация по заданию ADS \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



В принтере нет бумаги.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**\_печать задания \_ ADS**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Задание печати напечатано.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_Задание ADS \_ удалено**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Задание печати было удалено.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Адсстс. h</dt> </dl> |



 

 





