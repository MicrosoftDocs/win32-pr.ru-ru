---
description: 'Метод Ипортабледевицепропвариантколлектион:: RemoveAt — метод RemoveAt удаляет элемент, хранящийся в расположении, указанном заданным индексом.'
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
ms.openlocfilehash: 5c62df57a95a9f5a8238ff61c4ca6dc3cb73ed36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109951"
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



 

## <a name="remarks"></a>Remarks

Необходимо указать Отсчитываемый от нуля индекс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




