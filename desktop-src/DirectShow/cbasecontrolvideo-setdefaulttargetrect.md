---
description: Метод Сетдефаулттаржетрект задает целевой видеопрямоугольник по умолчанию (чистый виртуальный). Это внутренняя функция-член, которая вызывается при сбросе исходного прямоугольника.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Кбасеконтролвидео. Сетдефаулттаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ab9cf310ffc35df07ecd9e332325bb5f20f3cb4884ee17e672294b89c5abc9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087484"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>Кбасеконтролвидео. Сетдефаулттаржетрект, метод

`SetDefaultTargetRect`Метод задает целевой видеопрямоугольник по умолчанию (чистый виртуальный). Это внутренняя функция-член, которая вызывается при сбросе исходного прямоугольника.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Производные классы должны переопределять этот параметр, чтобы сбросить конечный прямоугольник видео. Он вызывается из функции-члена [**кбасеконтролвидео:: сетдефаултдестинатионпоситион**](cbasecontrolvideo-setdefaultdestinationposition.md) .

В следующем примере демонстрируется реализация этой функции в производном классе.


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) . \_Элемент данных m мтин, также определенный в производном классе, содержит объект [**кмедиатипе**](cmediatype.md) с типом носителя для входного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




