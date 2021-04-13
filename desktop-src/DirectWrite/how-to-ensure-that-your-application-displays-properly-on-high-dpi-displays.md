---
title: Как обеспечить правильное отображение приложения на дисплеях с высоким разрешением (DirectWrite)
description: Описывает создание окна, которое правильно отображается на дисплеях с высоким разрешением.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317eb3379963cec600ab9bac7deb3778f0874e59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338252"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>Как обеспечить правильное отображение приложения на дисплеях с высоким разрешением

Хотя [DirectWrite](direct-write-portal.md) устраняет множество проблем с высоким разрешением, необходимо выполнить два действия, чтобы убедиться, что приложение работает правильно на дисплеях с высоким разрешением.

-   [Шаг 1. Использование DPI системы при создании Windows](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [ИСПОЛЬЗОВАНИЕМ](#gdi)
-   [Шаг 2. объявление того, что в приложении учитывается DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [См. также](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Шаг 1. Использование DPI системы при создании Windows

Это можно сделать с помощью [Direct2D](../direct2d/direct2d-portal.md) или [GDI](../gdi/windows-gdi.md).

### <a name="direct2d"></a>Direct2D

Интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) предоставляет метод [**ЖЕТДЕСКТОПДПИ**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) для получения dpi системы. Он предоставляет горизонтальные и вертикальные размеры дисплея в точках на дюйм (DPI). Чтобы использовать эти значения для задания ширины окна, используйте следующую формулу:

< >  dpi \* по  < горизонтали *Ширина* в пикселях> и <*по умолчанию горизонтальное разрешение*>

... где *горизонтальное разрешение* — это значение, массивах по GetDpi, а *по горизонтали* — 96. Формула аналогична для вертикального размера:

<*вертикальное разрешение* >  \*  < *Высота* в пикселах>/<*по умолчанию для вертикального dpi*>

... где *Vertical dpi* — значение, полученное методом [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) , а *по вертикали* — 96.

В следующем коде используется метод [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) для создания окна 640 x 480 с масштабированием до уровня dpi системы. (В следующем коде *m \_ spD2DFactory* является интеллектуальным указателем на экземпляр [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .)


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



### <a name="gdi"></a>GDI

[GDI](interoperating-with-gdi.md) предоставляет функцию [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) для получения сведений об устройстве. Сведения о DPI можно получить, передав значения индекса *логпикселскс* и *логпикселси* . Формула для определения горизонтального и вертикального размера окна совпадает с приведенным выше примером [Direct2D](../direct2d/direct2d-portal.md) .

В следующем коде функция [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) используется для создания окна 640 x 480 с масштабированием до уровня dpi системы.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Шаг 2. объявление о том, что приложение DPI-Aware

Когда приложение объявляет себя для использования с учетом DPI, это инструкция, указывающая, что приложение правильно работает с параметрами DPI до 200 DPI. В Windows Vista и Windows 7 при включении виртуализации DPI приложения масштабируются, а приложения получают виртуализированные данные из системных API, таких как функция [**жетсистемметрик**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) . Чтобы объявить, что приложение учитывает DPI, выполните следующие действия.

1.  Создайте файл с именем Декларедпиаваре. manifest.
2.  Скопируйте следующий XML-код в файл и сохраните его:
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  В VCPROJ-файле проекта добавьте следующую запись в каждый элемент конфигурации в разделе Висуалстудиопрожект/Configurations:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Direct2D и высокое разрешение](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 