---
title: Результат кадрирования
description: Используйте эффекты кадрирования для вывода заданной области изображения.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- результат кадрирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e342bdef882fbff89d4c67c3accfbff7287a2ad9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472939"
---
# <a name="crop-effect"></a>Результат кадрирования

Используйте эффекты кадрирования для вывода заданной области изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1Crop.

-   [Пример изображения](#example-image)
-   [Свойства эффектов](#effect-properties)
-   [Битовая карта вывода](#output-bitmap)
-   [Требования](#requirements)
-   [Связанные темы](#related-topics)

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




| Отображаемое имя и перечисление индекса | Тип и значение по умолчанию | Описание | 
|------------------------------------|------------------------|-------------|
| Rect<br /> | D2D1_VECTOR_4F<br /> | Регион, который необходимо обрезать, заданный в виде вектора в форме (слева, сверху, по ширине, по высоте).<br /> | 
| D2D1_CROP_PROP_RECT<br /> | {-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}<br /> | Единицы измерения — DIP. <br /><blockquote><p>[!Note]</p><p>Параметр rect будет обрезан, если он пересекает границы границ входного изображения.<br /></p></blockquote><br /> | 
| D2D1_CROP_PROP_BORDER_MODE<br /> | D2D1_BORDER_MODE <br /> D2D1_BORDER_MODE_SOFT <br /> | <ul><li>D2D1_BORDER_MODE_SOFT: если прямоугольник кадрирования попадает на координаты в виде дробной части пикселя, то этот результат применяет сглаживание, что приводит к мягкому пограничным углу.</li><li>D2D1_BORDER_MODE_HARD: если прямоугольник кадрирования попадает на координаты в виде дробной части пикселя, то результат будет резким, что приводит к жесткой границе.</li></ul> | 




 

## <a name="output-bitmap"></a>Битовая карта вывода

Результатом этого действия является размер свойства Rect. Длина и ширина являются вычисляемыми

улатед с помощью уравнений здесь: <dl> Длина выходных данных в пикселях = (Rect. Right-Rect. Left) \* (dpi пользователя/96)  
Высота выходных данных в пикселях = (Rect. Bottom-Rect.Top) \* (dpi пользователя/96)  
</dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 8 и обновление платформы для Windows 7 \[ классических приложений \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 8 и обновление платформы для Windows 7 \[ классических приложений \| Windows приложения магазина\] |
| Заголовок                   | d2d1effects. h                                                                      |
| Библиотека                  | D2D1. lib, дксгуид. lib                                                               |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

