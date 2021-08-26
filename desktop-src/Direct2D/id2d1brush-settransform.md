---
title: Методы Сеттрансформ ID2D1Brush (D2d1 \_ 1. h)
description: Задает преобразование, применяемое к кисти.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Методы Сеттрансформ Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a5a30d4051303667402fdd1143f5a813d7515223c8093a5913294e6dd1722273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918043"
---
# <a name="id2d1brushsettransform-methods"></a>Методы ID2D1Brush:: Сеттрансформ

Задает преобразование, применяемое к кисти.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                       | Описание                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**Сеттрансформ (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Задает преобразование, применяемое к кисти.<br/> |
| [**Сеттрансформ (D2D1 \_ Matrix \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Задает преобразование, применяемое к кисти.<br/> |



## <a name="remarks"></a>Remarks

При рисовании с помощью кисти она рисуется в пространстве координат целевого объекта отрисовки. Кисти не размещаются автоматически, чтобы они совпадали с закрашиваемым объектом; по умолчанию они начинают рисовать в источнике (0, 0) целевого объекта отрисовки.

Можно «переместить» градиент, определенный [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , в целевую область, задав его начальную и конечную точки. Аналогичным образом можно переместить градиент, определенный [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , изменив его центр и радиусы.

Чтобы согласовать содержимое [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с закрашиваемой областью, можно использовать метод **сеттрансформ** для преобразования растрового изображения в нужное место. Это преобразование влияет только на кисть. Он не влияет на содержимое, рисуемое целевым объектом рендеринга.

На следующих иллюстрациях показан результат использования [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для заполнения прямоугольника, расположенного в (100, 100). На рисунке слева показан результат заполнения прямоугольника без преобразования кисти: точечный рисунок отображается в источнике целевого объекта рендеринга. В результате в прямоугольнике появляется только часть точечного рисунка.

На рисунке справа показан результат преобразования [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , чтобы его содержимое было смещено на 50 пикселей вправо и 50 пикселей вниз. Теперь точечный рисунок заполняет прямоугольник.

![Иллюстрация двух квадратов, одна закрашена растровым изображением без преобразованной кисти, а другая — преобразованной кистью](images/brushes-ovw-transform.png)

## <a name="examples"></a>Примеры

В следующем примере кода показано, как создать преобразование, показанное на схеме справа на предыдущем рисунке. Сначала примените перевод к [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), переместив кисть 50 пикселей вправо вдоль оси x и 50 пикселей вниз по оси y. Затем используйте **ID2D1BitmapBrush** для заполнения прямоугольника с верхним левым углом в (100, 100) и правом нижнем углу в (200, 200).


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D2d1 \_ 1. h (включение D2d1. h)</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор кистей](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
