---
title: Создание растровой кисти
description: Показывает, как создать растровую кисть с помощью Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672347"
---
# <a name="how-to-create-a-bitmap-brush"></a><span data-ttu-id="5b79a-103">Создание растровой кисти</span><span class="sxs-lookup"><span data-stu-id="5b79a-103">How to Create a Bitmap Brush</span></span>

<span data-ttu-id="5b79a-104">Чтобы создать растровую кисть, используйте метод [**ID2D1RenderTarget:: креатебитмапбруш**](id2d1rendertarget-createbitmapbrush.md) и укажите свойства растровой кисти.</span><span class="sxs-lookup"><span data-stu-id="5b79a-104">To create a bitmap brush, use the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the bitmap brush properties.</span></span> <span data-ttu-id="5b79a-105">Некоторые перегрузки позволяют задавать свойства кисти.</span><span class="sxs-lookup"><span data-stu-id="5b79a-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="5b79a-106">В следующем коде показано, как создать растровую кисть для заполнения квадрата и сплошную черную кисть для рисования контура квадрата.</span><span class="sxs-lookup"><span data-stu-id="5b79a-106">The following code shows how to create a bitmap brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="5b79a-107">Код создает выходные данные, показанные на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="5b79a-107">The code produces the output shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="5b79a-108">Начиная с Windows 8, можно использовать метод [**креатебитмапбруш**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) в интерфейсе [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) , чтобы создать [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) вместо **ID2D1BitmapBrush**.</span><span class="sxs-lookup"><span data-stu-id="5b79a-108">Starting with Windows 8, you can use the [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface to create a [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) instead of a **ID2D1BitmapBrush**.</span></span> <span data-ttu-id="5b79a-109">**ID2D1BitmapBrush1** добавляет высококачественные режимы масштабирования в растровую кисть.</span><span class="sxs-lookup"><span data-stu-id="5b79a-109">**ID2D1BitmapBrush1** adds high-quality scaling modes to the bitmap brush.</span></span>

 

![снимок экрана с квадратом, заполненным точечным рисунком завода](images/brushes-ovw-bitmap.png)

1.  <span data-ttu-id="5b79a-111">Объявите переменную типа [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="5b79a-111">Declare a variable of type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  <span data-ttu-id="5b79a-112">Загрузка растрового изображения из ресурса.</span><span class="sxs-lookup"><span data-stu-id="5b79a-112">Load a bitmap from a resource.</span></span> <span data-ttu-id="5b79a-113">Дополнительные сведения см. [в статье Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="5b79a-113">For more information, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
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

    

3.  <span data-ttu-id="5b79a-114">Выберите режимы расширения ([**\_ \_ режим расширения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) и режим интерполяции ([**\_ \_ \_ Режим интерполяции для растрового изображения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) кисти точечного рисунка, а затем вызовите метод [**креатебитмапбруш**](id2d1rendertarget-createbitmapbrush.md) для создания кисти, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="5b79a-114">Choose the extend modes ([**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) and interpolation mode ([**D2D1\_BITMAP\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) of the bitmap brush and then call the [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method to create a brush, as shown in the following code.</span></span>
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5b79a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5b79a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b79a-116">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="5b79a-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 