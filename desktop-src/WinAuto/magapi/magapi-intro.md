---
title: Общие сведения об API увеличения
description: В этом разделе описывается API для увеличения масштаба и объясняется его использование в приложении.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Увеличения
- приложения для увеличения масштаба экрана
- Увеличения
- обработка пользовательских изображений
- Magnification.dll
- Создание элементов управления "Экранная лупа"
- Выборочное увеличение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719134"
---
# <a name="magnification-api-overview"></a>Общие сведения об API увеличения

API увеличения позволяет разработчикам вспомогательных технологий разрабатывать приложения для увеличения масштаба экрана, работающие в Microsoft Windows. В этом разделе описывается API для увеличения масштаба и объясняется его использование в приложении. Он содержит следующие подразделы:

- [Начало работы](#getting-started)
- [Основные понятия](#basic-concepts)
  - [Типы экранных Лупы](#types-of-magnifiers)
  - [Коэффициент увеличения](#magnification-factor)
  - [Цветовые эффекты](#color-effects)
  - [Исходный прямоугольник](#source-rectangle)
  - [Список фильтров](#filter-list)
  - [Преобразование входных данных](#input-transform)
  - [Системный курсор](#system-cursor)
- [Инициализация библиотеки времени выполнения с помощью экранной лупы](#initializing-the-magnifier-run-time-library)
- [Использование экранной лупы Full-Screen](#using-the-full-screen-magnifier)
- [Использование элемента управления "Экранная лупа"](#using-the-magnifier-control)
  - [Создание элемента управления "Экранная лупа"](#creating-the-magnifier-control)
  - [Инициализация элемента управления](#initializing-the-control)
  - [Установка исходного прямоугольника](#setting-the-source-rectangle)
  - [Применение цветовых эффектов](#applying-color-effects)
  - [Выборочное увеличение](#selective-magnification)
- [См. также](#related-topics)

## <a name="getting-started"></a>Приступая к работе

Первоначальный выпуск API лупы поддерживается в Windows Vista и более поздних операционных системах. В Windows 8 и более поздних версиях API-интерфейс поддерживает дополнительные функции, включая увеличение масштаба экрана и настройку видимости увеличенного системного курсора.

Поддержка API увеличения предоставляется Magnification.dll. Чтобы скомпилировать приложение, включите увеличение. h и ссылку на увеличение. lib.

> [!Note]  
> API увеличения не поддерживается в WOW64; то есть 32-разрядное приложение с экранной лупой не будет правильно работать в 64-разрядной версии Windows.

## <a name="basic-concepts"></a>Основные понятия

В этом разделе описаны фундаментальные понятия, на которых основан API увеличения. Он содержит следующие компоненты:

- [Типы экранных Лупы](#types-of-magnifiers)
- [Коэффициент увеличения](#magnification-factor)
- [Цветовые эффекты](#color-effects)
- [Исходный прямоугольник](#source-rectangle)
- [Список фильтров](#filter-list)
- [Преобразование входных данных](#input-transform)
- [Системный курсор](#system-cursor)

### <a name="types-of-magnifiers"></a>Типы экранных Лупы

API поддерживает два типа экранной лупы: *полноэкранный* экран и *элемент управления "Экранная лупа*". Полноэкранная экранная лупа увеличивает содержимое всего экрана, а элемент управления "Экранная лупа" увеличивает содержимое определенной области экрана и отображает содержимое в окне. В обеих экранах отображаются изображения и текст, и они позволяют управлять объемом увеличения. К увеличенному экрану можно также применить цветовые эффекты, что облегчит их отображение для людей, имеющих цвет недостатки или требующих большего или меньшего контраста.

> [!Important]  
> API элемента управления "Экранная лупа" доступен в Windows Vista и более поздних операционных системах, а полноэкранный API экранной лупы доступен только в операционных системах Windows 8 и более поздних версий.

### <a name="magnification-factor"></a>Коэффициент увеличения

И экранная лупа, и элемент управления "Экранная лупа" применяют преобразование масштабирования для увеличения содержимого экрана. Величина увеличения, применяемая преобразованием «масштаб», называется *коэффициентом увеличения*. Он выражается в виде значения с плавающей запятой, где 1,0 соответствует без увеличения, а большие значения приводят к увеличению соответствующего объема. Например, значение 1,5 делает содержимое экрана 50 процентов больше. Коэффициент увеличения меньше 1,0 недопустим.

### <a name="color-effects"></a>Цветовые эффекты

Цветовые эффекты достигаются путем применения матрицы преобразования «5 в 5 цветов» к цветам увеличенного содержимого экрана. Матрица определяет интенситиесие красного, синего, зеленого и альфа-компонентов содержимого. Дополнительные сведения см. в разделе [Использование матрицы цветов для преобразования одного цвета](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) в документации по Windows GDI+.

### <a name="source-rectangle"></a>Исходный прямоугольник

Полноэкранная экранная лупа применяет преобразование «масштабирование» и «цвет» ко всему экрану. С другой стороны, элемент управления "Экранная лупа" копирует область экрана, называемую *исходным прямоугольником*, в растровое изображение вне экрана. Затем элемент управления применяет преобразование «масштаб» и преобразование «цвет» (при наличии) к растровому растру, расположенному на экране. Наконец, элемент управления отображает масштабированное и цветное растровое изображение в окне элемента управления "Экранная лупа".

### <a name="filter-list"></a>Список фильтров

По умолчанию элемент управления "Экранная лупа" увеличивает все окна в указанном прямоугольнике источника. Однако, предоставляя *список фильтров* дескрипторов окон, можно управлять тем, какие окна включены в увеличенное содержимое, а какие — нет. Дополнительные сведения см. в разделе [выборочное увеличение](#selective-magnification).

Полноэкранная экранная лупа не поддерживает список фильтров; Он всегда увеличивает все окна на экране.

### <a name="input-transform"></a>Преобразование входных данных

Как правило, увеличенное содержимое экрана — «невидимый» для пользовательского пера или сенсорного ввода. Например, если пользователь касается увеличенного изображения элемента управления, система не обязательно передает входные данные в элемент управления. Вместо этого система передает входные данные какому-либо элементу (если таковой имеется), расположенному на экранах с нажатием экрана, на неувеличенном рабочем столе. Функция [**магсетинпуттрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) позволяет указать *Преобразование ввода* , которое сопоставляет пространство координат увеличенного экрана с фактическим (неувеличенным) координатным пространством экрана. Это позволяет системе передавать перо или сенсорный ввод, введенный в увеличенном содержимом экрана, в нужный элемент пользовательского интерфейса на экране.

> [!Note]  
> Вызывающий процесс должен иметь привилегии UIAccess, чтобы задать входное преобразование. Дополнительные сведения см. в разделе [вопросы безопасности модели автоматизации пользовательского интерфейса](../uiauto-securityoverview.md) и [/MANIFESTUAC (Встраивание данных контроля учетных записей в манифест)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).

### <a name="system-cursor"></a>Системный курсор

Функция [**магшовсистемкурсор**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) позволяет отображать или скрывать системный курсор. При отображении системного курсора при активной экранной лупы, системный курсор всегда будет увеличиваться вместе с остальным содержимым экрана. Если вы скрываете системный курсор при активной экранной лупы, системный курсор не отображается вообще.

С помощью элемента управления "Экранная лупа" функция [**магшовсистемкурсор**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) показывает или скрывает неувеличенный системный курсор, но не влияет на увеличенный системный курсор. Видимость увеличенного системного курсора зависит от того, имеет ли элемент управления "Экранная лупа" стиль [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) . При наличии этого стиля элемент управления "Экранная лупа" отображает увеличенный системный курсор вместе с увеличенным содержимым экрана, когда системный курсор попадает в исходный прямоугольник.

## <a name="initializing-the-magnifier-run-time-library"></a>Инициализация библиотеки времени выполнения с помощью экранной лупы

Перед вызовом любых других функций API экранной лупы необходимо создать и инициализировать объекты времени выполнения экранной лупы, вызвав функцию [**магинитиализе**](/windows/win32/api/Magnification/nf-magnification-maginitialize) . Аналогичным образом после завершения использования API экранной лупы вызовите функцию [**магунинитиализе**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) , чтобы уничтожить объекты времени выполнения экранной лупы и освободить связанные системные ресурсы.

## <a name="using-the-full-screen-magnifier"></a>Использование экранной лупы Full-Screen

Чтобы использовать полноэкранную экранную лупу, вызовите функцию [**магсетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) . Параметр *маглевел* задает коэффициент увеличения. Параметры *ксоффсет* и *йоффсет* определяют, как увеличенное содержимое экрана располагается относительно экрана.

При увеличении содержимого экрана оно становится больше, чем само окно. Часть содержимого выходит за края экрана и невидима для пользователя. Параметры *ксоффсет* и *йоффсет* функции [**магсетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) определяют, какая часть увеличения содержимого экрана отображается на экране. Вместе параметры задают координаты точки в неувеличенном содержимом экрана. Когда содержимое будет увеличено, оно позиционируется с указанной точкой в верхнем левом углу экрана.

В следующем примере устанавливается коэффициент увеличения для полноэкранной экранной лупы, и центр увеличенного содержимого экрана помещается в центре экрана.

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

Используйте функцию [**магсетфуллскринколореффект**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) , чтобы применить цветовые эффекты к полноэкранному содержимому, задав матрицу преобразования цвета, определяемую приложением. Например, в следующем примере задается матрица преобразования цвета, которая преобразует цвета в градации серого.

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

Вы можете получить текущий коэффициент увеличения и значения смещения, вызвав функцию [**магжетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) . Вы можете получить матрицу текущего преобразования цвета, вызвав функцию [**магжетфуллскринколореффект**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .

## <a name="using-the-magnifier-control"></a>Использование элемента управления "Экранная лупа"

Элемент управления "Экранная лупа" увеличивает содержимое определенной области экрана и отображает содержимое в окне. В этом разделе описывается использование элемента управления "Экранная лупа". Он содержит следующие компоненты:

- [Создание элемента управления "Экранная лупа"](#creating-the-magnifier-control)
- [Инициализация элемента управления](#initializing-the-control)
- [Установка исходного прямоугольника](#setting-the-source-rectangle)
- [Применение цветовых эффектов](#applying-color-effects)
- [Выборочное увеличение](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>Создание элемента управления "Экранная лупа"

Элемент управления "Экранная лупа" должен размещаться в окне, созданном с помощью расширенного стиля [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) . После создания главного окна вызовите [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) , чтобы задать непрозрачность главного окна. Основное окно обычно имеет значение Полная прозрачность, чтобы предотвратить отображение базового содержимого экрана. В следующем примере показано, как задать полную непрозрачность для окна главного приложения.

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

Если применить стиль [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) к главному окну, щелчки мыши передаются в любой объект, находящийся за ведущим окном в расположении курсора мыши. Имейте в виду, что, поскольку главное окно не обрабатывает щелчки мыши, пользователь не сможет переместить или изменить размер окна лупы с помощью мыши.

Класс Window окна элемента управления "Экранная лупа" должен быть **WC_MAGNIFIER**. При применении стиля [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) элемент управления "Экранная лупа" включает системный курсор в увеличенном содержимом экрана, и этот курсор увеличен вместе с содержимым экрана.

После создания элемента управления "Экранная лупа" следует держать маркер окна, чтобы его можно было передать другим функциям.

В следующем примере показано, как создать элемент управления "Экранная лупа".

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a>Инициализация элемента управления

После создания элемента управления "Экранная лупа" необходимо вызвать функцию [**магсетвиндовтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) , чтобы указать коэффициент увеличения. Это просто вопрос указания матрицы

(*n*, 0,0, 0,0)

(0,0, *n*, 0,0)

(0,0, 0,0, 1,0)

где *n* — коэффициент увеличения.

В следующем примере показано, как задать коэффициент увеличения для элемента управления "Экранная лупа".

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a>Установка исходного прямоугольника

По мере того, как пользователь перемещает курсор мыши на экран, приложение вызывает функцию [**магсетвиндовсаурце**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) , чтобы указать часть базового экрана, которая будет увеличена.

В приведенном ниже примере функции вычисляется расположение и размеры исходного прямоугольника (на основе расположения мыши и размеров окна экранной лупы, деленного на коэффициент увеличения) и настраивает исходный прямоугольник соответствующим образом. Функция также выравнивает клиентскую область окна главного приложения в позиции мыши. Эта функция будет вызываться с интервалами для обновления окна лупы.

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a>Применение цветовых эффектов

Элемент управления "Экранная лупа", имеющий стиль [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) , применяет встроенную матрицу преобразования цвета, которая инвертирует цвета увеличенного содержимого экрана. На следующем рисунке показано содержимое экрана в элементе управления "Экранная лупа" с **MS_INVERTCOLORS** стилем.

![снимок экрана с увеличенным содержимым с инвертированными цветами](images/color-inversion.png)

Функция [**магсетколореффект**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) позволяет применять другие цветовые эффекты, устанавливая матрицу преобразования цветов, определяемую приложением. Например, следующая функция задает матрицу преобразования цвета, которая преобразует цвета в градации серого.


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

Дополнительные сведения о работе преобразований цветов см. в разделе [Использование матрицы цветов для преобразования одного цвета](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) в документации GDI+.

### <a name="selective-magnification"></a>Выборочное увеличение

По умолчанию увеличение применяется ко всем окнам, Кроме окна лупы. Чтобы указать, какие окна должны быть увеличены, вызовите функцию [**магсетвиндовфилтерлист**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) . Этот метод принимает либо список окон для увеличения, либо список окон, которые необходимо исключить из увеличения.

## <a name="related-topics"></a>См. также

[API увеличения](entry-magapi-sdk.md)