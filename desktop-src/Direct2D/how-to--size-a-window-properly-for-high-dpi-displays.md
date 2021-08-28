---
title: Правильное отображение на дисплее с высоким разрешением
description: Описание действий по созданию окна для приложения, которое правильно отображается на дисплеях с высоким разрешением.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8ebc6a7621623307d9b2cfd953a5fa3f3387fbacb3faeb345375d925044cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259964"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a>Правильное отображение на дисплее с высоким разрешением

Хотя Direct2D устраняет множество проблем с высоким разрешением, необходимо выполнить два действия, чтобы убедиться, что приложение работает правильно на дисплеях с высоким разрешением.

-   [Шаг 1. Использование DPI системы при создании Windows](#step-1-use-the-system-dpi-when-creating-windows)
-   [Шаг 2. объявление того, что в приложении учитывается DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Связанные темы](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Шаг 1. Использование DPI системы при создании Windows

Интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) предоставляет метод [**ЖЕТДЕСКТОПДПИ**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) для получения dpi системы. Он предоставляет горизонтальные и вертикальные размеры дисплея в точках на дюйм (DPI). Чтобы использовать эти значения для задания ширины окна, используйте следующую формулу:

< >  dpi \* по  < горизонтали *Ширина* в пикселях> и <*по умолчанию горизонтальное разрешение*>

... где *горизонтальное разрешение* — это значение, массивах по [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) , а *по горизонтали* — 96. Формула аналогична для вертикального размера:

<*вертикальное разрешение* >  \*  < *Высота* в пикселах>/<*по умолчанию для вертикального dpi*>

... где *Vertical dpi* — значение, полученное методом [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) , а *по вертикали* — 96.

В следующем коде метод [**жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) используется для получения DPI на уровне системы, а затем создается окно 640 × 480 с масштабированием до уровня dpi системы.


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
> начиная с Windows 8, для получения DPI на уровне системы можно использовать класс [**Windows:: Graphics::D воспроизведения::D исплайпропертиес**](/uwp/api/Windows.Graphics.Display.DisplayProperties) .

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Шаг 2. объявление о том, что приложение DPI-Aware

Когда приложение объявляет себя для использования с учетом DPI, это инструкция, указывающая, что приложение правильно работает с параметрами DPI до 200 DPI. в Windows Vista и Windows 7 при включении виртуализации dpi приложения масштабируются, а приложения получают виртуализированные данные из системных api, таких как функция [**жетсистемметрик**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Чтобы объявить, что приложение учитывает DPI, выполните следующие действия.

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

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Direct2D и высокое разрешение](direct2d-and-high-dpi.md)
</dt> </dl>

 

 