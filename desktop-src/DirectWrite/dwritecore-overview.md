---
title: Общие сведения о DWriteCore
description: Двритекоре — это реализация DirectWrite для Реюньон проекта.
keywords:
- Ядро DirectWrite
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351035"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="d5fae-105">Общие сведения о DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d5fae-105">DWriteCore overview</span></span>

<span data-ttu-id="d5fae-106">Двритекоре — это реализация [DirectWrite](./direct-write-portal.md)для [Реюньон проекта](/windows/apps/project-reunion/) .</span><span class="sxs-lookup"><span data-stu-id="d5fae-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md).</span></span> <span data-ttu-id="d5fae-107">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="d5fae-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="d5fae-108">В этом вводном разделе описывается, что такое Двритекоре, и показано, как установить его в среду разработки и программировать вместе с ней.</span><span class="sxs-lookup"><span data-stu-id="d5fae-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="d5fae-109">Ценность Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d5fae-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="d5fae-110">Сам по себе [DirectWrite](./direct-write-portal.md) поддерживает обширный набор функций, который делает его средством визуализации шрифтов в Windows для большинства приложений, &mdash; будь это через прямые вызовы или через [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="d5fae-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="d5fae-111">DirectWrite содержит независимую от устройства систему разметки текста, высококачественную подсистему [Microsoft ClearType](/typography/cleartype/) Text Rendering, текст с аппаратным ускорением, многоформатный текст, расширенные функции оформления [OpenType®](/typography/opentype/) , языковую поддержку и макет и отрисовку, совместимые с [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="d5fae-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="d5fae-112">DirectWrite был доступен с момента выпуска пакета обновления 2 (SP2) для Windows Vista и был изменен в течение нескольких лет для включения более сложных функций, таких как переменные шрифты, позволяющие разработчикам применять стили, веса и другие атрибуты к шрифту с одним ресурсом шрифта.</span><span class="sxs-lookup"><span data-stu-id="d5fae-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="d5fae-113">Однако из-за длительного времени существования DirectWrite усовершенствования в разработке приходили бы оставлять старые версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d5fae-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="d5fae-114">Кроме того, состояние DirectWrite в качестве технологии отрисовки текста уровня Premier ограничено только Windows, в результате чего межплатформенные приложения должны либо записывать собственный стек отрисовки текста, либо полагаться на сторонние решения.</span><span class="sxs-lookup"><span data-stu-id="d5fae-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="d5fae-115">Двритекоре решает фундаментальные проблемы, связанные с признаком версии и межплатформенной совместимостью, удаляя библиотеку из системы и нацеливание на все возможные Поддерживаемые конечные точки.</span><span class="sxs-lookup"><span data-stu-id="d5fae-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="d5fae-116">В конце концов, мы интегрированы в проект Двритекоре с общедоступным API, который поддерживается на всех конечных точках Windows до Windows 8, и открывает дверцу для использования кросс-платформенной платформы.</span><span class="sxs-lookup"><span data-stu-id="d5fae-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="d5fae-117">Основное значение, которое Двритекоре предоставляет разработчику в качестве разработчика, — это то, что оно предоставляет доступ ко всем текущим DirectWrite функциям на всех уровнях до Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5fae-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="d5fae-118">Все функции Двритекоре будут работать одинаково для всех версий нижнего уровня; другими словами, все текущие функции будут работать в Windows 8, 8,1 и всех версиях Windows 10 без каких бы то ни было ошибок, касающихся того, какие функции могут работать с какими версиями.</span><span class="sxs-lookup"><span data-stu-id="d5fae-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="d5fae-119">Демонстрационное приложение Двритекоре &mdash; двритекорегаллери</span><span class="sxs-lookup"><span data-stu-id="d5fae-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="d5fae-120">Двритекоре демонстрируется в примере приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , которое доступно для загрузки и изучения.</span><span class="sxs-lookup"><span data-stu-id="d5fae-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="d5fae-121">Начало работы с Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d5fae-121">Get started with DWriteCore</span></span>

<span data-ttu-id="d5fae-122">В настоящее время в предварительном выпуске Project Реюньон 0,1 мы не поддерживаем установку пакета NuGet для повторного объединения проектов в собственные проекты.</span><span class="sxs-lookup"><span data-stu-id="d5fae-122">For the Project Reunion 0.1 Prerelease, we currently don't support installing the Project Reunion NuGet package into your own projects.</span></span> <span data-ttu-id="d5fae-123">Вместо этого в настоящее время поддерживается возможность собственного программирования с помощью Двритекоре, которая начинается с проекта [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) Sample App и основывается на разработке проекта.</span><span class="sxs-lookup"><span data-stu-id="d5fae-123">Instead, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span>

<span data-ttu-id="d5fae-124">После этого можно удалить любой существующий исходный код (или файлы) из этого примера проекта, а также добавить в проект новый исходный код (или файлы).</span><span class="sxs-lookup"><span data-stu-id="d5fae-124">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span> <span data-ttu-id="d5fae-125">Дополнительные сведения о программировании с помощью Двритекоре см. в подразделе [программирование с помощью двритекоре](#programming-with-dwritecore) далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d5fae-125">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="d5fae-126">Фазы выпуска Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d5fae-126">The release phases of DWriteCore</span></span>

<span data-ttu-id="d5fae-127">Перенос DirectWrite в Двритекоре является достаточно большим проектом, охватывающим несколько циклов выпуска Windows.</span><span class="sxs-lookup"><span data-stu-id="d5fae-127">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="d5fae-128">Этот проект делится на этапы, каждый из которых соответствует блоку функциональности, предоставленному в выпуске.</span><span class="sxs-lookup"><span data-stu-id="d5fae-128">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="d5fae-129">Функции в текущем выпуске Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d5fae-129">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="d5fae-130">Версия Двритекоре, доступная в настоящее время, содержит базовые инструменты, которые вы, как разработчик, должны использовать Двритекоре, включая следующие функции.</span><span class="sxs-lookup"><span data-stu-id="d5fae-130">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="d5fae-131">Перечисление шрифтов.</span><span class="sxs-lookup"><span data-stu-id="d5fae-131">Font enumeration.</span></span>
- <span data-ttu-id="d5fae-132">API шрифтов.</span><span class="sxs-lookup"><span data-stu-id="d5fae-132">Font API.</span></span>
- <span data-ttu-id="d5fae-133">Упростить.</span><span class="sxs-lookup"><span data-stu-id="d5fae-133">Shaping.</span></span>
- <span data-ttu-id="d5fae-134">API-интерфейсы низкого уровня отрисовки.</span><span class="sxs-lookup"><span data-stu-id="d5fae-134">Low-level rendering APIs.</span></span> <span data-ttu-id="d5fae-135">Это частично на текущем этапе &mdash; двритекоре не взаимодействуют с [Direct2D](../direct2d/direct2d-portal.md), но можно использовать [**идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) и [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d5fae-135">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="d5fae-136">Основные функции макета текста.</span><span class="sxs-lookup"><span data-stu-id="d5fae-136">Basic text layout functionality.</span></span>
- <span data-ttu-id="d5fae-137">Интерфейсы API отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="d5fae-137">Text-rendering APIs.</span></span>
- <span data-ttu-id="d5fae-138">Целевой объект прорисовки битовой карты.</span><span class="sxs-lookup"><span data-stu-id="d5fae-138">Bitmap render target.</span></span>
- <span data-ttu-id="d5fae-139">Цветовые шрифты.</span><span class="sxs-lookup"><span data-stu-id="d5fae-139">Color fonts.</span></span>
- <span data-ttu-id="d5fae-140">Различные оптимизации (очистка кэша шрифта, загрузчик шрифтов в памяти и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d5fae-140">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="d5fae-141">Баннер на этом этапе — цветовые шрифты.</span><span class="sxs-lookup"><span data-stu-id="d5fae-141">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="d5fae-142">Цветовые шрифты позволяют отображать шрифты с более сложными цветовыми возможностями, чем простые одиночные цвета.</span><span class="sxs-lookup"><span data-stu-id="d5fae-142">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="d5fae-143">Например, цветовые шрифты определяют возможность отображения шрифтов эмодзи и значков панели инструментов (второй из которых используется в Office, например).</span><span class="sxs-lookup"><span data-stu-id="d5fae-143">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="d5fae-144">Цветовые шрифты впервые появились в Windows 8.1, но эта функция была в значительной степени расширена в Windows 10, версии 1607 (годовщина обновления).</span><span class="sxs-lookup"><span data-stu-id="d5fae-144">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="d5fae-145">Работа по очистке кэша шрифтов и загрузчику шрифтов в памяти позволяет ускорить загрузку шрифтов и улучшения памяти.</span><span class="sxs-lookup"><span data-stu-id="d5fae-145">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="d5fae-146">С помощью этих функций можно сразу приступить к работе с некоторыми современными основными функциями DirectWrite, &mdash; такими как переменные шрифты &mdash; нижнего уровня до Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5fae-146">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="d5fae-147">Эту итерацию библиотеки также можно использовать в [Android](https://www.android.com/)и **Linux**.</span><span class="sxs-lookup"><span data-stu-id="d5fae-147">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="d5fae-148">Переменные шрифты являются одной из наиболее важных функций для клиентов DirectWrite. они появились в Windows 10, версия 1709 (обновления для авторов обновлений), поэтому доступ к ним в предыдущих версиях является огромным boonом для разработчика.</span><span class="sxs-lookup"><span data-stu-id="d5fae-148">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="d5fae-149">Наше приглашение в качестве разработчика DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d5fae-149">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="d5fae-150">Двритекоре, а также другие компоненты для повторного объединения проектов, будут разработаны с открытой откликом для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="d5fae-150">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="d5fae-151">Мы приглашаем вас начать изучать Двритекоре, а также предоставить подробные сведения или запросы на разработку функций в нашем [репозитории GitHub](https://github.com/microsoft/ProjectReunion/)для нашего проекта.</span><span class="sxs-lookup"><span data-stu-id="d5fae-151">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="d5fae-152">Программирование с помощью Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d5fae-152">Programming with DWriteCore</span></span>

<span data-ttu-id="d5fae-153">Как уже упоминалось, в предварительном выпуске Project Реюньон 0,1 параметр, поддерживаемый в настоящее время для собственного программирования с помощью Двритекоре, начинается с проекта [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) Sample App.</span><span class="sxs-lookup"><span data-stu-id="d5fae-153">As already mentioned, for the Project Reunion 0.1 Prerelease, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project.</span></span>

<span data-ttu-id="d5fae-154">Как и в случае с [DirectWrite](./direct-write-portal.md), вы запрограммироване с помощью двритекоре с помощью API-интерфейса COM через интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="d5fae-154">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="d5fae-155">**Двритекорегаллери** уже включает `dwrite_core.h` файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="d5fae-155">**DWriteCoreGallery** already includes the `dwrite_core.h` header file.</span></span> <span data-ttu-id="d5fae-156">Этот заголовок сначала определяет маркер *DWRITE_CORE*, а затем включает `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="d5fae-156">That header first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="d5fae-157">Маркер *DWRITE_CORE* важен, так как он направляет все последующие включенные заголовки, чтобы сделать доступными все API-интерфейсы DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d5fae-157">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="d5fae-158">После включения проекта `dwrite_core.h` можно выполнить написание кода, сборку и запуск.</span><span class="sxs-lookup"><span data-stu-id="d5fae-158">Once a project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="d5fae-159">Новые или разные API для Двритекоре</span><span class="sxs-lookup"><span data-stu-id="d5fae-159">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="d5fae-160">Поверхность API Двритекоре в основном та же самая, что и для [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="d5fae-160">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="d5fae-161">Но существует небольшое количество новых API, которые доступны только в Двритекоре.</span><span class="sxs-lookup"><span data-stu-id="d5fae-161">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="d5fae-162">Создание объекта ограниченной фабрики</span><span class="sxs-lookup"><span data-stu-id="d5fae-162">Create a restricted factory object</span></span>

<span data-ttu-id="d5fae-163">Перечисление [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) содержит новую константную &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="d5fae-163">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_RESTRICTED**.</span></span> <span data-ttu-id="d5fae-164">Ограниченная фабрика больше заблокирована, чем изолированная фабрика.</span><span class="sxs-lookup"><span data-stu-id="d5fae-164">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="d5fae-165">Он не взаимодействует с межпроцессным или постоянным кэшем шрифтов каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="d5fae-165">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="d5fae-166">Кроме того, системная коллекция шрифтов, возвращаемая из этой фабрики, включает только хорошо известные шрифты.</span><span class="sxs-lookup"><span data-stu-id="d5fae-166">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="d5fae-167">Ниже показано, как можно использовать **DWRITE_FACTORY_TYPE_RESTRICTED** для создания объекта ограниченной фабрики при вызове функции Free [**двритекреатефактори**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="d5fae-167">Here's how you can use **DWRITE_FACTORY_TYPE_RESTRICTED** to create a restricted factory object when you call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="d5fae-168">При передаче **DWRITE_FACTORY_TYPE_RESTRICTED** в более старую версию DirectWrite, которая не поддерживается, **двритекреатефактори** возвращает **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="d5fae-168">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="d5fae-169">Рисование глифов в битовой карте системной памяти</span><span class="sxs-lookup"><span data-stu-id="d5fae-169">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="d5fae-170">DirectWrite имеет целевой интерфейс прорисовки растрового изображения, который поддерживает отображение глифов в битовую карту в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="d5fae-170">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="d5fae-171">Однако в настоящее время единственный способ получить доступ к базовым данным о пикселях — использовать GDI, поэтому API не может использоваться на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="d5fae-171">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="d5fae-172">Это легко исправлено, добавив метод для получения данных о точках.</span><span class="sxs-lookup"><span data-stu-id="d5fae-172">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="d5fae-173">Поэтому Двритекоре вводит интерфейс [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) и его метод [**IDWriteBitmapRenderTarget2::**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="d5fae-173">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="d5fae-174">Этот метод принимает параметр типа (указатель на) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), который является новой структурой.</span><span class="sxs-lookup"><span data-stu-id="d5fae-174">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="d5fae-175">Приложение создает целевой объект прорисовки растрового изображения путем вызова [идвритегдиинтероп:: креатебитмапрендертаржет](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d5fae-175">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="d5fae-176">В Windows целевой объект прорисовки растрового изображения инкапсулирует контроллер домена памяти GDI с выбранным в него точечным рисунком GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="d5fae-176">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="d5fae-177">[Идвритебитмапрендертаржет::D равглифрун](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) преобразует глифы в DIB.</span><span class="sxs-lookup"><span data-stu-id="d5fae-177">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="d5fae-178">DirectWrite отображает сами глифы без помощи GDI.</span><span class="sxs-lookup"><span data-stu-id="d5fae-178">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="d5fae-179">Приложение может получить **HDC** из целевого объекта прорисовки растрового изображения и использовать [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) для копирования пикселов в окно **HDC**.</span><span class="sxs-lookup"><span data-stu-id="d5fae-179">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="d5fae-180">На платформах, отличных от Windows, приложение по-прежнему может создавать целевой объект прорисовки битовой карты, но он просто Инкапсулирует массив системной памяти без **HDC** и не имеет DIB.</span><span class="sxs-lookup"><span data-stu-id="d5fae-180">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="d5fae-181">Без **HDC** для приложения должен быть другим способом получения пикселей точечного рисунка, чтобы он мог скопировать их, или иным образом использовать их.</span><span class="sxs-lookup"><span data-stu-id="d5fae-181">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="d5fae-182">Даже в Windows иногда бывает полезно получить фактические данные о пикселях, и мы покажем текущий способ сделать это в приведенном ниже примере кода.</span><span class="sxs-lookup"><span data-stu-id="d5fae-182">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="d5fae-183">Другие различия API между Двритекоре и DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d5fae-183">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="d5fae-184">Существует несколько интерфейсов API, являющихся только заглушками, или они работают несколько иначе на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="d5fae-184">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="d5fae-185">Например, [идвритегдиинтероп:: креатефонтфацефромхдк](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) возвращает **E_NOTIMPL** на платформах, отличных от Windows, поскольку параметр **HDC** без [GDI](../gdi/windows-gdi.md)отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d5fae-185">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="d5fae-186">И, наконец, существуют некоторые другие API Windows, которые обычно используются вместе с DirectWrite (Direct2D является важным примером).</span><span class="sxs-lookup"><span data-stu-id="d5fae-186">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="d5fae-187">Однако в настоящее время Direct2D и Двритекоре не взаимодействуют.</span><span class="sxs-lookup"><span data-stu-id="d5fae-187">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="d5fae-188">Например, если создать [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью двритекоре и передать его в [**D2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), то вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d5fae-188">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>