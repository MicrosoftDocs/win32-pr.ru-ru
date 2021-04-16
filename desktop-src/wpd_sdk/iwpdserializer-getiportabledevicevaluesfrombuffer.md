---
description: Метод Жетипортабледевицевалуесфромбуффер десериализует массив байтов в интерфейс Ипортабледевицевалуес.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Метод Ивпдсериализер:: Жетипортабледевицевалуесфромбуффер (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665124"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>Метод Ивпдсериализер:: Жетипортабледевицевалуесфромбуффер

Метод **жетипортабледевицевалуесфромбуффер** десериализует массив байтов в интерфейс **ипортабледевицевалуес** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pBuffer* \[ окне\]
</dt> <dd>

Указатель на буфер для десериализации.

</dd> <dt>

*двинпутбуфферленгс* \[ окне\]
</dt> <dd>

Значение **типа DWORD** , указывающее размер буфера в байтах.

</dd> <dt>

*пппарамс* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает указатель на интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) , созданный из буфера. Приложение отвечает за вызов **выпуска** в интерфейсе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                  | Описание                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод выполнен успешно.<br/>                     |
| <dl> <dt>**\_указатель E**</dt> </dl>    | Обязательный аргумент-указатель имеет **значение NULL**.<br/> |
| <dl> <dt>**\_непредвиденная E**</dt> </dl> | Произошла Неуказанная ошибка преобразования.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивпдсериализер**](iwpdserializer.md)
</dt> </dl>

 

 




