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
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657929"
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

## <a name="remarks"></a>Комментарии

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




