---
title: Использование DirectX с дисплеями с широким динамическим диапазоном и расширенным управлением цветами
description: В этом разделе представлен технический обзор визуализации содержимого Direct3D 11 и Direct3D 12 с высоким динамическим диапазоном на HDR10 дисплеи с помощью расширенной поддержки цветов Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104558900"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a><span data-ttu-id="4d566-103">Использование DirectX с высоким динамическим отображением диапазона и расширенным цветом</span><span class="sxs-lookup"><span data-stu-id="4d566-103">Using DirectX with high dynamic range Displays and Advanced Color</span></span>

<span data-ttu-id="4d566-104">В этом разделе представлен технический обзор содержимого Direct3D 11 и Direct3D 12 с высоким динамическим диапазоном (HDR) на HDR10 дисплее с помощью расширенной поддержки цветов Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4d566-104">This topic provides a technical overview of outputting high dynamic range (HDR) Direct3D 11 and Direct3D 12 content to an HDR10 display using Windows 10 advanced color support.</span></span> <span data-ttu-id="4d566-105">В нем приведены основные концептуальные различия между выводом в HDR10 в сравнении с отображаемыми традиционными стандартными динамическими диапазонами (SDR).</span><span class="sxs-lookup"><span data-stu-id="4d566-105">It summarizes some key conceptual differences between outputting to HDR10 displays as compared to traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="4d566-106">Он также охватывает ключевые технические требования для приложения, чтобы обеспечить правильную поддержку расширенного цвета Windows, а также рекомендации и рекомендации.</span><span class="sxs-lookup"><span data-stu-id="4d566-106">It also covers the key technical requirements for your app to properly support Windows advanced color, as well as recommendations and best practices.</span></span>

## <a name="introduction"></a><span data-ttu-id="4d566-107">Введение</span><span class="sxs-lookup"><span data-stu-id="4d566-107">Introduction</span></span>

<span data-ttu-id="4d566-108">Windows 10 поддерживает HDR и другие расширенные экраны цвета, которые обеспечивают значительно более высокую качество цветопередачи по сравнению с традиционными дисплеями SDR.</span><span class="sxs-lookup"><span data-stu-id="4d566-108">Windows 10 supports HDR and other advanced color displays, which provide significantly higher color fidelity than traditional SDR displays.</span></span> <span data-ttu-id="4d566-109">Вы можете использовать Direct3D, Direct2D и другие графические API для отображения HDR-содержимого в пригодном для просмотра виде.</span><span class="sxs-lookup"><span data-stu-id="4d566-109">You can use Direct3D, Direct2D and other graphics APIs to render HDR content to a capable display.</span></span>

<span data-ttu-id="4d566-110">Расширенный цвет Windows относится к нескольким связанным технологиям, впервые представленным в Windows 10 версии 1703, которые обеспечивают поддержку для отображения, превышающих возможности цветового отображения традиционных стандартных динамических диапазонов (SDR).</span><span class="sxs-lookup"><span data-stu-id="4d566-110">Windows advanced color refers to several related technologies, first introduced with Windows 10 version 1703, that provide support for displays that exceed the color capabilities of traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="4d566-111">Ниже описаны три основные расширенные возможности.</span><span class="sxs-lookup"><span data-stu-id="4d566-111">The three major extended capabilities are described below.</span></span> <span data-ttu-id="4d566-112">Наиболее распространенный тип расширенного представления цвета, HDR10, поддерживает все три расширенные возможности.</span><span class="sxs-lookup"><span data-stu-id="4d566-112">The most common type of advanced color display, HDR10, supports all three extended capabilities.</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="4d566-113">Высокий динамический диапазон</span><span class="sxs-lookup"><span data-stu-id="4d566-113">High dynamic range</span></span>

<span data-ttu-id="4d566-114">Динамический диапазон — это разница между максимальной и минимальной яркостью в сцене; часто это измеряется в НИТС (Канделас на квадратный сантиметр).</span><span class="sxs-lookup"><span data-stu-id="4d566-114">Dynamic range refers to the difference between the maximum and minimum luminance in a scene; this is often measured in nits (candelas per square centimeter).</span></span> <span data-ttu-id="4d566-115">Реальные сцены, такие как этот закат, часто имеют динамические диапазоны из 10 заказов на величину освещенности. человеческий глаз может назначить еще больший диапазон после адаптации.</span><span class="sxs-lookup"><span data-stu-id="4d566-115">Real world scenes, such as this sunset, often have dynamic ranges of 10 orders of magnitude of luminance; the human eye can discern an even greater range after adaptation.</span></span>

![изображение заката с ярко-темными точками в сцене с пометкой](images/HDR-HDR.jpg)

<span data-ttu-id="4d566-117">За пререшениями Direct3D 9 обработчики графики могут внутреннно визуализировать свои сцены на уровне физической точности.</span><span class="sxs-lookup"><span data-stu-id="4d566-117">Ever since Direct3D 9, graphics engines have been able to internally render their scenes with this level of physically accurate fidelity.</span></span> <span data-ttu-id="4d566-118">Однако типичный стандарт динамического отображения диапазона может воспроизводить всего более 3 заказов на степень освещенности, поэтому все содержимое, визуализированное HDR, должно быть тонемаппед (сжато) в ограниченный диапазон отображения.</span><span class="sxs-lookup"><span data-stu-id="4d566-118">However, a typical standard dynamic range display can reproduce only a little more than 3 orders of magnitude of luminance, and therefore any HDR-rendered content had to be tonemapped (compressed) into the limited range of the display.</span></span> <span data-ttu-id="4d566-119">Новые HDR-отображения, в том числе те, которые соответствуют стандарту HDR10 (BT. 2100), нарушают это ограничение.</span><span class="sxs-lookup"><span data-stu-id="4d566-119">New HDR displays, including those that comply with the HDR10 (BT.2100) standard, break through this limitation.</span></span>

### <a name="wide-color-gamut-with-automatic-system-color-management"></a><span data-ttu-id="4d566-120">Широкая цветовая палитра с автоматическим управлением системой управления цветом</span><span class="sxs-lookup"><span data-stu-id="4d566-120">Wide color gamut with automatic system color management</span></span>

<span data-ttu-id="4d566-121">Цветовая палитра относится к диапазону и насыщенности оттенков, которые может воспроизводить изображение.</span><span class="sxs-lookup"><span data-stu-id="4d566-121">Color gamut refers to the range and saturation of hues that a display can reproduce.</span></span> <span data-ttu-id="4d566-122">Самый насыщенный естественный цвет, который может воспринимать человеческим глазом, — чистый, монохромный, например, то, что создается лазером.</span><span class="sxs-lookup"><span data-stu-id="4d566-122">The most saturated natural color the human eye can perceive is pure, monochromatic light such as what is produced by a laser.</span></span> <span data-ttu-id="4d566-123">Однако основная часть отображения потребителей часто может воспроизводить цвета только в пределах палитры sRGB, что представляет примерно 35% всех цветов воспринимаемого.</span><span class="sxs-lookup"><span data-stu-id="4d566-123">However, mainstream consumer displays can often reproduce colors only within the sRGB gamut, which represents only about 35% of all human-perceivable colors.</span></span> <span data-ttu-id="4d566-124">На приведенной ниже схеме представлено представление Спектрал очага или всех цветов воспринимаемого (на определенном уровне освещенности), где маленький треугольник — это цвет sRGB.</span><span class="sxs-lookup"><span data-stu-id="4d566-124">The diagram below is a representation of the human "spectral locus", or all perceivable colors (at a given luminance level), where the smaller triangle is the sRGB gamut.</span></span>

![Схема цветового охвата Спектрал очага и sRGB](images/HDR-WCG.jpg)

