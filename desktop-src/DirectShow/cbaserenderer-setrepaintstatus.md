---
description: Метод Сетрепаинтстатус включает или отключает перерисовки событий.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Кбасерендерер. Сетрепаинтстатус, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669343"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>Кбасерендерер. Сетрепаинтстатус, метод

`SetRepaintStatus`Метод включает или отключает перерисовки событий.

## <a name="syntax"></a>Синтаксис


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*bRepaint* 
</dt> <dd>

Логическое значение, указывающее, включены ли события перерисовки. Если **значение — true**, фильтр отправит события [**\_ перерисовки EC**](ec-repaint.md) в Диспетчер графа фильтров. В противном случае он не будет отсылать \_ события ПЕРЕрисовки EC.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод гарантирует, что диспетчер графов фильтров не будет переполняться избыточными \_ событиями ПЕРЕрисовки EC. После того как фильтр отправит событие [**\_ перерисовки EC**](ec-repaint.md) , он вызывает этот метод со значением **true**. Фильтр не отправляет дополнительные \_ события ПЕРЕрисовки EC, пока он не получит больше данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




