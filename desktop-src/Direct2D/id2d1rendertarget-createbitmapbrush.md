---
title: ID2D1RenderTarget Креатебитмапбруш методы
description: Создает объект ID2D1BitmapBrush из указанного растрового изображения.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- Методы Креатебитмапбруш Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 411ae2dd81fce88bec5d6a3717fe79d942de84f060c53a90b83cae461d6a49de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053094"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>Методы ID2D1RenderTarget:: Креатебитмапбруш

Создает объект [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) из указанного растрового изображения.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                                                               | Описание                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатебитмапбруш (ID2D1Bitmap \* , \_& свойства D2D1 для растровой \_ кисти \_ , \_ Свойства кисти D2D1 \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Создает объект [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) из указанного растрового изображения.<br/>                                                                                                    |
| [**Креатебитмапбруш (ID2D1Bitmap \* , \_ Свойства кисти точечного рисунка D2D1 \_ \_ \* , \_ Свойства кисти D2D1 \_ \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Создает объект [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) из указанного растрового изображения.<br/>                                                                                                    |
| [**Креатебитмапбруш (ID2D1Bitmap \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Создает объект [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) из указанного растрового изображения. Кисть использует значения по умолчанию для его режима расширения, режима интерполяции, непрозрачности и преобразования.<br/> |
| [**Креатебитмапбруш (ID2D1Bitmap \* , \_ Свойства растровой \_ кисти D2D1 \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Создает объект [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) из указанного растрового изображения. Кисть использует значения по умолчанию для его непрозрачности и преобразования.<br/>                                   |



## <a name="examples"></a>Примеры

Пример, показывающий, как закрасить область с помощью растровой кисти, см. [в разделе Создание растровой кисти](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Создание растровой кисти](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Обзор кистей](direct2d-brushes-overview.md)
</dt> </dl>

 

