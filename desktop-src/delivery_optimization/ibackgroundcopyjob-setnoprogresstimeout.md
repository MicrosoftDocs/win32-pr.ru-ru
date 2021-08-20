---
title: Метод использованием метода ibackgroundcopyjob Сетнопрогресстимеаут (Deliveryoptimization. h)
description: Задает период времени, в течение которого оптимизация доставки (DO) пытается передавать файл после возникновения временной ошибки. Если происходит выполнение, таймер сбрасывается.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Метод Сетнопрогресстимеаут
- Метод Сетнопрогресстимеаут, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Сетнопрогресстимеаут
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcf6905388d54103aaac34ae934c89e2fd8ccc16ce32a384eb730376606351b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542931"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>Метод использованием метода ibackgroundcopyjob:: Сетнопрогресстимеаут

Задает период времени, в течение которого оптимизация доставки (DO) пытается передавать файл после возникновения временной ошибки. Если происходит выполнение, таймер сбрасывается.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ретрипериод* \[ окне\]
</dt> <dd>

Время в секундах, которое пытается переместить файл после того, как он не был выполнен. Период повтора по умолчанию для задания с высоким приоритетом составляет 3600 секунд (1 час), а для задания с низким приоритетом — 86400 секунд (24 часа).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                                          | Описание                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Период повтора успешно задан.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Remarks

Если не выполняется в течение периода повтора, то состояние задания перемещается с BG_JOB_STATE_TRANSIENT_ERROR на BG_JOB_STATE_ERROR. Если вы запрашиваете уведомление об ошибке, выполните вызов обратного вызова [**жоберрор**](https://www.bing.com/search?q=**JobError**) .

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

[**Использованием метода ibackgroundcopyjob:: Жетнопрогресстимеаут**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





