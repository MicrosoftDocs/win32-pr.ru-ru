---
description: Метод Сетсаурцерект задает текущий исходный видеопрямоугольник (чистый виртуальный). Это внутренняя функция-член, которая вызывается при изменении исходного прямоугольника.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Кбасеконтролвидео. Сетсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669237"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a>Кбасеконтролвидео. Сетсаурцерект, метод

`SetSourceRect`Метод задает текущий исходный видеопрямоугольник (чистый виртуальный). Это внутренняя функция-член, которая вызывается при изменении исходного прямоугольника.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псаурцерект* 
</dt> <dd>

Указатель на исходный прямоугольник.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Производные классы должны переопределять эту функцию члена, чтобы иметь представление об изменении исходного прямоугольника. Он вызывается из следующих функций-членов.

-   [**Кбасеконтролвидео:: Сетсаурцепоситион**](cbasecontrolvideo-setsourceposition.md)
-   [**Кбасеконтролвидео::p UT \_ саурцелефт**](cbasecontrolvideo-put-sourceleft.md)
-   [**Кбасеконтролвидео::p UT \_ саурцевидс**](cbasecontrolvideo-put-sourcewidth.md)
-   [**Кбасеконтролвидео::p UT \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**Кбасеконтролвидео::p UT \_ саурцехеигхт**](cbasecontrolvideo-put-sourceheight.md)

В следующем примере демонстрируется реализация этой функции в производном классе.


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
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

 

 




