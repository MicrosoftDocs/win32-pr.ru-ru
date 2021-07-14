---
title: Общие сведения о DWriteCore
description: двритекоре — это DirectWrite реализация пакета SDK для приложений Windows.
keywords:
- DirectWrite Центральный
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 644ce3c5715e1cc57129b36047169c20e80a6697
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689197"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="afcba-105">Общие сведения о DWriteCore</span><span class="sxs-lookup"><span data-stu-id="afcba-105">DWriteCore overview</span></span>

<span data-ttu-id="afcba-106">двритекоре — это [Windows реализация пакета SDK для приложений](/windows/apps/windows-app-sdk/) [DirectWrite](./direct-write-portal.md) (DirectWrite является API DirectX для высококачественной отрисовки текста, независимыми от разрешения шрифтов, а также полной поддержкой текста и макета в юникоде).</span><span class="sxs-lookup"><span data-stu-id="afcba-106">DWriteCore is the [Windows App SDK](/windows/apps/windows-app-sdk/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="afcba-107">двритекоре — это форма DirectWrite, которая работает в версиях Windows Windows 10, версия 1809 (10,0; Сборка 17763) и открывает дверцу для использования кросс-платформенной платформы.</span><span class="sxs-lookup"><span data-stu-id="afcba-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 10, version 1809 (10.0; Build 17763), and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="afcba-108">В этом вводном разделе описывается, что такое Двритекоре, и показано, как установить его в среду разработки и программировать вместе с ней.</span><span class="sxs-lookup"><span data-stu-id="afcba-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

> [!TIP]
> <span data-ttu-id="afcba-109">Описание и ссылки на компоненты DirectX в активной разработке см. на [странице размещения DirectX](https://devblogs.microsoft.com/directx/landing-page/)в записи блога.</span><span class="sxs-lookup"><span data-stu-id="afcba-109">For descriptions of and links to DirectX components in active development, see the blog post [DirectX Landing Page](https://devblogs.microsoft.com/directx/landing-page/).</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="afcba-110">Ценность Двритекоре</span><span class="sxs-lookup"><span data-stu-id="afcba-110">The value proposition of DWriteCore</span></span>

<span data-ttu-id="afcba-111">сам по себе [DirectWrite](./direct-write-portal.md) поддерживает обширный набор функций, который делает его средством визуализации шрифтов, которое выбирается в Windows для большинства приложений, &mdash; будь это через прямые вызовы или через [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="afcba-111">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="afcba-112">DirectWrite содержит независимую от устройства систему разметки текста, высококачественную подсистему [Microsoft ClearType](/typography/cleartype/) text rendering, текст с аппаратным ускорением, многоформатный текст, расширенные функции оформления [OpenType®](/typography/opentype/) , языковую поддержку и макет и отрисовку, совместимые с [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="afcba-112">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="afcba-113">DirectWrite был доступен с момента выпуска Windows Vista с пакетом обновления 2 (SP2), а также в течение нескольких лет, чтобы включить более сложные функции, такие как переменные шрифты, позволяющие применять стили, веса и другие атрибуты к шрифту с одним ресурсом шрифта.</span><span class="sxs-lookup"><span data-stu-id="afcba-113">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="afcba-114">однако из-за длительного времени существования DirectWrite в разработке были внесены старые версии Windows.</span><span class="sxs-lookup"><span data-stu-id="afcba-114">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="afcba-115">кроме того, состояние DirectWrite в качестве технологии отрисовки текста уровня premier ограничено только Windows, то есть межплатформенные приложения должны либо писать собственный стек для отрисовки текста, либо полагаться на сторонние решения.</span><span class="sxs-lookup"><span data-stu-id="afcba-115">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="afcba-116">Двритекоре решает фундаментальные проблемы, связанные с признаком версии и межплатформенной совместимостью, удаляя библиотеку из системы и нацеливание на все возможные Поддерживаемые конечные точки.</span><span class="sxs-lookup"><span data-stu-id="afcba-116">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="afcba-117">для этого мы интегрированы двритекоре в пакет SDK для приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="afcba-117">To that end, we've integrated DWriteCore into Windows App SDK.</span></span>

<span data-ttu-id="afcba-118">основное значение, которое двритекоре предоставляет разработчику в качестве разработчика в пакете SDK для приложений Windows, заключается в том, что он предоставляет доступ ко многим (и, в конечном итоге, всем) DirectWrite функциям.</span><span class="sxs-lookup"><span data-stu-id="afcba-118">The primary value that DWriteCore gives you, as a developer, in Windows App SDK is that it provides access to many (and eventually all) DirectWrite features.</span></span> <span data-ttu-id="afcba-119">Все функции Двритекоре будут работать одинаково во всех версиях нижнего уровня без какого-либо нарушения связи с тем, какие функции могут работать с этими версиями.</span><span class="sxs-lookup"><span data-stu-id="afcba-119">All features of DWriteCore will function the same on all down-level versions without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="afcba-120">Демонстрационное приложение Двритекоре &mdash; двритекорегаллери</span><span class="sxs-lookup"><span data-stu-id="afcba-120">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="afcba-121">Двритекоре демонстрируется в примере приложения [двритекорегаллери](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) , которое доступно для загрузки и изучения.</span><span class="sxs-lookup"><span data-stu-id="afcba-121">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="afcba-122">Начало работы с Двритекоре</span><span class="sxs-lookup"><span data-stu-id="afcba-122">Get started with DWriteCore</span></span>

<span data-ttu-id="afcba-123">двритекоре входит в состав [пакета SDK для приложений Windows 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span><span class="sxs-lookup"><span data-stu-id="afcba-123">DWriteCore is part of [Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span></span> <span data-ttu-id="afcba-124">В этом разделе описывается настройка среды разработки для программирования с помощью Двритекоре.</span><span class="sxs-lookup"><span data-stu-id="afcba-124">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-windows-app-sdk-08-vsix"></a><span data-ttu-id="afcba-125">установка пакета SDK для Windows приложений 0,8 VSIX</span><span class="sxs-lookup"><span data-stu-id="afcba-125">Install the Windows App SDK 0.8 VSIX</span></span>

<span data-ttu-id="afcba-126">в Visual Studio щелкните **расширения**  >  **управление расширениями**, найдите *пакет sdk для Windows приложений* и скачайте расширение пакета sdk для приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="afcba-126">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Windows App SDK*, and download the Windows App SDK extension.</span></span> <span data-ttu-id="afcba-127">закройте и снова откройте Visual Studio и следуйте инструкциям по установке расширения.</span><span class="sxs-lookup"><span data-stu-id="afcba-127">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="afcba-128">дополнительные сведения см. в разделе [Windows пакет SDK для приложений 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) и [настройка среды разработки](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="afcba-128">For more info, see [Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) and [Set up your development environment](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="afcba-129">Создание нового проекта</span><span class="sxs-lookup"><span data-stu-id="afcba-129">Create a new project</span></span>

<span data-ttu-id="afcba-130">в Visual Studio создайте новый проект из шаблона проекта **пустое приложение, упакованное (винуи 3 в рабочем столе)** .</span><span class="sxs-lookup"><span data-stu-id="afcba-130">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="afcba-131">Чтобы найти шаблон проекта, выберите язык: *C++*. platform: *пакет SDK для Windows приложений*; Тип проекта: *Рабочий стол*.</span><span class="sxs-lookup"><span data-stu-id="afcba-131">You can find that project template by choosing language: *C++*; platform: *Windows App SDK*; project type: *Desktop*.</span></span>

<span data-ttu-id="afcba-132">дополнительные сведения см. в разделе [шаблоны Project для винуи 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span><span class="sxs-lookup"><span data-stu-id="afcba-132">For more info, see [Project templates for WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="afcba-133">установка пакета NuGet Microsoft. прожектреунион. дврите</span><span class="sxs-lookup"><span data-stu-id="afcba-133">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="afcba-134">в Visual Studio щелкните **Project** \> **управление пакетами NuGet...** \> **обзор**, введите или вставьте **Microsoft. прожектреунион. дврите** в поле поиска, выберите элемент в результатах поиска, а затем нажмите кнопку **установить** , чтобы установить пакет для этого проекта.</span><span class="sxs-lookup"><span data-stu-id="afcba-134">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="afcba-135">Кроме того, начнем с примера приложения Двритекорегаллери.</span><span class="sxs-lookup"><span data-stu-id="afcba-135">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="afcba-136">Кроме того, можно программировать с помощью Двритекоре, начиная с проекта примера приложения [двритекорегаллери](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) , и основывать разработку на этом проекте.</span><span class="sxs-lookup"><span data-stu-id="afcba-136">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) sample app project, and base your development on that project.</span></span> <span data-ttu-id="afcba-137">После этого можно удалить любой существующий исходный код (или файлы) из этого примера проекта, а также добавить в проект новый исходный код (или файлы).</span><span class="sxs-lookup"><span data-stu-id="afcba-137">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="afcba-138">Использование Двритекоре в проекте</span><span class="sxs-lookup"><span data-stu-id="afcba-138">Use DWriteCore in your project</span></span>

<span data-ttu-id="afcba-139">Дополнительные сведения о программировании с помощью Двритекоре см. в подразделе [программирование с помощью двритекоре](#programming-with-dwritecore) далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="afcba-139">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="afcba-140">Фазы выпуска Двритекоре</span><span class="sxs-lookup"><span data-stu-id="afcba-140">The release phases of DWriteCore</span></span>

<span data-ttu-id="afcba-141">перенос DirectWrite в двритекоре — достаточно большой проект, охватывающий несколько Windows циклов выпусков.</span><span class="sxs-lookup"><span data-stu-id="afcba-141">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="afcba-142">Этот проект делится на этапы, каждый из которых соответствует блоку функциональности, предоставленному в выпуске.</span><span class="sxs-lookup"><span data-stu-id="afcba-142">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="afcba-143">Функции в текущем выпуске Двритекоре</span><span class="sxs-lookup"><span data-stu-id="afcba-143">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="afcba-144">версия двритекоре, доступная в настоящее время, входит в состав [пакета SDK для приложений Windows 0,8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span><span class="sxs-lookup"><span data-stu-id="afcba-144">The version of DWriteCore currently available is part of [Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span></span> <span data-ttu-id="afcba-145">Он содержит основные инструменты, которые вы, как разработчик, должны использовать Двритекоре, включая следующие функции.</span><span class="sxs-lookup"><span data-stu-id="afcba-145">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="afcba-146">Перечисление шрифтов.</span><span class="sxs-lookup"><span data-stu-id="afcba-146">Font enumeration.</span></span>
- <span data-ttu-id="afcba-147">API шрифтов.</span><span class="sxs-lookup"><span data-stu-id="afcba-147">Font API.</span></span>
- <span data-ttu-id="afcba-148">Упростить.</span><span class="sxs-lookup"><span data-stu-id="afcba-148">Shaping.</span></span>
- <span data-ttu-id="afcba-149">API-интерфейсы низкого уровня отрисовки.</span><span class="sxs-lookup"><span data-stu-id="afcba-149">Low-level rendering APIs.</span></span> <span data-ttu-id="afcba-150">Это частично на текущем этапе &mdash; двритекоре не взаимодействуют с [Direct2D](../direct2d/direct2d-portal.md), но можно использовать [**идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) и [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="afcba-150">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="afcba-151">Основные функции макета текста.</span><span class="sxs-lookup"><span data-stu-id="afcba-151">Basic text layout functionality.</span></span>
- <span data-ttu-id="afcba-152">Интерфейсы API отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="afcba-152">Text-rendering APIs.</span></span>
- <span data-ttu-id="afcba-153">Целевой объект прорисовки битовой карты.</span><span class="sxs-lookup"><span data-stu-id="afcba-153">Bitmap render target.</span></span>
- <span data-ttu-id="afcba-154">Цветовые шрифты.</span><span class="sxs-lookup"><span data-stu-id="afcba-154">Color fonts.</span></span>
- <span data-ttu-id="afcba-155">Различные оптимизации (очистка кэша шрифта, загрузчик шрифтов в памяти и т. д.).</span><span class="sxs-lookup"><span data-stu-id="afcba-155">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>
- <span data-ttu-id="afcba-156">Поддержка подчеркивания &mdash; см. в разделе [**идвритетекстлайаут:: Черкивания**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) и [**идвритетекстлайаут:: сетундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline).</span><span class="sxs-lookup"><span data-stu-id="afcba-156">Support for underline&mdash;see [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) and [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline).</span></span>
- <span data-ttu-id="afcba-157">Поддержка зачеркнутый &mdash; см. в разделе [**идвритетекстлайаут:: зачеркнуть**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough) и [**идвритетекстлайаут:: сетстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough).</span><span class="sxs-lookup"><span data-stu-id="afcba-157">Support for strikethrough&mdash;see [**IDWriteTextLayout::GetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough) and [**IDWriteTextLayout::SetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough).</span></span>
- <span data-ttu-id="afcba-158">Поддержка вертикального текста с помощью [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) &mdash; см. в разделе [вертикальный текст](/windows/win32/directwrite/vertical-text).</span><span class="sxs-lookup"><span data-stu-id="afcba-158">Support for vertical text via [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)&mdash;see [Vertical text](/windows/win32/directwrite/vertical-text).</span></span>
- <span data-ttu-id="afcba-159">Реализуются все методы интерфейсов [**идвритетекстанализер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) и [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) .</span><span class="sxs-lookup"><span data-stu-id="afcba-159">All of the methods of the [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) and [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) interfaces are implemented.</span></span>

<span data-ttu-id="afcba-160">Баннер — это цветовые шрифты.</span><span class="sxs-lookup"><span data-stu-id="afcba-160">A banner feature is color fonts.</span></span> <span data-ttu-id="afcba-161">Цветовые шрифты позволяют отображать шрифты с более сложными цветовыми возможностями, чем простые одиночные цвета.</span><span class="sxs-lookup"><span data-stu-id="afcba-161">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="afcba-162">например, цветовые шрифты заключаются в возможности отображения шрифтов эмодзи и значков панели инструментов (второй из которых используется Office, например).</span><span class="sxs-lookup"><span data-stu-id="afcba-162">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="afcba-163">цветовые шрифты впервые появились в Windows 8.1, но функция была значительно расширена в Windows 10, версии 1607 (годовщина обновления).</span><span class="sxs-lookup"><span data-stu-id="afcba-163">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="afcba-164">Работа по очистке кэша шрифтов и загрузчику шрифтов в памяти позволяет ускорить загрузку шрифтов и улучшения памяти.</span><span class="sxs-lookup"><span data-stu-id="afcba-164">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="afcba-165">с помощью этих функций можно сразу приступить к работе с некоторыми современными основными функциями DirectWrite, &mdash; такими как переменные шрифты.</span><span class="sxs-lookup"><span data-stu-id="afcba-165">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts.</span></span> <span data-ttu-id="afcba-166">переменные шрифты являются одной из наиболее важных функций для DirectWrite клиентов.</span><span class="sxs-lookup"><span data-stu-id="afcba-166">Variable fonts are one of the most important features for DirectWrite customers.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="afcba-167">наше приглашение в качестве разработчика DirectWrite</span><span class="sxs-lookup"><span data-stu-id="afcba-167">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="afcba-168">двритекоре, а также другие компоненты пакета SDK для приложений Windows, будут разработаны с открытой откликом для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="afcba-168">DWriteCore, along with other Windows App SDK components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="afcba-169">мы приглашаем вас начать исследование двритекоре, а также предоставить ценные сведения или запросы на разработку функций в [GitHub репозитории пакета SDK для приложений Windows](https://github.com/microsoft/ProjectReunion/).</span><span class="sxs-lookup"><span data-stu-id="afcba-169">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Windows App SDK GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="afcba-170">Программирование с помощью Двритекоре</span><span class="sxs-lookup"><span data-stu-id="afcba-170">Programming with DWriteCore</span></span>

<span data-ttu-id="afcba-171">как и в случае с [DirectWrite](./direct-write-portal.md), вы двритекоре с помощью API-интерфейса COM через интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="afcba-171">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="afcba-172">Чтобы использовать Двритекоре, необходимо включить `dwrite_core.h` заголовочный файл.</span><span class="sxs-lookup"><span data-stu-id="afcba-172">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="afcba-173">`dwrite_core.h`Сначала файл заголовка определяет маркер *DWRITE_CORE*, а затем включает `dwrite_3.h` файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="afcba-173">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="afcba-174">маркер *DWRITE_CORE* важен, так как он направляет все последующие включенные заголовки, чтобы сделать доступными все DirectWrite api.</span><span class="sxs-lookup"><span data-stu-id="afcba-174">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="afcba-175">После включения проекта `dwrite_core.h` можно выполнить написание кода, сборку и запуск.</span><span class="sxs-lookup"><span data-stu-id="afcba-175">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="afcba-176">Новые или разные API для Двритекоре</span><span class="sxs-lookup"><span data-stu-id="afcba-176">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="afcba-177">Поверхность API Двритекоре в основном такая же, как и для [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="afcba-177">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="afcba-178">Но существует небольшое количество новых API, которые доступны только в Двритекоре.</span><span class="sxs-lookup"><span data-stu-id="afcba-178">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="afcba-179">Создание объекта фабрики</span><span class="sxs-lookup"><span data-stu-id="afcba-179">Create a factory object</span></span>

<span data-ttu-id="afcba-180">Функция [**двритекорекреатефактори**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) Free создает объект фабрики, который используется для последующего создания отдельных объектов двритекоре.</span><span class="sxs-lookup"><span data-stu-id="afcba-180">The [**DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="afcba-181">**Двритекорекреатефактори** функционирует так же, как функция [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , экспортируемая системной версией DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="afcba-181">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="afcba-182">Функция Двритекоре имеет другое имя, чтобы избежать неоднозначности.</span><span class="sxs-lookup"><span data-stu-id="afcba-182">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="afcba-183">Создание объекта ограниченной фабрики</span><span class="sxs-lookup"><span data-stu-id="afcba-183">Create a restricted factory object</span></span>

<span data-ttu-id="afcba-184">Перечисление [**DWRITE_FACTORY_TYPE**](/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type) содержит новую константную &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, обозначающую ограниченную фабрику.</span><span class="sxs-lookup"><span data-stu-id="afcba-184">The [**DWRITE_FACTORY_TYPE**](/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="afcba-185">Ограниченная фабрика больше заблокирована, чем изолированная фабрика.</span><span class="sxs-lookup"><span data-stu-id="afcba-185">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="afcba-186">Он не взаимодействует с межпроцессным или постоянным кэшем шрифтов каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="afcba-186">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="afcba-187">Кроме того, системная коллекция шрифтов, возвращаемая из этой фабрики, включает только хорошо известные шрифты.</span><span class="sxs-lookup"><span data-stu-id="afcba-187">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="afcba-188">Ниже показано, как можно использовать **DWRITE_FACTORY_TYPE_ISOLATED2** для создания объекта ограниченной фабрики при вызове функции Free [**двритекорекреатефактори**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="afcba-188">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="afcba-189">при передаче **DWRITE_FACTORY_TYPE_ISOLATED2** в более старую версию DirectWrite, которая не поддерживается, **двритекреатефактори** возвращает **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="afcba-189">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="afcba-190">Рисование глифов в битовой карте системной памяти</span><span class="sxs-lookup"><span data-stu-id="afcba-190">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="afcba-191">DirectWrite имеет целевой интерфейс прорисовки изображения, который поддерживает отображение глифов в битовую карту в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="afcba-191">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="afcba-192">Однако в настоящее время единственный способ получить доступ к базовым данным о пикселях — использовать GDI, поэтому API не может использоваться на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="afcba-192">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="afcba-193">Это легко исправлено, добавив метод для получения данных о точках.</span><span class="sxs-lookup"><span data-stu-id="afcba-193">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="afcba-194">Поэтому Двритекоре вводит интерфейс [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) и его метод [**IDWriteBitmapRenderTarget2::**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata).</span><span class="sxs-lookup"><span data-stu-id="afcba-194">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata).</span></span> <span data-ttu-id="afcba-195">Этот метод принимает параметр типа (указатель на) [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32), который является новой структурой.</span><span class="sxs-lookup"><span data-stu-id="afcba-195">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32), which is a new struct.</span></span>

<span data-ttu-id="afcba-196">Приложение создает целевой объект прорисовки растрового изображения путем вызова [идвритегдиинтероп:: креатебитмапрендертаржет](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="afcba-196">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="afcba-197">в Windows целевой объект отрисовки растрового изображения инкапсулирует контроллер домена памяти gdi с выбранным в нем точечным рисунком gdi (dib).</span><span class="sxs-lookup"><span data-stu-id="afcba-197">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="afcba-198">[Идвритебитмапрендертаржет::D равглифрун](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) преобразует глифы в DIB.</span><span class="sxs-lookup"><span data-stu-id="afcba-198">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="afcba-199">DirectWrite отображает сами глифы без помощи GDI.</span><span class="sxs-lookup"><span data-stu-id="afcba-199">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="afcba-200">Приложение может получить **HDC** из целевого объекта прорисовки растрового изображения и использовать [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) для копирования пикселов в окно **HDC**.</span><span class="sxs-lookup"><span data-stu-id="afcba-200">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="afcba-201">на платформах, отличных от Windows, приложение по-прежнему может создавать целевой объект прорисовки битовой карты, но он просто инкапсулирует массив системной памяти без **HDC** и не имеет DIB.</span><span class="sxs-lookup"><span data-stu-id="afcba-201">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="afcba-202">Без **HDC** для приложения должен быть другим способом получения пикселей точечного рисунка, чтобы он мог скопировать их, или иным образом использовать их.</span><span class="sxs-lookup"><span data-stu-id="afcba-202">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="afcba-203">Даже в Windows, иногда бывает полезно получить фактические данные о пикселях, и мы покажем текущий способ сделать это в приведенном ниже примере кода.</span><span class="sxs-lookup"><span data-stu-id="afcba-203">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="afcba-204">Другие различия API между Двритекоре и DirectWrite</span><span class="sxs-lookup"><span data-stu-id="afcba-204">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="afcba-205">существует несколько интерфейсов api, которые являются заглушками, или они работают несколько иначе на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="afcba-205">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="afcba-206">например, [идвритегдиинтероп:: креатефонтфацефромхдк](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) возвращает **E_NOTIMPL** на платформах, отличных от Windows, так как не существует такого объекта, как **HDC** без [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="afcba-206">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="afcba-207">и, наконец, существуют некоторые другие Windows интерфейсы api, которые обычно используются вместе с DirectWrite (Direct2D является важным примером).</span><span class="sxs-lookup"><span data-stu-id="afcba-207">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="afcba-208">Однако в настоящее время Direct2D и Двритекоре не взаимодействуют.</span><span class="sxs-lookup"><span data-stu-id="afcba-208">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="afcba-209">Например, если создать [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью двритекоре и передать его в [**D2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), то вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="afcba-209">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
