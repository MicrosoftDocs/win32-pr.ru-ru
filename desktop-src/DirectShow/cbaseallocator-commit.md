---
description: 'Метод Commit выделяет память для буферов. Этот метод реализует метод Имемаллокатор:: Commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Метод Кбасеаллокатор. Commit (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba9c373a15d5200d6466fef5c519a59a1052c8e5854ebe38c5a8b027d21188a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087584"
---
# <a name="cbaseallocatorcommit-method"></a>Кбасеаллокатор. Commit, метод

`Commit`Метод выделяет память для буферов. Этот метод реализует метод [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения перечислены в следующем списке.



| Код возврата                                                                                       | Описание                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>              | Успешно.<br/>                                |
| <dl> <dt>**VFW \_ E \_ сизенотсет**</dt> </dl> | Не указаны требования к буферу.<br/> |



 

## <a name="remarks"></a>Remarks

Перед вызовом этого метода вызовите метод [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) , чтобы указать требования к буферу.

Этот метод вызывает виртуальный метод [**кбасеаллокатор:: Alloc**](cbaseallocator-alloc.md) , чтобы выделить память для буферов. Производные классы могут переопределять **Alloc**. Если операция отмены фиксации отложена, она отменяется.

Этот метод необходимо вызвать перед вызовом метода [**кбасеаллокатор:: with buffer**](cbaseallocator-getbuffer.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




