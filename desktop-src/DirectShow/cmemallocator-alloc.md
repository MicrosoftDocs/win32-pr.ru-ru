---
description: Кмемаллокатор. Alloc, метод Alloc выделяет память для буферов.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Метод Кмемаллокатор. Alloc (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099042"
---
# <a name="cmemallocatoralloc-method"></a>Кмемаллокатор. Alloc, метод

`Alloc`Метод выделяет память для буферов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                       | Описание                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>              | Успешно.<br/>                          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Недостаточно памяти.<br/>              |
| <dl> <dt>**VFW \_ E \_ сизенотсет**</dt> </dl> | Не заданы требования к буферу.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод вызывается методом [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) . Он выделяет непрерывный блок памяти, достаточный для требований к буферу, заданным в методе [**кмемаллокатор:: SetProperties**](cmemallocator-setproperties.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




