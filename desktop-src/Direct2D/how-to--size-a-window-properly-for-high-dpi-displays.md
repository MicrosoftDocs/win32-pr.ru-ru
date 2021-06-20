---
title: Правильное отображение на дисплее с высоким разрешением
description: Описание действий по созданию окна для приложения, которое правильно отображается на дисплеях с высоким разрешением.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd45b4b654556fc251575410cc11f9b66961263
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406157"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="b9cd3-103">Правильное отображение на дисплее с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="b9cd3-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="b9cd3-104">Хотя Direct2D устраняет множество проблем с высоким разрешением, необходимо выполнить два действия, чтобы убедиться, что приложение работает правильно на дисплеях с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="b9cd3-105">Шаг 1. Использование DPI системы при создании Windows</span><span class="sxs-lookup"><span data-stu-id="b9cd3-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="b9cd3-106">Шаг 2. объявление того, что в приложении учитывается DPI</span><span class="sxs-lookup"><span data-stu-id="b9cd3-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="b9cd3-107">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b9cd3-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="b9cd3-108">Шаг 1. Использование DPI системы при создании Windows</span><span class="sxs-lookup"><span data-stu-id="b9cd3-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="b9cd3-109">Интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) предоставляет метод [**ЖЕТДЕСКТОПДПИ**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) для получения dpi системы.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="b9cd3-110">Он предоставляет горизонтальные и вертикальные размеры дисплея в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="b9cd3-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="b9cd3-111">Чтобы использовать эти значения для задания ширины окна, используйте следующую формулу:</span><span class="sxs-lookup"><span data-stu-id="b9cd3-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="b9cd3-112">< >  dpi \* по  < горизонтали *Ширина* в пикселях> и <*по умолчанию горизонтальное разрешение*></span><span class="sxs-lookup"><span data-stu-id="b9cd3-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="b9cd3-113">... где *горизонтальное разрешение* — это значение, массивах по [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) , а *по горизонтали* — 96.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="b9cd3-114">Формула аналогична для вертикального размера:</span><span class="sxs-lookup"><span data-stu-id="b9cd3-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="b9cd3-115"><*вертикальное разрешение* >  \*  < *Высота* в пикселах>/<*по умолчанию для вертикального dpi*></span><span class="sxs-lookup"><span data-stu-id="b9cd3-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="b9cd3-116">... где *Vertical dpi* — значение, полученное методом [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) , а *по вертикали* — 96.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="b9cd3-117">В следующем коде метод [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) используется для получения DPI на уровне системы, а затем создается окно 640 × 480 с масштабированием до уровня dpi системы.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


```C++
        // Because the CreateWindow function takes its size in pixels,
        // obtain the system DPI and use it to scale the window size.
        FLOAT dpiX, dpiY;

        // The factory returns the current system DPI. This is also the value it will use
        // to create its own windows.
        m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


        // Create the window.
        m_hwnd = CreateWindow(
            L"D2DDemoApp",
            L"Direct2D Demo App",
            WS_OVERLAPPEDWINDOW,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
            static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );
```



> [!Note]
>
> <span data-ttu-id="b9cd3-118">Начиная с Windows 8, для получения DPI на уровне системы можно использовать класс [**Windows:: Graphics::D Play::D исплайпропертиес**](/uwp/api/Windows.Graphics.Display.DisplayProperties) .</span><span class="sxs-lookup"><span data-stu-id="b9cd3-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="b9cd3-119">Шаг 2. объявление о том, что приложение DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="b9cd3-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="b9cd3-120">Когда приложение объявляет себя для использования с учетом DPI, это инструкция, указывающая, что приложение правильно работает с параметрами DPI до 200 DPI.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="b9cd3-121">В Windows Vista и Windows 7 при включении виртуализации DPI приложения масштабируются, а приложения получают виртуализированные данные из системных API, таких как функция [**жетсистемметрик**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="b9cd3-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="b9cd3-122">Чтобы объявить, что приложение учитывает DPI, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="b9cd3-123">Создайте файл с именем Декларедпиаваре. manifest.</span><span class="sxs-lookup"><span data-stu-id="b9cd3-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="b9cd3-124">Скопируйте следующий XML-код в файл и сохраните его:</span><span class="sxs-lookup"><span data-stu-id="b9cd3-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="b9cd3-125">В VCPROJ-файле проекта добавьте следующую запись в каждый элемент конфигурации в разделе Висуалстудиопрожект/Configurations:</span><span class="sxs-lookup"><span data-stu-id="b9cd3-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b9cd3-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b9cd3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9cd3-127">Direct2D и высокое разрешение</span><span class="sxs-lookup"><span data-stu-id="b9cd3-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 