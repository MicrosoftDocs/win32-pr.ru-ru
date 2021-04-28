---
description: Кбасеаутпутпин. Active Method — активный метод уведомляет ПИН-код о том, что фильтр активен.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Метод Кбасеаутпутпин. Active (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096212"
---
# <a name="cbaseoutputpinactive-method"></a>Кбасеаутпутпин. активный метод

`Active`Метод уведомляет ПИН-код о том, что фильтр активен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Active();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                          | Описание                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                 | Успешно.<br/>                   |
| <dl> <dt>**VFW \_ E \_ без \_ распределителя**</dt> </dl> | Распределитель недоступен.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасепин:: Active**](cbasepin-active.md) . Он вызывает метод [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) для распределителя, чтобы выделить память для буферов.

При переопределении этого метода вызовите метод базового класса из переопределяющего метода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




