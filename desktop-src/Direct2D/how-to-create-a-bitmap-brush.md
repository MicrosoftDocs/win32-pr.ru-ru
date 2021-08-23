---
title: Создание растровой кисти
description: Показывает, как создать растровую кисть с помощью Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274d359b8ad8298a4e45d01014a6e9b19aa58c4b81725c5d8c41ac931e24eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569303"
---
# <a name="how-to-create-a-bitmap-brush"></a>Создание растровой кисти

Чтобы создать растровую кисть, используйте метод [**ID2D1RenderTarget:: креатебитмапбруш**](id2d1rendertarget-createbitmapbrush.md) и укажите свойства растровой кисти. Некоторые перегрузки позволяют задавать свойства кисти. В следующем коде показано, как создать растровую кисть для заполнения квадрата и сплошную черную кисть для рисования контура квадрата. Код создает выходные данные, показанные на следующем снимке экрана.

> [!Note]  
> начиная с Windows 8 можно использовать метод [**креатебитмапбруш**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) в интерфейсе [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) , чтобы создать [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) вместо **ID2D1BitmapBrush**. **ID2D1BitmapBrush1** добавляет высококачественные режимы масштабирования в растровую кисть.

 

![снимок экрана с квадратом, заполненным точечным рисунком завода](images/brushes-ovw-bitmap.png)

1.  Объявите переменную типа [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Загрузка растрового изображения из ресурса. Дополнительные сведения см. [в статье Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  Выберите режимы расширения ([**\_ \_ режим расширения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) и режим интерполяции ([**\_ \_ \_ Режим интерполяции для растрового изображения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) кисти точечного рисунка, а затем вызовите метод [**креатебитмапбруш**](id2d1rendertarget-createbitmapbrush.md) для создания кисти, как показано в следующем коде.
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 