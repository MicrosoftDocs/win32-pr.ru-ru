---
title: Как применять двумерные преобразования
description: В этом разделе показано, как применять двумерные преобразования к визуальному элементу с помощью Microsoft DirectComposition.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- как применять DirectComposition 2D-преобразования
- DirectComposition 2D-преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52d2e0ce9fbb56547c42ea4ea18d57d173a7e40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413456"
---
# <a name="how-to-apply-2d-transforms"></a><span data-ttu-id="a92c2-105">Как применять двумерные преобразования</span><span class="sxs-lookup"><span data-stu-id="a92c2-105">How to apply 2D transforms</span></span>

> [!NOTE]
> <span data-ttu-id="a92c2-106">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="a92c2-106">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="a92c2-107">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="a92c2-107">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="a92c2-108">В этом разделе показано, как применять двумерные преобразования к визуальному элементу с помощью Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="a92c2-108">This topic demonstrates how to apply 2D transforms to a visual by using Microsoft DirectComposition.</span></span> <span data-ttu-id="a92c2-109">В примере в этом разделе применяется группа преобразований, которые:</span><span class="sxs-lookup"><span data-stu-id="a92c2-109">The example in this topic applies a group of transforms that:</span></span>

1.  <span data-ttu-id="a92c2-110">Поворот визуального элемента на 180 градусов.</span><span class="sxs-lookup"><span data-stu-id="a92c2-110">Rotate the visual by 180 degrees.</span></span>
2.  <span data-ttu-id="a92c2-111">Увеличение масштаба визуального элемента до трех его исходных размеров.</span><span class="sxs-lookup"><span data-stu-id="a92c2-111">Scale up the visual to three times its original size.</span></span>
3.  <span data-ttu-id="a92c2-112">Сдвиг (перемещение) визуальных элементов 150 пикселей справа от его исходной точки.</span><span class="sxs-lookup"><span data-stu-id="a92c2-112">Translate (move) the visual 150 pixels to the right of its original position.</span></span>

<span data-ttu-id="a92c2-113">На следующем снимке экрана показан визуальный элемент до и после применения 2D-преобразований.</span><span class="sxs-lookup"><span data-stu-id="a92c2-113">The following screen shots show the visual before and after applying the 2D transforms.</span></span>

