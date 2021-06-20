---
title: Как обеспечить правильное отображение приложения на дисплеях с высоким разрешением (DirectWrite)
description: Описывает, как убедиться, что приложение создает окно, которое правильно отображается на дисплеях с высоким разрешением.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71166d312fe666644c683fe2ece7dd3ced59f765
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406427"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a><span data-ttu-id="01115-103">Как обеспечить правильное отображение приложения на дисплеях с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="01115-103">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>

<span data-ttu-id="01115-104">Хотя [DirectWrite](direct-write-portal.md) устраняет множество проблем с высоким разрешением, необходимо выполнить два действия, чтобы убедиться, что приложение работает правильно на дисплеях с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="01115-104">Although [DirectWrite](direct-write-portal.md) addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="01115-105">Шаг 1. Использование DPI системы при создании Windows</span><span class="sxs-lookup"><span data-stu-id="01115-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
    -   [<span data-ttu-id="01115-106">Direct2D</span><span class="sxs-lookup"><span data-stu-id="01115-106">Direct2D</span></span>](#direct2d)
    -   [<span data-ttu-id="01115-107">ИСПОЛЬЗОВАНИЕМ</span><span class="sxs-lookup"><span data-stu-id="01115-107">GDI</span></span>](#gdi)
-   [<span data-ttu-id="01115-108">Шаг 2. объявление того, что в приложении учитывается DPI</span><span class="sxs-lookup"><span data-stu-id="01115-108">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="01115-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="01115-109">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="01115-110">Шаг 1. Использование DPI системы при создании Windows</span><span class="sxs-lookup"><span data-stu-id="01115-110">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="01115-111">Это можно сделать с помощью [Direct2D](../direct2d/direct2d-portal.md) или [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="01115-111">This can be done by using [Direct2D](../direct2d/direct2d-portal.md) or by using [GDI](../gdi/windows-gdi.md).</span></span>

### <a name="direct2d"></a><span data-ttu-id="01115-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="01115-112">Direct2D</span></span>

<span data-ttu-id="01115-113">Интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) предоставляет метод [**ЖЕТДЕСКТОПДПИ**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) для получения dpi системы.</span><span class="sxs-lookup"><span data-stu-id="01115-113">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="01115-114">Он предоставляет горизонтальные и вертикальные размеры дисплея в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="01115-114">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="01115-115">Чтобы использовать эти значения для задания ширины окна, используйте следующую формулу:</span><span class="sxs-lookup"><span data-stu-id="01115-115">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="01115-116">< >  dpi \* по  < горизонтали *Ширина* в пикселях> и <*по умолчанию горизонтальное разрешение*></span><span class="sxs-lookup"><span data-stu-id="01115-116"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="01115-117">... где *горизонтальное разрешение* — это значение, массивах по GetDpi, а *по горизонтали* — 96.</span><span class="sxs-lookup"><span data-stu-id="01115-117">...where *horizontal DPI* is the value retrived by GetDpi and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="01115-118">Формула аналогична для вертикального размера:</span><span class="sxs-lookup"><span data-stu-id="01115-118">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="01115-119"><*вертикальное разрешение* >  \*  < *Высота* в пикселах>/<*по умолчанию для вертикального dpi*></span><span class="sxs-lookup"><span data-stu-id="01115-119"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="01115-120">... где *Vertical dpi* — значение, полученное методом [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) , а *по вертикали* — 96.</span><span class="sxs-lookup"><span data-stu-id="01115-120">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="01115-121">В следующем коде используется метод [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) для создания окна 640 x 480 с масштабированием до уровня dpi системы.</span><span class="sxs-lookup"><span data-stu-id="01115-121">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to create a 640 x 480 window, scaled to the system DPI.</span></span> <span data-ttu-id="01115-122">(В следующем коде *m \_ spD2DFactory* является интеллектуальным указателем на экземпляр [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .)</span><span class="sxs-lookup"><span data-stu-id="01115-122">(In the following code, *m\_spD2DFactory* is a smart pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) instance.)</span></span>


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



### <a name="gdi"></a><span data-ttu-id="01115-123">GDI</span><span class="sxs-lookup"><span data-stu-id="01115-123">GDI</span></span>

<span data-ttu-id="01115-124">[GDI](interoperating-with-gdi.md) предоставляет функцию [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) для получения сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="01115-124">[GDI](interoperating-with-gdi.md) provides the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function for retrieving device information.</span></span> <span data-ttu-id="01115-125">Сведения о DPI можно получить, передав значения индекса *логпикселскс* и *логпикселси* .</span><span class="sxs-lookup"><span data-stu-id="01115-125">You can retrieve DPI information by passing the *LOGPIXELSX* and *LOGPIXELSY* index values.</span></span> <span data-ttu-id="01115-126">Формула для определения горизонтального и вертикального размера окна совпадает с приведенным выше примером [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="01115-126">The formula for determining the horizontal and vertical size of a window is the same as with the [Direct2D](../direct2d/direct2d-portal.md) example above.</span></span>

<span data-ttu-id="01115-127">В следующем коде функция [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) используется для создания окна 640 x 480 с масштабированием до уровня dpi системы.</span><span class="sxs-lookup"><span data-stu-id="01115-127">The following code uses the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function to create a 640 x 480 window, scaled to the system DPI.</span></span>


```C++
FLOAT dpiX, dpiY;

HDC screen = GetDC(0);
dpiX = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSX));
dpiY = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSY));
ReleaseDC(0, screen);

hWnd = CreateWindow(
         TEXT("DirectWriteApp"),
         TEXT("DirectWrite Demo App"),
         WS_OVERLAPPEDWINDOW,
         CW_USEDEFAULT,
         CW_USEDEFAULT,
         static_cast<INT>(dpiX * 640.f / 96.f),
         static_cast<INT>(dpiY * 480.f / 96.f),
         NULL,
         NULL,
         hInstance,
         NULL
         );
```



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="01115-128">Шаг 2. объявление о том, что приложение DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="01115-128">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="01115-129">Когда приложение объявляет себя для использования с учетом DPI, это инструкция, указывающая, что приложение правильно работает с параметрами DPI до 200 DPI.</span><span class="sxs-lookup"><span data-stu-id="01115-129">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="01115-130">В Windows Vista и Windows 7 при включении виртуализации DPI приложения масштабируются, а приложения получают виртуализированные данные из системных API, таких как функция [**жетсистемметрик**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="01115-130">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="01115-131">Чтобы объявить, что приложение учитывает DPI, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="01115-131">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="01115-132">Создайте файл с именем Декларедпиаваре. manifest.</span><span class="sxs-lookup"><span data-stu-id="01115-132">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="01115-133">Скопируйте следующий XML-код в файл и сохраните его:</span><span class="sxs-lookup"><span data-stu-id="01115-133">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="01115-134">В VCPROJ-файле проекта добавьте следующую запись в каждый элемент конфигурации в разделе Висуалстудиопрожект/Configurations:</span><span class="sxs-lookup"><span data-stu-id="01115-134">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="01115-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="01115-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01115-136">Direct2D и высокое разрешение</span><span class="sxs-lookup"><span data-stu-id="01115-136">Direct2D and High-DPI</span></span>](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 