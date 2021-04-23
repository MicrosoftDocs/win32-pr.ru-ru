---
title: Обновление существующих подключаемых модулей DSP
description: Обновление существующих подключаемых модулей DSP
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Подключаемые модули проигрывателя Windows Media, обработка цифровых сигналов (DSP)
- подключаемые модули, обработка цифровых сигналов (DSP)
- подключаемые модули обработки цифровых сигналов, обновление
- Подключаемые модули DSP, обновление
- версии проигрывателя Windows Media, подключаемые модули DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788743"
---
# <a name="updating-existing-dsp-plug-ins"></a><span data-ttu-id="e8062-108">Обновление существующих подключаемых модулей DSP</span><span class="sxs-lookup"><span data-stu-id="e8062-108">Updating Existing DSP Plug-ins</span></span>

<span data-ttu-id="e8062-109">Подключаемые модули DSP, созданные до выпуска пакета SDK для проигрывателя Windows Media 11, могут не работать должным образом с проигрывателем Windows Media 11, работающим в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8062-109">DSP plug-ins created before the release of the Windows Media Player 11 SDK might not work as expected with Windows Media Player 11 running on Windows Vista.</span></span> <span data-ttu-id="e8062-110">Чтобы гарантировать, что клиенты, использующие проигрыватель Windows Media 11 в Windows Vista, могут использовать ваши подключаемые модули, необходимо внести некоторые изменения в код подключаемого модуля DSP, перекомпилировать проект и распространить обновленный подключаемый модуль для клиентов.</span><span class="sxs-lookup"><span data-stu-id="e8062-110">To ensure that customers who run Windows Media Player 11 on Windows Vista can use your plug-ins, you must make some changes to your DSP plug-in code, recompile your project, and distribute the updated plug-in to your customers.</span></span>

