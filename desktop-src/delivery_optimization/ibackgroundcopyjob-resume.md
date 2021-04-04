---
title: Метод Resume использованием метода ibackgroundcopyjob (Deliveryoptimization. h)
description: Активирует новое задание или перезапускает приостановленное задание.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Метод Resume
- Метод Resume, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135475"
---
# <a name="ibackgroundcopyjobresume-method"></a>Метод использованием метода ibackgroundcopyjob:: Resume

Активирует новое задание или перезапускает приостановленное задание.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                                          | Описание                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Задание успешно перезапущено.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | Нет файлов для передачи.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Комментарии

При создании задания изначально его работа приостанавливается. Вызов **Resume** перемещает задание в состояние передачи. Обратите внимание, что задание должно содержать один или несколько файлов перед вызовом этого метода.

Если задание находится в состоянии BG_JOB_STATE_TRANSIENT_ERROR или BG_JOB_STATE_ERROR, вызовите метод **Resume** , чтобы перезапустить задание после устранения ошибки.

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

[**Использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





