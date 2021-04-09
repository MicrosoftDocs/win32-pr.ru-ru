---
title: Обрезка с помощью объекта прямоугольной обрезки
description: В этом разделе показано, как использовать объект прямоугольной картинки для обрезки визуального или визуального дерева.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070834"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a><span data-ttu-id="1f483-103">Обрезка с помощью объекта прямоугольной обрезки</span><span class="sxs-lookup"><span data-stu-id="1f483-103">How to clip with a rectangle clip object</span></span>

> [!NOTE]
> <span data-ttu-id="1f483-104">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="1f483-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="1f483-105">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="1f483-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="1f483-106">В этом разделе показано, как использовать объект прямоугольной картинки для обрезки визуального или визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="1f483-106">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span>

<span data-ttu-id="1f483-107">Пример в этом разделе определяет прямоугольный клип, центрированный по положению мыши, и применяет этот клип к визуальному элементу, расположенному в клиентской области окна цели композиции.</span><span class="sxs-lookup"><span data-stu-id="1f483-107">The example in this topic defines a rectangular clip that is centered at the mouse location, and applies the clip to a visual that is centered in the client area of the composition target window.</span></span> <span data-ttu-id="1f483-108">На этом снимке экрана показан результат применения объекта прямоугольной картинки к визуальному элементу.</span><span class="sxs-lookup"><span data-stu-id="1f483-108">This screen shot shows the result of applying the rectangle clip object to the visual.</span></span>

