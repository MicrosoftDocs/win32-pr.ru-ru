---
title: Обзорное размытие DWM
description: Один из эффектов Signature диспетчер окон рабочего стола (DWM) является полупрозрачной и размытой неклиентской областью. Интерфейсы API DWM позволяют приложениям применять эти эффекты к клиентской области своих окон верхнего уровня.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Диспетчер окон рабочего стола (DWM), эффект размытия позади
- DWM (диспетчер окон рабочего стола), эффект размытия позади
- эффект размытия позади
- Полупрозрачный результат
- эффект прозрачного стекла
- Диспетчер окон рабочего стола (DWM), полупрозрачный результат
- DWM (диспетчер окон рабочего стола), полупрозрачный результат
- Диспетчер окон рабочего стола (DWM), эффект прозрачного стекла
- DWM (диспетчер окон рабочего стола), эффект прозрачного стекла
- Диспетчер окон рабочего стола (DWM), расширение рамки окна в клиентскую область
- DWM (диспетчер окон рабочего стола), расширение рамки окна на клиентскую область
- расширение рамки окна на клиентскую область
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070519"
---
# <a name="dwm-blur-behind-overview"></a><span data-ttu-id="fb132-116">Обзорное размытие DWM</span><span class="sxs-lookup"><span data-stu-id="fb132-116">DWM Blur Behind Overview</span></span>

<span data-ttu-id="fb132-117">Один из эффектов Signature диспетчер окон рабочего стола (DWM) является полупрозрачной и размытой неклиентской областью.</span><span class="sxs-lookup"><span data-stu-id="fb132-117">One of the signature Desktop Window Manager (DWM) effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="fb132-118">Интерфейсы API DWM позволяют приложениям применять эти эффекты к клиентской области своих окон верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="fb132-118">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span>

> [!Note]  
> <span data-ttu-id="fb132-119">Windows Vista Home Basic Edition не поддерживает эффект прозрачного стекла.</span><span class="sxs-lookup"><span data-stu-id="fb132-119">Windows Vista Home Basic edition does not support the transparent glass effect.</span></span> <span data-ttu-id="fb132-120">Области, которые обычно отображаются с эффектом прозрачного стекла в других выпусках Windows, отображаются как непрозрачные.</span><span class="sxs-lookup"><span data-stu-id="fb132-120">Areas that would typically render with the transparent glass effect on other Windows editions are rendered as opaque.</span></span>
> <span data-ttu-id="fb132-121">Начиная с Windows 8, вызов этой функции не приводит к эффекту размытия из-за изменения стиля в способе отрисовки окон.</span><span class="sxs-lookup"><span data-stu-id="fb132-121">Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>


 

<span data-ttu-id="fb132-122">В этом разделе обсуждаются следующие сценарии размытия клиента, которые предоставляет DWM.</span><span class="sxs-lookup"><span data-stu-id="fb132-122">This topic discusses the following client blur-behind scenarios that the DWM enables.</span></span>

