---
title: 'Метод IDeliveryOptimizationFile2:: SetProperty'
description: 'Этот метод возвращает одно свойство файла DO. | Метод IDeliveryOptimizationFile2:: SetProperty'
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IDeliveryOptimizationFile2
- Интерфейс IDeliveryOptimizationFile2, метод SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 99ed42acb94f260e229abfe9df428aaa61d3658cb887892b84bb73fd6e7e63e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635724"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>Метод IDeliveryOptimizationFile2:: SetProperty

Этот метод возвращает одно свойство файла DO.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*propId* \[ окне\]
</dt> <dd>

Обязательный идентификатор свойства для набора типа Дофилепропертид.

</dd> <dt>

*пропвалуе* \[ окне\]
</dt> <dd>

Заданное значение свойства типа VARIANT.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения HRESULT.

| Код возврата                  | Описание                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Success                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | Неизвестный идентификатор свойства                                                |
| **DO_E_INVALID_STATE**       | Задание в настоящее время не находится в состоянии, допускающем установку свойства |

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

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
