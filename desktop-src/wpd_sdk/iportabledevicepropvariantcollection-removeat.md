---
description: Метод RemoveAt удаляет элемент, хранящийся в расположении, заданном по заданному индексу.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'Метод Ипортабледевицепропвариантколлектион:: RemoveAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694742"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>Метод Ипортабледевицепропвариантколлектион:: RemoveAt

Метод **RemoveAt** удаляет элемент, хранящийся в расположении, заданном по заданному индексу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

Указывает индекс удаляемого элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                  | Описание                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод выполнен успешно.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Указанный индекс выходит за пределы допустимого диапазона.<br/> |



 

## <a name="remarks"></a>Комментарии

Необходимо указать Отсчитываемый от нуля индекс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




