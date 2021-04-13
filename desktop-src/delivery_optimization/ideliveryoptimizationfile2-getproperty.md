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
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353725"
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
| Минимальная версия клиента  | \[Только для настольных приложений Windows 10 версии 1803\]                                   |
| Минимальная версия сервера  | \[Только для настольных приложений Windows Server версии 1709\]                               |
| Header                    | Deliveryoptimization. h                                                           |
| IDL                       | DeliveryOptimization. idl                                                         |
| Библиотека                   | Досвк. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>См. также раздел

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
