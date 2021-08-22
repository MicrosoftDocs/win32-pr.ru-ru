---
title: 'IDeliveryOptimizationFile2:: метод Property'
description: 'Этот метод возвращает одно свойство файла DO. | IDeliveryOptimizationFile2:: метод Property'
keywords:
- Метод GetProperty
- Метод Property, интерфейс IDeliveryOptimizationFile2
- Интерфейс IDeliveryOptimizationFile2, метод метода Property
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f181eebe2aff8ccbbbf6d5400e3d5a78f123e2304567a413ecf4a35357229b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542094"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2:: метод Property

Этот метод возвращает одно свойство файла DO.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*propId* \[ окне\]
</dt> <dd>

Обязательный идентификатор свойства для получения типа Дофилепропертид.

</dd> <dt>

*пропвалуе* \[ заполняет\]
</dt> <dd>

Значение свойства, хранящееся в ВАРИАНТе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения HRESULT.

| Код возврата                  | Описание                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Успешно                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | Неизвестный идентификатор свойства.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | Свойство доступно только для записи и не может быть прочитано.      |
| **E_NOT_SET**                | Свойство не было задано с помощью метода SetProperty. |
| **E_OUTOFMEMORY**            |  Ошибка выделения памяти                          |

## <a name="requirements"></a>Требования

| Требование | Значение |
|---------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента  | Windows 10, только для \[ настольных приложений версии 1803\]                                   |
| Минимальная версия сервера  | Windows Server, только для \[ настольных приложений версии 1709\]                               |
| Header                    | Deliveryoptimization. h                                                           |
| IDL                       | DeliveryOptimization. idl                                                         |
| Библиотека                   | Досвк. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>См. также раздел

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
