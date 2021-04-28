---
description: 'Метод Ипортабледевицекэйколлектион:: RemoveAt — метод RemoveAt удаляет элемент, хранящийся в расположении, указанном заданным индексом.'
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Метод Ипортабледевицекэйколлектион:: RemoveAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3ec2b1137e7959a646c2943ab1aa7a5c3428d3c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109950"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a>Метод Ипортабледевицекэйколлектион:: RemoveAt

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

[**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> </dl>

 

 




