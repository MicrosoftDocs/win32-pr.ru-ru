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
ms.openlocfilehash: cdca86cb374eded0eabcc1d623d2218a6dc1f4cd5613a18e16b4ec9ab93156b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811255"
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
| **S_OK**                     | Success              |
| **DO_E_UNKNOWN_PROPERTY_ID** | Неизвестный идентификатор свойства. |

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|---------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента  | Windows 10, только для \[ настольных приложений версии 1803\]                                   |
| Минимальная версия сервера  | Windows Server, только для \[ настольных приложений версии 1709\]                               |
| Заголовок                    | Deliveryoptimization. h                                                           |
| IDL                       | DeliveryOptimization. idl                                                         |
| Библиотека                   | Досвк. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>См. также

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
