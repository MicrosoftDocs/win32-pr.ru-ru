---
description: Метод Pause приостанавливает фильтр.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Метод Кбасерендерер. Pause (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669404"
---
# <a name="cbaserendererpause-method"></a>Кбасерендерер. Pause, метод

`Pause`Метод приостанавливает фильтр.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения перечислены в следующей таблице.



| Код возврата                                                                             | Описание                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | Переход завершен.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Переход не завершен.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасефилтер::P Аусе**](cbasefilter-pause.md) . Он выполняет следующие действия:

-   Вызывает метод **кбасефилтер::P Аусе** .
-   Фиксирует распределитель. (См. [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Если предыдущее состояние было остановлено, фильтр выпустит любой пример, который он удерживает. (Образец больше не является допустимым.)
-   Вызывает метод [**кбасерендерер:: комплетестатечанже**](cbaserenderer-completestatechange.md) и возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




