---
title: Методы Креателинеарградиентбруш ID2D1RenderTarget (D2d1. h)
description: Создает объект ID2D1LinearGradientBrush для рисования областей с линейным градиентом.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Методы Креателинеарградиентбруш Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685278"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>Методы ID2D1RenderTarget:: Креателинеарградиентбруш

Создает объект [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) для рисования областей с линейным градиентом.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                       | Описание                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креателинеарградиентбруш ( \_ \_ Свойства кисти линейного градиента D2D1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Создает объект [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , содержащий указанные позиции градиента, не имеет преобразования и имеет базовую прозрачность 1,0. <br/> |
| [**Креателинеарградиентбруш ( \_ \_ Свойства кисти линейного градиента D2D1 \_ \_&, \_ Свойства кисти D2D1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Создает объект [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , содержащий указанные позиции градиента и имеющий заданное преобразование и базовую прозрачность. <br/> |
| [**Креателинеарградиентбруш ( \_ \_ Свойства кисти линейного градиента D2D1 \_ \_ \* , \_ Свойства кисти D2D1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Создает объект [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , содержащий указанные позиции градиента и имеющий заданное преобразование и базовую прозрачность. <br/> |



## <a name="examples"></a>Примеры

Пример, демонстрирующий создание коллекции ограничителей градиента и его использование для определения линейного градиента, см. [в разделе Создание кисти линейного градиента](how-to-create-a-linear-gradient-brush.md).

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

[**креатеградиентстопколлектион**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Создание кисти линейного градиента](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Обзор кистей](direct2d-brushes-overview.md)
</dt> </dl>

�

�
