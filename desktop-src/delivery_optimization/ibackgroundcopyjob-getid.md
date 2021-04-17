---
title: Метод использованием метода ibackgroundcopyjob GetId (Deliveryoptimization. h)
description: Возвращает идентификатор, используемый для идентификации задания в очереди.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId - метод
- Метод GetId, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691840"
---
# <a name="ibackgroundcopyjobgetid-method"></a>Метод использованием метода ibackgroundcopyjob:: GetId

Возвращает идентификатор, используемый для идентификации задания в очереди.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пжобид* \[ заполняет\]
</dt> <dd>

Идентификатор GUID, определяющий задание в очереди DO.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.

## <a name="remarks"></a>Комментарии

Служба создает идентификатор при [создании](ibackgroundcopymanager-createjob.md) задания. Чтобы использовать идентификатор для получения указателя на интерфейс [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md) для задания, вызовите метод [**Ибаккграундкопиманажер:: жетжоб**](ibackgroundcopymanager-getjob.md) .

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

[**Ибаккграундкопиманажер:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**Ибаккграундкопиманажер:: Жетжоб**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





