---
title: Общие сведения о DWriteCore
description: Двритекоре — это реализация DirectWrite для Реюньон проекта.
keywords:
- Ядро DirectWrite
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 1ebb85ae2628a2c9abce86e0ce146c0d24828267
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925680"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="d2dca-105">Общие сведения о DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d2dca-105">DWriteCore overview</span></span>

<span data-ttu-id="d2dca-106">Двритекоре — это реализация [DirectWrite](./direct-write-portal.md) для повторного [объединения проектов](/windows/apps/project-reunion/) (DirectWrite — это API DirectX для высококачественной отрисовки текста, независимых от разрешения шрифтов, а также полной поддержки текста и макета в Юникоде).</span><span class="sxs-lookup"><span data-stu-id="d2dca-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="d2dca-107">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="d2dca-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="d2dca-108">В этом вводном разделе описывается, что такое Двритекоре, и показано, как установить его в среду разработки и программировать вместе с ней.</span><span class="sxs-lookup"><span data-stu-id="d2dca-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="d2dca-109">Ценность Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d2dca-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="d2dca-110">Сам по себе [DirectWrite](./direct-write-portal.md) поддерживает обширный набор функций, который делает его средством визуализации шрифтов в Windows для большинства приложений, &mdash; будь это через прямые вызовы или через [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="d2dca-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="d2dca-111">DirectWrite содержит независимую от устройства систему разметки текста, высококачественную подсистему [Microsoft ClearType](/typography/cleartype/) Text Rendering, текст с аппаратным ускорением, многоформатный текст, расширенные функции оформления [OpenType®](/typography/opentype/) , языковую поддержку и макет и отрисовку, совместимые с [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="d2dca-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="d2dca-112">DirectWrite был доступен с момента выпуска пакета обновления 2 (SP2) для Windows Vista и был изменен в течение нескольких лет для включения более сложных функций, таких как переменные шрифты, которые позволяют применять стили, весовые коэффициенты и другие атрибуты к шрифту с одним ресурсом шрифта.</span><span class="sxs-lookup"><span data-stu-id="d2dca-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="d2dca-113">Однако из-за длительного времени существования DirectWrite усовершенствования в разработке приходили бы оставлять старые версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d2dca-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="d2dca-114">Кроме того, состояние DirectWrite в качестве технологии отрисовки текста уровня Premier ограничено только Windows, в результате чего межплатформенные приложения должны либо записывать собственный стек отрисовки текста, либо полагаться на сторонние решения.</span><span class="sxs-lookup"><span data-stu-id="d2dca-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="d2dca-115">Двритекоре решает фундаментальные проблемы, связанные с признаком версии и межплатформенной совместимостью, удаляя библиотеку из системы и нацеливание на все возможные Поддерживаемые конечные точки.</span><span class="sxs-lookup"><span data-stu-id="d2dca-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="d2dca-116">В конце концов, мы интегрированы в проект Двритекоре с общедоступным API, который поддерживается на всех конечных точках Windows до Windows 8, и открывает дверцу для использования кросс-платформенной платформы.</span><span class="sxs-lookup"><span data-stu-id="d2dca-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="d2dca-117">Основное значение, которое Двритекоре предоставляет разработчику в качестве разработчика, — это то, что оно предоставляет доступ ко всем текущим DirectWrite функциям на всех уровнях до Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d2dca-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="d2dca-118">Все функции Двритекоре будут работать одинаково для всех версий нижнего уровня; другими словами, все текущие функции будут работать в Windows 8, 8,1 и всех версиях Windows 10 без каких бы то ни было ошибок, касающихся того, какие функции могут работать с какими версиями.</span><span class="sxs-lookup"><span data-stu-id="d2dca-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="d2dca-119">Демонстрационное приложение Двритекоре &mdash; двритекорегаллери</span><span class="sxs-lookup"><span data-stu-id="d2dca-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="d2dca-120">Двритекоре демонстрируется в примере приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , которое доступно для загрузки и изучения.</span><span class="sxs-lookup"><span data-stu-id="d2dca-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="d2dca-121">Начало работы с Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d2dca-121">Get started with DWriteCore</span></span>

<span data-ttu-id="d2dca-122">Двритекоре является частью [проекта union 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="d2dca-122">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="d2dca-123">В этом разделе описывается настройка среды разработки для программирования с помощью Двритекоре.</span><span class="sxs-lookup"><span data-stu-id="d2dca-123">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="d2dca-124">Установка VSIX 0,5 проекта</span><span class="sxs-lookup"><span data-stu-id="d2dca-124">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="d2dca-125">В Visual Studio щелкните **расширения**  >  **Управление расширениями**, выполните поиск по запросу *объединить в проект* и скачайте расширение Union проекта.</span><span class="sxs-lookup"><span data-stu-id="d2dca-125">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="d2dca-126">Закройте и снова откройте Visual Studio и следуйте инструкциям по установке расширения.</span><span class="sxs-lookup"><span data-stu-id="d2dca-126">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="d2dca-127">Дополнительные сведения см. в разделе [Project реюньон 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)и [Создание настольных приложений Windows с помощью предложения UNION 0,5](/windows/apps/project-reunion/#set-up-your-development-environment).</span><span class="sxs-lookup"><span data-stu-id="d2dca-127">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Build desktop Windows apps with Project Reunion 0.5](/windows/apps/project-reunion/#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="d2dca-128">Создание нового проекта</span><span class="sxs-lookup"><span data-stu-id="d2dca-128">Create a new project</span></span>

<span data-ttu-id="d2dca-129">В Visual Studio создайте новый проект из шаблона проекта " **пустое приложение", упакованное (винуи 3 в рабочем столе)** .</span><span class="sxs-lookup"><span data-stu-id="d2dca-129">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="d2dca-130">Чтобы найти шаблон проекта, выберите язык: *C++*. Платформа: *объединение проектов*; Тип проекта: *Рабочий стол*.</span><span class="sxs-lookup"><span data-stu-id="d2dca-130">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="d2dca-131">Дополнительные сведения см. в разделе [шаблоны проектов для винуи 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span><span class="sxs-lookup"><span data-stu-id="d2dca-131">For more info, see [Project templates for WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="d2dca-132">Установка пакета NuGet Microsoft. Прожектреунион. Дврите</span><span class="sxs-lookup"><span data-stu-id="d2dca-132">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="d2dca-133">В Visual Studio щелкните **проект** \> **Управление пакетами NuGet...** \> **Обзор**, введите или вставьте **Microsoft. прожектреунион. дврите** в поле поиска, выберите элемент в результатах поиска и нажмите кнопку **установить** , чтобы установить пакет для этого проекта.</span><span class="sxs-lookup"><span data-stu-id="d2dca-133">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="d2dca-134">Кроме того, начнем с примера приложения Двритекорегаллери.</span><span class="sxs-lookup"><span data-stu-id="d2dca-134">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="d2dca-135">Кроме того, можно программировать с помощью Двритекоре, начиная с проекта примера приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , и основывать разработку на этом проекте.</span><span class="sxs-lookup"><span data-stu-id="d2dca-135">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="d2dca-136">После этого можно удалить любой существующий исходный код (или файлы) из этого примера проекта, а также добавить в проект новый исходный код (или файлы).</span><span class="sxs-lookup"><span data-stu-id="d2dca-136">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="d2dca-137">Использование Двритекоре в проекте</span><span class="sxs-lookup"><span data-stu-id="d2dca-137">Use DWriteCore in your project</span></span>

<span data-ttu-id="d2dca-138">Дополнительные сведения о программировании с помощью Двритекоре см. в подразделе [программирование с помощью двритекоре](#programming-with-dwritecore) далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d2dca-138">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="d2dca-139">Фазы выпуска Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d2dca-139">The release phases of DWriteCore</span></span>

<span data-ttu-id="d2dca-140">Перенос DirectWrite в Двритекоре является достаточно большим проектом, охватывающим несколько циклов выпуска Windows.</span><span class="sxs-lookup"><span data-stu-id="d2dca-140">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="d2dca-141">Этот проект делится на этапы, каждый из которых соответствует блоку функциональности, предоставленному в выпуске.</span><span class="sxs-lookup"><span data-stu-id="d2dca-141">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="d2dca-142">Функции в текущем выпуске Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d2dca-142">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="d2dca-143">Версия Двритекоре, доступная в настоящее время, является частью [объединения проектов 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="d2dca-143">The version of DWriteCore currently available is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="d2dca-144">Он содержит основные инструменты, которые вы, как разработчик, должны использовать Двритекоре, включая следующие функции.</span><span class="sxs-lookup"><span data-stu-id="d2dca-144">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="d2dca-145">Перечисление шрифтов.</span><span class="sxs-lookup"><span data-stu-id="d2dca-145">Font enumeration.</span></span>
- <span data-ttu-id="d2dca-146">API шрифтов.</span><span class="sxs-lookup"><span data-stu-id="d2dca-146">Font API.</span></span>
- <span data-ttu-id="d2dca-147">Упростить.</span><span class="sxs-lookup"><span data-stu-id="d2dca-147">Shaping.</span></span>
- <span data-ttu-id="d2dca-148">API-интерфейсы низкого уровня отрисовки.</span><span class="sxs-lookup"><span data-stu-id="d2dca-148">Low-level rendering APIs.</span></span> <span data-ttu-id="d2dca-149">Это частично на текущем этапе &mdash; двритекоре не взаимодействуют с [Direct2D](../direct2d/direct2d-portal.md), но можно использовать [**идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) и [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d2dca-149">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="d2dca-150">Основные функции макета текста.</span><span class="sxs-lookup"><span data-stu-id="d2dca-150">Basic text layout functionality.</span></span>
- <span data-ttu-id="d2dca-151">Интерфейсы API отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="d2dca-151">Text-rendering APIs.</span></span>
- <span data-ttu-id="d2dca-152">Целевой объект прорисовки битовой карты.</span><span class="sxs-lookup"><span data-stu-id="d2dca-152">Bitmap render target.</span></span>
- <span data-ttu-id="d2dca-153">Цветовые шрифты.</span><span class="sxs-lookup"><span data-stu-id="d2dca-153">Color fonts.</span></span>
- <span data-ttu-id="d2dca-154">Различные оптимизации (очистка кэша шрифта, загрузчик шрифтов в памяти и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d2dca-154">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="d2dca-155">Баннер — это цветовые шрифты.</span><span class="sxs-lookup"><span data-stu-id="d2dca-155">A banner feature is color fonts.</span></span> <span data-ttu-id="d2dca-156">Цветовые шрифты позволяют отображать шрифты с более сложными цветовыми возможностями, чем простые одиночные цвета.</span><span class="sxs-lookup"><span data-stu-id="d2dca-156">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="d2dca-157">Например, цветовые шрифты определяют возможность отображения шрифтов эмодзи и значков панели инструментов (второй из которых используется в Office, например).</span><span class="sxs-lookup"><span data-stu-id="d2dca-157">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="d2dca-158">Цветовые шрифты впервые появились в Windows 8.1, но эта функция была в значительной степени расширена в Windows 10, версии 1607 (годовщина обновления).</span><span class="sxs-lookup"><span data-stu-id="d2dca-158">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="d2dca-159">Работа по очистке кэша шрифтов и загрузчику шрифтов в памяти позволяет ускорить загрузку шрифтов и улучшения памяти.</span><span class="sxs-lookup"><span data-stu-id="d2dca-159">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="d2dca-160">С помощью этих функций можно сразу приступить к работе с некоторыми современными основными функциями DirectWrite, &mdash; такими как переменные шрифты &mdash; нижнего уровня до Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d2dca-160">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="d2dca-161">Переменные шрифты являются одной из наиболее важных функций для клиентов DirectWrite. они появились в Windows 10, версия 1709 (обновления для дизайнеров), поэтому доступ к ним в предыдущих версиях является значительным преимуществом для разработчика.</span><span class="sxs-lookup"><span data-stu-id="d2dca-161">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a significant benefit to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="d2dca-162">Наше приглашение в качестве разработчика DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d2dca-162">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="d2dca-163">Двритекоре, а также другие компоненты для повторного объединения проектов, будут разработаны с открытой откликом для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="d2dca-163">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="d2dca-164">Мы приглашаем вас начать изучать Двритекоре, а также предоставить подробные сведения или запросы на разработку функций в нашем [репозитории GitHub](https://github.com/microsoft/ProjectReunion/)для нашего проекта.</span><span class="sxs-lookup"><span data-stu-id="d2dca-164">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="d2dca-165">Программирование с помощью Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d2dca-165">Programming with DWriteCore</span></span>

<span data-ttu-id="d2dca-166">Как и в случае с [DirectWrite](./direct-write-portal.md), вы запрограммироване с помощью двритекоре с помощью API-интерфейса COM через интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="d2dca-166">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="d2dca-167">Чтобы использовать Двритекоре, необходимо включить `dwrite_core.h` заголовочный файл.</span><span class="sxs-lookup"><span data-stu-id="d2dca-167">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="d2dca-168">`dwrite_core.h`Сначала файл заголовка определяет маркер *DWRITE_CORE*, а затем включает `dwrite_3.h` файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="d2dca-168">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="d2dca-169">Маркер *DWRITE_CORE* важен, так как он направляет все последующие включенные заголовки, чтобы сделать доступными все API-интерфейсы DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d2dca-169">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="d2dca-170">После включения проекта `dwrite_core.h` можно выполнить написание кода, сборку и запуск.</span><span class="sxs-lookup"><span data-stu-id="d2dca-170">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="d2dca-171">Новые или разные API для Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d2dca-171">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="d2dca-172">Поверхность API Двритекоре в основном та же самая, что и для [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="d2dca-172">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="d2dca-173">Но существует небольшое количество новых API, которые доступны только в Двритекоре.</span><span class="sxs-lookup"><span data-stu-id="d2dca-173">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="d2dca-174">Создание объекта фабрики</span><span class="sxs-lookup"><span data-stu-id="d2dca-174">Create a factory object</span></span>

<span data-ttu-id="d2dca-175">Функция [**двритекорекреатефактори**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) Free создает объект фабрики, который используется для последующего создания отдельных объектов двритекоре.</span><span class="sxs-lookup"><span data-stu-id="d2dca-175">The [**DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="d2dca-176">**Двритекорекреатефактори** функционально совпадает с функцией [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , экспортируемой с помощью системной версии DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d2dca-176">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="d2dca-177">Функция Двритекоре имеет другое имя, чтобы избежать неоднозначности.</span><span class="sxs-lookup"><span data-stu-id="d2dca-177">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="d2dca-178">Создание объекта ограниченной фабрики</span><span class="sxs-lookup"><span data-stu-id="d2dca-178">Create a restricted factory object</span></span>

<span data-ttu-id="d2dca-179">Перечисление [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) содержит новую константную &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, обозначающую ограниченную фабрику.</span><span class="sxs-lookup"><span data-stu-id="d2dca-179">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="d2dca-180">Ограниченная фабрика больше заблокирована, чем изолированная фабрика.</span><span class="sxs-lookup"><span data-stu-id="d2dca-180">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="d2dca-181">Он не взаимодействует с межпроцессным или постоянным кэшем шрифтов каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="d2dca-181">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="d2dca-182">Кроме того, системная коллекция шрифтов, возвращаемая из этой фабрики, включает только хорошо известные шрифты.</span><span class="sxs-lookup"><span data-stu-id="d2dca-182">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="d2dca-183">Ниже показано, как можно использовать **DWRITE_FACTORY_TYPE_ISOLATED2** для создания объекта ограниченной фабрики при вызове функции Free **двритекорекреатефактори** .</span><span class="sxs-lookup"><span data-stu-id="d2dca-183">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the **DWriteCoreCreateFactory** free function.</span></span>

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

<span data-ttu-id="d2dca-184">При передаче **DWRITE_FACTORY_TYPE_ISOLATED2** в более старую версию DirectWrite, которая не поддерживается, **двритекреатефактори** возвращает **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="d2dca-184">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="d2dca-185">Рисование глифов в битовой карте системной памяти</span><span class="sxs-lookup"><span data-stu-id="d2dca-185">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="d2dca-186">DirectWrite имеет целевой интерфейс прорисовки растрового изображения, который поддерживает отображение глифов в битовую карту в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="d2dca-186">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="d2dca-187">Однако в настоящее время единственный способ получить доступ к базовым данным о пикселях — использовать GDI, поэтому API не может использоваться на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="d2dca-187">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="d2dca-188">Это легко исправлено, добавив метод для получения данных о точках.</span><span class="sxs-lookup"><span data-stu-id="d2dca-188">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="d2dca-189">Поэтому Двритекоре вводит интерфейс [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) и его метод [**IDWriteBitmapRenderTarget2::**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="d2dca-189">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="d2dca-190">Этот метод принимает параметр типа (указатель на) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), который является новой структурой.</span><span class="sxs-lookup"><span data-stu-id="d2dca-190">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="d2dca-191">Приложение создает целевой объект прорисовки растрового изображения путем вызова [идвритегдиинтероп:: креатебитмапрендертаржет](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d2dca-191">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="d2dca-192">В Windows целевой объект прорисовки растрового изображения инкапсулирует контроллер домена памяти GDI с выбранным в него точечным рисунком GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="d2dca-192">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="d2dca-193">[Идвритебитмапрендертаржет::D равглифрун](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) преобразует глифы в DIB.</span><span class="sxs-lookup"><span data-stu-id="d2dca-193">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="d2dca-194">DirectWrite отображает сами глифы без помощи GDI.</span><span class="sxs-lookup"><span data-stu-id="d2dca-194">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="d2dca-195">Приложение может получить **HDC** из целевого объекта прорисовки растрового изображения и использовать [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) для копирования пикселов в окно **HDC**.</span><span class="sxs-lookup"><span data-stu-id="d2dca-195">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="d2dca-196">На платформах, отличных от Windows, приложение по-прежнему может создавать целевой объект прорисовки битовой карты, но он просто Инкапсулирует массив системной памяти без **HDC** и не имеет DIB.</span><span class="sxs-lookup"><span data-stu-id="d2dca-196">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="d2dca-197">Без **HDC** для приложения должен быть другим способом получения пикселей точечного рисунка, чтобы он мог скопировать их, или иным образом использовать их.</span><span class="sxs-lookup"><span data-stu-id="d2dca-197">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="d2dca-198">Даже в Windows иногда бывает полезно получить фактические данные о пикселях, и мы покажем текущий способ сделать это в приведенном ниже примере кода.</span><span class="sxs-lookup"><span data-stu-id="d2dca-198">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="d2dca-199">Другие различия API между Двритекоре и DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d2dca-199">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="d2dca-200">Существует несколько интерфейсов API, являющихся только заглушками, или они работают несколько иначе на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="d2dca-200">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="d2dca-201">Например, [идвритегдиинтероп:: креатефонтфацефромхдк](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) возвращает **E_NOTIMPL** на платформах, отличных от Windows, поскольку параметр **HDC** без [GDI](../gdi/windows-gdi.md)отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d2dca-201">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="d2dca-202">И, наконец, существуют некоторые другие API Windows, которые обычно используются вместе с DirectWrite (Direct2D является важным примером).</span><span class="sxs-lookup"><span data-stu-id="d2dca-202">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="d2dca-203">Однако в настоящее время Direct2D и Двритекоре не взаимодействуют.</span><span class="sxs-lookup"><span data-stu-id="d2dca-203">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="d2dca-204">Например, если создать [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью двритекоре и передать его в [**D2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), то вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d2dca-204">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
