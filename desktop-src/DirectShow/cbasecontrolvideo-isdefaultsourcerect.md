---
description: Метод Исдефаултсаурцерект определяет, использует ли модуль подготовки отчетов исходный прямоугольник по умолчанию (чисто виртуальный).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Кбасеконтролвидео. Исдефаултсаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669184"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a>Кбасеконтролвидео. Исдефаултсаурцерект, метод

`IsDefaultSourceRect`Метод определяет, использует ли модуль подготовки отчетов исходный прямоугольник по умолчанию (чисто виртуальный).

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК, если модуль подготовки отчетов использует источник по умолчанию; в противном случае возвращает \_ значение false.

## <a name="remarks"></a>Комментарии

Эта функция члена должна быть реализована в производном классе. Он вызывается функцией-членом [**кбасеконтролвидео:: исусингдефаултсаурце**](cbasecontrolvideo-isusingdefaultsource.md) .

В следующем примере демонстрируется реализация этой функции в производном классе.


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



В этом примере Квидеотекст является классом, производным от [**кбасеконтролвидео**](cbasecontrolvideo.md), m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md), и \_ член данных m DrawImage, определенный в производном классе, содержит объект [**кдравимаже**](cdrawimage.md) . \_Элемент данных m мтин, также определенный в производном классе, содержит объект [**кмедиатипе**](cmediatype.md) с типом носителя для входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




