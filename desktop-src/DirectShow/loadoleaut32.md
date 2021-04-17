---
description: Функция LoadOLEAut32 загружает библиотеку динамической компоновки (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Функция LoadOLEAut32 (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685132"
---
# <a name="loadoleaut32-function"></a>Функция LoadOLEAut32

Функция **LoadOLEAut32** загружает библиотеку динамической компоновки (OleAut32.dll).

## <a name="syntax"></a>Синтаксис


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для экземпляра библиотеки DLL службы автоматизации.

## <a name="remarks"></a>Комментарии

Когда деструктор [**кбасеобжект**](cbaseobject.md) уничтожает объект, который загрузил OleAut32.dll, он выгружает библиотеку, если она все еще загружена.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Вспомогательные функции COM**](com-helper-functions.md)
</dt> </dl>

 

 




