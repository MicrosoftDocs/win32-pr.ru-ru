---
title: Метод использованием метода ibackgroundcopyjob-Error (Deliveryoptimization. h)
description: Возвращает интерфейс ошибки после возникновения ошибки.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Метод метода с ошибками
- Метод использованием метода ibackgroundcopyjob, интерфейс
- Интерфейс использованием метода ibackgroundcopyjob, метод method
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415533"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>Метод использованием метода ibackgroundcopyjob:: Error

Возвращает интерфейс ошибки после возникновения ошибки.

Оптимизация доставки (DO) создает объект Error, если состояние задания — BG_JOB_STATE_ERROR или BG_JOB_STATE_TRANSIENT_ERROR. Служба не создает объект Error при сбое вызова метода интерфейса **ибаккграундкопикскскскс** . Объект Error доступен до тех пор, пока не начнется передача данных (состояние задания меняется на BG_JOB_STATE_TRANSFERRING) для задания или до выхода из приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пперрор* \[ заполняет\]
</dt> <dd>

Интерфейс ошибки, который предоставляет код ошибки, описание ошибки и контекст, в котором произошла ошибка. Этот параметр также определяет файл, который передается в момент возникновения ошибки. Выпустите *пперрор* по завершении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                                                           | Описание                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                              | Объект ошибки успешно создан.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | Интерфейс Error доступен только после возникновения ошибки (BG_JOB_STATE_ERROR или BG_JOB_STATE_TRANSIENT_ERROR) и перед началом передачи данных (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Комментарии

Задание помещается в состояние ошибки при неустранимых ошибках. Чтобы определить, является ли задание ошибкой, используйте один из следующих параметров:

-   Чтобы опросить состояние задания, вызовите метод [**использованием метода ibackgroundcopyjob:: with State**](ibackgroundcopyjob-getstate.md) . Задание находится в ошибке, если состояние BG_JOB_STATE_ERROR.
-   Чтобы получить уведомление при возникновении ошибки, реализуйте интерфейс [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) (в частности, метод [**жоберрор**](https://www.bing.com/search?q=**JobError**) ). Затем вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md) , чтобы зарегистрировать обратный вызов и метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](ibackgroundcopyjob-setnotifyflags.md) для установки флага BG_NOTIFY_JOB_ERROR.

Интерфейс [**ибаккграундкоперрор**](ibackgroundcopyerror.md) содержит сведения, которые используются для определения причины ошибки, а также в случае, если процесс перемещения может быть продолжен. Определив причину ошибки, выполните одно из следующих действий.

-   Чтобы отменить задание, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Чтобы сохранить файлы, которые были успешно переданы до возникновения ошибки, вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .
-   Чтобы завершить обработку задания, устраните проблему, а затем вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .

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

[**Ибаккграундкопикаллбакк:: Жоберрор**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**ибаккграундкоперрор**](ibackgroundcopyerror.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: State**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





