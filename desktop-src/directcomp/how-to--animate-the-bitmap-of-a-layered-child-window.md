---
title: Как анимировать растровое изображение для разслойного дочернего окна
description: В этом разделе описывается создание и Анимация визуального элемента, который использует растровое изображение многоуровневого окна в качестве содержимого визуального элемента.
ms.assetid: 8912CCF9-C343-45CB-AB31-55D26C118AF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038ae3d32fd49a8f795a35f35c6c87889e4c9406
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412984"
---
# <a name="how-to-animate-the-bitmap-of-a-layered-child-window"></a><span data-ttu-id="05213-103">Как анимировать растровое изображение для разслойного дочернего окна</span><span class="sxs-lookup"><span data-stu-id="05213-103">How to animate the bitmap of a layered child window</span></span>

> [!NOTE]
> <span data-ttu-id="05213-104">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="05213-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="05213-105">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="05213-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="05213-106">В этом разделе описывается создание и Анимация визуального элемента, который использует растровое изображение многоуровневого окна в качестве содержимого визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="05213-106">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <span data-ttu-id="05213-107">В примере, описанном в этом разделе, используется преобразование «анимированное масштабирование» для увеличения размеров дочернего окна от размера бегунка до полного размера.</span><span class="sxs-lookup"><span data-stu-id="05213-107">The example described in this topic uses an animated scale transformation to "grow" the bitmap of a child window from thumb size to full size.</span></span> <span data-ttu-id="05213-108">Дополнительные сведения о многоуровневых окнах см. в разделе [точечные рисунки окна](bitmap-surfaces.md).</span><span class="sxs-lookup"><span data-stu-id="05213-108">For more information about layered windows, see [Window Bitmaps](bitmap-surfaces.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="05213-109">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="05213-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="05213-110">Технологии</span><span class="sxs-lookup"><span data-stu-id="05213-110">Technologies</span></span>

-   [<span data-ttu-id="05213-111">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="05213-111">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="05213-112">Графика Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="05213-112">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="05213-113">Графическая инфраструктура DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="05213-113">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="05213-114">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="05213-114">Prerequisites</span></span>

-   <span data-ttu-id="05213-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="05213-115">C/C++</span></span>
-   <span data-ttu-id="05213-116">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="05213-116">Microsoft Win32</span></span>
-   <span data-ttu-id="05213-117">Модель COM</span><span class="sxs-lookup"><span data-stu-id="05213-117">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="05213-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="05213-118">Instructions</span></span>

### <a name="step-1-create-a-layered-child-window"></a><span data-ttu-id="05213-119">Шаг 1. Создание иерархического дочернего окна</span><span class="sxs-lookup"><span data-stu-id="05213-119">Step 1: Create a layered child window</span></span>

<span data-ttu-id="05213-120">Чтобы создать разслойное дочернее окно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="05213-120">Use the following steps to create a layered child window.</span></span>

1.  <span data-ttu-id="05213-121">Зарегистрируйте класс дочернего окна и создайте дочернее окно [**с \_ \_ Многоуровневый**](/windows/desktop/winmsg/extended-window-styles) стилем WS.</span><span class="sxs-lookup"><span data-stu-id="05213-121">Register the child window class and create a child window that has the [**WS\_EX\_LAYERED**](/windows/desktop/winmsg/extended-window-styles) style.</span></span> <span data-ttu-id="05213-122">В следующем примере `m_dpiX` и `m_dpiY` Укажите разрешение экрана в пикселях на логический дюйм, а `m_hwndMain` — это маркер главного окна приложения.</span><span class="sxs-lookup"><span data-stu-id="05213-122">In the following example, `m_dpiX` and `m_dpiY` specify the screen resolution in pixels per logical inch, and `m_hwndMain` is the handle of the main application window.</span></span>
```C++
    HWND m_hwndLayeredChild;

    
HRESULT hr = S_OK;

    WNDCLASSEXW wcex;
    wcex.cbSize         = sizeof(wcex);
    wcex.style          = 0;
    wcex.lpfnWndProc    = DemoApp::ChildWndProc;
    wcex.cbClsExtra     = 0;
    wcex.cbWndExtra     = 0;
    wcex.hInstance      = HINST_THISCOMPONENT;
    wcex.hIcon          = NULL;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH) GetStockObject (GRAY_BRUSH);
    wcex.lpszMenuName   = NULL;
    wcex.lpszClassName  = L&quot;DCompLayeredChildWindow&quot;;
    wcex.hIconSm        = NULL;

    if (!RegisterClassExW(&wcex))
    {
        return FALSE;
    }

    m_hwndLayeredChild = CreateWindowEx(WS_EX_LAYERED,
        L&quot;DCompLayeredChildWindow&quot;,                
        NULL,                                    
        WS_CHILD | WS_CLIPSIBLINGS,             
        0, 
        0, 
        static_cast<UINT>(ceil(640.0f * m_dpiX / 96.0f)),
        static_cast<UINT>(ceil(480.0f * m_dpiY / 96.0f)),                                  
        m_hwndMain,                               
        NULL,                                     
        HINST_THISCOMPONENT,                    
        this);                                   
```



    

2.  <span data-ttu-id="05213-123">Вызовите функцию [**SetLayeredWindowAttributes**](/windows/desktop/api/winuser/nf-winuser-setlayeredwindowattributes) , чтобы задать ключ цвета прозрачности и прозрачность для разслойного дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="05213-123">Call the [**SetLayeredWindowAttributes**](/windows/desktop/api/winuser/nf-winuser-setlayeredwindowattributes) function to set the transparency color key and opacity of the layered child window.</span></span> <span data-ttu-id="05213-124">Следующий код задает для ключа цвета прозрачности значение 0, а для параметра Opacity — значение непрозрачности 255 (непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="05213-124">The following code sets the transparency color key to zero and the opacity to 255 (opaque).</span></span>

```C++
    if (!SetLayeredWindowAttributes(m_hwndLayeredChild, 0, 255, LWA_ALPHA))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
```

    

3.  <span data-ttu-id="05213-125">Отображение некоторого содержимого в дочернем окне.</span><span class="sxs-lookup"><span data-stu-id="05213-125">Render some content to the child window.</span></span>

### <a name="step-2-initialize-directcomposition-objects"></a><span data-ttu-id="05213-126">Шаг 2. Инициализация объектов DirectComposition</span><span class="sxs-lookup"><span data-stu-id="05213-126">Step 2: Initialize DirectComposition objects</span></span>

<span data-ttu-id="05213-127">Создайте объект устройства и целевой объект композиции.</span><span class="sxs-lookup"><span data-stu-id="05213-127">Create the device object and the composition target object.</span></span> <span data-ttu-id="05213-128">Дополнительные сведения см. [в разделе как инициализировать DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="05213-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-3-create-a-visual-object-and-set-the-layered-child-windows-bitmap-as-the-content-property"></a><span data-ttu-id="05213-129">Шаг 3. Создание визуального объекта и установка точечного рисунка разслойного дочернего окна в качестве свойства содержимого</span><span class="sxs-lookup"><span data-stu-id="05213-129">Step 3: Create a visual object and set the layered child window's bitmap as the content property</span></span>

<span data-ttu-id="05213-130">Выполните следующие действия, чтобы создать визуальный элемент, задать его свойство содержимого для использования растрового изображения разслойного дочернего окна, а затем добавить визуальный элемент в визуальное дерево.</span><span class="sxs-lookup"><span data-stu-id="05213-130">Use the following steps to create a visual, set its content property to use the layered child window's bitmap, and then add the visual to the visual tree.</span></span>

1.  <span data-ttu-id="05213-131">Вызовите метод [**идкомпоситиондевице:: креатевисуал**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) , чтобы создать визуальный объект.</span><span class="sxs-lookup"><span data-stu-id="05213-131">Call [**IDCompositionDevice::CreateVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) to create a visual object.</span></span>
2.  <span data-ttu-id="05213-132">Создайте поверхность Microsoft DirectComposition для разслойного дочернего окна, передав маркер дочернего окна в функцию [**креатесурфацефромхвнд**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhwnd) .</span><span class="sxs-lookup"><span data-stu-id="05213-132">Create a Microsoft DirectComposition surface for the layered child window by passing the child window's handle to the [**CreateSurfaceFromHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhwnd) function.</span></span>
3.  <span data-ttu-id="05213-133">Вызовите метод [**идкомпоситионвисуал:: сетконтент**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) визуального объекта, чтобы задать новую поверхность в качестве визуального содержимого для многослойного дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="05213-133">Call the visual object's [**IDCompositionVisual::SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) method to set the new surface as the visual content of the layered child window.</span></span>
4.  <span data-ttu-id="05213-134">Добавьте визуальный объект в визуальное дерево.</span><span class="sxs-lookup"><span data-stu-id="05213-134">Add the visual object to the visual tree.</span></span> <span data-ttu-id="05213-135">Чтобы добавить визуальный элемент в корень дерева, вызовите метод [**идкомпоситионтаржет:: сетрут**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) .</span><span class="sxs-lookup"><span data-stu-id="05213-135">To add the visual to the root of the tree, call the [**IDCompositionTarget::SetRoot**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) method.</span></span> <span data-ttu-id="05213-136">Чтобы добавить визуальный элемент в качестве дочернего для другого визуального элемента, используйте метод [**идкомпоситионвисуал:: аддвисуал**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-addvisual) родительского визуального объекта.</span><span class="sxs-lookup"><span data-stu-id="05213-136">To add the visual as a child of another visual, use the [**IDCompositionVisual::AddVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-addvisual) method of the parent visual.</span></span>

<span data-ttu-id="05213-137">В следующем примере создается визуальный объект, устанавливается его свойство содержимого для использования точечного рисунка дочернего окна слоя и добавляется визуальный элемент в корень визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="05213-137">The following example creates a visual object, sets its Content property to use the layered child window's bitmap, and adds the visual to the root of the visual tree.</span></span>


```C++
IDCompositionVisual *pVisual = nullptr;
IUnknown* pSurface    = nullptr;

hr = m_pDevice->CreateVisual(&pVisual);
if (SUCCEEDED(hr))
{
    hr = m_pDevice->CreateSurfaceFromHwnd(m_hwndLayeredChild, &pSurface);
}

if (SUCCEEDED(hr))
{
    hr = pVisual->SetContent(pSurface);
}

if (SUCCEEDED(hr))
{
    hr = m_pCompTarget->SetRoot(pVisual);
}
```



### <a name="step-4-create-an-animation-object-and-a-scale-transform-object"></a><span data-ttu-id="05213-138">Шаг 4. Создание объекта анимации и объекта преобразования масштабирования</span><span class="sxs-lookup"><span data-stu-id="05213-138">Step 4: Create an animation object and a scale transform object</span></span>

<span data-ttu-id="05213-139">Используйте метод [**идкомпоситиондевице:: креатеаниматион**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) для создания объекта анимации и метод [**Идкомпоситиондевице:: креатескалетрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform) для создания объекта преобразования масштаба.</span><span class="sxs-lookup"><span data-stu-id="05213-139">Use the [**IDCompositionDevice::CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) method to create an animation object, and the [**IDCompositionDevice::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform) method to create a scale transform object.</span></span>


```C++
IDCompositionAnimation *pAnimateScale = NULL;
IDCompositionScaleTransform *pScale = NULL;

if (SUCCEEDED(hr))
{
    hr = m_pDevice->CreateAnimation(&pAnimateScale);
}

if (SUCCEEDED(hr))
{
    // Create the scale transform object.
    hr = m_pDevice->CreateScaleTransform(&pScale);
}
```



### <a name="step-5-build-the-animation-function"></a><span data-ttu-id="05213-140">Шаг 5. построение функции анимации</span><span class="sxs-lookup"><span data-stu-id="05213-140">Step 5: Build the animation function</span></span>

<span data-ttu-id="05213-141">Используйте методы интерфейса [**идкомпоситионаниматион**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) объекта Animation для создания функции анимации.</span><span class="sxs-lookup"><span data-stu-id="05213-141">Use the methods of the animation object's [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) interface to build an animation function.</span></span>

<span data-ttu-id="05213-142">В следующем примере создается простая функция анимации, состоящая из одного сегмента полинома в кубических и одного конечного сегмента.</span><span class="sxs-lookup"><span data-stu-id="05213-142">The following example builds a simple animation function that consists of one cubic polynomial segment and one end segment.</span></span>


```C++
pAnimateScale->AddCubic(
    0.0f,  // offset from beginning of animation function, in seconds
    0.0f,  // constant coefficient  
    1.0f,  // linear coefficient
    0.0f,  // quadratic coefficient
    0.0f); // cubic coefficient
pAnimateScale->End(1.0f, 1.0f);
```



### <a name="step-6-apply-the-animation-object-to-properties-of-the-scale-transform-object"></a><span data-ttu-id="05213-143">Шаг 6. применение объекта анимации к свойствам объекта преобразования масштаба</span><span class="sxs-lookup"><span data-stu-id="05213-143">Step 6: Apply the animation object to properties of the scale transform object</span></span>

<span data-ttu-id="05213-144">Используйте методы [**идкомпоситионскале:: сетскалекс**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscalex(idcompositionanimation)) и [**сетскалэй**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscaley(idcompositionanimation)) , чтобы применить объект анимации к свойствам ScaleX и scale объекта преобразования масштаба.</span><span class="sxs-lookup"><span data-stu-id="05213-144">Use the [**IDCompositionScale::SetScaleX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscalex(idcompositionanimation)) and [**SetScaleY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscaley(idcompositionanimation)) methods to apply the animation object to the ScaleX and ScaleY properties of the scale transform object.</span></span>


```C++
// Find the center of the child window.
RECT rcChild = { };
GetClientRect(m_hwndLayeredChild, &rcChild);
float centerX = rcChild.right / 2.0f;
float centerY = rcChild.bottom / 2.0f;

// Scale from the center point of the child window's bitmap.
pScale->SetCenterX(centerX);
pScale->SetCenterY(centerY);

// Use the same animation object to animate the X and Y scale
// factors.
pScale->SetScaleX(pAnimateScale);
pScale->SetScaleY(pAnimateScale);
```



### <a name="step-7-apply-the-scale-transform-object-to-the-transform-property-of-the-visual"></a><span data-ttu-id="05213-145">Шаг 7. применение объекта преобразования масштаба к свойству Transform визуального элемента</span><span class="sxs-lookup"><span data-stu-id="05213-145">Step 7: Apply the scale transform object to the transform property of the visual</span></span>

<span data-ttu-id="05213-146">Используйте метод [**идкомпоситионвисуал:: сеттрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) , чтобы применить объект преобразования масштаба к свойству Transform визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="05213-146">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) method to apply the scale transform object to the Transform property of the visual.</span></span>


```C++
hr = pVisual->SetTransform(pScale);
```



### <a name="step-8-cloak-the-layered-child-window"></a><span data-ttu-id="05213-147">Шаг 8. Маскировка разслойного дочернего окна</span><span class="sxs-lookup"><span data-stu-id="05213-147">Step 8: Cloak the layered child window</span></span>

<span data-ttu-id="05213-148">Перед фиксацией анимации используйте функцию [**двмсетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) с флагом [**\_ маскировки двмва**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) , чтобы «маскировать» разслойное дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="05213-148">Before committing the animation, use the [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) function with the [**DWMWA\_CLOAK**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag to "cloak" the layered child window.</span></span> <span data-ttu-id="05213-149">Маскировка удаляет разслойное дочернее окно из представления, в то время как анимированная версия представления растрового изображения окна отображается на экране.</span><span class="sxs-lookup"><span data-stu-id="05213-149">Cloaking removes the layered child window from view while the animated version of the window's bitmap view is being rendered to the screen.</span></span>


```C++
BOOL fCloak = TRUE;
DwmSetWindowAttribute(pDemoApp->m_hwndLayeredChild,
    DWMWA_CLOAK,
    &fCloak,
    sizeof(fCloak));
```



### <a name="step-9-commit-the-composition"></a><span data-ttu-id="05213-150">Шаг 9. Фиксация композиции</span><span class="sxs-lookup"><span data-stu-id="05213-150">Step 9: Commit the composition</span></span>

<span data-ttu-id="05213-151">Используйте метод [**идкомпоситиондевице:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) для фиксации пакета команд в Microsoft DirectComposition для обработки.</span><span class="sxs-lookup"><span data-stu-id="05213-151">Use the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="05213-152">Анимация появится в целевом окне.</span><span class="sxs-lookup"><span data-stu-id="05213-152">The animation will appear in the target window.</span></span>

### <a name="step-10-uncloak-the-layered-child-window"></a><span data-ttu-id="05213-153">Шаг 10. Отмена маскировки дочернего окна слоя</span><span class="sxs-lookup"><span data-stu-id="05213-153">Step 10: Uncloak the layered child window</span></span>

<span data-ttu-id="05213-154">После завершения анимации используйте функцию [**двмсетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) с флагом **\_ маскировки двмва** , чтобы отменить маскировку многослойного дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="05213-154">After the animation is finished, use the [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) function with the **DWMWA\_CLOAK** flag to uncloak the layered child window.</span></span>

### <a name="step-11-release-directcomposition-objects"></a><span data-ttu-id="05213-155">Шаг 11. освобождение объектов DirectComposition</span><span class="sxs-lookup"><span data-stu-id="05213-155">Step 11: Release DirectComposition objects</span></span>

<span data-ttu-id="05213-156">Не забудьте освободить все объекты DirectComposition, если они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="05213-156">Be sure to release all DirectComposition objects when you no longer need them.</span></span> <span data-ttu-id="05213-157">В следующем примере вызывается определяемый приложением макрос [**саферелеасе**](/windows/desktop/medfound/saferelease) для высвобождения объектов DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="05213-157">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
SafeRelease(&pVisual);
SafeRelease(&pAnimateScale);
SafeRelease(&pScale);


SafeRelease(&m_pDevice);
SafeRelease(&m_pCompTarget);
```





## <a name="complete-example"></a><span data-ttu-id="05213-158">Полный пример</span><span class="sxs-lookup"><span data-stu-id="05213-158">Complete example</span></span>


```C++
//
// AnimateLayeredChildWindow.h
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>
#include <wincodec.h>

// C RunTime Header Files
#include <math.h>

// DirectComposition Header File
#include <dcomp.h>

// Direct2D Header Files
#include <d2d1.h>
#include <d2d1helper.h>

// Desktop Window Manager (DWM) Header File
#include <dwmapi.h>


/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT InitializeMainWindow();
    HRESULT InitializeLayeredChildWindow();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionObjects();

    HRESULT CreateDeviceIndependentResources();
    HRESULT CreateDeviceResources();
    void DiscardDeviceResources();

    HRESULT OnChildClick();
    HRESULT OnChildRender();

    HRESULT LoadResourceD2DBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
        ID2D1Bitmap **ppBitmap
        );

    static LRESULT CALLBACK MainWndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

    static LRESULT CALLBACK ChildWndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );
    
 private:
    int m_dpiX;
    int m_dpiY;
    int m_childOffsetX;
    int m_childOffsetY;

    HWND m_hwndMain;
    HWND m_hwndLayeredChild;

    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
    ID2D1HwndRenderTarget *m_pRenderTarget;
    ID2D1Factory *m_pD2DFactory;
    ID2D1Bitmap *m_pBitmap;
    IWICImagingFactory *m_pWICFactory;

 };


//
// AnimateLayeredChildWindow.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Click the thumnail image to animate the transition
//   of the child window from thumbsize to fullsize. Click the child
//   window again to reset.

#include &quot;AnimateLayeredChildWindow.h&quot;

#define TIMER_ID 100

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE   /* hInstance */,
    HINSTANCE   /* hPrevInstance */,
    LPSTR       /* lpCmdLine */,
    int         /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.InitializeMainWindow()) && SUCCEEDED(app.InitializeLayeredChildWindow()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                        *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_dpiX(0),
    m_dpiY(0),
    m_childOffsetX(20),
    m_childOffsetY(40),
    m_hwndMain(NULL),
    m_hwndLayeredChild(NULL),
    m_pDevice(NULL),
    m_pCompTarget(NULL),
    m_pRenderTarget(NULL),
    m_pBitmap(NULL),
    m_pD2DFactory(NULL),
    m_pWICFactory(NULL)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pRenderTarget);
    SafeRelease(&m_pBitmap),
    SafeRelease(&m_pD2DFactory);
    SafeRelease(&m_pWICFactory);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::InitializeMainWindow()
{
    HRESULT hr = S_OK;

    // Initialize device-independent resources, such 
    // as the Direct2D factory.
    hr = CreateDeviceIndependentResources();
    if (SUCCEEDED(hr))
    {
        // Register the main window class.
        WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
        wcex.style         = 0;
        wcex.lpfnWndProc   = DemoApp::MainWndProc;
        wcex.cbClsExtra    = 0;
        wcex.cbWndExtra    = sizeof(LONG_PTR);
        wcex.hInstance     = HINST_THISCOMPONENT;
        wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
        wcex.lpszMenuName  = NULL;
        wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
        wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

        RegisterClassEx(&wcex);

        RECT rect = { };
        SetRect(&rect, 0, 0, 640, 480);
        AdjustWindowRect(&rect, WS_OVERLAPPED | WS_SYSMENU, FALSE); 

        // Create the main application window.
        //

        // Because the CreateWindow function takes its size in pixels, we
        // obtain the system DPI and use it to scale the window size.
        HDC hdc = GetDC(NULL);
        if (hdc)
        {
            m_dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
            m_dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
            ReleaseDC(NULL, hdc);
        }

        float width = static_cast<float>(rect.right - rect.left);
        float height = static_cast<float>(rect.bottom - rect.top);

        m_hwndMain = CreateWindow(
            L&quot;DirectCompDemoApp&quot;,
            L&quot;DirectComposition Demo Application&quot;,
            WS_OVERLAPPED | WS_SYSMENU,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(width * m_dpiX / 96.f)),
            static_cast<UINT>(ceil(height * m_dpiY / 96.f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );
    }

    hr = m_hwndMain ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Create and initialize the DirectCompositoin objects.
        hr =  InitializeDirectCompositionObjects();
    }

    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwndMain, SW_SHOWNORMAL);
        UpdateWindow(m_hwndMain);
    }
  
    return hr;
}

