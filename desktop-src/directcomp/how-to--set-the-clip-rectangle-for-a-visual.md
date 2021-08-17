---
title: Обрезка с помощью объекта прямоугольной обрезки
description: В этом разделе показано, как использовать объект прямоугольной картинки для обрезки визуального или визуального дерева.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10386f3e99dead7fff04a57463c2ee753bd1d712e9a59e6b928136c32f25ae75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119106"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Обрезка с помощью объекта прямоугольной обрезки

> [!NOTE]
> для приложений на Windows 10 рекомендуется использовать интерфейсы api Windows. UI. компоновки вместо DirectComposition. Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).

В этом разделе показано, как использовать объект прямоугольной картинки для обрезки визуального или визуального дерева.

Пример в этом разделе определяет прямоугольный клип, центрированный по положению мыши, и применяет этот клип к визуальному элементу, расположенному в клиентской области окна цели композиции. На этом снимке экрана показан результат применения объекта прямоугольной картинки к визуальному элементу.

![результат применения объекта прямоугольной картинки к визуальному элементу](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [DirectComposition](directcomposition-portal.md)
-   [Графика Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [Графическая инфраструктура DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Обязательные условия

-   C/C++
-   Microsoft Win32
-   Модель COM

## <a name="instructions"></a>Инструкции

### <a name="step-1-initialize-directcomposition-objects"></a>Шаг 1. Инициализация объектов DirectComposition

1.  Создайте объект устройства и целевой объект композиции.
2.  Создайте визуальный элемент, задайте его содержимое и добавьте его в визуальное дерево.

Дополнительные сведения см. [в разделе как инициализировать DirectComposition](initialize-directcomposition.md).

### <a name="step-2-create-the-rectangle-clip-object"></a>Шаг 2. Создание объекта прямоугольной обрезки

Используйте метод [**идкомпоситиондевице:: креатеректанглеклип**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) , чтобы создать экземпляр объекта прямоугольной картинки.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Шаг 3. Задание свойств объекта «прямоугольный ролик»

Вызовите методы интерфейса [**идкомпоситионректанглеклип**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) объекта прямоугольной коллекции, чтобы задать свойства прямоугольника обрезки.

В следующем примере определяется прямоугольник клипа, центрированный вокруг текущего положения указателя мыши. `m_offsetX` `m_offsetY` Переменные члена и содержат значения свойств Оффсеткс и offset визуального элемента.


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



Обратите внимание, что интерфейс [**идкомпоситионректанглеклип**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) включает следующие методы для определения прямоугольника обрезки с закругленными углами:

-   [**сеттоплефтрадиускс**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**сеттоплефтрадиуси**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**сеттопригхтрадиускс**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**сеттопригхтрадиуси**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Шаг 4. Задание свойства Clip визуального элемента

Используйте метод [**идкомпоситионвисуал:: сетклип**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) , чтобы связать свойство Clip визуального элемента с объектом прямоугольной картинки.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Шаг 5. Фиксация композиции

Вызовите метод [**идкомпоситиондевице:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) , чтобы зафиксировать пакет команд в Microsoft DirectComposition для обработки. Результат применения прямоугольника обрезки появится в целевом окне.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Шаг 6. освобождение объектов DirectComposition

Не забудьте освободить прямоугольный объект Rectangle, если он больше не нужен, а также объект устройства, целевой объект композиции и все визуальные объекты. В следующем примере вызывается определяемый приложением макрос [**саферелеасе**](/windows/desktop/medfound/saferelease) для высвобождения объектов DirectComposition.


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Усечение](clipping.md)
</dt> </dl>

 

 