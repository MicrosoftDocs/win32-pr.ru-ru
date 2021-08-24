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
ms.openlocfilehash: 0ca5832246e90e1df207754dc33380547b8193829394d81e6b2b757fccf79a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502314"
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

## <a name="remarks"></a>Remarks

Когда деструктор [**кбасеобжект**](cbaseobject.md) уничтожает объект, который загрузил OleAut32.dll, он выгружает библиотеку, если она все еще загружена.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Вспомогательные функции COM**](com-helper-functions.md)
</dt> </dl>

 

 