/*******************************************************************
*                                                                  *
* Create the layered child window.                                 *
*                                                                  *
/******************************************************************/

HRESULT DemoApp::InitializeLayeredChildWindow()
{
    int thumbWidth = 48;
    int thumbHeight = 32;

    HRESULT hr = S_OK;

    WNDCLASSEXW wcex;
    wcex.cbSize         = sizeof(wcex);
    wcex.style          = 0;
    wcex.lpfnWndProc    = DemoApp::ChildWndProc;
    wcex.cbClsExtra     = 0;
    wcex.cbWndExtra     = 0;
    wcex.hInstance      = HINST_THISCOMPONENT;
    wcex.hIcon          = NULL;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH) GetStockObject (GRAY_BRUSH);
    wcex.lpszMenuName   = NULL;
    wcex.lpszClassName  = L&quot;DCompLayeredChildWindow&quot;;
    wcex.hIconSm        = NULL;
    
    if (!RegisterClassExW(&wcex))
    {
        return FALSE;
    }

    m_hwndLayeredChild = CreateWindowEx(WS_EX_LAYERED,
        L&quot;DCompLayeredChildWindow&quot;,                
        NULL,                                    
        WS_CHILD | WS_CLIPSIBLINGS,             
        0, 
        0, 
        static_cast<UINT>(ceil(640.0f * m_dpiX / 96.0f)),
        static_cast<UINT>(ceil(480.0f * m_dpiY / 96.0f)),                                  
        m_hwndMain,                               
        NULL,                                     
        HINST_THISCOMPONENT,                    
        this);                                   

    hr = m_hwndLayeredChild ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Set the opacity and transparency color key of the layered 
        // child window.
        if (!SetLayeredWindowAttributes(m_hwndLayeredChild, 0, 255, LWA_ALPHA))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // While the child window is fullsize, load the bitmap resource and
        // render it to the child window.  
        hr = CreateDeviceResources(); 
    }
    
    if (SUCCEEDED(hr))
    {
        // Reduce the window to thumbsize.
        MoveWindow(m_hwndLayeredChild, m_childOffsetX, m_childOffsetY, 
            thumbWidth, thumbHeight, TRUE);
        ShowWindow(m_hwndLayeredChild, SW_SHOWNORMAL);
        UpdateWindow(m_hwndLayeredChild);
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionObjects()
{
    HRESULT hr = S_OK;

    // Create a DirectComposition device object. 
    hr = DCompositionCreateDevice(nullptr, __uuidof(IDCompositionDevice), 
        reinterpret_cast<void**>(&m_pDevice));

    if (SUCCEEDED(hr))
    {
        // Create the composition target object.
        hr = m_pDevice->CreateTargetForHwnd(m_hwndMain, TRUE, &m_pCompTarget);   
    }

    return hr;
}


/******************************************************************
*                                                                 *
*  This method is used to create resources which are not bound    *
*  to any device. Their lifetime effectively extends for the      *
*  duration of the app.                                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pWICFactory)
        );

    if (SUCCEEDED(hr))
    {
        // Create a Direct2D factory.
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the D2D bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateDeviceResources()
{
    HRESULT hr = S_OK;

    RECT rc;
    GetClientRect(m_hwndLayeredChild, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(
        rc.right - rc.left,
        rc.bottom - rc.top
        );

    // Create a Direct2D render target.
    hr = m_pD2DFactory->CreateHwndRenderTarget(
        D2D1::RenderTargetProperties(),
        D2D1::HwndRenderTargetProperties(m_hwndLayeredChild, size),
        &m_pRenderTarget
        );

    if (SUCCEEDED(hr))
    {
        hr = LoadResourceD2DBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L&quot;WhiteFlowers&quot;,
            L&quot;Image&quot;,
            &m_pBitmap
            );
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardDeviceResources()
{
    SafeRelease(&m_pRenderTarget);
    SafeRelease(&m_pBitmap);
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message handler.                             *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::MainWndProc(HWND hwnd, UINT message, 
    WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {
 
            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardDeviceResources();
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
}

/******************************************************************
*                                                                 *
*  The layered child window&#39;s message handler.                    *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::ChildWndProc(HWND hwnd, UINT message, 
    WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {
            case WM_PAINT:
                {
                    pDemoApp->OnChildRender();
                    ValidateRect(hwnd, NULL);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_LBUTTONDOWN:
                {
                    HRESULT hr = S_OK;
                    static BOOL fThumbsize = TRUE;

                    // If the child window is already fullsize, reset
                    // the visual tree and return the child window
                    // to thumbsize and move it to its initial location.
                    if (!fThumbsize)
                    {
                        pDemoApp->m_pCompTarget->SetRoot(NULL);
                        hr = pDemoApp->m_pDevice->Commit();  

                        MoveWindow(pDemoApp->m_hwndLayeredChild, 
                            pDemoApp->m_childOffsetX, 
                            pDemoApp->m_childOffsetY, 48, 32, TRUE);

                        pDemoApp->OnChildRender();
                    }   
                    else
                    {
                        // Cloak the child window.
                        BOOL fCloak = TRUE;
                        DwmSetWindowAttribute(pDemoApp->m_hwndLayeredChild,
                            DWMWA_CLOAK,
                            &fCloak,
                            sizeof(fCloak));

                        pDemoApp->OnChildClick();
                    }                    
                    fThumbsize = !fThumbsize;
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_TIMER:
                {
                    // Uncloak the child window.
                    BOOL fCloak = FALSE;
                    DwmSetWindowAttribute(pDemoApp->m_hwndLayeredChild,
                        DWMWA_CLOAK,
                        &fCloak,
                        sizeof(fCloak)); 
                    KillTimer(pDemoApp->m_hwndLayeredChild, TIMER_ID);
                }
                wasHandled = true;
                result = 0;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
}


/******************************************************************
*                                                                 *
*  Draws a bitmap in the layered child window.                    *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnChildRender()
{
    HRESULT hr = S_OK;
 
    // Retrieve the size of the render target.
    D2D1_SIZE_F size = m_pRenderTarget->GetSize();
    
    m_pRenderTarget->BeginDraw();
    
    // Draw a bitmap scaled to fill the window.
    m_pRenderTarget->DrawBitmap(
        m_pBitmap,
        D2D1::RectF(0.0f, 0.0f, size.width, size.height)
        );

    hr = m_pRenderTarget->EndDraw();

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Handles a mouse click in the layered child window by animating *
*  the transition from a thumbsize window to a fullsize window.   *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnChildClick()
{
    int fullWidth = 640;
    int fullHeight = 480;
    HRESULT hr = S_OK;

    IDCompositionVisual *pVisual = nullptr;
    IUnknown* pSurface    = nullptr;

    hr = m_pDevice->CreateVisual(&pVisual);
    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->CreateSurfaceFromHwnd(m_hwndLayeredChild, &pSurface);
    }

    if (SUCCEEDED(hr))
    {
        hr = pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        hr = m_pCompTarget->SetRoot(pVisual);
    }

    if (SUCCEEDED(hr))
    {
       // Position the visual at the same location as the
       // the child window.
        hr = pVisual->SetOffsetX(static_cast<float>(m_childOffsetX));
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(static_cast<float>(m_childOffsetY));  
        }
    }


    IDCompositionAnimation *pAnimateX = NULL;
    IDCompositionAnimation *pAnimateY = NULL;

    if (SUCCEEDED(hr))
    {
        // Create the animation objects.
        hr = m_pDevice->CreateAnimation(&pAnimateX);
        if (SUCCEEDED(hr))
        {
            hr = m_pDevice->CreateAnimation(&pAnimateY);
        }
    }

    IDCompositionAnimation *pAnimateScale = NULL;
    IDCompositionScaleTransform *pScale = NULL;

    if (SUCCEEDED(hr))
    {
        hr = m_pDevice->CreateAnimation(&pAnimateScale);
    }

    if (SUCCEEDED(hr))
    {
        // Create the scale transform object.
        hr = m_pDevice->CreateScaleTransform(&pScale);
    }

    if (SUCCEEDED(hr))
    {
        // Calculate the X and Y offsets that will position the child window 
        // in the center of the main window&#39;s client area.
        RECT rcParent = { };
        RECT rcChild = { };
        GetClientRect(m_hwndMain, &rcParent);
        GetClientRect(m_hwndLayeredChild, &rcChild);
        float endValX = rcParent.right / 2.0f - rcChild.right / 2.0f;
        float endValY = rcParent.bottom / 2.0f - rcChild.bottom / 2.0f;
 
        // Build the animation functions that will move the visual to the 
        // center of the main window&#39;s client area.
        pAnimateX->AddCubic(0.0f, static_cast<float>(m_childOffsetX), 
            endValX - m_childOffsetX, 0.0f, 0.0f);
        pAnimateX->End(0.9f, endValX);

        pAnimateY->AddCubic(0.0f, static_cast<float>(m_childOffsetY), 
            endValY - m_childOffsetY, 0.0f, 0.0f);
        pAnimateY->End(0.9f, endValY);

        // Associate the animation objects with the offset properties of 
        // the visual.
        hr = pVisual->SetOffsetX(pAnimateX);
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(pAnimateY);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual tree.
        hr = m_pDevice->Commit();  

        // Give the animation a chance to run.
        Sleep(900);
    }

    if (SUCCEEDED(hr))
    {
        // Align the visual with the upper-left corner of the
        // parent window&#39;s client area.
        pVisual->SetOffsetX(0.0);
        pVisual->SetOffsetY(0.0);

        // Enlarge the child window to fill the main window.
        if (!MoveWindow(m_hwndLayeredChild, 0, 0, fullWidth, fullHeight, TRUE))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // Add animation primitives that define the animation object function 
        // used to scale up the child window&#39;s bitmap.
        pAnimateScale->AddCubic(
            0.0f,  // offset from beginning of animation function, in seconds
            0.0f,  // constant coefficient  
            1.0f,  // linear coefficient
            0.0f,  // quadratic coefficient
            0.0f); // cubic coefficient
        pAnimateScale->End(1.0f, 1.0f);

        // Find the center of the child window.
        RECT rcChild = { };
        GetClientRect(m_hwndLayeredChild, &rcChild);
        float centerX = rcChild.right / 2.0f;
        float centerY = rcChild.bottom / 2.0f;

        // Scale from the center point of the child window&#39;s bitmap.
        pScale->SetCenterX(centerX);
        pScale->SetCenterY(centerY);

        // Use the same animation object to animate the X and Y scale
        // factors.
        pScale->SetScaleX(pAnimateScale);
        pScale->SetScaleY(pAnimateScale);

        // Set the Transform property of the visual to use the scale 
        // transform.
        hr = pVisual->SetTransform(pScale);
    }
    
    if (SUCCEEDED(hr))
    {   // Commit the visual tree.
        hr = m_pDevice->Commit();  

        // Use a WM_TIMER message in the child window procedure 
        // to uncloak the child window. 
        SetTimer(m_hwndLayeredChild, TIMER_ID, 1000, NULL);
    }

    SafeRelease(&pAnimateX);
    SafeRelease(&pAnimateY);
    SafeRelease(&pVisual);
    SafeRelease(&pAnimateScale);
    SafeRelease(&pScale);
    
    return hr;
}


/******************************************************************
*                                                                 *
*  This method will create a Direct2D bitmap from an application  *
*  resource.                                                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceD2DBitmap(
    ID2D1RenderTarget *pRenderTarget,
    IWICImagingFactory *pIWICFactory,
    PCWSTR resourceName,
    PCWSTR resourceType,
    ID2D1Bitmap **ppBitmap
    )
{
    HRESULT hr = S_OK;
    IWICBitmapDecoder *pDecoder = NULL;
    IWICBitmapFrameDecode *pSource = NULL;
    IWICStream *pStream = NULL;
    IWICFormatConverter *pConverter = NULL;

    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource.
    imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);

    hr = imageResHandle ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Load the resource.
        imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

        hr = imageResDataHandle ? S_OK : E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        // Lock it to get a system memory pointer.
        pImageFile = LockResource(imageResDataHandle);

        hr = pImageFile ? S_OK : E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        // Calculate the size.
        imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

        hr = imageFileSize ? S_OK : E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        // Create a WIC stream to map onto the memory.
        hr = pIWICFactory->CreateStream(&pStream);
    }

    if (SUCCEEDED(hr))
    {
        // Initialize the stream with the memory pointer and size.
        hr = pStream->InitializeFromMemory(
            reinterpret_cast<BYTE*>(pImageFile),
            imageFileSize
            );
    }

    if (SUCCEEDED(hr))
    {
        // Create a decoder for the stream.
        hr = pIWICFactory->CreateDecoderFromStream(
            pStream,
            NULL,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
    }

    if (SUCCEEDED(hr))
    {
        // Create the initial frame.
        hr = pDecoder->GetFrame(0, &pSource);
    }

    if (SUCCEEDED(hr))
    {
        // Convert the image format to 32bppPBGRA
        // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
        hr = pIWICFactory->CreateFormatConverter(&pConverter);
    }

    if (SUCCEEDED(hr))
    {
        hr = pConverter->Initialize(
            pSource,
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            NULL,
            0.f,
            WICBitmapPaletteTypeMedianCut
            );
    }

    if (SUCCEEDED(hr))
    {
        // Create a Direct2D bitmap from the WIC bitmap.
        hr = pRenderTarget->CreateBitmapFromWicBitmap(
            pConverter,
            NULL,
            ppBitmap
            );
    }

    SafeRelease(&pDecoder);
    SafeRelease(&pSource);
    SafeRelease(&pStream);
    SafeRelease(&pConverter);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="05213-159">См. также</span><span class="sxs-lookup"><span data-stu-id="05213-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05213-160">Анимация</span><span class="sxs-lookup"><span data-stu-id="05213-160">Animation</span></span>](animation.md)
</dt> <dt>

[<span data-ttu-id="05213-161">Растровые объекты</span><span class="sxs-lookup"><span data-stu-id="05213-161">Bitmap objects</span></span>](bitmap-surfaces.md)
</dt> <dt>

[<span data-ttu-id="05213-162">Пример дочернего окна многоуровневого DirectComposition</span><span class="sxs-lookup"><span data-stu-id="05213-162">DirectComposition layered child window sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionLayeredChildWindow)
</dt> </dl>

 

 