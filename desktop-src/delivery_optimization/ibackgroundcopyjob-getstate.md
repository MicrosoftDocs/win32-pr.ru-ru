---
title: Метод использованием метода ibackgroundcopyjob-State (Deliveryoptimization. h)
description: Возвращает состояние задания.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Метод WebMethod
- Метод WebMethod, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод методаического состояния
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64a26d1cc301230a9bb8330b9a2b2daf3178b1538ec95f593cd5e3f4d3099d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755304"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>Метод использованием метода ibackgroundcopyjob:: with State

Возвращает состояние задания.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пжобстате* \[ заполняет\]
</dt> <dd>

Состояние задания. Например, состояние показывает, что задание находится в состоянии ошибки, передаче данных или приостановлено. Список состояний заданий см. в разделе Перечисление [**BG_JOB_STATE**](bg-job-state-.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                              | Описание                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Состояние задания успешно получено.<br/> |



 

## <a name="remarks"></a>Remarks

Если вы хотите узнать, когда задание находится в состоянии ошибки или передало все файлы в задании, можно использовать этот метод для опроса состояния задания или регистрации для получения уведомлений о наступлении событий. Дополнительные сведения о регистрации для получения уведомлений о событиях см. в разделе интерфейс [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) .

## <a name="requirements"></a>Requirements (Требования)



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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





