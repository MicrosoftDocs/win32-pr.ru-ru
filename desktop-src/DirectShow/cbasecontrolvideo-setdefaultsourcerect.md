---
description: Метод Сетдефаултсаурцерект задает исходный видеопрямоугольник по умолчанию (чистый виртуальный). Это во внутренней функции-члене, которая вызывается при сбросе исходного прямоугольника.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Кбасеконтролвидео. Сетдефаултсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae7f2e88e170b0c21187b2615029fcb4ed2bed4717af09b60eb4309aee2bea0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432614"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a>Кбасеконтролвидео. Сетдефаултсаурцерект, метод

`SetDefaultSourceRect`Метод задает исходный видеопрямоугольник по умолчанию (чистый виртуальный). Это во внутренней функции-члене, которая вызывается при сбросе исходного прямоугольника.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Производные классы должны переопределять этот параметр, чтобы сбросить исходный прямоугольник. Он вызывается из [**кбасеконтролвидео:: сетдефаултсаурцепоситион**](cbasecontrolvideo-setdefaultsourceposition.md).

В следующем примере демонстрируется реализация этой функции в производном классе.


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) . \_Элемент данных m мтин, также определенный в производном классе, содержит объект [**кмедиатипе**](cmediatype.md) с типом носителя для входного контакта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




