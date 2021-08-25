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
ms.openlocfilehash: 0a664c752bd28b176189cdd77e955684236cfa23c6b384378610336335651fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635954"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 определен как 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





