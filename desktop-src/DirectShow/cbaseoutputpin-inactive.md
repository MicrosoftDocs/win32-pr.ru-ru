---
description: Кбасеаутпутпин. Inactive-метод. неактивный метод уведомляет ПИН-код о том, что фильтр больше не активен.
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: Метод Кбасеаутпутпин. Inactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0600402301bf416dc0863c4ccff05cac698ec53871b03fd8a84f3873fd43163a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983424"
---
# <a name="cbaseoutputpininactive-method"></a>Кбасеаутпутпин. Inactive, метод

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
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




