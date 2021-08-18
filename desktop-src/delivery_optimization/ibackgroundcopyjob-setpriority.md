---
title: Метод использованием метода ibackgroundcopyjob SetPriority (Deliveryoptimization. h)
description: Указывает уровень приоритета задания. Уровень приоритета определяет, когда задание обрабатывается относительно других заданий в очереди обмена.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Метод SetPriority
- Метод SetPriority, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод SetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ed1852d6990b94a000ac6affcec6020d266aaac5fae4611c3985a6f5c203aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542875"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>Метод использованием метода ibackgroundcopyjob:: SetPriority

Указывает уровень приоритета задания. Уровень приоритета определяет, когда задание обрабатывается относительно других заданий в очереди обмена.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Приоритет* \[ окне\]
</dt> <dd>

Указывает уровень приоритета задания относительно других заданий в очереди обмена. Значение по умолчанию — BG_JOB_PRIORITY_NORMAL. Список уровней приоритета см. в разделе Перечисление [**BG_JOB_PRIORITY**](bg-job-priority-.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                              | Описание                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Приоритет задания успешно установлен.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: предшествовал**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