-   [<span data-ttu-id="fb132-123">Добавление размытия в конкретный регион клиентской области</span><span class="sxs-lookup"><span data-stu-id="fb132-123">Adding Blur to a Specific Region of the Client Area</span></span>](#adding-blur-to-a-specific-region-of-the-client-area)
-   [<span data-ttu-id="fb132-124">Расширение рамки окна в клиентскую область</span><span class="sxs-lookup"><span data-stu-id="fb132-124">Extending the Window Frame into the Client Area</span></span>](#extending-the-window-frame-into-the-client-area)
-   [<span data-ttu-id="fb132-125">См. также</span><span class="sxs-lookup"><span data-stu-id="fb132-125">Related topics</span></span>](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a><span data-ttu-id="fb132-126">Добавление размытия в конкретный регион клиентской области</span><span class="sxs-lookup"><span data-stu-id="fb132-126">Adding Blur to a Specific Region of the Client Area</span></span>

<span data-ttu-id="fb132-127">Приложение может применить эффект размытия для всей клиентской области окна или для конкретной подобласти.</span><span class="sxs-lookup"><span data-stu-id="fb132-127">An application can apply the blur effect behind the whole client region of the window or to a specific subregion.</span></span> <span data-ttu-id="fb132-128">Это позволяет приложениям добавлять контуры в стиле и панели поиска, которые визуально отделены от остальной части приложения.</span><span class="sxs-lookup"><span data-stu-id="fb132-128">This enables applications to add styled path and search bars that are visually separate from the rest of the application.</span></span>

<span data-ttu-id="fb132-129">API, используемый в этом сценарии, — это функция [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , которая использует [**размытие DWM за константами**](dwm-bb-constants.md) и структуру [**DWM \_ блурбехинд**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .</span><span class="sxs-lookup"><span data-stu-id="fb132-129">The API used in this scenario is the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function, which makes use of the [**DWM Blur Behind Constants**](dwm-bb-constants.md) and the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure.</span></span>

<span data-ttu-id="fb132-130">В следующем примере функции `EnableBlurBehind` показано, как применить эффект размытия для всего окна.</span><span class="sxs-lookup"><span data-stu-id="fb132-130">The following example function, `EnableBlurBehind`, illustrates how to apply the blur-behind effect to the whole window.</span></span>


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="fb132-131">Обратите внимание, что в параметре *хргнблур* указано **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="fb132-131">Note that **NULL** is specified in the *hRgnBlur* parameter.</span></span> <span data-ttu-id="fb132-132">Это означает, что DWM будет применять размытие позади всего окна.</span><span class="sxs-lookup"><span data-stu-id="fb132-132">This tells the DWM to apply the blur behind the whole window.</span></span>

<span data-ttu-id="fb132-133">На следующем рисунке показан эффект размытия, применяемый ко всему окну.</span><span class="sxs-lookup"><span data-stu-id="fb132-133">The following image illustrates the blur-behind effect applied to the whole window.</span></span>

![эффект размытия, применяемый к окну](images/dwm-blurbehindwindow.png)

<span data-ttu-id="fb132-135">Чтобы применить размытие за подрегионом, примените допустимый маркер области (ХРГН) к элементу **хргнблур** структуры [**DWM \_ Блурбехинд**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) и добавьте флаг **DWM \_ BB \_ блуррегион** к элементу **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="fb132-135">To apply the blur behind a subregion, apply a valid region handle (HRGN) to the **hRgnBlur** member of the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure and add the **DWM\_BB\_BLURREGION** flag to the **dwFlags** member.</span></span>

<span data-ttu-id="fb132-136">При применении эффект размытия для подобласти окна используется альфа-канал окна для неразмытой области.</span><span class="sxs-lookup"><span data-stu-id="fb132-136">When you apply the blur-behind effect to a subregion of the window, the alpha channel of the window is used for the nonblurred area.</span></span> <span data-ttu-id="fb132-137">Это может вызвать непредвиденную прозрачность в неразмытой области окна.</span><span class="sxs-lookup"><span data-stu-id="fb132-137">This can cause an unexpected transparency in the nonblurred region of a window.</span></span> <span data-ttu-id="fb132-138">Поэтому будьте внимательны при применении к подобласти эффект размытия.</span><span class="sxs-lookup"><span data-stu-id="fb132-138">Therefore, be careful when you apply a blur effect to a subregion.</span></span>

## <a name="extending-the-window-frame-into-the-client-area"></a><span data-ttu-id="fb132-139">Расширение рамки окна в клиентскую область</span><span class="sxs-lookup"><span data-stu-id="fb132-139">Extending the Window Frame into the Client Area</span></span>

<span data-ttu-id="fb132-140">Приложение может расширять размытие рамки окна в клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="fb132-140">An application can extend the blur of the window frame into the client area.</span></span> <span data-ttu-id="fb132-141">Это полезно, если применить эффект размытия для окна с закрепленной панелью инструментов или визуально отделять элементы управления от остальной части приложения.</span><span class="sxs-lookup"><span data-stu-id="fb132-141">This is useful when you apply the blur effect behind a window with a docked toolbar or visually separate controls from the rest of an application.</span></span> <span data-ttu-id="fb132-142">Эта функция предоставляется функцией [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="fb132-142">This functionality is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span>

<span data-ttu-id="fb132-143">Чтобы включить размытие с помощью [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), используйте структуру [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) , чтобы указать степень расширения в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="fb132-143">To enable blur by using [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use the [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) structure to indicate how much to extend into the client area.</span></span> <span data-ttu-id="fb132-144">Следующий пример функции, `ExtendIntoClientBottom` ,, переключает расширение размытия в нижней части неклиентской рамки в клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="fb132-144">The following example function, `ExtendIntoClientBottom`, toggles the blur extension on the bottom of the non-client frame into the client area.</span></span>


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="fb132-145">На следующем рисунке показан эффект размытия за рамку, расширенный в нижней части клиентской области.</span><span class="sxs-lookup"><span data-stu-id="fb132-145">The following image illustrates the blur-behind effect extended into the bottom of the client area.</span></span>

![изображение, показывающее эффект размытия в нижней части клиентской области](images/dwm-extendedbottom.png)

<span data-ttu-id="fb132-147">Кроме того, с помощью метода [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) можно применить эффект «страница стекла», где эффект размытия применяется ко всей области окна без видимой границы окна.</span><span class="sxs-lookup"><span data-stu-id="fb132-147">Also available through the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) method is the "sheet of glass" effect, where the blur effect is applied to the whole surface of the window without a visible window border.</span></span> <span data-ttu-id="fb132-148">В следующем примере показан этот результат, когда клиентская область отображается без границы окна.</span><span class="sxs-lookup"><span data-stu-id="fb132-148">The following example demonstrates this effect where the client area is rendered without a window border.</span></span>


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="fb132-149">На следующем рисунке показано размытие в стиле окна «окно стекла».</span><span class="sxs-lookup"><span data-stu-id="fb132-149">The following image illustrates the blur-behind in the "sheet of glass" window style.</span></span>

![изображение, демонстрирующее эффект размытия в стиле окна "окно стекла"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a><span data-ttu-id="fb132-151">См. также</span><span class="sxs-lookup"><span data-stu-id="fb132-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb132-152">Общие сведения о диспетчере окон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="fb132-152">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="fb132-153">Включение и контроль композиции DWM</span><span class="sxs-lookup"><span data-stu-id="fb132-153">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="fb132-154">Вопросы производительности и рекомендации</span><span class="sxs-lookup"><span data-stu-id="fb132-154">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 