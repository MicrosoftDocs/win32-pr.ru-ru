---
title: 'IDeliveryOptimizationJob2:: метод Property'
description: Возвращает одно свойство задания DO.
keywords:
- Метод GetProperty
- Метод Property, интерфейс IDeliveryOptimizationJob2
- Интерфейс IDeliveryOptimizationJob2, метод метода Property
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489825"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2:: метод Property

Этот метод возвращает одно свойство задания DO.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*propId* \[ окне\]
</dt> <dd>

Требуемый идентификатор свойства для получения. Поддерживается только **DOJobPropertyId_ExtendedErrorInfo** типа VT_BSTR.

</dd> <dt>

*пропвалуе* \[ заполняет\]
</dt> <dd>

Результирующее значение свойства, хранящееся в типе VARIANT.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения HRESULT.

| Код возврата                  | Описание          |
|------------------------------|----------------------|
| **S_OK**                     | Успешно              |
| **DO_E_UNKNOWN_PROPERTY_ID** | Неизвестный идентификатор свойства. |

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
