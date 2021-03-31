---
title: Метод IBackgroundCopyFile5-Property (Deliveryoptimization. h)
description: Возвращает универсальное свойство передачи файла оптимизации доставки (DO).
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Метод GetProperty
- Метод Property, интерфейс IBackgroundCopyFile5
- Интерфейс IBackgroundCopyFile5, метод метода Property
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135742"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>IBackgroundCopyFile5:: метод Property

Возвращает универсальное свойство передачи файла оптимизации доставки (DO).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PropertyId* \[ окне\]
</dt> <dd>

Указывает свойство файла, значение которого необходимо извлечь.

</dd> <dt>

*Propertyvalue* \[ заполняет\]
</dt> <dd>

Значение свойства, возвращаемое как указатель на BITS_FILE_PROPERTY_VALUEное объединение. Используйте поле Union, подходящее для значения идентификатора свойства, переданного в.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается с ошибкой, возвращается **S_OK**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 определен как 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





