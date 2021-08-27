---
description: Метод Жоинфилтерграф отправляет \_ \_ уведомление о событии, уничтоженное ОКНОм EC, при удалении фильтра из графа фильтра.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Кбасевидеорендерер. Жоинфилтерграф, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3aed2c887bc7a452cda978e96cd369a71cad4fab60a72e0c914ebe9d9790a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052214"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>Кбасевидеорендерер. Жоинфилтерграф, метод

`JoinFilterGraph`Метод отправляет уведомление о событии, [**\_ \_ уничтоженное окном EC**](ec-window-destroyed.md) , при удалении фильтра из графа фильтра.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пграф* 
</dt> <dd>

Указатель на граф фильтра для объединения.

</dd> <dt>

*pName* \[ окне\]
</dt> <dd>

Указатель на имя добавляемого фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Эта функция члена переопределяет функцию члена [**кбасефилтер:: жоинфилтерграф**](cbasefilter-joinfiltergraph.md) . Если фильтр выходит за пределы графа фильтра (*пграф* имеет **значение NULL**), он отправляет уведомление о событии в [**окне EC, \_ \_**](ec-window-destroyed.md) чтобы диспетчер ресурсов не удерживал обработчик в качестве объекта фокуса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




