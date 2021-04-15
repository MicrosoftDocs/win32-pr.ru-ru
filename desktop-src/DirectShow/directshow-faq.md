---
description: Вопросы и ответы по DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: Вопросы и ответы по DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537499"
---
# <a name="directshow-faq"></a><span data-ttu-id="f1dcb-103">Вопросы и ответы по DirectShow</span><span class="sxs-lookup"><span data-stu-id="f1dcb-103">DirectShow FAQ</span></span>

<span data-ttu-id="f1dcb-104">В этой статье содержатся ответы на многие часто задаваемые вопросы о Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-104">This article answers many frequently asked questions about Microsoft DirectShow.</span></span>

<span data-ttu-id="f1dcb-105">**Какие операционные системы поддерживает DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-105">**What operating systems does DirectShow support?**</span></span>

<span data-ttu-id="f1dcb-106">DirectShow доступна во всех поддерживаемых версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-106">DirectShow is available in all supported versions of Windows.</span></span>

<span data-ttu-id="f1dcb-107">**Какой объем базы знаний COM необходим для программирования с помощью DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-107">**How much COM knowledge do I need to program with DirectShow?**</span></span>

<span data-ttu-id="f1dcb-108">Для разработки приложений необходимо понимать основы работы с COM-объектами: создание экземпляров, доступ к предоставляемым им интерфейсам и Управление счетчиками ссылок на этих интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-108">For application development, you need to understand the basics of working with COM objects: how to instantiate them, access the interfaces they expose, and manage reference counts on those interfaces.</span></span> <span data-ttu-id="f1dcb-109">Для разработки фильтров требуются дополнительные знания COM.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-109">Filter development requires more COM knowledge.</span></span>

<span data-ttu-id="f1dcb-110">**Какие форматы поддерживает DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-110">**What formats does DirectShow support?**</span></span>

