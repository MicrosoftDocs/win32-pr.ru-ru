---
title: Перечисление BITS_JOB_PROPERTY_ID (Deliveryoptimization. h)
description: Перечисление BITS_JOB_PROPERTY_ID указывает идентификатор свойства для задания DO. Это перечисление используется в объединении BITS_JOB_PROPERTY_VALUE для определения типа значения, содержащегося в объединении.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- Перечисление BITS_JOB_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 803e776bd635cd600bf664354dda8703d224dffcd63ea751919875a6ea69233d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047152"
---
# <a name="bits_job_property_id-enumeration"></a>Перечисление BITS_JOB_PROPERTY_ID

Перечисление **BITS_JOB_PROPERTY_ID** указывает идентификатор свойства для задания Do. Это перечисление используется в объединении [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) для определения типа значения, содержащегося в объединении.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**
</dt> <dd>

Идентификатор, используемый для [управления поведением передачи](https://www.bing.com/search?q=control+transfer+behavior) по сотовой или подобной сети. Это свойство можно изменить, пока выполняется перемещение. новые флаги стоимости вступят в силу немедленно.

Это свойство использует поле **Dword** **BITS_JOB_PROPERTY_VALUE** .

</dd> <dt>

<span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**
</dt> <dd>

Идентификатор, используемый для [регистрации обратного вызова com](https://www.bing.com/search?q=register+a+COM+callback) по CLSID для получения уведомлений о ходе выполнения и выполнении задания. CLSID должен ссылаться на класс, связанный с зарегистрированным серверным COM-сервером. Его также можно установить в **GUID_NULL** , чтобы очистить ранее установленный CLSID уведомления.

Это свойство использует поле **CLsID** **BITS_JOB_PROPERTY_VALUE** s.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**
</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**
</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**
</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**
</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**
</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**
</dt> <dd>

Не поддерживается.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> <dt>

[**IBackgroundCopyJob5:: SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[**IBackgroundCopyJob5:: Property**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