<span data-ttu-id="e8062-111">Проекты, созданные с помощью последней версии мастера подключаемых модулей проигрывателя Windows Media, будут содержать необходимые обновления.</span><span class="sxs-lookup"><span data-stu-id="e8062-111">Projects created using the latest version of the Windows Media Player plug-in wizard will contain the required updates.</span></span> <span data-ttu-id="e8062-112">См. раздел [обновления мастера подключаемых модулей DSP для проигрывателя Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="e8062-112">See [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span> <span data-ttu-id="e8062-113">(Рекомендуется запустить мастер, чтобы создать новый пример проекта, а затем использовать такие средства, как Windiff.exe, которые входят в состав Visual Studio, чтобы проверить различия между образцом кода и рабочим кодом.)</span><span class="sxs-lookup"><span data-stu-id="e8062-113">(It is a good idea to run the wizard to create a new sample project and then use a tool like Windiff.exe, which comes with Visual Studio, to inspect the differences between the sample code and your production code.)</span></span>

<span data-ttu-id="e8062-114">Существуют три основных изменения, которые необходимо внести в существующие подключаемые модули DSP.</span><span class="sxs-lookup"><span data-stu-id="e8062-114">There are three main changes you will need to make to any existing DSP plug-ins:</span></span>

-   <span data-ttu-id="e8062-115">Изменение способа регистрации подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="e8062-115">Change the way the plug-in registers.</span></span> <span data-ttu-id="e8062-116">Существующий подключаемый модуль, вероятно, регистрирует модель потоков как "подразделение".</span><span class="sxs-lookup"><span data-stu-id="e8062-116">Your existing plug-in probably registers the threading model as "Apartment".</span></span> <span data-ttu-id="e8062-117">Проигрыватель Windows Media 11, работающий в Windows Vista, требует, чтобы подключаемые модули DSP регистрировали модель потоков как "оба".</span><span class="sxs-lookup"><span data-stu-id="e8062-117">Windows Media Player 11 running on Windows Vista requires that DSP plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="e8062-118">Это можно исправить, изменив значение модели потоков в файле *имяПроекта*. RGS следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e8062-118">You can fix this by changing the threading model value in your *projectname*.rgs file, as follows:</span></span>

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > <span data-ttu-id="e8062-119">При указании модели потоков как "оба" удаляется любая сериализация, предоставляемая COM для вызовов пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e8062-119">Specifying the threading model as "Both" removes any serialization that COM provides for calls to custom interfaces.</span></span> <span data-ttu-id="e8062-120">При вызове пользовательских интерфейсов из нескольких потоков необходимо предоставить такую сериализацию самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="e8062-120">If you make calls to your custom interfaces from multiple threads, you must provide this serialization yourself.</span></span>

     

    <span data-ttu-id="e8062-121">Проигрыватель Windows Media 11 обеспечивает правильную сериализацию вызовов интерфейсов DMO.</span><span class="sxs-lookup"><span data-stu-id="e8062-121">Windows Media Player 11 ensures that calls to DMO interfaces are properly serialized.</span></span>

    1.  <span data-ttu-id="e8062-122">Добавьте вызовы [ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) и [Ивмпмедиаплугинрегистрар:: вмпунрегистерплайерплугин](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) с новым типом подключаемого модуля: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC в DllRegisterServer и DllUnregisterServer в файле *projectnamedll*. cpp.</span><span class="sxs-lookup"><span data-stu-id="e8062-122">Add calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC in DllRegisterServer and DllUnregisterServer in your *projectnamedll*.cpp file.</span></span> <span data-ttu-id="e8062-123">Дополнительные сведения см. на страницах справочника по этим методам.</span><span class="sxs-lookup"><span data-stu-id="e8062-123">See the reference pages for these methods for details.</span></span>
    2.  <span data-ttu-id="e8062-124">Создайте и распространите БИБЛИОТЕКУ прокси-сервера или заглушки, чтобы включить маршалирование COM любого пользовательского интерфейса, реализованного или созданного классом подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="e8062-124">Create and distribute a proxy/stub DLL to enable COM marshaling of any custom interface implemented on or created by the plug-in class.</span></span> <span data-ttu-id="e8062-125">Пользовательский интерфейс — это любой собственный интерфейс, который определяется и реализуется для использования объектом подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="e8062-125">A custom interface is any proprietary interface that you define and implement for use by the plug-in object.</span></span> <span data-ttu-id="e8062-126">К ним относится пользовательский интерфейс, используемый страницей свойств, если он указан, но также может включать интерфейсы, подключающиеся к подключаемым модулям пользовательского интерфейса, например.</span><span class="sxs-lookup"><span data-stu-id="e8062-126">This includes the custom interface used by your property page, if you provided one, but might also include interfaces that connect to UI plug-ins, for example.</span></span> <span data-ttu-id="e8062-127">Примером настраиваемого интерфейса, созданного с помощью мастера подключаемых модулей, является *ипрожектнаме*.</span><span class="sxs-lookup"><span data-stu-id="e8062-127">An example of a custom interface created by the plug-in wizard is *Iprojectname*.</span></span> <span data-ttu-id="e8062-128">Примеры интерфейсов, которые не являются пользовательскими интерфейсами, включают **имедиаобжект** и **ивмпплугиненабле**.</span><span class="sxs-lookup"><span data-stu-id="e8062-128">Examples of interfaces that are not custom interfaces include **IMediaObject** and **IWMPPluginEnable**.</span></span>

<span data-ttu-id="e8062-129">Если подключаемый модуль DSP обрабатывает аудио, необходимо также добавить поддержку следующих новых форматов звука:</span><span class="sxs-lookup"><span data-stu-id="e8062-129">If your DSP plug-in processes audio, you must also add support for the following new audio formats:</span></span>

-   <span data-ttu-id="e8062-130">\_Формат волны \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="e8062-130">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
-   <span data-ttu-id="e8062-131">\_Формат Wave \_ , расширяемый с подформатом КСДАТАФОРМАТ \_ подтипа \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="e8062-131">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

<span data-ttu-id="e8062-132">Если подключаемый модуль DSP обрабатывает видео, необходимо добавить поддержку формата видео NV12.</span><span class="sxs-lookup"><span data-stu-id="e8062-132">If your DSP plug-in processes video, you must add support for the NV12 video format.</span></span>

<span data-ttu-id="e8062-133">См. образец подключаемого модуля DSP аудио или видео, создаваемый мастером, для примера обработки этих типов форматов.</span><span class="sxs-lookup"><span data-stu-id="e8062-133">See the sample audio or video DSP plug-in that the wizard creates for an example of how to process these format types.</span></span>

## <a name="about-the-proxystub-project"></a><span data-ttu-id="e8062-134">О проекте прокси-сервера/заглушки</span><span class="sxs-lookup"><span data-stu-id="e8062-134">About the Proxy/Stub Project</span></span>

<span data-ttu-id="e8062-135">Возможно, самый простой способ создать проект прокси-сервера или библиотеки DLL-заглушки для подключаемого модуля DSP — запустить мастер подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="e8062-135">Perhaps the simplest way to create a proxy/stub DLL project for your DSP plug-in is to run the DSP plug-in wizard.</span></span> <span data-ttu-id="e8062-136">В результате будет создан пример проекта прокси-сервера, который можно изменить для работы с существующим кодом.</span><span class="sxs-lookup"><span data-stu-id="e8062-136">This will create a sample proxy/stub project that you can modify to work with your existing code.</span></span> <span data-ttu-id="e8062-137">Необходимо внести следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="e8062-137">You will need to make the following changes:</span></span>

1.  <span data-ttu-id="e8062-138">Удалите все существующие определения для пользовательских интерфейсов из кода.</span><span class="sxs-lookup"><span data-stu-id="e8062-138">Remove any existing definitions for your custom interfaces from your code.</span></span> <span data-ttu-id="e8062-139">Например, мастер подключаемых модулей DSP из пакета SDK проигрывателя Windows Media 10 создал определение интерфейса *ипрожектнаме* в файле *имяПроекта*. h с помощью ключевого слова **Interface** .</span><span class="sxs-lookup"><span data-stu-id="e8062-139">For example, the DSP plug-in wizard from the Windows Media Player 10 SDK created the *Iprojectname* interface definition in the *projectname*.h file by using the **interface** keyword.</span></span>
2.  <span data-ttu-id="e8062-140">Определите пользовательские интерфейсы в IDL-файле проекта прокси или заглушки.</span><span class="sxs-lookup"><span data-stu-id="e8062-140">Define your custom interfaces in the proxy/stub project's IDL file.</span></span>
3.  <span data-ttu-id="e8062-141">Создайте проект прокси-сервера или заглушки перед основным проектом.</span><span class="sxs-lookup"><span data-stu-id="e8062-141">Build the proxy/stub project before your main project.</span></span> <span data-ttu-id="e8062-142">Вы можете настроить Visual Studio для автоматического выполнения этой операции, если оба проекта являются частью одного решения.</span><span class="sxs-lookup"><span data-stu-id="e8062-142">You can configure Visual Studio to do this automatically if both projects are part of the same solution.</span></span>
4.  <span data-ttu-id="e8062-143">Компилятор MIDL создаст новый файл заголовка с именем в формате *имя_проекта* \_ х.х.</span><span class="sxs-lookup"><span data-stu-id="e8062-143">The MIDL compiler will create a new header file having a name in the format *projectname*\_h.h.</span></span> <span data-ttu-id="e8062-144">Этот заголовок необходимо включить в основной проект (в *имяПроекта*. h).</span><span class="sxs-lookup"><span data-stu-id="e8062-144">You must include this header in your main project (in *projectname*.h).</span></span> <span data-ttu-id="e8062-145">Он содержит определения для пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e8062-145">It contains the definitions for your custom interfaces.</span></span>

## <a name="distributing-the-updated-plug-in"></a><span data-ttu-id="e8062-146">Распространение обновленного подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="e8062-146">Distributing the Updated Plug-in</span></span>

<span data-ttu-id="e8062-147">Вы можете установить обновленный подключаемый модуль на компьютерах пользователей точно так же, как в прошлом.</span><span class="sxs-lookup"><span data-stu-id="e8062-147">You can install the updated plug-in on your users' computers exactly as you have in the past.</span></span> <span data-ttu-id="e8062-148">Однако теперь необходимо также распространять и регистрировать библиотеку DLL прокси-сервера и заглушки.</span><span class="sxs-lookup"><span data-stu-id="e8062-148">However, you must now also distribute and register the proxy/stub DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8062-149">См. также</span><span class="sxs-lookup"><span data-stu-id="e8062-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8062-150">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="e8062-150">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