<span data-ttu-id="f1dcb-111">См. раздел [Поддерживаемые форматы в DirectShow](supported-formats-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="f1dcb-111">See [Supported Formats in DirectShow](supported-formats-in-directshow.md).</span></span>

<span data-ttu-id="f1dcb-112">**Имеется ли список совместимого оборудования DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-112">**Is there a DirectShow Hardware Compatibility List (HCL)?**</span></span>

<span data-ttu-id="f1dcb-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-113">No.</span></span> <span data-ttu-id="f1dcb-114">DirectShow использует возможности Microsoft DirectDraw и оборудования Microsoft DirectSound, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-114">DirectShow uses Microsoft DirectDraw and Microsoft DirectSound hardware capabilities if they are available.</span></span> <span data-ttu-id="f1dcb-115">Если специального оборудования нет, DirectShow использует GDI для рисования видео и  \* мультимедийных API-интерфейсов для воспроизведения аудио.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-115">When no special hardware is available, DirectShow uses GDI to draw video and the **waveOut** \* multimedia APIs to play audio.</span></span>

<span data-ttu-id="f1dcb-116">**Какие языки можно использовать для написания приложения DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-116">**What languages can I use to write a DirectShow application?**</span></span>

<span data-ttu-id="f1dcb-117">DirectShow разработана в основном для разработки на C++.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-117">DirectShow is designed primarily for C++ development.</span></span> <span data-ttu-id="f1dcb-118">Небольшой поднабор API-интерфейса DirectShow предоставляется через Visual Basic 6,0; Однако эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-118">A small sub-set of the DirectShow API is exposed through Visual Basic 6.0; however, this feature is deprecated.</span></span>

<span data-ttu-id="f1dcb-119">**Будет ли доступно DirectShow через управляемый код?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-119">**Will DirectShow ever be accessible through managed code?**</span></span>

<span data-ttu-id="f1dcb-120">Корпорация Майкрософт не имеет текущих планов для реализации управляемого API DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-120">Microsoft has no current plans to implement a managed DirectShow API.</span></span>

<span data-ttu-id="f1dcb-121">**Какой компилятор требуется для разработки DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-121">**What compiler do I need for DirectShow development?**</span></span>

<span data-ttu-id="f1dcb-122">Любой компилятор, способный создавать COM-объекты, должен работать после правильной настройки среды компилятора.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-122">Any compiler capable of generating Component Object Model (COM) objects should work once the compiler's environment has been configured correctly.</span></span>

<span data-ttu-id="f1dcb-123">**Как DirectShow связана с Microsoft DirectX?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-123">**How does DirectShow relate to Microsoft DirectX?**</span></span>

<span data-ttu-id="f1dcb-124">На внутреннем уровне DirectShow использует DirectSound и DirectDraw, когда оборудование поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-124">Internally, DirectShow uses DirectSound and DirectDraw when the hardware supports it.</span></span> <span data-ttu-id="f1dcb-125">Фильтры "модуль подготовки видео" и "микшер оверлея" используют поверхности DirectDraw 3 и DirectDraw 5.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-125">The Video Renderer and Overlay Mixer filters use DirectDraw 3 and DirectDraw 5 surfaces.</span></span> <span data-ttu-id="f1dcb-126">Устройство микширования видео 7 (только для Windows XP) использует поверхности DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-126">The Video Mixing Renderer 7 (Windows XP only) uses DirectDraw 7 surfaces.</span></span> <span data-ttu-id="f1dcb-127">Устройство микширования видео 9 и Улучшенный модуль визуализации видео используют новейшие API-интерфейсы Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-127">The Video Mixing Renderer 9 and the Enhanced Video Renderer use the latest Microsoft Direct3D APIs.</span></span> <span data-ttu-id="f1dcb-128">Для написания приложения DirectShow не нужно использовать другие API-интерфейсы DirectX, хотя их можно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-128">You do not need to use the other DirectX APIs to write a DirectShow application, although it is possible to combine them.</span></span>

<span data-ttu-id="f1dcb-129">**Как DirectShow связана с Microsoft ActiveMovie?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-129">**How does DirectShow relate to Microsoft ActiveMovie?**</span></span>

<span data-ttu-id="f1dcb-130">ActiveMovie — это исходное имя для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-130">ActiveMovie was the original name for DirectShow.</span></span> <span data-ttu-id="f1dcb-131">Термин ActiveMovie больше не используется.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-131">The term ActiveMovie is no longer used.</span></span>

<span data-ttu-id="f1dcb-132">**Доступен ли исходный код для программы Графедит? Можно ли Графедит распространять?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-132">**Is the source code to the GraphEdit utility available? Can GraphEdit be redistributed?**</span></span>

<span data-ttu-id="f1dcb-133">Нет, источник недоступен, а Graphedt.exe не является распространяемым.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-133">No, the source is not available, and Graphedt.exe is not redistributable.</span></span>

<span data-ttu-id="f1dcb-134">**Дмос ли заменить фильтры DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-134">**Do DMOs replace DirectShow filters?**</span></span>

<span data-ttu-id="f1dcb-135">Объекты мультимедиа Microsoft DirectX (дмос) можно использовать в приложении DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-135">Microsoft DirectX Media Objects (DMOs) can be used in a DirectShow application.</span></span> <span data-ttu-id="f1dcb-136">Для кодировщиков, декодеров и эффектов рекомендуется писать объекты DMO вместо фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-136">For encoders, decoders, and effects, you are encouraged to write a DMO instead of a DirectShow filter.</span></span> <span data-ttu-id="f1dcb-137">(Примечание. Если вы хотите использовать ускорение видео DirectX в декодере, необходимо реализовать его в качестве фильтра.) Для других целей фильтр DirectShow может быть более подходящим.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-137">(Note: If you want to use DirectX Video Acceleration in your decoder, you must implement it as a filter.) For other purposes, a DirectShow filter might be more appropriate.</span></span> <span data-ttu-id="f1dcb-138">Дополнительные сведения о дмос см. в разделе [DirectX Media Objects](directx-media-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f1dcb-138">For more information about DMOs, see [DirectX Media Objects](directx-media-objects.md).</span></span>

<span data-ttu-id="f1dcb-139">**Я воспроизводить файл формата AVI с проигрывателем Windows Media. Я могу слышать звуковой сигнал, но вместо него кажется, что я вижу черный цвет. Что не так?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-139">**I'm playing an AVI format file with Windows Media Player. I can hear the audio, but there doesn't seem to be any video-instead, I just see black. What's wrong?**</span></span>

<span data-ttu-id="f1dcb-140">Возможно, файл был закодирован с помощью кодека, который отсутствует в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-140">Probably the file was encoded with a codec that is not present on your system.</span></span> <span data-ttu-id="f1dcb-141">Хотя формат AVI является распространенным, AVI-файлы можно создавать с помощью различных форматов сжатия (кодеков).</span><span class="sxs-lookup"><span data-stu-id="f1dcb-141">Although the AVI file format is common, AVI files can be created with many different compression formats (codecs).</span></span> <span data-ttu-id="f1dcb-142">Если вы попытаетесь воспроизвести AVI-файл, который использует неподдерживаемый кодек, вы можете услышать звуковой компонент, но видео будет отображаться как черный экран или содержимое экрана останется без изменений.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-142">If you try to play an AVI file that uses an unsupported codec, you might hear the audio component, but the video will display as a black screen or the screen contents will remain unchanged.</span></span>

> [!Note]  
> <span data-ttu-id="f1dcb-143">Проигрыватель Windows Media часто пытается загрузить и установить кодек, если он отсутствует в системе.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-143">Windows Media Player often attempts to download and install a codec if it is not present on your system.</span></span>

 

<span data-ttu-id="f1dcb-144">**Разделы справки создать приложение? Какие библиотеки и файлы заголовков нужны?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-144">**How do I build my application? What libraries and header files do I need?**</span></span>

<span data-ttu-id="f1dcb-145">См. раздел [Настройка среды сборки](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="f1dcb-145">See [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="f1dcb-146">**Графедит отображает множество фильтров, которые не документированы. Что такое фильтры?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-146">**GraphEdit displays a lot of filters that aren't documented. What are these filters?**</span></span>

<span data-ttu-id="f1dcb-147">Графедит перечисляет все фильтры, зарегистрированные в системе в категории фильтров.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-147">GraphEdit enumerates all of the filters that are registered on your system in a filter category.</span></span> <span data-ttu-id="f1dcb-148">Это могут быть фильтры, установленные сторонними приложениями или установленные другими технологиями Майкрософт, такими как Windows Media или NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-148">This might include filters installed by third-party applications, or installed by other Microsoft technologies, such as Windows Media or NetMeeting.</span></span> <span data-ttu-id="f1dcb-149">Кроме того, некоторые фильтры DirectShow работают как оболочки для кодеков или устройств, при этом каждый кодек или устройство появлялся как отдельный фильтр.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-149">Also, some DirectShow filters act as wrappers for codecs or hardware devices, with each codec or device appearing as a distinct filter.</span></span> <span data-ttu-id="f1dcb-150">Видеокодек Microsoft H. 263 используется в NetMeeting и больше не поддерживается в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-150">The Microsoft H.263 Video Codec is used by NetMeeting and is no longer supported in DirectShow.</span></span> <span data-ttu-id="f1dcb-151">Дополнительные сведения см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="f1dcb-151">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="f1dcb-152">**У меня возникают проблемы при создании пользовательского графа программным способом.**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-152">**I'm having trouble building my custom graph programmatically.**</span></span>

<span data-ttu-id="f1dcb-153">Сначала попытайтесь построить граф фильтра с помощью Графедит.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-153">First try building the filter graph with GraphEdit.</span></span> <span data-ttu-id="f1dcb-154">Это средство позволяет быстро имитировать множество возможностей.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-154">This tool enables you to simulate lots of possibilities quickly.</span></span> <span data-ttu-id="f1dcb-155">Графедит всегда является отличным местом для тестирования графа, прежде чем пытаться построить его с помощью исходного кода.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-155">GraphEdit is always a great place to test out the graph before attempting to build it with source code.</span></span>

<span data-ttu-id="f1dcb-156">Дополнительные сведения о построении графов см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="f1dcb-156">For more information about graph building, see the following articles:</span></span>

-   [<span data-ttu-id="f1dcb-157">Построение графа фильтра</span><span class="sxs-lookup"><span data-stu-id="f1dcb-157">Building the Filter Graph</span></span>](building-the-filter-graph.md)
-   [<span data-ttu-id="f1dcb-158">Перечисление объектов в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="f1dcb-158">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)

<span data-ttu-id="f1dcb-159">**Как определить, установлена ли DirectShow на данном компьютере?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-159">**How can I detect whether DirectShow is installed on a given machine?**</span></span>

<span data-ttu-id="f1dcb-160">Вызовите **CoCreateInstance** , чтобы создать экземпляр диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-160">Call **CoCreateInstance** to create an instance of the Filter Graph Manager.</span></span> <span data-ttu-id="f1dcb-161">Если этот вызов будет выполнен, на компьютере будет установлена DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-161">If this call succeeds, DirectShow is installed on the machine.</span></span> <span data-ttu-id="f1dcb-162">В следующем коде показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-162">The following code shows how to do this:</span></span>


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



<span data-ttu-id="f1dcb-163">**Разделы справки изменить параметры фильтра без отображения страницы свойств?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-163">**How do I change a filter's settings without displaying the property page?**</span></span>

<span data-ttu-id="f1dcb-164">Большинство фильтров предоставляют один или несколько интерфейсов для установки свойств фильтра.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-164">Most filters expose one or more interfaces for setting properties on the filter.</span></span> <span data-ttu-id="f1dcb-165">Просмотрите страницу справочника по рассматриваемому фильтру.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-165">Consult the reference page for the filter in question.</span></span> <span data-ttu-id="f1dcb-166">(См. раздел [фильтры DirectShow](directshow-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="f1dcb-166">(See [DirectShow Filters](directshow-filters.md).)</span></span>

<span data-ttu-id="f1dcb-167">**Можно ли протестировать фильтр с помощью Графедит?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-167">**Can I test my filter with GraphEdit?**</span></span>

<span data-ttu-id="f1dcb-168">При разработке фильтра Графедит может помочь визуализировать соединения между фильтрами.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-168">While you are developing a filter, GraphEdit can help you to visualize the connections between filters.</span></span> <span data-ttu-id="f1dcb-169">Кроме того, он может обеспечить быструю проверку функциональности фильтра.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-169">It can also provide a quick test of a filter's functionality.</span></span> <span data-ttu-id="f1dcb-170">Однако это не является надежной платформой тестирования.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-170">However, it is not meant as a robust test platform.</span></span>

<span data-ttu-id="f1dcb-171">**Какие фильтры работают с привилегиями Ring?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-171">**At what privilege ring do filters run?**</span></span>

<span data-ttu-id="f1dcb-172">Фильтры выполняются в кольцо 3, хотя некоторые фильтры контролируют потоковые устройства, которые работают в кольцевой 0.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-172">Filters run at ring 3, although some filters control streaming devices that run at ring 0.</span></span> <span data-ttu-id="f1dcb-173">Дополнительные сведения см. [в разделе как аппаратные устройства участвуют в графе фильтра](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="f1dcb-173">For more information, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>

<span data-ttu-id="f1dcb-174">**Нужно ли использовать отладчик ядра?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-174">**Do I need to use a kernel debugger?**</span></span>

<span data-ttu-id="f1dcb-175">Это зависит от конкретного проекта.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-175">That depends on your specific project.</span></span> <span data-ttu-id="f1dcb-176">Установка библиотек среды выполнения DirectX Debug означает, что устанавливаются отладочные драйверы и другие компоненты режима ядра, и что если приложение вызывает утверждение отладки в одном из этих компонентов, компьютер будет автоматически перезагружен, если к процессу не подключен отладчик ядра.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-176">Installing the DirectX debug runtime libraries means that you are installing debug drivers and other kernel mode components, and that if your application causes a debug assert in one of these components, your machine will automatically reboot unless you have a kernel debugger attached to your process.</span></span>

<span data-ttu-id="f1dcb-177">**При запуске приложения в отладчике происходит сбой.**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-177">**When I run my application in the debugger, it crashes.**</span></span>

<span data-ttu-id="f1dcb-178">Некоторые декодеры не работают, пока приложение подключено к отладчику.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-178">Some decoders are designed not to work while the application is attached to the debugger.</span></span> <span data-ttu-id="f1dcb-179">Попробуйте запустить приложение вне отладчика.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-179">Try running the application outside the debugger.</span></span>

<span data-ttu-id="f1dcb-180">**Как \_ работает макрос define GUID?**</span><span class="sxs-lookup"><span data-stu-id="f1dcb-180">**How does the DEFINE\_GUID macro work?**</span></span>

<span data-ttu-id="f1dcb-181">Макрос **define \_ GUID** решает проблему объявления `extern` ссылок на значения GUID в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-181">The **DEFINE\_GUID** macro solves the problem of declaring `extern` references to GUID values in your source code.</span></span> <span data-ttu-id="f1dcb-182">Например, предположим, что в проекте есть три исходных файла, Src1. cpp, Src2. cpp и Src3. cpp, а во всех трех файлах используется определенное значение идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-182">For example, suppose that your project has three source files, Src1.cpp, Src2.cpp, and Src3.cpp, and all three files use a certain GUID value that you have defined.</span></span> <span data-ttu-id="f1dcb-183">Значение GUID должно быть определено в проекте ровно один раз, а другие исходные файлы должны объявлять `extern` ссылки на него.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-183">The GUID value must be defined exactly once in your project, and the other source files must declare `extern` references to it.</span></span> <span data-ttu-id="f1dcb-184">С помощью макроса **define \_ GUID** можно использовать один и тот же файл заголовка для обоих целей.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-184">With the **DEFINE\_GUID** macro, you can use the same header file for both purposes.</span></span> <span data-ttu-id="f1dcb-185">В файле заголовка объявите GUID следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1dcb-185">In your header file, declare the GUID as follows:</span></span>


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



<span data-ttu-id="f1dcb-186">(Если этот пример содержит нули, укажите фактические значения идентификатора GUID.) Вы можете использовать служебную программу Guidgen.exe, чтобы создать новый GUID и вставить его в заголовочный файл в формате **определения \_ GUID** .</span><span class="sxs-lookup"><span data-stu-id="f1dcb-186">(Where this example has zeroes, put the actual GUID values.) You can use the Guidgen.exe utility to create a new GUID and paste it into the header file in the **DEFINE\_GUID** format.</span></span> <span data-ttu-id="f1dcb-187">Включите этот заголовочный файл в каждый исходный файл, который ссылается на GUID.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-187">Include this header file in every source file that references the GUID.</span></span> <span data-ttu-id="f1dcb-188">В точности один из исходных файлов включает файл заголовка Инитгуид. h перед файлом заголовка.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-188">In exactly one of the source files, include the header file Initguid.h before your header file.</span></span> <span data-ttu-id="f1dcb-189">Пример:</span><span class="sxs-lookup"><span data-stu-id="f1dcb-189">For example:</span></span>


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



<span data-ttu-id="f1dcb-190">Когда файл заголовка Инитгуид. h не включен, макрос **define \_ GUID** создает `extern` ссылку на значение GUID.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-190">Wherever the Initguid.h header file is not included, the **DEFINE\_GUID** macro creates an `extern` reference to the GUID value.</span></span> <span data-ttu-id="f1dcb-191">При включении файла заголовка Инитгуид. h он переопределяет макрос **define \_ GUID** , чтобы **определение \_ GUID** создавало определяющее объявление идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-191">When the Initguid.h header file is included, it redefines the **DEFINE\_GUID** macro so that **DEFINE\_GUID** creates a defining declaration of the GUID.</span></span>

<span data-ttu-id="f1dcb-192">Если Инитгуид. h не включен ни в один из исходных файлов, появится сообщение об ошибке ссылки "неразрешенный внешний символ".</span><span class="sxs-lookup"><span data-stu-id="f1dcb-192">If you do not include Initguid.h in any of the source files, you will get a link error "unresolved external symbol."</span></span> <span data-ttu-id="f1dcb-193">Если дважды включить Инитгуид. h для одного и того же идентификатора GUID, будет получено сообщение об ошибке компиляции "Redefinition; Множественная инициализация ".</span><span class="sxs-lookup"><span data-stu-id="f1dcb-193">If you include Initguid.h twice for the same GUID, you will get a compile error "redefinition; multiple initialization."</span></span> <span data-ttu-id="f1dcb-194">Чтобы устранить эти ошибки, убедитесь, что Инитгуид. h включен ровно один раз.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-194">To resolve these errors, make sure that Initguid.h is included exactly once.</span></span> <span data-ttu-id="f1dcb-195">Кроме того, не включайте Инитгуид. h в файл предкомпилированного заголовка, поскольку в силу этого предкомпилированный заголовок включается в каждый исходный файл.</span><span class="sxs-lookup"><span data-stu-id="f1dcb-195">Also, do not include Initguid.h inside a precompiled header file, because in effect the precompiled header is included in every source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1dcb-196">См. также</span><span class="sxs-lookup"><span data-stu-id="f1dcb-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1dcb-197">Введение в DirectShow</span><span class="sxs-lookup"><span data-stu-id="f1dcb-197">Introduction to DirectShow</span></span>](introduction-to-directshow.md)
</dt> </dl>

 

 



