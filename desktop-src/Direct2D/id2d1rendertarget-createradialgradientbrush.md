---
title: Методы Креатерадиалградиентбруш ID2D1RenderTarget (D2d1. h)
description: Создает объект ID2D1RadialGradientBrush, который можно использовать для рисования областей с радиальным градиентом.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Методы Креатерадиалградиентбруш Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675130"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>Методы ID2D1RenderTarget:: Креатерадиалградиентбруш

Создает объект [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , который можно использовать для рисования областей с радиальным градиентом.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                       | Описание                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатерадиалградиентбруш ( \_ \_ Свойства кисти радиального градиента D2D1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | Создает объект [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , содержащий указанные позиции градиента, не имеет преобразования и имеет базовую прозрачность 1,0. <br/> |
| [**Креатерадиалградиентбруш ( \_ \_ Свойства кисти радиального градиента D2D1 \_ \_&, \_ Свойства кисти D2D1 \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | Создает объект [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , содержащий указанные позиции градиента и имеющий заданное преобразование и базовую прозрачность. <br/> |
| [**Креатерадиалградиентбруш ( \_ \_ Свойства кисти радиального градиента D2D1 \_ \_ \* , \_ Свойства кисти D2D1 \_ \* , ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | Создает объект [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , содержащий указанные позиции градиента и имеющий заданное преобразование и базовую прозрачность. <br/> |



## <a name="examples"></a>Примеры

Пример см. в разделе [Создание кисти радиального градиента](how-to-create-a-radial-gradient-brush.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Создание кисти радиального градиента](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Обзор кистей](direct2d-brushes-overview.md)
</dt> </dl>

�

�
