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
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891809"
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



 

## <a name="remarks"></a>Комментарии

Задание можно отменить в любое время. Однако задание нельзя восстановить после его отмены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
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

 

 





