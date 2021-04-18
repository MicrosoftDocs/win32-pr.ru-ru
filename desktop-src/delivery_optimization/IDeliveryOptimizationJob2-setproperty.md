---
title: 'Метод IDeliveryOptimizationJob2:: SetProperty'
description: Этот метод не используется.
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IDeliveryOptimizationJob2
- Интерфейс IDeliveryOptimizationJob2, метод SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415652"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a>Метод IDeliveryOptimizationJob2:: SetProperty

Этот метод не используется.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*propId* \[ окне\]
</dt> <dd>

Не используется.

</dd> <dt>

*пропвалуе* \[ окне\]
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если propId имеет **DOJobPropertyId_ExtendedErrorInfo**, возвращаемое значение равно **DO_E_READ_ONLY_PROPERTY**, в противном случае функция возвращает **DO_E_UNKNOWN_PROPERTY_ID**.

## <a name="requirements"></a>Требования

| Требование | Значение |
|---------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента  | \[Только для настольных приложений Windows 10 версии 1803\]                                   |
| Минимальная версия сервера  | \[Только для настольных приложений Windows Server версии 1709\]                               |
| Header                    | Deliveryoptimization. h                                                           |
| IDL                       | DeliveryOptimization. idl                                                         |
| Библиотека                   | Досвк. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>См. также раздел

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
