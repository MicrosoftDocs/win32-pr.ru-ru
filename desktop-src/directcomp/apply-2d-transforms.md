---
title: Как применять двумерные преобразования
description: В этом разделе показано, как применять двумерные преобразования к визуальному элементу с помощью Microsoft DirectComposition.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- как применять DirectComposition 2D-преобразования
- DirectComposition 2D-преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef965ce98bb064eb63b34de569160c9b68932c96ce757e3e5d13450f73098b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281963"
---
# <a name="how-to-apply-2d-transforms"></a>Как применять двумерные преобразования

> [!NOTE]
> для приложений на Windows 10 рекомендуется использовать интерфейсы api Windows. UI. компоновки вместо DirectComposition. Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).

В этом разделе показано, как применять двумерные преобразования к визуальному элементу с помощью Microsoft DirectComposition. В примере в этом разделе применяется группа преобразований, которые:

1.  Поворот визуального элемента на 180 градусов.
2.  Увеличение масштаба визуального элемента до трех его исходных размеров.
3.  Сдвиг (перемещение) визуальных элементов 150 пикселей справа от его исходной точки.

На следующем снимке экрана показан визуальный элемент до и после применения 2D-преобразований.

![результат применения группы 2D-преобразований к визуальному элементу](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [DirectComposition](directcomposition-portal.md)
-   [Графика Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [Графическая инфраструктура DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Microsoft Win32
-   Модель COM

## <a name="instructions"></a>Instructions

### <a name="step-1-initialize-directcomposition-objects"></a>Шаг 1. Инициализация объектов DirectComposition

1.  Создайте объект устройства и целевой объект композиции.
2.  Создайте визуальный элемент, задайте его содержимое и добавьте его в визуальное дерево.

Дополнительные сведения см. [в разделе как инициализировать DirectComposition](initialize-directcomposition.md).

### <a name="step-2-create-the-transform-group-array"></a>Шаг 2. Создание массива группы преобразований


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a>Шаг 3. Создание объектов преобразования, установка их свойств и добавление их в массив группы преобразования

1.  Используйте методы [**идкомпоситиондевице:: креатеротатетрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: креатескалетрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)и [**:: креатетранслатетрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) для создания объектов Transform.
2.  Используйте функции элементов интерфейсов [**идкомпоситионротатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**идкомпоситионскалетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)и [**идкомпоситионтранслатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) , чтобы задать свойства преобразований.
3.  Скопируйте указатели интерфейса преобразования в массив группы преобразования.


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



### <a name="step-4-create-the-transform-group-object"></a>Шаг 4. Создание объекта группы преобразования

Вызовите метод [**идкомпоситиондевице:: креатетрансформграуп**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) , чтобы создать объект группы преобразования.


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a>Шаг 5. применение объекта группы преобразования к визуальному элементу

Используйте метод [**идкомпоситионвисуал:: сеттрансформ**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) , чтобы связать свойство Transform визуального элемента с объектом группы преобразования.


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a>Шаг 6. Фиксация композиции

Вызовите метод [**идкомпоситиондевице:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) , чтобы зафиксировать обновления для визуализации в DirectComposition для обработки. Результат применения группы 2D-преобразований появится в целевом окне.


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a>Шаг 7. освобождение объектов DirectComposition

Не забудьте освободить группу объектов 2D-преобразования, если они больше не нужны. В следующем примере вызывается определяемый приложением макрос [**саферелеасе**](/windows/desktop/medfound/saferelease) для высвобождения объектов преобразования.


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



Также не забудьте освободить объект устройства, целевой объект композиции и визуальные элементы до выхода из приложения.

## <a name="complete-example"></a>Полный пример


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразования](transforms.md)
</dt> </dl>

 

 