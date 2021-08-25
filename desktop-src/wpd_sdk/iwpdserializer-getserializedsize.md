---
description: Метод Жетсериализедсизе вычисляет размер буфера, необходимого для хранения сериализованного интерфейса Ипортабледевицевалуес.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Метод Ивпдсериализер:: Жетсериализедсизе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae6b8381928c64b7d16e9f5daa4dd9fd85acd9b61c13531365d871563ef6afe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704524"
---
# <a name="iwpdserializergetserializedsize-method"></a>Метод Ивпдсериализер:: Жетсериализедсизе

Метод **жетсериализедсизе** вычисляет размер буфера, необходимого для хранения сериализованного интерфейса [**ипортабледевицевалуес**](iportabledevicevalues.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псаурце* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) , размер которого необходимо запросить.

</dd> <dt>

*пдвсизе* \[ заполняет\]
</dt> <dd>

Указатель на **DWORD** , указывающий размер буфера, необходимый для сериализации *псаурце*, в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                   | Описание                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Метод выполнен успешно.<br/>                                       |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Обязательный аргумент-указатель имеет **значение NULL**.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно свободной памяти для создания буфера.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивпдсериализер**](iwpdserializer.md)
</dt> </dl>

 

 




