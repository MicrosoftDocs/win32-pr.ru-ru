---
title: Результат кадрирования
description: Используйте эффекты кадрирования для вывода заданной области изображения.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- результат кадрирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891885"
---
# <a name="crop-effect"></a>Результат кадрирования

Используйте эффекты кадрирования для вывода заданной области изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1Crop.

-   [Пример изображения](#example-image)
-   [Свойства эффектов](#effect-properties)
-   [Битовая карта вывода](#output-bitmap)
-   [Требования](#requirements)
-   [См. также](#related-topics)

## <a name="example-image"></a>Пример изображения



| До                                                     |
|------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg) |
| После                                                      |
| ![изображение после преобразования.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Свойства эффектов



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Отображаемое имя и перечисление индекса</th>
<th>Тип и значение по умолчанию</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rect<br/></td>
<td>D2D1_VECTOR_4F<br/></td>
<td>Регион, который необходимо обрезать, заданный в виде вектора в форме (слева, сверху, по ширине, по высоте).<br/></td>
</tr>
<tr class="even">
<td>D2D1_CROP_PROP_RECT<br/></td>
<td>{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}<br/></td>
<td>Единицы измерения — DIP. <br/>
<blockquote>
<p>[!Note]</p>
<p>Параметр rect будет обрезан, если он пересекает границы границ входного изображения.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D2D1_CROP_PROP_BORDER_MODE<br/></td>
<td>D2D1_BORDER_MODE <br/> D2D1_BORDER_MODE_SOFT <br/></td>
<td><ul>
<li>D2D1_BORDER_MODE_SOFT: если прямоугольник кадрирования попадает на координаты в виде дробной части пикселя, то этот результат применяет сглаживание, что приводит к мягкому пограничным углу.</li>
<li>D2D1_BORDER_MODE_HARD: если прямоугольник кадрирования попадает на координаты в виде дробной части пикселя, то результат будет резким, что приводит к жесткой границе.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a>Битовая карта вывода

Результатом этого действия является размер свойства Rect. Длина и ширина являются вычисляемыми

улатед с помощью уравнений здесь: <dl> Длина выходных данных в пикселях = (Rect. Right-Rect. Left) \* (dpi пользователя/96)  
Высота выходных данных в пикселях = (Rect. Bottom-Rect.Top) \* (dpi пользователя/96)  
</dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\] |
| Минимальная версия сервера | Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\] |
| Header                   | d2d1effects. h                                                                      |
| Библиотека                  | D2D1. lib, дксгуид. lib                                                               |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

