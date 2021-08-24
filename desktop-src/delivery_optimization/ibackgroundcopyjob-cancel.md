---
title: Метод Cancel использованием метода ibackgroundcopyjob (Deliveryoptimization. h)
description: Удаляет задание из очереди передачи и удаляет связанные временные файлы из клиента (загрузки) и сервера (отправки).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Метод Cancel
- Метод Cancel, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c30fa0d7dcc4aa6137fbfef8d40a91d4839bc59d624c8ba2c942fb6c2041fccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635854"
---
# <a name="ibackgroundcopyjobcancel-method"></a>Метод использованием метода ibackgroundcopyjob:: Cancel

Удаляет задание из очереди передачи и удаляет связанные временные файлы из клиента (загрузки) и сервера (отправки).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                                          | Описание                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Задание успешно отменено.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Невозможно отменить задание, состояние которого BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Remarks

Задание можно отменить в любое время. Однако задание нельзя восстановить после его отмены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





