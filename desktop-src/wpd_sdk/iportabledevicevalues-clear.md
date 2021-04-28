---
description: 'Метод Ипортабледевицевалуес:: Clear. метод Clear удаляет все элементы из коллекции.'
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'Метод Ипортабледевицевалуес:: Clear (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8e1df59cd972bc470607ac2b49d05f43dba8b3a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109902"
---
# <a name="iportabledevicevaluesclear-method"></a>Метод Ипортабледевицевалуес:: Clear

Метод **clear** удаляет все элементы из коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод освобождает память для всех динамически выделяемых элементов в коллекции. Для интерфейсов он вызывает метод **Release**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> </dl>

 

 