<span data-ttu-id="4d566-126">В верхней части на профессиональном компьютере отображаются длинные поддерживаемые цветовые палитры, которые значительно шире, чем sRGB, например Adobe RGB и D65-P3.</span><span class="sxs-lookup"><span data-stu-id="4d566-126">High end, professional PC displays have long supported color gamuts that are significantly wider than sRGB, such as Adobe RGB and D65-P3.</span></span> <span data-ttu-id="4d566-127">И эти широкие экранные палитры становятся более распространенными.</span><span class="sxs-lookup"><span data-stu-id="4d566-127">And these wide gamut displays are becoming more common.</span></span> <span data-ttu-id="4d566-128">Однако до расширенного цвета Windows не выполняло Управление цветом на уровне системы для приложений.</span><span class="sxs-lookup"><span data-stu-id="4d566-128">However, prior to advanced color, Windows didn't perform any system-level color management for applications.</span></span> <span data-ttu-id="4d566-129">Это означало, что при отрисовке приложения DirectX, например чистого красного цвета или RGB (1,0, 0,0, 0,0) в цепочку буферов, Windows будет просто просканировать наиболее насыщенный красный цвет, который может воспроизводить дисплей, независимо от фактической палитры цветов на дисплее.</span><span class="sxs-lookup"><span data-stu-id="4d566-129">This meant that if a DirectX app rendered, for example, a pure red or RGB(1.0, 0.0, 0.0) to its swap chain, then Windows would simply scan out the most saturated red that the display could reproduce, regardless of what the actual color gamut of the display was.</span></span>

<span data-ttu-id="4d566-130">Приложения, которым требовалась высокая точность цвета, могут запрашивать цветовые возможности экрана (например, с помощью ICC-профилей), а также выполнять собственные функции управления цветом, чтобы правильно ориентироваться в цветовой палитре экрана.</span><span class="sxs-lookup"><span data-stu-id="4d566-130">Apps that needed high color accuracy could query the color capabilities of the display (for example, using ICC profiles), and perform their own in-process color management to correctly target the display's color gamut.</span></span> <span data-ttu-id="4d566-131">Однако подавляющее большинство приложений и визуального содержимого предполагает, что дисплей имеет значение sRGB, и для выполнения этого предположений используются операционные системы.</span><span class="sxs-lookup"><span data-stu-id="4d566-131">However, the vast majority of apps and visual content assume that the display is sRGB, and they rely on the operating system to fulfill this assumption.</span></span>

<span data-ttu-id="4d566-132">Расширенный цвет Windows добавляет автоматическое управление цветом на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="4d566-132">Windows advanced color adds automatic system-level color management.</span></span> <span data-ttu-id="4d566-133">Диспетчер окон рабочего стола (DWM) является компоновщиком Windows.</span><span class="sxs-lookup"><span data-stu-id="4d566-133">The Desktop Window Manager (DWM) is Windows' compositor.</span></span> <span data-ttu-id="4d566-134">Если включен расширенный цвет, DWM выполняет явное преобразование цвета из колорспаце визуального содержимого приложения в каноническое цветовое пространство композиции, которое является scRGB.</span><span class="sxs-lookup"><span data-stu-id="4d566-134">When advanced color is enabled, the DWM performs an explicit color conversion from the app visual content's colorspace to a canonical composition color space, which is scRGB.</span></span> <span data-ttu-id="4d566-135">Windows, затем цвет преобразует составное содержимое буфера кадров в собственное цветовое пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="4d566-135">Windows then color-converts the composed framebuffer content to the display's native color space.</span></span> <span data-ttu-id="4d566-136">Таким образом, традиционное содержимое sRGB автоматически получает точную цветопередачу, в то время как расширенные приложения, поддерживающие цвета, могут использовать возможности полного цветового представления.</span><span class="sxs-lookup"><span data-stu-id="4d566-136">In this way, traditional sRGB content automatically gets color-accurate behavior, while advanced color-aware apps can take advantage of the full color capabilities of the display.</span></span>

### <a name="deep-precisionbit-depth"></a><span data-ttu-id="4d566-137">Глубокая точность или глубина бита</span><span class="sxs-lookup"><span data-stu-id="4d566-137">Deep precision/bit depth</span></span>

<span data-ttu-id="4d566-138">Числовая точность или битовая глубина означает представление или различение похожих, но различных цветов без чередования и артефактов.</span><span class="sxs-lookup"><span data-stu-id="4d566-138">Numerical precision, or bit depth, refers to representing or distinguishing between similar but distinct colors without banding nor artifacts.</span></span> <span data-ttu-id="4d566-139">Основной компьютер отображает 8 бит на цветовой канал, в то время как человеческий глаз требует не менее 10-12 бит точности, чтобы избежать воспринимаемого искажений, не прибегая к таким методам, как дизеринг или в зависимости от условий просмотра.</span><span class="sxs-lookup"><span data-stu-id="4d566-139">Mainstream PC displays support 8 bits per color channel, while the human eye requires at least 10-12 bits of precision to avoid perceivable distortions, without resorting to techniques such as dithering or depending on viewing conditions.</span></span>

![Рисунок Виндмиллс в смоделированных двух битах на цветовой канал и 8 бит на канал](images/HDR-bitdepth.jpg)

<span data-ttu-id="4d566-141">До расширенного цвета оконное приложение DWM ограничило вывод содержимого только по 8 битам на цветовой канал, даже если дисплей поддерживает более высокую глубину.</span><span class="sxs-lookup"><span data-stu-id="4d566-141">Prior to advanced color, the DWM restricted windowed apps to output content at only 8 bits per color channel, even if the display supported a higher bit depth.</span></span> <span data-ttu-id="4d566-142">Если включен расширенный цвет, DWM выполняет свою композицию с использованием IEEE половинной точности с плавающей запятой (FP16), устраняя узкие места и позволяя использовать полную точность экрана.</span><span class="sxs-lookup"><span data-stu-id="4d566-142">When advanced color is enabled, the DWM performs its composition using IEEE half-precision floating point (FP16), eliminating any bottlenecks, and allowing the full precision of the display to be used.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="4d566-143">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="4d566-143">System Requirements</span></span>

### <a name="operating-system-os"></a><span data-ttu-id="4d566-144">Операционная система (ОС)</span><span class="sxs-lookup"><span data-stu-id="4d566-144">Operating system (OS)</span></span>

<span data-ttu-id="4d566-145">Расширенная поддержка цветов впервые поставляется с Windows 10, версия 1703 и значительно улучшена при каждом обновлении.</span><span class="sxs-lookup"><span data-stu-id="4d566-145">Advanced color support first shipped with Windows 10, version 1703, and it has been significantly improved with each update.</span></span> <span data-ttu-id="4d566-146">В этом разделе предполагается, что ваше приложение предназначено для Windows 10, версии 1903 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="4d566-146">This topic assumes that your app is targeting Windows 10, version 1903, or later.</span></span>

### <a name="display"></a><span data-ttu-id="4d566-147">Отображение</span><span class="sxs-lookup"><span data-stu-id="4d566-147">Display</span></span>

