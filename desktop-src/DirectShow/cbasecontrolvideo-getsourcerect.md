---
description: Метод Жетсаурцерект извлекает исходный прямоугольник. Это внутренний метод.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Кбасеконтролвидео. Жетсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a637e0f5ab5c97494dc072458a29920110363a3e4f07ba8bb7313947996bdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057054"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a>Кбасеконтролвидео. Жетсаурцерект, метод

`GetSourceRect`Метод получает исходный прямоугольник. Это внутренний метод.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псаурцерект* 
</dt> <dd>

Указатель на полученный исходный прямоугольник.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена должна быть переопределена в производном классе для возврата исходного прямоугольника, удерживаемого модулем подготовки видео. Он вызывается из следующих функций-членов [**кбасеконтролвидео**](cbasecontrolvideo.md) .

-   [**Кбасеконтролвидео:: Жетсаурцепоситион**](cbasecontrolvideo-getsourceposition.md)
-   [**Кбасеконтролвидео::p UT \_ саурцелефт**](cbasecontrolvideo-put-sourceleft.md)
-   [**Кбасеконтролвидео:: Get \_ саурцелефт**](cbasecontrolvideo-get-sourceleft.md)
-   [**Кбасеконтролвидео::p UT \_ саурцевидс**](cbasecontrolvideo-put-sourcewidth.md)
-   [**Кбасеконтролвидео:: Get \_ саурцевидс**](cbasecontrolvideo-get-sourcewidth.md)
-   [**Кбасеконтролвидео::p UT \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**Кбасеконтролвидео:: Get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)
-   [**Кбасеконтролвидео::p UT \_ саурцехеигхт**](cbasecontrolvideo-put-sourceheight.md)
-   [**Кбасеконтролвидео:: Get \_ саурцехеигхт**](cbasecontrolvideo-get-sourceheight.md)

В следующем примере демонстрируется реализация этой функции в производном классе.


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
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

 

 




