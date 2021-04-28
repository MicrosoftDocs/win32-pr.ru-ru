---
description: Кбасеинпутпин. Inactive-метод. неактивный метод уведомляет ПИН-код о том, что фильтр больше не активен.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Метод Кбасеинпутпин. Inactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1324e9e2641e5e05bc3b0429ee269098c13d4bae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099732"
---
# <a name="cbaseinputpininactive-method"></a>Кбасеинпутпин. Inactive, метод

`Inactive`Метод уведомляет ПИН-код о том, что фильтр больше не активен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                          | Описание                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                 | Успешно.<br/>                          |
| <dl> <dt>**VFW \_ E \_ без \_ распределителя**</dt> </dl> | Распределитель памяти недоступен.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасепин:: Inactive**](cbasepin-inactive.md) . Он вызывает метод [**имемаллокатор::D екоммит**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) для дефиксации распределителя памяти.

При переопределении этого метода вызовите метод базового класса из переопределяющего метода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




