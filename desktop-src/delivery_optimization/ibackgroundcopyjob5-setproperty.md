---
title: Метод SetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Универсальный метод для установки свойств задания оптимизации доставки (DO).
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IBackgroundCopyJob5
- Интерфейс IBackgroundCopyJob5, метод SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803293"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>Метод IBackgroundCopyJob5:: SetProperty

Универсальный метод для установки свойств задания оптимизации доставки (DO).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PropertyId* \[ окне\]
</dt> <dd>

Идентификатор свойства, которое задается как значение перечисления [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

</dd> <dt>

*Propertyvalue* \[ окне\]
</dt> <dd>

Значение свойства, которое задается. Для хранения значения, тип которого соответствует свойству, это значение указывается с помощью [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) объединения, состоящего из всех известных типов свойств.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает следующие возвращаемые значения.



| Код возврата                                                                          | Описание        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Успешно<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 определяется как E847030C-БББА-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5:: Property**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





