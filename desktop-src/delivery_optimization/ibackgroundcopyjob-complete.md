---
title: Метод использованием метода ibackgroundcopyjob Complete (Deliveryoptimization. h)
description: Завершает задание и сохраняет перенесенные файлы на клиенте.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Метод Complete
- Метод Complete, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72ace8890e724e529e96c5292a439042f13bc2bfad77e6d990a6dbb2fa18f5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736229"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>Метод использованием метода ibackgroundcopyjob:: Complete

Завершает задание и сохраняет перенесенные файлы на клиенте.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** . Метод также может возвращать ошибки, связанные с переименованием временных копий переданных файлов по заданным именам.



| Код возврата                                                                                          | Описание                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Все файлы успешно переданы.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Для загрузки состояние задания не может быть BG_JOB_STATE_CANCELLED или BG_JOB_STATE_ACKNOWLEDGED. <br/> Для отправки состояние задания должно быть BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Remarks

Все файлы были успешно переданы, если состояние задания — **BG_JOB_STATE_TRANSFERRED**. Чтобы проверить состояние задания, вызовите метод [**использованием метода ibackgroundcopyjob:: with State**](ibackgroundcopyjob-getstate.md) . Можно также реализовать интерфейс [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) для получения уведомлений о том, что все файлы были переданы клиенту.

Сохраняются только задания, срок действия которых меньше 30 дней. Все более старые задания будут удалены. Не поддерживает групповая политика [жобинактивититимеаут](https://www.bing.com/search?q=JobInactivityTimeout) .

Для заданий загрузки можно вызвать метод **Complete** в любое время в процессе перемещения; Однако сохраняются только те файлы, которые были успешно переданы клиенту до вызова этого метода. Например, при вызове метода **Complete** во время обработки третьей из пяти файлов сохраняются только первые два файла. Чтобы определить, какие файлы были переданы, вызовите метод [**ибаккграундкопифиле:: Progress**](ibackgroundcopyfile-getprogress-method.md) и сравните элемент **BytesTransferred** с элементом **битестотал** структуры [**BG_FILE_PROGRESS**](bg-file-progress.md) .

Для заданий отправки можно вызвать метод **Complete** , только если задание находится в состоянии **BG_JOB_STATE_TRANSFERRED**.

Владельцем файла является пользователь, выполнивший вызов. Например, если администратор выполняет задание другого пользователя, он не является владельцем задания.

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

[**Использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: State**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





