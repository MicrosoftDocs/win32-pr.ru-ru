---
title: Метод Ибаккграундкопикаллбакк Жоберрор (Deliveryoptimization. h)
description: Оптимизация доставки (DO) вызывает реализацию метода Жоберрор, когда состояние задания изменяется на BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Метод Жоберрор
- Метод Жоберрор, интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, метод Жоберрор
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 307ab18a0f956e5a2f4f14e9782f90b8ec6bff723da04aa9866566d95c53dca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543136"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>Метод Ибаккграундкопикаллбакк:: Жоберрор

Оптимизация доставки (DO) вызывает реализацию метода [**жоберрор**](https://www.bing.com/search?q=**JobError**) , когда состояние задания изменяется на BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пжоб* \[ окне\]
</dt> <dd>

Содержит сведения, связанные с заданиями, такие как число байтов и файлов, переданных до возникновения ошибки. Он также содержит методы для возобновления и отмены задания. Не освобождайте *пжоб*; Выпускайте интерфейс, когда метод [**жоберрор**](https://www.bing.com/search?q=**JobError**) возвращает значение.

</dd> <dt>

*perror* \[ окне\]
</dt> <dd>

Содержит сведения об ошибке, такие как обрабатываемый файл во время возникновения неустранимой ошибки и описание ошибки. Не освобождайте *perror*; Выпускайте интерфейс, когда метод [**жоберрор**](https://www.bing.com/search?q=**JobError**) возвращает значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод должен возвращать **S_OK**; в противном случае Вызывайте этот метод до тех пор, пока не будет возвращено **S_OK** . В целях повышения производительности следует ограничить количество возвращаемых значений, кроме **S_OK** , в несколько раз. В качестве альтернативы возврату кода ошибки рекомендуется всегда возвращать **S_OK** и обрабатывать ошибку внутренним образом. Интервал, с которым вызывается этот метод, является произвольным.

## <a name="remarks"></a>Remarks

Определив причину ошибки, выполните одно из следующих действий.

-   Чтобы отменить задание, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Чтобы принять часть задания, которая успешно передалася до возникновения ошибки, вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) . Этот параметр не применяется для отправки заданий. часть задания отправки выполнить нельзя.
-   Чтобы завершить обработку задания, устраните проблему, а затем вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .

Временные ошибки не создают вызовы метода [**жоберрор**](https://www.bing.com/search?q=**JobError**) .

Функция возвращает BG_ERROR_CONTEXT_REMOTE_FILE, если задание вызвало ошибку HTTP 403, BG_ERROR_CONTEXT_NONE в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback определен как 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md)
</dt> <dt>

[**ибаккграундкоперрор**](ibackgroundcopyerror.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





