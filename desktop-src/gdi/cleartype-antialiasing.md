---
description: Сглаживание Microsoft ClearType — это метод сглаживания, улучшающий разрешение экрана с помощью традиционных сглаживания.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Сглаживание ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985048"
---
# <a name="cleartype-antialiasing"></a><span data-ttu-id="326cd-103">Сглаживание ClearType</span><span class="sxs-lookup"><span data-stu-id="326cd-103">ClearType Antialiasing</span></span>

<span data-ttu-id="326cd-104">Сглаживание Microsoft ClearType — это метод сглаживания, улучшающий разрешение экрана с помощью традиционных сглаживания.</span><span class="sxs-lookup"><span data-stu-id="326cd-104">Microsoft ClearType antialiasing is a smoothing method that improves font display resolution over traditional antialiasing.</span></span> <span data-ttu-id="326cd-105">Это значительно повышает удобочитаемость на цветных ЖК-мониторах с помощью цифрового интерфейса, такого как ноутбуки и высококачественные дисплеи с плоским настольным ПК.</span><span class="sxs-lookup"><span data-stu-id="326cd-105">It dramatically improves readability on color LCD monitors with a digital interface, such as those in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="326cd-106">Удобочитаемость на экранах CRT также немного улучшена.</span><span class="sxs-lookup"><span data-stu-id="326cd-106">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="326cd-107">Однако технология ClearType зависит от ориентации и порядка полос LCD.</span><span class="sxs-lookup"><span data-stu-id="326cd-107">However, ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="326cd-108">В настоящее время технология ClearType реализована только для LCDs с вертикальными полосами, которые упорядочиваются по RGB.</span><span class="sxs-lookup"><span data-stu-id="326cd-108">Currently, ClearType is implemented only for LCDs with vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="326cd-109">В частности, это влияет на Планшетные ПК, где дисплей может быть ориентирован в любом направлении, а также на экраны, которые можно включить в книжную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="326cd-109">In particular, this affects tablet PCs, where the display can be oriented in any direction, and those screens that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="326cd-110">Допускается сглаживание ClearType:</span><span class="sxs-lookup"><span data-stu-id="326cd-110">ClearType antialiasing is allowed:</span></span>

-   <span data-ttu-id="326cd-111">Для 16-, 24-и 32-разрядного цвета (отключено для 256 цветов или меньше)</span><span class="sxs-lookup"><span data-stu-id="326cd-111">For 16-, 24-, and 32-bit color (disabled for 256 colors or less)</span></span>
-   <span data-ttu-id="326cd-112">Для экрана DC и DC памяти (не для контроллера домена)</span><span class="sxs-lookup"><span data-stu-id="326cd-112">For screen DC and memory DC (not for printer DC)</span></span>
-   <span data-ttu-id="326cd-113">Для шрифтов TrueType и шрифтов OpenType с контурами TrueType</span><span class="sxs-lookup"><span data-stu-id="326cd-113">For TrueType fonts and OpenType fonts with TrueType outlines</span></span>

<span data-ttu-id="326cd-114">Сглаживание ClearType отключено:</span><span class="sxs-lookup"><span data-stu-id="326cd-114">ClearType antialiasing is disabled:</span></span>

-   <span data-ttu-id="326cd-115">В разделе клиент сервера терминалов</span><span class="sxs-lookup"><span data-stu-id="326cd-115">Under terminal server client</span></span>
-   <span data-ttu-id="326cd-116">Для точечных шрифтов, векторных шрифтов, шрифтов устройства, типа 1 шрифтов или шрифтов OpenType PostScript без контуров TrueType</span><span class="sxs-lookup"><span data-stu-id="326cd-116">For bitmap fonts, vector fonts, device fonts, Type 1 fonts, or Postscript OpenType fonts without TrueType outlines</span></span>
-   <span data-ttu-id="326cd-117">Если шрифт настраивает внедренные точечные рисунки, только для тех размеров шрифтов, которые содержат внедренные точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="326cd-117">If the font has tuned embedded bitmaps, only for those font sizes that contain the embedded bitmaps</span></span>

<span data-ttu-id="326cd-118">Чтобы активировать сглаживание ClearType, вызовите [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) один раз, чтобы включить смягчение шрифтов, а затем еще раз, чтобы установить тип сглаживания Fe \_ фонтсмусингклеартипе, как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="326cd-118">To activate ClearType antialiasing, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) once to turn on font smoothing and then a second time to set the smoothing type to FE\_FONTSMOOTHINGCLEARTYPE, as shown in the following code sample:</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="326cd-119">Можно настроить внешний вид текста, изменив значение контрастности, используемое в алгоритме ClearType.</span><span class="sxs-lookup"><span data-stu-id="326cd-119">You can adjust the appearance of text by changing the contrast value used in the ClearType algorithm.</span></span> <span data-ttu-id="326cd-120">Значение по умолчанию — 1 400, но оно может быть любым значением от 1 000 до 2 200.</span><span class="sxs-lookup"><span data-stu-id="326cd-120">The default is 1,400, but it can be any value from 1,000 to 2,200.</span></span> <span data-ttu-id="326cd-121">В зависимости от устройства дисплея и от чувствительности пользователя к цвету, более высокое или низкое значение контрастности может повысить удобочитаемость.</span><span class="sxs-lookup"><span data-stu-id="326cd-121">Depending on the display device and the user's sensitivity to colors, a higher or lower contrast value may improve readability.</span></span> <span data-ttu-id="326cd-122">Чтобы изменить контрастность, вызовите [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) с SPI \_ сетфонтсмусингконтраст.</span><span class="sxs-lookup"><span data-stu-id="326cd-122">To change the contrast, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETFONTSMOOTHINGCONTRAST.</span></span> <span data-ttu-id="326cd-123">Следующий код задает значение контраста равным 1 600.</span><span class="sxs-lookup"><span data-stu-id="326cd-123">The following code sets the contrast value to 1,600.</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="326cd-124">Для обеспечения совместимости приложений следует учитывать следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="326cd-124">You should consider the following details for application compatibility:</span></span>