<span data-ttu-id="4d566-148">Чтобы воспользоваться преимуществами высокого динамического диапазона, необходимо иметь дисплей, поддерживающий стандарт HDR10.</span><span class="sxs-lookup"><span data-stu-id="4d566-148">To take advantage of high dynamic range, you must have a display that supports the HDR10 standard.</span></span> <span data-ttu-id="4d566-149">Windows лучше работает с дисплеями, [сертифицированными](https://displayhdr.org/)по стандарту VESA дисплайхдр.</span><span class="sxs-lookup"><span data-stu-id="4d566-149">Windows works best with displays that are [VESA DisplayHDR certified](https://displayhdr.org/).</span></span>

### <a name="graphics-processor-gpu"></a><span data-ttu-id="4d566-150">Графический процессор (GPU)</span><span class="sxs-lookup"><span data-stu-id="4d566-150">Graphics processor (GPU)</span></span>

<span data-ttu-id="4d566-151">Требуется недавний GPU.</span><span class="sxs-lookup"><span data-stu-id="4d566-151">A recent GPU is required.</span></span> <span data-ttu-id="4d566-152">Для поддержки HDR10 отображения Windows 10 требуется один из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="4d566-152">To support HDR10 displays, Windows 10 requires one of the following.</span></span>

* <span data-ttu-id="4d566-153">NVIDIA GeForce 1000 Series (Pascal) или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4d566-153">Nvidia GeForce 1000 series (Pascal), or newer</span></span>
* <span data-ttu-id="4d566-154">AMD Radeon RX 400 (Поларис) или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4d566-154">AMD Radeon RX 400 series (Polaris), or newer</span></span>
* <span data-ttu-id="4d566-155">Выбранная серия Intel Core 7 (Каби Lake) или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="4d566-155">Selected Intel Core 7 series (Kaby Lake), or newer</span></span>

<span data-ttu-id="4d566-156">Обратите внимание, что в зависимости от сценариев применяются дополнительные требования к оборудованию, включая аппаратное ускорение (10 бит HEVC, 10 бит VP9 и т. д.) и поддержку PlayReady (SL3000).</span><span class="sxs-lookup"><span data-stu-id="4d566-156">Note that additional hardware requirements apply depending on the scenarios, including hardware codec acceleration (10 bit HEVC, 10 bit VP9, etc.) and PlayReady support (SL3000).</span></span> <span data-ttu-id="4d566-157">Для получения более подробной информации обратитесь к поставщику GPU.</span><span class="sxs-lookup"><span data-stu-id="4d566-157">Contact your GPU vendor for more specific information.</span></span>

### <a name="graphics-driver-wddm"></a><span data-ttu-id="4d566-158">Драйвер графики (WDDM)</span><span class="sxs-lookup"><span data-stu-id="4d566-158">Graphics driver (WDDM)</span></span>

<span data-ttu-id="4d566-159">Самый последний доступный графический драйвер настоятельно рекомендуется в Центр обновления Windows или у поставщика GPU или на веб-сайте производителя ПК.</span><span class="sxs-lookup"><span data-stu-id="4d566-159">The latest available graphics driver is strongly recommended, either from Windows Update or from the GPU vendor or PC manufacturer's website.</span></span> <span data-ttu-id="4d566-160">Для Windows 10, версии 1903 и более поздних версий рекомендуется использовать драйверы, поддерживающие по крайней мере Windows (WDDM) версии 2,6.</span><span class="sxs-lookup"><span data-stu-id="4d566-160">For Windows 10, version 1903, and later, we recommend drivers that support at least Windows Display Driver Model (WDDM) version 2.6.</span></span>

## <a name="supported-rendering-apis"></a><span data-ttu-id="4d566-161">Поддерживаемые API-интерфейсы подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="4d566-161">Supported rendering APIs</span></span>

<span data-ttu-id="4d566-162">Windows 10 поддерживает разнообразные API-интерфейсы и платформы для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="4d566-162">Windows 10 supports a wide variety of rendering APIs and frameworks.</span></span> <span data-ttu-id="4d566-163">Расширенная поддержка цветов в основном зависит от приложения, которое может выполнять современные презентации с помощью DXGI или API визуального уровня.</span><span class="sxs-lookup"><span data-stu-id="4d566-163">Advanced color support fundamentally relies on your app being able to perform modern presentation using either DXGI or the Visual Layer APIs.</span></span>

* [<span data-ttu-id="4d566-164">Графическая инфраструктура DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="4d566-164">DirectX Graphics Infrastructure (DXGI)</span></span>](../direct3ddxgi/dx-graphics-dxgi.md)
* [<span data-ttu-id="4d566-165">Визуальный слой (Windows. UI. композиция)</span><span class="sxs-lookup"><span data-stu-id="4d566-165">Visual Layer (Windows.UI.Composition)</span></span>](/windows/uwp/composition/visual-layer)

<span data-ttu-id="4d566-166">Таким образом, любой API отрисовки, который может выводить в один из этих методов, может поддерживать расширенный цвет.</span><span class="sxs-lookup"><span data-stu-id="4d566-166">Therefore, any rendering API that can output to one of these presentations methods can support advanced color.</span></span> <span data-ttu-id="4d566-167">К ним относятся, но не ограничиваются.</span><span class="sxs-lookup"><span data-stu-id="4d566-167">This includes but is not limited to these.</span></span>

* [<span data-ttu-id="4d566-168">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4d566-168">Direct3D 11</span></span>](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="4d566-169">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4d566-169">Direct3D 12</span></span>](../direct3d12/direct3d-12-graphics.md)
* [<span data-ttu-id="4d566-170">Direct2D</span><span class="sxs-lookup"><span data-stu-id="4d566-170">Direct2D</span></span>](../direct2d/direct2d-portal.md)
* [<span data-ttu-id="4d566-171">Win2D</span><span class="sxs-lookup"><span data-stu-id="4d566-171">Win2D</span></span>](https://github.com/Microsoft/Win2D)
  * <span data-ttu-id="4d566-172">Требует использования API-интерфейсов нижнего уровня **канвассвапчаин** или **канвассвапчаинпанел** .</span><span class="sxs-lookup"><span data-stu-id="4d566-172">Requires using the lower level **CanvasSwapChain** or **CanvasSwapChainPanel** APIs.</span></span>
* [<span data-ttu-id="4d566-173">**Windows.UI.Input.Inking**</span><span class="sxs-lookup"><span data-stu-id="4d566-173">**Windows.UI.Input.Inking**</span></span>](/uwp/api/Windows.UI.Input.Inking)
  * <span data-ttu-id="4d566-174">Поддерживает собственную отрисовку рукописного ввода с помощью DirectX.</span><span class="sxs-lookup"><span data-stu-id="4d566-174">Supports custom dry ink rendering using DirectX.</span></span>
* [<span data-ttu-id="4d566-175">XAML</span><span class="sxs-lookup"><span data-stu-id="4d566-175">XAML</span></span>](/windows/uwp/xaml-platform/)
  * <span data-ttu-id="4d566-176">Поддерживает воспроизведение HDR-видео с помощью **медиаплайерелемент**.</span><span class="sxs-lookup"><span data-stu-id="4d566-176">Supports playback of HDR videos using **MediaPlayerElement**.</span></span>
  * <span data-ttu-id="4d566-177">Поддерживает декодирование изображений XR JPEG с помощью элемента **Image** .</span><span class="sxs-lookup"><span data-stu-id="4d566-177">Supports decode of JPEG XR images using **Image** element.</span></span>
  * <span data-ttu-id="4d566-178">Поддерживает взаимодействие DirectX с помощью **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="4d566-178">Supports DirectX interop using **SwapChainPanel**.</span></span>

## <a name="handling-dynamic-display-capabilities"></a><span data-ttu-id="4d566-179">Обработка возможностей динамического просмотра</span><span class="sxs-lookup"><span data-stu-id="4d566-179">Handling dynamic display capabilities</span></span>

<span data-ttu-id="4d566-180">Windows 10 поддерживает огромные разнообразные дисплеи с поддержкой цветов, от эффективных интегрированных панелей до высокопроизводительных игровых мониторов и телевизоров.</span><span class="sxs-lookup"><span data-stu-id="4d566-180">Windows 10 supports an enormous range of advanced color-capable displays, from power-efficient integrated panels to high end gaming monitors and TVs.</span></span> <span data-ttu-id="4d566-181">Пользователи Windows предполагают, что ваше приложение будет беспрепятственно работать со всеми этими вариациями, включая повсеместно существующие экраны SDR.</span><span class="sxs-lookup"><span data-stu-id="4d566-181">Windows users expect that your app will seamlessly handle all of these variations, including ubiquitous existing SDR displays.</span></span>

<span data-ttu-id="4d566-182">Windows 10 предоставляет пользователю возможность управлять HDR и расширенными возможностями цвета.</span><span class="sxs-lookup"><span data-stu-id="4d566-182">Windows 10 provides control over HDR and advanced color capabilities to the user.</span></span> <span data-ttu-id="4d566-183">Приложение должно определить конфигурацию текущего экрана и динамически реагировать на любые изменения в возможности.</span><span class="sxs-lookup"><span data-stu-id="4d566-183">Your app must detect the current display's configuration, and respond dynamically to any changes in capability.</span></span> <span data-ttu-id="4d566-184">Это может произойти по многим причинам, например, если пользователь включил или отключил функцию или переместил приложение между разными дисплеями или изменилось состояние электропитания системы.</span><span class="sxs-lookup"><span data-stu-id="4d566-184">This could occur for many reasons, for example, because the user enabled or disabled a feature, or moved the app between different displays, or the system's power state changed.</span></span>

### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="4d566-185">Приложения универсальной платформы Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="4d566-185">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="4d566-186">Если вы создаете приложение UWP, независимо от используемого API графической отрисовки, используйте [**адванцедколоринфо**](/uwp/api/windows.graphics.display.advancedcolorinfo) , чтобы получить возможности отображения.</span><span class="sxs-lookup"><span data-stu-id="4d566-186">If you're writing a UWP app, regardless of the graphics rendering API you're using, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get display capabilities.</span></span> <span data-ttu-id="4d566-187">Получите экземпляр **адванцедколоринфо** из [**DisplayInformation:: жетадванцедколоринфо**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span><span class="sxs-lookup"><span data-stu-id="4d566-187">Obtain an instance of **AdvancedColorInfo** from [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span></span>

<span data-ttu-id="4d566-188">Чтобы проверить, какой расширенный тип цвета активен в данный момент, используйте свойство [**куррентадванцедколоркинд**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) .</span><span class="sxs-lookup"><span data-stu-id="4d566-188">To check what advanced color kind is currently active, use the [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) property.</span></span> <span data-ttu-id="4d566-189">В Windows 10 версия 1903 и более поздние версии возвращают одно из трех возможных значений: **SDR**, **ВКГ** или **HDR**.</span><span class="sxs-lookup"><span data-stu-id="4d566-189">In Windows 10, version 1903, and later, this returns one of three possible values: **SDR**, **WCG**, or **HDR**.</span></span> <span data-ttu-id="4d566-190">Это наиболее важное свойство, которое необходимо проверить, и вы должны настроить конвейер отрисовки и представления в ответ на активный вид.</span><span class="sxs-lookup"><span data-stu-id="4d566-190">This is the most important property to check, and you should configure your render and presentation pipeline in response to the active kind.</span></span>

<span data-ttu-id="4d566-191">Чтобы проверить, какие расширенные виды цветов поддерживаются, но не обязательно являются активными, вызовите [**исадванцедколоркиндаваилабле**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span><span class="sxs-lookup"><span data-stu-id="4d566-191">To check what advanced color kinds are supported, but not necessarily active, call [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span></span> <span data-ttu-id="4d566-192">Эти сведения можно использовать, например, чтобы запросить у пользователя возможность перехода к приложению "Параметры Windows", чтобы они могли включить HDR или ВКГ.</span><span class="sxs-lookup"><span data-stu-id="4d566-192">You could use this information, for example, to prompt the user to navigate to the Windows Settings app so that they can enable HDR or WCG.</span></span>

<span data-ttu-id="4d566-193">Другие члены **адванцедколоринфо** предоставляют количественную информацию о том физическом цвете (светимость и чроминанце), соответствующий SMPTE St. 2086 статические метаданные HDR.</span><span class="sxs-lookup"><span data-stu-id="4d566-193">The other members of **AdvancedColorInfo** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="4d566-194">Эти сведения следует использовать для настройки сопоставления тонемаппинг и цветового охвата приложения.</span><span class="sxs-lookup"><span data-stu-id="4d566-194">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="4d566-195">Чтобы обрабатывались изменения в расширенных возможностях цвета, зарегистрируйте событие [**адванцедколоринфочанжед**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) .</span><span class="sxs-lookup"><span data-stu-id="4d566-195">To handle changes in advanced color capabilities, register for the [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) event.</span></span> <span data-ttu-id="4d566-196">Это событие возникает, если любой из причин изменяется любой параметр расширенных возможностей цвета экрана.</span><span class="sxs-lookup"><span data-stu-id="4d566-196">This event is raised if any parameter of the display's advanced color capabilities changes for any reason.</span></span>

<span data-ttu-id="4d566-197">Обработайте это событие, получив новый экземпляр **адванцедколоринфо**, и проверив, какие значения были изменены.</span><span class="sxs-lookup"><span data-stu-id="4d566-197">Handle this event by obtaining a new instance of **AdvancedColorInfo**, and checking which values have changed.</span></span>

### <a name="desktop-win32-directx-apps"></a><span data-ttu-id="4d566-198">Приложения DirectX для Desktop (Win32)</span><span class="sxs-lookup"><span data-stu-id="4d566-198">Desktop (Win32) DirectX apps</span></span>

<span data-ttu-id="4d566-199">Если вы создаете приложение Win32 и используете DirectX для подготовки к просмотру, используйте [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) , чтобы получить возможности отображения.</span><span class="sxs-lookup"><span data-stu-id="4d566-199">If you're writing a Win32 app, and using DirectX to render, then use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get display capabilities.</span></span> <span data-ttu-id="4d566-200">Получите экземпляр этой структуры с помощью [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span><span class="sxs-lookup"><span data-stu-id="4d566-200">Obtain an instance of this struct via [**IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span></span>

<span data-ttu-id="4d566-201">Чтобы проверить, какой расширенный тип цвета активен в данный момент, используйте свойство **колорспаце** , которое имеет тип [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), и содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4d566-201">To check what advanced color kind is currently active, use the **ColorSpace** property, which is of type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), and contains one of the following values:</span></span>

* <span data-ttu-id="4d566-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span><span class="sxs-lookup"><span data-stu-id="4d566-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span></span>
* <span data-ttu-id="4d566-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span><span class="sxs-lookup"><span data-stu-id="4d566-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span></span>

> [!Note]
> <span data-ttu-id="4d566-204">Другие расширенные типы цветов, например ВКГ, обрабатываются как SDR с помощью DXGI.</span><span class="sxs-lookup"><span data-stu-id="4d566-204">Other advanced color kinds such as WCG are treated as SDR by DXGI.</span></span> <span data-ttu-id="4d566-205">Вы не можете использовать DXGI для обнаружения ВКГ дисплея.</span><span class="sxs-lookup"><span data-stu-id="4d566-205">You can't use DXGI to identify a WCG display.</span></span>

> [!Note]
> <span data-ttu-id="4d566-206">DXGI не позволяет проверить, какие расширенные виды цветов поддерживаются, но не активны в данный момент.</span><span class="sxs-lookup"><span data-stu-id="4d566-206">DXGI doesn't let you check what advanced color kinds are supported but not active at the moment.</span></span>

<span data-ttu-id="4d566-207">Большинство других членов **DXGI_OUTPUT_DESC1** предоставляют количественную информацию о физическом цветовом томе (светимости и чроминанце) панели, соответствующей статическим МЕТАДАННЫМ SMPTE St. 2086.</span><span class="sxs-lookup"><span data-stu-id="4d566-207">Most of the other members of **DXGI_OUTPUT_DESC1** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="4d566-208">Эти сведения следует использовать для настройки сопоставления тонемаппинг и цветового охвата приложения.</span><span class="sxs-lookup"><span data-stu-id="4d566-208">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="4d566-209">Приложения Win32 не имеют собственного механизма для реагирования на расширенные изменения возможностей цвета.</span><span class="sxs-lookup"><span data-stu-id="4d566-209">Win32 apps don't have a native mechanism to respond to advanced color capability changes.</span></span> <span data-ttu-id="4d566-210">Вместо этого, если приложение использует цикл подготовки к просмотру, необходимо запросить [**IDXGIFactory1::-Current**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="4d566-210">Instead, if your app uses a render loop, then you should query [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) with each frame.</span></span> <span data-ttu-id="4d566-211">Если он возвращает **значение false**, то следует получить новый **DXGI_OUTPUT_DESC1** и проверить, какие значения были изменены.</span><span class="sxs-lookup"><span data-stu-id="4d566-211">If it reports **FALSE**, then you should obtain a new **DXGI_OUTPUT_DESC1**, and check which values have changed.</span></span>

<span data-ttu-id="4d566-212">Кроме того, конвейер сообщений Win32 должен обменяться сообщением [**WM_SIZE**](../winmsg/wm-size.md) , которое указывает, что приложение могло перемещаться между разными дисплеями.</span><span class="sxs-lookup"><span data-stu-id="4d566-212">In addition, your Win32 message pump should handle the [**WM_SIZE**](../winmsg/wm-size.md) message, which indicates that your app may have moved between different displays.</span></span>

> [!Note]
> <span data-ttu-id="4d566-213">Чтобы получить новый **DXGI_OUTPUT_DESC1**, необходимо получить текущее отображение.</span><span class="sxs-lookup"><span data-stu-id="4d566-213">To obtain a new **DXGI_OUTPUT_DESC1**, you must obtain the current display.</span></span> <span data-ttu-id="4d566-214">Однако не следует вызывать метод **идксгисвапчаин:: жетконтаинингаутпут**.</span><span class="sxs-lookup"><span data-stu-id="4d566-214">However, you should not call **IDXGISwapChain::GetContainingOutput**.</span></span> <span data-ttu-id="4d566-215">Это обусловлено тем, что цепочки переключения будут возвращать устаревшие выходные данные DXGI, когда **дксгифактори:: Current** имеет значение false, и повторное создание цепочки буферов для получения текущих выходных данных приводит к временному черному экрану.</span><span class="sxs-lookup"><span data-stu-id="4d566-215">This is because swap chains will return a stale DXGI output once **DXGIFactory::IsCurrent** is false, and recreating the swap chain to get a current output results in a temporary black screen.</span></span> <span data-ttu-id="4d566-216">Вместо этого рекомендуется перечислить границы всех выходов DXGI и определить, какая из них имеет наибольшее пересечение с границами окна приложения.</span><span class="sxs-lookup"><span data-stu-id="4d566-216">Instead, we recommend that you enumerate through the bounds of all DXGI outputs, and determine which one has the greatest intersection with your app window's bounds.</span></span>

<span data-ttu-id="4d566-217">Следующий пример кода взят из [репозитория DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="4d566-217">The following code example comes from the [DirectX-Graphics-Samples repository](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span>

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a><span data-ttu-id="4d566-218">Настройка цепочки буфера обмена DirectX</span><span class="sxs-lookup"><span data-stu-id="4d566-218">Setting up Your DirectX swap chain</span></span>

<span data-ttu-id="4d566-219">После определения того, что в настоящее время в дисплее поддерживаются дополнительные возможности цвета, настройте цепочку подкачки следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4d566-219">Once you have determined that the display currently supports advanced color capabilities, configure your swap chain as follows.</span></span>

### <a name="use-a-flip-presentation-model-effect"></a><span data-ttu-id="4d566-220">Использование эффектов "перевернуть модель представления"</span><span class="sxs-lookup"><span data-stu-id="4d566-220">Use a flip presentation model effect</span></span>

<span data-ttu-id="4d566-221">При создании цепочки подкачки с помощью **креатесвапчаинфор [HWND | Композиция | CoreWindow]** методы, необходимо использовать модель перелистывания DXGI, выбрав параметр **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** или **DXGI_SWAP_EFFECT_FLIP_DISCARD** , который делает цепочку подкачки доступной для расширенной цветовой обработки из DWM и различных оптимизаций на весь экран.</span><span class="sxs-lookup"><span data-stu-id="4d566-221">When creating your swap chain using the **CreateSwapChainFor[Hwnd|Composition|CoreWindow]** methods, you must use the DXGI flip model by selecting either the **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** or **DXGI_SWAP_EFFECT_FLIP_DISCARD** option, which makes your swap chain eligible for advanced color processing from DWM and various fullscreen optimizations.</span></span> <span data-ttu-id="4d566-222">Дополнительные сведения см. в разделе [для достижения оптимальной производительности используйте модель перелистывания DXGI](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .</span><span class="sxs-lookup"><span data-stu-id="4d566-222">For more information, refer to the [For best performance, use DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) topic.</span></span>

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a><span data-ttu-id="4d566-223">Вариант 1.</span><span class="sxs-lookup"><span data-stu-id="4d566-223">Option 1.</span></span> <span data-ttu-id="4d566-224">Использовать формат пикселей FP16 и цветовое пространство scRGB</span><span class="sxs-lookup"><span data-stu-id="4d566-224">Use FP16 pixel format and scRGB color space</span></span>

<span data-ttu-id="4d566-225">Windows 10 поддерживает два основных сочетания формата пикселей и цветового пространства для расширенного цвета.</span><span class="sxs-lookup"><span data-stu-id="4d566-225">Windows 10 supports two main combinations of pixel format and color space for advanced color.</span></span> <span data-ttu-id="4d566-226">Выберите один из них в зависимости от конкретных требований приложения.</span><span class="sxs-lookup"><span data-stu-id="4d566-226">Select one based on your app's specific requirements.</span></span>

<span data-ttu-id="4d566-227">Для приложений общего назначения при создании цепочки подкачки рекомендуется указывать [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="4d566-227">For general-purpose apps, when creating your swap chain we recommend specifying [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="4d566-228">Это также называется *FP16* в [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="4d566-228">That's also known as *FP16* in your [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="4d566-229">По умолчанию цепочка буферов, созданная с помощью формата пикселей с плавающей точкой, обрабатывается так, как если бы она использовала [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) цветовое пространство, которое также называется *ScRGB*.</span><span class="sxs-lookup"><span data-stu-id="4d566-229">By default, a swap chain created with a floating point pixel format is treated as if it uses the [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color space, which is also known as *scRGB*.</span></span>

<span data-ttu-id="4d566-230">Это сочетание предоставляет числовой диапазон и точность для указания практически любого физического цвета и выполнения произвольной обработки, включая смешивание.</span><span class="sxs-lookup"><span data-stu-id="4d566-230">This combination provides you with the numeric range and precision to specify almost any physically possible color, and perform arbitrary processing including blending.</span></span> <span data-ttu-id="4d566-231">Кроме того, если вы используете Direct2D, Win2D или Windows. UI. композиция, это единственное поддерживаемое сочетание для любой цепочки буферов или промежуточного целевого объекта, содержащего расширенное содержимое цвета.</span><span class="sxs-lookup"><span data-stu-id="4d566-231">In addition, if you're using Direct2D, Win2D, or Windows.UI.Composition, then this is the only supported combination for any swap chain or intermediate target that contains advanced color content.</span></span> 

<span data-ttu-id="4d566-232">Основным компромиссом этого варианта является то, что он потребляет 64 бит на пиксель, что удваивает пропускную способность GPU и потребление памяти по сравнению с традиционными форматами точек SDR в формате UINT8.</span><span class="sxs-lookup"><span data-stu-id="4d566-232">The main tradeoff of this option is that it consumes 64 bits per pixel, which doubles GPU bandwidth and memory consumption compared to the traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="4d566-233">Кроме того, scRGB использует числовые значения, находящиеся за пределами нормализованного диапазона [0, 1], для представления цветов, находящихся за пределами палитры sRGB и/или более 80 НИТС светимости.</span><span class="sxs-lookup"><span data-stu-id="4d566-233">In addition, scRGB uses numeric values that are outside the normalized [0, 1] range to represent colors that are outside the sRGB gamut and/or greater than 80 nits of luminance.</span></span> <span data-ttu-id="4d566-234">Например, scRGB (1,0, 1,0, 1,0) кодирует стандартный белый D65 в 80 НИТС; Однако scRGB (12,5, 12,5, 12,5) кодирует тот же белый D65 с более ярким НИТС 1000.</span><span class="sxs-lookup"><span data-stu-id="4d566-234">For example, scRGB (1.0, 1.0, 1.0) encodes the standard D65 white at 80 nits; but scRGB (12.5, 12.5, 12.5) encodes the same D65 white at a much brighter 1000 nits.</span></span> <span data-ttu-id="4d566-235">Для некоторых графических операций требуется нормализованный числовой диапазон, и необходимо либо изменить операцию, либо повторно нормализовать значения цвета.</span><span class="sxs-lookup"><span data-stu-id="4d566-235">Some graphics operations require a normalized numeric range, and you must either modify the operation, or re-normalize color values.</span></span>

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a><span data-ttu-id="4d566-236">Вариант 2. Использование формата пикселей UINT10/RGB10 и HDR10/BT. 2100. цветовое пространство</span><span class="sxs-lookup"><span data-stu-id="4d566-236">Option 2: Use UINT10/RGB10 pixel format and HDR10/BT.2100 color space</span></span>

<span data-ttu-id="4d566-237">Для приложений, использующих HDR10-кодированное содержимое, например проигрывателей мультимедиа или приложений, которые должны использоваться в основном в полноэкранных сценариях, таких как игры, при создании цепочки подкачки следует рассмотреть возможность указания [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) в [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="4d566-237">For apps that consume HDR10-encoded content, such as media players, or apps that are expected to be used mainly in fullscreen scenarios such as games, when creating your swap chain you should consider specifying [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="4d566-238">По умолчанию это рассматривается как использование цветового пространства sRGB. Поэтому необходимо явно вызвать [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)и задать в качестве цветового пространства [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), также известного как HDR10/BT. 2100.</span><span class="sxs-lookup"><span data-stu-id="4d566-238">By default, this is treated as using the sRGB color space; therefore, you must explicitly call [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1), and set as your color space [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), also known as HDR10/BT.2100.</span></span>

<span data-ttu-id="4d566-239">Это сочетание имеет более строгие ограничения, чем FP16.</span><span class="sxs-lookup"><span data-stu-id="4d566-239">This combination has more stringent restrictions than FP16.</span></span> <span data-ttu-id="4d566-240">Его можно использовать только с Direct3D 11 или Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="4d566-240">You can use this only with Direct3D 11 or Direct3D 12.</span></span> <span data-ttu-id="4d566-241">Кроме того, UINT10/HDR10 имеет ограничения в виде промежуточного формата, поскольку в нем используется функция ST. 2084 ЕОТФ ("гамма"), которая является очень нелинейной и оптимизирована в виде сетевого формата, и потому, что она предлагает только 2 бита альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="4d566-241">In addition, UINT10/HDR10 has limitations as an intermediate format because it uses the ST.2084 EOTF ("gamma" function), which is highly nonlinear, and optimized as a wire format, and because it offers only 2 bits of alpha.</span></span>

<span data-ttu-id="4d566-242">Однако это сочетание может обеспечить эффективную оптимизацию производительности при использовании в окончательном выводе приложения.</span><span class="sxs-lookup"><span data-stu-id="4d566-242">However, this combination can offer powerful performance optimizations when used in your app's final output.</span></span> <span data-ttu-id="4d566-243">Он потребляет один и тот же 32 бит на пиксель в виде традиционных форматов пикселей SDR в формате UINT8.</span><span class="sxs-lookup"><span data-stu-id="4d566-243">It consumes the same 32 bits per pixel as traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="4d566-244">Кроме того, в некоторых полноэкранных сценариях операционная система может оптимизировать производительность, напрямую проверяя поверхность HDR10.</span><span class="sxs-lookup"><span data-stu-id="4d566-244">In addition, in certain fullscreen scenarios, the OS can optimize performance by directly scanning out the HDR10 surface.</span></span>

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a><span data-ttu-id="4d566-245">Использование расширенной цепочки цветовой подкачки, когда дисплей находится в режиме SDR</span><span class="sxs-lookup"><span data-stu-id="4d566-245">Using an advanced color swap chain when the display is in SDR mode</span></span>

<span data-ttu-id="4d566-246">Можно использовать расширенную цепочку цветовой подкачки, даже если дисплей не поддерживает некоторые или все дополнительные возможности цвета, необходимые для содержимого.</span><span class="sxs-lookup"><span data-stu-id="4d566-246">You can use an advanced color swap chain even if the display doesn't support some or all of the advanced color capabilities your content requires.</span></span> <span data-ttu-id="4d566-247">В таких случаях диспетчер окон рабочего стола (DWM) будет довнконверт содержимое в соответствии с возможностями экрана.</span><span class="sxs-lookup"><span data-stu-id="4d566-247">In those cases, the Desktop Window Manager (DWM) will downconvert your content to fit the display's capabilities.</span></span> <span data-ttu-id="4d566-248">В Windows 10 версии 1903 и более поздних выводятся вырезание чисел. Например, если вы готовитесь к просмотру в цепочке FP16 scRGB, то все, что находится за пределами числового диапазона [0, 1], обрезается.</span><span class="sxs-lookup"><span data-stu-id="4d566-248">In Windows 10, version 1903, and later, it will perform numeric clipping; for example, if you render to an FP16 scRGB swap chain, then everything outside of the [0, 1] numeric range is clipped.</span></span>

<span data-ttu-id="4d566-249">Это поведение довнконверсион также возникает, если окно приложения находится на двух или более экранах с различными расширенными возможностями цвета.</span><span class="sxs-lookup"><span data-stu-id="4d566-249">This downconversion behavior will also occur if your app window is straddling two or more displays with differing advanced color capabilities.</span></span> <span data-ttu-id="4d566-250">**Адванцедколоринфо** и **IDXGIOutput6** являются абстрактными, чтобы сообщить только о характеристиках экрана "Main" (определенных как дисплей, содержащий центр окна).</span><span class="sxs-lookup"><span data-stu-id="4d566-250">**AdvancedColorInfo** and **IDXGIOutput6** are abstracted to report only the "main" display's characteristics (defined as the display containing the center of the window).</span></span>

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a><span data-ttu-id="4d566-251">Правильная визуализация содержимого SDR с белым уровнем ссылки SDR</span><span class="sxs-lookup"><span data-stu-id="4d566-251">Correctly render SDR content with SDR reference white level</span></span>

<span data-ttu-id="4d566-252">Во многих случаях приложение будет отображать содержимое SDR и HDR. Например, отображение субтитров или элементов управления транспорта в HDR-видео или пользовательского интерфейса в игровой сцене.</span><span class="sxs-lookup"><span data-stu-id="4d566-252">In many scenarios, your app will want to render both SDR and HDR content; for example, rendering subtitles or transport controls over HDR video, or UI into a game scene.</span></span> <span data-ttu-id="4d566-253">Важно понимать концепцию *белого уровня ссылок SDR* , чтобы убедиться, что содержимое SDR выглядит правильно на HDR-дисплее.</span><span class="sxs-lookup"><span data-stu-id="4d566-253">It is important to understand the concept of *SDR reference white level* to ensure that your SDR content looks correct on an HDR display.</span></span>

<span data-ttu-id="4d566-254">Windows рассматривает HDR-содержимое как _упоминаемое_, что означает, что определенное значение цвета должно отображаться на уровне яркости. Например, scRGB (1,0, 1,0, 1,0) и HDR10 (497, 497, 497) кодируются точно D65 белого по 80 НИТС светимости.</span><span class="sxs-lookup"><span data-stu-id="4d566-254">Windows treats HDR content as _scene-referred_, meaning that a particular color value should be displayed at a specific luminance level; for example, scRGB (1.0, 1.0, 1.0) and HDR10 (497, 497, 497) both encode exactly D65 white at 80 nits luminance.</span></span> <span data-ttu-id="4d566-255">В то же время, содержимое SDR обычно _выводится_ на экран (или отображается на экране), что означает, что его светимость остается для пользователя или устройства. Например, sRGB (1,0, 1,0, 1,0) кодирует белый D65 как в HDR-примерах, но с любой максимальной яркостью, для которой настроено отображение.</span><span class="sxs-lookup"><span data-stu-id="4d566-255">Meanwhile, SDR content traditionally has been _output-referred_ (or display-referred), meaning that its luminance is left up to the user or the device; for example sRGB (1.0, 1.0, 1.0) encodes D65 white as in the HDR examples, but at whatever maximum luminance the display is configured for.</span></span> <span data-ttu-id="4d566-256">Windows позволяет пользователю изменить _уровень ссылки SDR на белый_ по своему усмотрению. Это светимость, которую Windows будет отображать sRGB (1,0, 1,0, 1,0) по адресу.</span><span class="sxs-lookup"><span data-stu-id="4d566-256">Windows allows the user to adjust the _SDR reference white level_ to their preference; this is the luminance that Windows will render sRGB (1.0, 1.0, 1.0) at.</span></span> <span data-ttu-id="4d566-257">На настольных мониторах в режиме HDR ссылки на уровне ссылок SDR обычно устанавливаются в около 200 НИТС.</span><span class="sxs-lookup"><span data-stu-id="4d566-257">On desktop HDR monitors, SDR reference white levels are typically set to around 200 nits.</span></span>

> [!Note]
> <span data-ttu-id="4d566-258">На дисплее, поддерживающем управление яркостью, например на ноутбуке, Windows также регулирует светимость содержимого HDR (на основе сцены), чтобы соответствовать желаемому уровню яркости пользователя, но это невидимо для приложения.</span><span class="sxs-lookup"><span data-stu-id="4d566-258">On a display that supports a brightness control, such as on a laptop, Windows will also adjust the luminance of HDR (scene-referred) content to match the user's desired brightness level, but this is invisible to the app.</span></span> <span data-ttu-id="4d566-259">Если вы не пытаетесь гарантировать точное воспроизведение сигнала HDR, вы можете игнорировать это.</span><span class="sxs-lookup"><span data-stu-id="4d566-259">Unless you're trying to guarantee bit-accurate reproduction of the HDR signal, you can generally ignore this.</span></span>

<span data-ttu-id="4d566-260">Если приложение всегда отображает SDR и HDR в отдельных поверхностях и использует композицию ОС, Windows автоматически выполнит правильную корректировку для увеличения содержимого SDR до нужного белого уровня.</span><span class="sxs-lookup"><span data-stu-id="4d566-260">If your app always renders SDR and HDR to separate surfaces, and relies on OS composition, then Windows will automatically perform the correct adjustment to boost SDR content to the desired white level.</span></span> <span data-ttu-id="4d566-261">Например, если приложение использует XAML и Преобразовывает содержимое HDR в собственный **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="4d566-261">For example, if your app uses XAML and renders HDR content to its own **SwapChainPanel**.</span></span>

<span data-ttu-id="4d566-262">Однако если приложение выполняет собственную композицию SDR и HDR-содержимого в одну поверхность, вы несете ответственность за выполнение корректировки белого уровня на уровне SDR.</span><span class="sxs-lookup"><span data-stu-id="4d566-262">However, if your app performs its own composition of SDR and HDR content into a single surface, then you're responsible for performing the SDR reference white level adjustment yourself.</span></span> <span data-ttu-id="4d566-263">В противном случае содержимое SDR может показаться слишком темным, предполагая типичные условия просмотра рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="4d566-263">Otherwise the SDR content might appear too dim assuming typical desktop viewing conditions.</span></span> <span data-ttu-id="4d566-264">Сначала необходимо получить текущий белый уровень ссылки SDR, а затем изменить значения цвета для любого содержимого SDR, которое вы готовите к просмотру.</span><span class="sxs-lookup"><span data-stu-id="4d566-264">First, you must obtain the current SDR reference white level, and then you must adjust the color values of any SDR content you're rendering.</span></span>

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a><span data-ttu-id="4d566-265">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="4d566-265">Step 1.</span></span> <span data-ttu-id="4d566-266">Получение белого уровня ссылки на текущий контрольное значение SDR</span><span class="sxs-lookup"><span data-stu-id="4d566-266">Obtain the current SDR reference white level</span></span>

<span data-ttu-id="4d566-267">Сейчас только приложения UWP могут получить текущий белый уровень ссылки SDR через [**адванцедколоринфо. сдрвхителевелиннитс**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span><span class="sxs-lookup"><span data-stu-id="4d566-267">Currently, only UWP apps can obtain the current SDR reference white level via [**AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span></span> <span data-ttu-id="4d566-268">Для этого API требуется [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="4d566-268">This API requires a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

### <a name="step-2-adjust-color-values-of-sdr-content"></a><span data-ttu-id="4d566-269">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="4d566-269">Step 2.</span></span> <span data-ttu-id="4d566-270">Настройка цветовых значений SDR Content</span><span class="sxs-lookup"><span data-stu-id="4d566-270">Adjust color values of SDR content</span></span>

<span data-ttu-id="4d566-271">Windows определяет номинальный или используемый по умолчанию белый уровень ссылок в 80 НИТС; Поэтому, если бы в цепочке FP16 swap отображалось стандартное значение sRGB (1,0, 1,0, 1,0), оно будет воссоздано при 80 НИТС светимости.</span><span class="sxs-lookup"><span data-stu-id="4d566-271">Windows defines the nominal, or default, reference white level at 80 nits; therefore if you were to render a standard sRGB (1.0, 1.0, 1.0) white to an FP16 swap chain, it would be reproduced at 80 nits luminance.</span></span> <span data-ttu-id="4d566-272">Чтобы обеспечить соответствие фактического уровня ссылки, определяемого пользователем, необходимо настроить содержимое SDR с 80 НИТС на уровень, указанный с помощью **адванцедколоринфо. сдрвхителевелиннитс**.</span><span class="sxs-lookup"><span data-stu-id="4d566-272">In order to match the actual user-defined reference white level, you must adjust SDR content from 80 nits to the level specified via **AdvancedColorInfo.SdrWhiteLevelInNits**.</span></span>

<span data-ttu-id="4d566-273">При отрисовке с использованием FP16 и ScRGB или любого цветового пространства, которое использует линейную гамму (1,0), можно просто умножить значение цвета SDR на _адванцедколоринфо. сдрвхителевелиннитс_  /  _80_.</span><span class="sxs-lookup"><span data-stu-id="4d566-273">If you're rendering using FP16 and scRGB, or any color space that uses linear (1.0) gamma, then you can simply multiply the SDR color value by _AdvancedColorInfo.SdrWhiteLevelInNits_ / _80_.</span></span> <span data-ttu-id="4d566-274">Если вы используете Direct2D, то существует предопределенная константа [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), которая имеет значение 80.</span><span class="sxs-lookup"><span data-stu-id="4d566-274">If you're using Direct2D, there is a predefined constant [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), which has a value of 80.</span></span>

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

<span data-ttu-id="4d566-275">При отрисовке с использованием нелинейного цветового пространства, такого как HDR10, выполнение корректировки белого уровня SDR более сложно; При написании собственного шейдера пикселей следует рассмотреть возможность преобразования в линейную гамму для применения коррекции.</span><span class="sxs-lookup"><span data-stu-id="4d566-275">If you're rendering using a nonlinear gamma color space such as HDR10, then performing SDR white level adjustment is more complex; if you're writing your own pixel shader you should consider converting into linear gamma to apply the adjustment.</span></span>

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a><span data-ttu-id="4d566-276">Адаптация HDR-содержимого к возможностям дисплея с помощью тонемаппинг</span><span class="sxs-lookup"><span data-stu-id="4d566-276">Adapt HDR content to the display's capabilities using tonemapping</span></span>

<span data-ttu-id="4d566-277">HDR и дополнительные цвета могут сильно различаться с точки зрения их возможностей.</span><span class="sxs-lookup"><span data-stu-id="4d566-277">HDR and advanced color displays vary greatly in terms of their capabilities.</span></span> <span data-ttu-id="4d566-278">Например, минимальная и максимальная светимость и цветовой охват, которые они могут воссоздавать.</span><span class="sxs-lookup"><span data-stu-id="4d566-278">For example, the minimum and maximum luminance and the color gamut they are capable of reproducing.</span></span> <span data-ttu-id="4d566-279">Во многих случаях содержимое HDR будет содержать цвета, превышающие возможности экрана.</span><span class="sxs-lookup"><span data-stu-id="4d566-279">In many cases, your HDR content will contain colors that exceed the display's capabilities.</span></span> <span data-ttu-id="4d566-280">Для наилучшего качества изображения это важно для выполнения тонемаппинг HDR, по сути сжимают диапазон цветов в соответствии с отображением, позволяя лучше сохранить визуальную цель содержимого.</span><span class="sxs-lookup"><span data-stu-id="4d566-280">For the best image quality it is important for you to perform HDR tonemapping, essentially compressing the range of colors to fit the display while best preserving the visual intent of the content.</span></span>

<span data-ttu-id="4d566-281">Самым важным единственным параметром, который следует адаптировать для, является максимальная светимость, также известная как Максклл (уровень содержимого Light); более сложные тонемапперс также адаптируют минимальные светимости (Минклл) и (или) цветовые первичные цвета.</span><span class="sxs-lookup"><span data-stu-id="4d566-281">The most important single parameter to adapt for is max luminance, also known as MaxCLL (content light level); more sophisticated tonemappers will also adapt min luminance (MinCLL) and/or color primaries.</span></span>

### <a name="step-1-get-the-displays-color-volume-capabilities"></a><span data-ttu-id="4d566-282">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="4d566-282">Step 1.</span></span> <span data-ttu-id="4d566-283">Получить возможности цветового тома экрана</span><span class="sxs-lookup"><span data-stu-id="4d566-283">Get the display's color volume capabilities</span></span>

#### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="4d566-284">Приложения универсальной платформы Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="4d566-284">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="4d566-285">Используйте [**адванцедколоринфо**](/uwp/api/windows.graphics.display.advancedcolorinfo) для получения цветового тома экрана.</span><span class="sxs-lookup"><span data-stu-id="4d566-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get the display's color volume.</span></span>

#### <a name="win32-desktop-directx-apps"></a><span data-ttu-id="4d566-286">Приложения DirectX (для настольных систем)</span><span class="sxs-lookup"><span data-stu-id="4d566-286">Win32 (desktop) DirectX apps</span></span>

<span data-ttu-id="4d566-287">Для получения цветового тома экрана используйте [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) .</span><span class="sxs-lookup"><span data-stu-id="4d566-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get the display's color volume.</span></span>

### <a name="step-2-get-the-contents-color-volume-information"></a><span data-ttu-id="4d566-288">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="4d566-288">Step 2.</span></span> <span data-ttu-id="4d566-289">Получение сведений о цветовых томах содержимого</span><span class="sxs-lookup"><span data-stu-id="4d566-289">Get the content's color volume information</span></span>

<span data-ttu-id="4d566-290">В зависимости от того, откуда поступило HDR-содержимое, существует несколько потенциальных способов определить его светимость и цветовую палитру.</span><span class="sxs-lookup"><span data-stu-id="4d566-290">Depending on where your HDR content came from, there are multiple potential ways to determine its luminance and color gamut information.</span></span> <span data-ttu-id="4d566-291">В определенных HDR-видео и файлах изображений содержатся метаданные SMPTE ST. 2086.</span><span class="sxs-lookup"><span data-stu-id="4d566-291">Certain HDR video and image files contain SMPTE ST.2086 metadata.</span></span> <span data-ttu-id="4d566-292">Если содержимое было подготовлено к просмотру динамически, возможно, вы сможете извлечь сведения о сцене из внутренних стадий отрисовки, например самый светлый источник освещения в сцене.</span><span class="sxs-lookup"><span data-stu-id="4d566-292">If your content was rendered dynamically, then you may be able to extract scene information from the internal rendering stages, for example the brightest light source in a scene.</span></span>

<span data-ttu-id="4d566-293">Более общим, но дорогостоящим решением является выполнение гистограммы или другого этапа анализа для отображаемого кадра.</span><span class="sxs-lookup"><span data-stu-id="4d566-293">A more general but computationally expensive solution is to run a histogram or other analysis pass on the rendered frame.</span></span> <span data-ttu-id="4d566-294">В [примере пакета SDK Direct2D Advanced Color Images](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) показано, как это сделать с помощью Direct2D. Ниже приведены наиболее подходящие фрагменты кода.</span><span class="sxs-lookup"><span data-stu-id="4d566-294">The [Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstrates how to do this using Direct2D; the most relevant code snippets are included below:</span></span>

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a><span data-ttu-id="4d566-295">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="4d566-295">Step 3.</span></span> <span data-ttu-id="4d566-296">Выполнение операции HDR тонемаппинг</span><span class="sxs-lookup"><span data-stu-id="4d566-296">Perform the HDR tonemapping operation</span></span>

<span data-ttu-id="4d566-297">Тонемаппинг по своей природе является процессом потери данных и может быть оптимизирован для ряда искусственного или объективных метрик, поэтому нет ни одного стандартного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="4d566-297">Tonemapping is inherently a lossy process, and can be optimized for a number of perceptual or objective metrics, so there is no one standard algorithm.</span></span> <span data-ttu-id="4d566-298">Windows предоставляет встроенный [тонемапперный результат HDR](../direct2d/hdr-tone-map-effect.md) в составе Direct2D, а также в конвейере воспроизведения видео Media Foundation HDR.</span><span class="sxs-lookup"><span data-stu-id="4d566-298">Windows provides a built-in [HDR tonemapper effect](../direct2d/hdr-tone-map-effect.md) as part of Direct2D as well as in the Media Foundation HDR video playback pipeline.</span></span> <span data-ttu-id="4d566-299">Некоторые другие часто используемые алгоритмы включают в себя элементы управления "пленка", "Реинхард" и ITU-R BT. 2390-3 ИТФ (функция электрической электрической пересылки).</span><span class="sxs-lookup"><span data-stu-id="4d566-299">Some other commonly used algorithms include ACES Filmic, Reinhard, and ITU-R BT.2390-3 EETF (electrical-electrical transfer function).</span></span>

<span data-ttu-id="4d566-300">Ниже показан упрощенный оператор Реинхард тонемаппер.</span><span class="sxs-lookup"><span data-stu-id="4d566-300">A simplified Reinhard tonemapper operator is shown below.</span></span>

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a><span data-ttu-id="4d566-301">Запись содержимого HDR и ВКГ</span><span class="sxs-lookup"><span data-stu-id="4d566-301">Capturing HDR and WCG content</span></span>

<span data-ttu-id="4d566-302">Интерфейсы API, которые поддерживают указание форматов пикселей, например, в пространстве имен [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) и метод [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , предоставляют возможность захвата содержимого HDR и ВКГ без потери сведений о точках.</span><span class="sxs-lookup"><span data-stu-id="4d566-302">APIs that support specifying pixel formats, such as those in the [**Windows.Graphics.Capture**](/uwp/api/windows.graphics.capture) namespace, and the [**IDXGIOutput5::DuplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) method, provide the capability to capture HDR and WCG content without losing pixel information.</span></span> <span data-ttu-id="4d566-303">Обратите внимание, что после получения кадров содержимого требуется дополнительная обработка.</span><span class="sxs-lookup"><span data-stu-id="4d566-303">Note that after acquiring content frames, additional processing is required.</span></span> <span data-ttu-id="4d566-304">Например, сопоставление тонов HDR-to-SDR (например, снимок экрана SDR для общего доступа к Интернету) и сохранение содержимого в правильном формате (например, JPEG XR).</span><span class="sxs-lookup"><span data-stu-id="4d566-304">For example, HDR-to-SDR tone mapping (for example, SDR screenshot copy for Internet sharing) and content saving with proper format (for example, JPEG XR).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d566-305">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d566-305">Additional resources</span></span>

* <span data-ttu-id="4d566-306">*Использование визуализации HDR с набором средств DirectX* для DirectX [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span><span class="sxs-lookup"><span data-stu-id="4d566-306">*Using HDR Rendering with the DirectX Tool Kit* for [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering) / [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span></span> <span data-ttu-id="4d566-307">Пошаговое руководство по добавлению поддержки HDR в приложение DirectX с помощью набора средств DirectX (Директкстк).</span><span class="sxs-lookup"><span data-stu-id="4d566-307">Walkthrough of how to add HDR support to a DirectX app using the DirectX Tool Kit (DirectXTK).</span></span>
* <span data-ttu-id="4d566-308">[Пример пакета SDK для расширенных цветовых изображений Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span><span class="sxs-lookup"><span data-stu-id="4d566-308">[Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span></span> <span data-ttu-id="4d566-309">Пример пакета SDK для UWP, который реализует расширенное средство просмотра изображений HDR и ВКГ с поддержкой цветов с помощью Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4d566-309">UWP SDK sample implementing an advanced color-aware HDR and WCG image viewer using Direct2D.</span></span> <span data-ttu-id="4d566-310">Демонстрирует полный спектр рекомендаций для приложений UWP, включая реагирование на изменения возможностей дисплея и настройку для белого уровня SDR.</span><span class="sxs-lookup"><span data-stu-id="4d566-310">Demonstrates the full range of best practices for UWP apps, including responding to display capability changes and adjusting for SDR white level.</span></span>
* <span data-ttu-id="4d566-311">[Пример Direct3D 12 для рабочего стола HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="4d566-311">[Direct3D 12 HDR desktop sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span> <span data-ttu-id="4d566-312">Пример пакета SDK для Desktop реализует базовую сцену HDR с Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="4d566-312">Desktop SDK sample implementing a basic Direct3D 12 HDR scene.</span></span>
* <span data-ttu-id="4d566-313">[Пример HDR UWP для Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="4d566-313">[Direct3D 12 HDR UWP sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span></span> <span data-ttu-id="4d566-314">Набор UWP, эквивалентный приведенному выше примеру.</span><span class="sxs-lookup"><span data-stu-id="4d566-314">UWP equivalent of the above sample.</span></span>
* <span data-ttu-id="4d566-315">[Пример для Xbox АТГ СИМПЛЕХДР PC](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span><span class="sxs-lookup"><span data-stu-id="4d566-315">[Xbox ATG SimpleHDR PC sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span></span> <span data-ttu-id="4d566-316">Пример пакета SDK для Desktop, реализующий базовую сцену HDR с Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="4d566-316">Desktop SDK sample implementing a basic Direct3D 11 HDR scene.</span></span>