![результат применения объекта прямоугольной картинки к визуальному элементу](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="1f483-110">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="1f483-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1f483-111">Технологии</span><span class="sxs-lookup"><span data-stu-id="1f483-111">Technologies</span></span>

-   [<span data-ttu-id="1f483-112">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="1f483-112">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="1f483-113">Графика Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1f483-113">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="1f483-114">Графическая инфраструктура DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="1f483-114">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="1f483-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1f483-115">Prerequisites</span></span>

-   <span data-ttu-id="1f483-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="1f483-116">C/C++</span></span>
-   <span data-ttu-id="1f483-117">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="1f483-117">Microsoft Win32</span></span>
-   <span data-ttu-id="1f483-118">Модель COM</span><span class="sxs-lookup"><span data-stu-id="1f483-118">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="1f483-119">Инструкции</span><span class="sxs-lookup"><span data-stu-id="1f483-119">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="1f483-120">Шаг 1. Инициализация объектов DirectComposition</span><span class="sxs-lookup"><span data-stu-id="1f483-120">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="1f483-121">Создайте объект устройства и целевой объект композиции.</span><span class="sxs-lookup"><span data-stu-id="1f483-121">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="1f483-122">Создайте визуальный элемент, задайте его содержимое и добавьте его в визуальное дерево.</span><span class="sxs-lookup"><span data-stu-id="1f483-122">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="1f483-123">Дополнительные сведения см. [в разделе как инициализировать DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="1f483-123">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-rectangle-clip-object"></a><span data-ttu-id="1f483-124">Шаг 2. Создание объекта прямоугольной обрезки</span><span class="sxs-lookup"><span data-stu-id="1f483-124">Step 2: Create the rectangle clip object</span></span>

<span data-ttu-id="1f483-125">Используйте метод [**идкомпоситиондевице:: креатеректанглеклип**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) , чтобы создать экземпляр объекта прямоугольной картинки.</span><span class="sxs-lookup"><span data-stu-id="1f483-125">Use the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method to create an instance of the rectangle clip object.</span></span>


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a><span data-ttu-id="1f483-126">Шаг 3. Задание свойств объекта «прямоугольный ролик»</span><span class="sxs-lookup"><span data-stu-id="1f483-126">Step 3: Set the properties of the rectangle clip object</span></span>

<span data-ttu-id="1f483-127">Вызовите методы интерфейса [**идкомпоситионректанглеклип**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) объекта прямоугольной коллекции, чтобы задать свойства прямоугольника обрезки.</span><span class="sxs-lookup"><span data-stu-id="1f483-127">Call the methods of the rectangle clip object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the clip rectangle.</span></span>

<span data-ttu-id="1f483-128">В следующем примере определяется прямоугольник клипа, центрированный вокруг текущего положения указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="1f483-128">The following example defines a clip rectangle that is centered around the current mouse location.</span></span> <span data-ttu-id="1f483-129">`m_offsetX` `m_offsetY` Переменные члена и содержат значения свойств Оффсеткс и offset визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="1f483-129">The `m_offsetX` and `m_offsetY` member variables contain the values of the OffsetX and OffsetY properties of the visual.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



<span data-ttu-id="1f483-130">Обратите внимание, что интерфейс [**идкомпоситионректанглеклип**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) включает следующие методы для определения прямоугольника обрезки с закругленными углами:</span><span class="sxs-lookup"><span data-stu-id="1f483-130">Note that the [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface includes the following methods for defining a clip rectangle that has rounded corners:</span></span>

-   <span data-ttu-id="1f483-131">[**сеттоплефтрадиускс**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="1f483-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span></span>
-   <span data-ttu-id="1f483-132">[**сеттоплефтрадиуси**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="1f483-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span></span>
-   <span data-ttu-id="1f483-133">[**сеттопригхтрадиускс**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="1f483-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span></span>
-   <span data-ttu-id="1f483-134">[**сеттопригхтрадиуси**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="1f483-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span></span>

### <a name="step-4-set-the-clip-property-of-the-visual"></a><span data-ttu-id="1f483-135">Шаг 4. Задание свойства Clip визуального элемента</span><span class="sxs-lookup"><span data-stu-id="1f483-135">Step 4: Set the Clip property of the visual</span></span>

<span data-ttu-id="1f483-136">Используйте метод [**идкомпоситионвисуал:: сетклип**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) , чтобы связать свойство Clip визуального элемента с объектом прямоугольной картинки.</span><span class="sxs-lookup"><span data-stu-id="1f483-136">Use the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) method to associate the Clip property of the visual with the rectangle clip object.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a><span data-ttu-id="1f483-137">Шаг 5. Фиксация композиции</span><span class="sxs-lookup"><span data-stu-id="1f483-137">Step 5: Commit the composition</span></span>

<span data-ttu-id="1f483-138">Вызовите метод [**идкомпоситиондевице:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) , чтобы зафиксировать пакет команд в Microsoft DirectComposition для обработки.</span><span class="sxs-lookup"><span data-stu-id="1f483-138">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="1f483-139">Результат применения прямоугольника обрезки появится в целевом окне.</span><span class="sxs-lookup"><span data-stu-id="1f483-139">The result of applying the clip rectangle appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a><span data-ttu-id="1f483-140">Шаг 6. освобождение объектов DirectComposition</span><span class="sxs-lookup"><span data-stu-id="1f483-140">Step 6: Free the DirectComposition objects</span></span>

<span data-ttu-id="1f483-141">Не забудьте освободить прямоугольный объект Rectangle, если он больше не нужен, а также объект устройства, целевой объект композиции и все визуальные объекты.</span><span class="sxs-lookup"><span data-stu-id="1f483-141">Be sure to free the rectangle clip object when you no longer need it, as well as the device object, the composition target object, and any visual objects.</span></span> <span data-ttu-id="1f483-142">В следующем примере вызывается определяемый приложением макрос [**саферелеасе**](/windows/desktop/medfound/saferelease) для высвобождения объектов DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="1f483-142">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a><span data-ttu-id="1f483-143">См. также</span><span class="sxs-lookup"><span data-stu-id="1f483-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f483-144">Вырезая</span><span class="sxs-lookup"><span data-stu-id="1f483-144">Clipping</span></span>](clipping.md)
</dt> </dl>

 

 