![результат применения группы 2D-преобразований к визуальному элементу](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="a92c2-115">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="a92c2-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a92c2-116">Технологии</span><span class="sxs-lookup"><span data-stu-id="a92c2-116">Technologies</span></span>

-   [<span data-ttu-id="a92c2-117">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="a92c2-117">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="a92c2-118">Графика Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a92c2-118">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="a92c2-119">Графическая инфраструктура DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="a92c2-119">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="a92c2-120">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a92c2-120">Prerequisites</span></span>

-   <span data-ttu-id="a92c2-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="a92c2-121">C/C++</span></span>
-   <span data-ttu-id="a92c2-122">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="a92c2-122">Microsoft Win32</span></span>
-   <span data-ttu-id="a92c2-123">Модель COM</span><span class="sxs-lookup"><span data-stu-id="a92c2-123">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="a92c2-124">Инструкции</span><span class="sxs-lookup"><span data-stu-id="a92c2-124">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="a92c2-125">Шаг 1. Инициализация объектов DirectComposition</span><span class="sxs-lookup"><span data-stu-id="a92c2-125">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="a92c2-126">Создайте объект устройства и целевой объект композиции.</span><span class="sxs-lookup"><span data-stu-id="a92c2-126">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="a92c2-127">Создайте визуальный элемент, задайте его содержимое и добавьте его в визуальное дерево.</span><span class="sxs-lookup"><span data-stu-id="a92c2-127">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="a92c2-128">Дополнительные сведения см. [в разделе как инициализировать DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="a92c2-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-transform-group-array"></a><span data-ttu-id="a92c2-129">Шаг 2. Создание массива группы преобразований</span><span class="sxs-lookup"><span data-stu-id="a92c2-129">Step 2: Create the transform group array</span></span>


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a><span data-ttu-id="a92c2-130">Шаг 3. Создание объектов преобразования, установка их свойств и добавление их в массив группы преобразования</span><span class="sxs-lookup"><span data-stu-id="a92c2-130">Step 3: Create the transform objects, set their properties, and add them to the transform group array</span></span>

1.  <span data-ttu-id="a92c2-131">Используйте методы [**идкомпоситиондевице:: креатеротатетрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: креатескалетрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)и [**:: креатетранслатетрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) для создания объектов Transform.</span><span class="sxs-lookup"><span data-stu-id="a92c2-131">Use the [**IDCompositionDevice::CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform), and [**::CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) methods to create the transform objects.</span></span>
2.  <span data-ttu-id="a92c2-132">Используйте функции элементов интерфейсов [**идкомпоситионротатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**идкомпоситионскалетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)и [**идкомпоситионтранслатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) , чтобы задать свойства преобразований.</span><span class="sxs-lookup"><span data-stu-id="a92c2-132">Use the member functions of the [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform), and [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) interfaces to set the properties of the transforms.</span></span>
3.  <span data-ttu-id="a92c2-133">Скопируйте указатели интерфейса преобразования в массив группы преобразования.</span><span class="sxs-lookup"><span data-stu-id="a92c2-133">Copy the transform interface pointers to the transform group array.</span></span>


```C++
IDCompositionRotateTransform *pRotateTransform = nullptr;
IDCompositionScaleTransform *pScaleTransform = nullptr;
IDCompositionTranslateTransform *pTranslateTransform = nullptr;
IDCompositionTransform *pTransformGroup = nullptr;

// Create the rotate transform.
hr = pDevice->CreateRotateTransform(&pRotateTransform);

if (SUCCEEDED(hr))
{
    // Set the center of rotation to the center point of the visual.
    hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
    
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
    }

    // Set the rotate angle to 180 degrees.
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetAngle(180.0f);
    }

    // Add the rotate transform to the transform group array.
    pTransforms[0] = pRotateTransform;

    // Create the scale transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Set the scaling origin to the upper-right corner of the visual.
    hr = pScaleTransform->SetCenterX(0.0f);
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetCenterY(0.0f);
    }

    // Set the scaling factor to three for both the width and height. 
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleX(3.0f);
    }
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleY(3.0f);
    }

    // Add the scale transform to the transform group array.
    pTransforms[1] = pScaleTransform;

    // Create the translate transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Move the visual 150 pixels to the right.
    hr = pTranslateTransform->SetOffsetX(150.0f);
    if (SUCCEEDED(hr)) {
        hr = pTranslateTransform->SetOffsetY(0.0f);
    }

    // Add the translate transform to the transform group array.
    pTransforms[2] = pTranslateTransform;
}
```



### <a name="step-4-create-the-transform-group-object"></a><span data-ttu-id="a92c2-134">Шаг 4. Создание объекта группы преобразования</span><span class="sxs-lookup"><span data-stu-id="a92c2-134">Step 4: Create the transform group object</span></span>

<span data-ttu-id="a92c2-135">Вызовите метод [**идкомпоситиондевице:: креатетрансформграуп**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) , чтобы создать объект группы преобразования.</span><span class="sxs-lookup"><span data-stu-id="a92c2-135">Call the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method to create the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a><span data-ttu-id="a92c2-136">Шаг 5. применение объекта группы преобразования к визуальному элементу</span><span class="sxs-lookup"><span data-stu-id="a92c2-136">Step 5: Apply the transform group object to the visual</span></span>

<span data-ttu-id="a92c2-137">Используйте метод [**идкомпоситионвисуал:: сеттрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) , чтобы связать свойство Transform визуального элемента с объектом группы преобразования.</span><span class="sxs-lookup"><span data-stu-id="a92c2-137">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) method to associate the Transform property of the visual with the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a><span data-ttu-id="a92c2-138">Шаг 6. Фиксация композиции</span><span class="sxs-lookup"><span data-stu-id="a92c2-138">Step 6: Commit the composition</span></span>

<span data-ttu-id="a92c2-139">Вызовите метод [**идкомпоситиондевице:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) , чтобы зафиксировать обновления для визуализации в DirectComposition для обработки.</span><span class="sxs-lookup"><span data-stu-id="a92c2-139">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the updates to the visual to DirectComposition for processing.</span></span> <span data-ttu-id="a92c2-140">Результат применения группы 2D-преобразований появится в целевом окне.</span><span class="sxs-lookup"><span data-stu-id="a92c2-140">The result of applying the group of 2D transforms appears in the target window.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a><span data-ttu-id="a92c2-141">Шаг 7. освобождение объектов DirectComposition</span><span class="sxs-lookup"><span data-stu-id="a92c2-141">Step 7: Free the DirectComposition objects</span></span>

<span data-ttu-id="a92c2-142">Не забудьте освободить группу объектов 2D-преобразования, если они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="a92c2-142">Be sure to free the group of 2D transform objects when you no longer need them.</span></span> <span data-ttu-id="a92c2-143">В следующем примере вызывается определяемый приложением макрос [**саферелеасе**](/windows/desktop/medfound/saferelease) для высвобождения объектов преобразования.</span><span class="sxs-lookup"><span data-stu-id="a92c2-143">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the transform objects.</span></span>


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



<span data-ttu-id="a92c2-144">Также не забудьте освободить объект устройства, целевой объект композиции и визуальные элементы до выхода из приложения.</span><span class="sxs-lookup"><span data-stu-id="a92c2-144">Also remember to free the device object, the composition target object, and the visuals before your application exits.</span></span>

## <a name="complete-example"></a><span data-ttu-id="a92c2-145">Полный пример</span><span class="sxs-lookup"><span data-stu-id="a92c2-145">Complete example</span></span>


```C++
#define BITMAP_WIDTH  80.0
#define BITMAP_HEIGHT 80.0

HRESULT DemoApp::ApplyTransformGroup(IDCompositionDevice *pDevice, 
                                     IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;

    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG; 
    
    IDCompositionTransform *pTransforms[3];

    IDCompositionRotateTransform *pRotateTransform = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;
    IDCompositionTranslateTransform *pTranslateTransform = nullptr;
    IDCompositionTransform *pTransformGroup = nullptr;

    // Create the rotate transform.
    hr = pDevice->CreateRotateTransform(&pRotateTransform);

    if (SUCCEEDED(hr))
    {
        // Set the center of rotation to the center point of the visual.
        hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
        
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
        }

        // Set the rotate angle to 180 degrees.
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetAngle(180.0f);
        }

        // Add the rotate transform to the transform group array.
        pTransforms[0] = pRotateTransform;

        // Create the scale transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateScaleTransform(&pScaleTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the scaling origin to the upper-right corner of the visual.
        hr = pScaleTransform->SetCenterX(0.0f);
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetCenterY(0.0f);
        }

        // Set the scaling factor to three for both the width and height. 
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleX(3.0f);
        }
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleY(3.0f);
        }

        // Add the scale transform to the transform group array.
        pTransforms[1] = pScaleTransform;

        // Create the translate transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Move the visual 150 pixels to the right.
        hr = pTranslateTransform->SetOffsetX(150.0f);
        if (SUCCEEDED(hr)) {
            hr = pTranslateTransform->SetOffsetY(0.0f);
        }

        // Add the translate transform to the transform group array.
        pTransforms[2] = pTranslateTransform;
    }

    if (SUCCEEDED(hr))
    {
        // Create the transform group.
        hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the transform group to the visual.
        hr = pVisual->SetTransform(pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition.
        hr = pDevice->Commit();
    }

    // Release the transform objects.
    for (int i = 0; i < 3; i++)
    {
        SafeRelease(&pTransforms[i]);
    }

    // Release the transform group pointer.
    SafeRelease(&pTransformGroup);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a92c2-146">См. также</span><span class="sxs-lookup"><span data-stu-id="a92c2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a92c2-147">Преобразования</span><span class="sxs-lookup"><span data-stu-id="a92c2-147">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 