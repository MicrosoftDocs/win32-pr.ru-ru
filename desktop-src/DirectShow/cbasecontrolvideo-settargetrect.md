---
description: Метод Сеттаржетрект задает текущий целевой прямоугольник (чисто виртуальный). Это внутренняя функция-член, которая вызывается при изменении прямоугольника назначения.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Кбасеконтролвидео. Сеттаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3af420d9280d21ccf11bfdc6a23b63b33f10c1bf5a360f1770647dcb51655cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017412"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>Кбасеконтролвидео. Сеттаржетрект, метод

`SetTargetRect`Метод задает текущий целевой прямоугольник (чисто виртуальный). Это внутренняя функция-член, которая вызывается при изменении прямоугольника назначения.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птаржетрект* 
</dt> <dd>

Указатель на прямоугольник назначения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Производные классы должны переопределять этот параметр, чтобы иметь представление об изменении прямоугольника назначения. Он вызывается из следующих функций-членов.

-   [**Кбасеконтролвидео:: Сетдестинатионпоситион**](cbasecontrolvideo-setdestinationposition.md)
-   [**Кбасеконтролвидео::p UT \_ дестинатионлефт**](cbasecontrolvideo-put-destinationleft.md)
-   [**Кбасеконтролвидео::p UT \_ дестинатионвидс**](cbasecontrolvideo-put-destinationwidth.md)
-   [**Кбасеконтролвидео::p UT \_ дестинатионтоп**](cbasecontrolvideo-put-destinationtop.md)
-   [**Кбасеконтролвидео::p UT \_ дестинатионхеигхт**](cbasecontrolvideo-put-destinationheight.md)

В следующем примере демонстрируется реализация этой функции в производном классе.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