-   <span data-ttu-id="326cd-125">Отрисовка текста с помощью технологии ClearType немного медленнее, чем при стандартном сглаживание.</span><span class="sxs-lookup"><span data-stu-id="326cd-125">Text rendering with ClearType is slightly slower than with standard antialiasing.</span></span>
-   <span data-ttu-id="326cd-126">Приложения не должны использовать XOR для показа выбранного текста.</span><span class="sxs-lookup"><span data-stu-id="326cd-126">Applications should not use XOR to display selected text.</span></span> <span data-ttu-id="326cd-127">Приложения должны задать цвет фона и повторно отобразить выделенный текст.</span><span class="sxs-lookup"><span data-stu-id="326cd-127">Applications should set the background color and redisplay the selected text.</span></span>
-   <span data-ttu-id="326cd-128">Приложения не должны закрашивать один и тот же текст поверх самого себя в прозрачном режиме.</span><span class="sxs-lookup"><span data-stu-id="326cd-128">Applications should not paint the same text on top of itself in transparent mode.</span></span> <span data-ttu-id="326cd-129">Если это происходит, то граничные Пиксели с сглаженными цветами будут объединяться с самим собой, а не с цветом фона.</span><span class="sxs-lookup"><span data-stu-id="326cd-129">If this occurs, the edge pixels that are antialiased will color merge with themselves instead of with the background color.</span></span> <span data-ttu-id="326cd-130">Это приводит к затемнению и цвету краев.</span><span class="sxs-lookup"><span data-stu-id="326cd-130">This results in darkened and colorful edges.</span></span>
-   <span data-ttu-id="326cd-131">Приложения не должны закрашивать текст путем рисования отдельных символов в непрозрачном режиме, так как границы символа могут обрезаться следующим символом.</span><span class="sxs-lookup"><span data-stu-id="326cd-131">Applications should not paint text by painting the characters individually when in opaque mode because the edge of a character may be clipped by the following character.</span></span> <span data-ttu-id="326cd-132">Это происходит потому, что символ, сглаженный с помощью ClearType, может иметь отрицательную ширину или с, где обычный символ имеет положительную или с.</span><span class="sxs-lookup"><span data-stu-id="326cd-132">This occurs because a character that is smoothed with ClearType may have a negative A or C width where the regular character has a positive A or C width.</span></span> <span data-ttu-id="326cd-133">Только ширина символа в B гарантирована одинакова.</span><span class="sxs-lookup"><span data-stu-id="326cd-133">Only the B width of the character is guaranteed to be the same.</span></span> <span data-ttu-id="326cd-134">Аналогично, приложения должны быть внимательны, если сглаженный текст находится рядом с несглаженным текстом.</span><span class="sxs-lookup"><span data-stu-id="326cd-134">Likewise, applications should be careful if smoothed text is next to unsmoothed text.</span></span>
-   <span data-ttu-id="326cd-135">Если приложение визуализирует текст, а затем манипулирует точечным рисунком, необходимо отключить сглаживание шрифтов, установив для элемента **лфкуалити** структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) значение нонантиалиасед \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="326cd-135">If an application renders text and then manipulates the bitmap, font smoothing should be turned off by setting the **lfQuality** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to NONANTIALIASED\_QUALITY.</span></span> <span data-ttu-id="326cd-136">Например, игра может добавить эффект тени к растровому изображению или текст, отображаемый в растровом изображении, можно масштабировать для создания сумбвиев.</span><span class="sxs-lookup"><span data-stu-id="326cd-136">For example, a game may add a bitmap shadow effect, or text rendered into a bitmap may be scaled to produce a thumbview.</span></span>
-   <span data-ttu-id="326cd-137">Если пользователь работает в книжной ориентации (то есть чередование ведется горизонтально), сглаживание ClearType должно быть отключено.</span><span class="sxs-lookup"><span data-stu-id="326cd-137">If the user is running in portrait mode (that is, monitor striping is horizontal) ClearType antialiasing should be disabled.</span></span>

<span data-ttu-id="326cd-138">Параметр *фдвкуалити* в [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) и член **ЛФКУАЛИТИ** [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) принимают \_ флаг качества CLEARTYPE.</span><span class="sxs-lookup"><span data-stu-id="326cd-138">The *fdwQuality* parameter in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) and the **lfQuality** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accept the CLEARTYPE\_QUALITY flag.</span></span> <span data-ttu-id="326cd-139">Растрирование шрифтов, созданных с помощью этого флага, будет использовать средство прорисовки ClearType.</span><span class="sxs-lookup"><span data-stu-id="326cd-139">Rasterization of fonts created with this flag will use the ClearType rasterizer.</span></span> <span data-ttu-id="326cd-140">Этот флаг не влияет на предыдущие версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="326cd-140">This flag has no effect on previous versions of the operating system.</span></span>

 

 
