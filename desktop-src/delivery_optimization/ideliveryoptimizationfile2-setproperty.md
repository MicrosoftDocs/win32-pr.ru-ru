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
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713397"
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
| **S_OK**                     | Успешно                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | Неизвестный идентификатор свойства                                                |
| **DO_E_INVALID_STATE**       | Задание в настоящее время не находится в состоянии, допускающем установку свойства |

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

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
