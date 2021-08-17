---
title: Метод Ибаккграундкопиманажер Жетжоб (Deliveryoptimization. h)
description: Извлекает указанное задание из очереди обмена. Как правило, приложение сохраняет идентификатор задания, поэтому позже можно получить задание из очереди.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Метод Жетжоб
- Метод Жетжоб, интерфейс Ибаккграундкопиманажер
- Интерфейс Ибаккграундкопиманажер, метод Жетжоб
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d8d05b496eaa0d6f1520f22efeed8a39af5eb8e4c338457e18c65a7913489472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542292"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>Метод Ибаккграундкопиманажер:: Жетжоб

Извлекает указанное задание из очереди обмена. Как правило, приложение сохраняет идентификатор задания, поэтому позже можно получить задание из очереди.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

Идентификатор *задания* \[ окне\]
</dt> <dd>

Определяет задание, извлекаемое из очереди обмена. Метод [**CreateJob**](ibackgroundcopymanager-createjob.md) возвращает идентификатор задания.

</dd> <dt>

*ппжоб* \[ заполняет\]
</dt> <dd>

Указатель интерфейса [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md) на задание, заданное параметром *JOBID*. По завершении выпустите *ппжоб*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                                      | Описание                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>         | Задание успешно получено из очереди обмена.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | Задание не найдено в очереди.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | У пользователя нет разрешения на получение задания.<br/>      |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager определен как 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопиманажер**](ibackgroundcopymanager.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**Ибаккграундкопиманажер:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





