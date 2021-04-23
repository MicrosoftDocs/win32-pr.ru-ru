---
title: Работа с шаблонами соответствия устройств
description: Работа с шаблонами соответствия устройств
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- профили, шаблоны соответствия устройств
- профили, шаблоны соответствия
- кодеки, шаблоны соответствия устройств
- кодеки, шаблоны соответствия
- шаблоны соответствия устройств, сведения
- шаблоны соответствия
- шаблоны, шаблоны соответствия устройств
- Расширенный формат систем (ASF), шаблоны соответствия устройств
- ASF (Расширенный системный формат), шаблоны соответствия устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133483"
---
# <a name="working-with-device-conformance-templates"></a><span data-ttu-id="80cb3-112">Работа с шаблонами соответствия устройств</span><span class="sxs-lookup"><span data-stu-id="80cb3-112">Working with Device Conformance Templates</span></span>

<span data-ttu-id="80cb3-113">Из-за высокой гибкости файлов ASF часто бывает трудно определить, подходит ли файл для воспроизведения на определенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="80cb3-113">Because of the great flexibility of ASF files, it is often difficult to determine whether a file is appropriate for playback on a specific device.</span></span> <span data-ttu-id="80cb3-114">Например, файлы, записанные для локального воспроизведения на настольных компьютерах, не подходят для использования на карманных устройствах.</span><span class="sxs-lookup"><span data-stu-id="80cb3-114">For example, files written for local playback on desktop computers are not optimal for use on handheld devices.</span></span> <span data-ttu-id="80cb3-115">Шаблоны соответствия устройств позволяют приложениям быстро находить тип устройства воспроизведения, для которого предназначен файл.</span><span class="sxs-lookup"><span data-stu-id="80cb3-115">Device conformance templates enable applications to quickly identify the type of playback device for which a file was intended.</span></span> <span data-ttu-id="80cb3-116">Если шаблон соответствия устройств не соответствует устройству, приложение может информировать пользователя о том, что файл не подходит для устройства.</span><span class="sxs-lookup"><span data-stu-id="80cb3-116">If the device conformance template does not match the device, the application can inform the user that the file is inappropriate for the device.</span></span> <span data-ttu-id="80cb3-117">Таким образом, пользователь может быть уверен в возможности воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="80cb3-117">In this way, the user can be assured of a better playback experience.</span></span>

<span data-ttu-id="80cb3-118">Если вы пишете файлы исключительно для использования на персональных компьютерах, шаблоны соответствия устройств не будут настолько значительными при создании профилей.</span><span class="sxs-lookup"><span data-stu-id="80cb3-118">If you are writing files exclusively for use on personal computers, device conformance templates will not be as much of a factor in creating profiles.</span></span> <span data-ttu-id="80cb3-119">Главным назначением этих шаблонов является обеспечение совместимости файлов, созданных для использования с особым оборудованием, с целым рядом устройств, а не только с одним устройством.</span><span class="sxs-lookup"><span data-stu-id="80cb3-119">The main purpose of these templates is to ensure that files created for use with special hardware are compatible with a whole range of devices and not just a single device.</span></span>

<span data-ttu-id="80cb3-120">Шаблон соответствия устройств является утверждением того, что файл ASF содержит данные, закодированные в определенных параметрах.</span><span class="sxs-lookup"><span data-stu-id="80cb3-120">A device conformance template is an assertion that an ASF file contains data encoded within certain parameters.</span></span> <span data-ttu-id="80cb3-121">Дополнительные сведения о параметрах, соответствующих индивидуальным шаблонам, см. в разделе [Параметры шаблона соответствия устройств](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="80cb3-121">For more information about the settings appropriate to the individual templates, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="80cb3-122">Шаблоны соответствия устройств поддерживаются следующими кодеками.</span><span class="sxs-lookup"><span data-stu-id="80cb3-122">The following codecs support device conformance templates:</span></span>

-   <span data-ttu-id="80cb3-123">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="80cb3-123">Windows Media Video 9</span></span>
-   <span data-ttu-id="80cb3-124">Windows Media Audio 9 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="80cb3-124">Windows Media Audio 9 and later</span></span>
-   <span data-ttu-id="80cb3-125">Windows Media Audio 9 профессиональная и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="80cb3-125">Windows Media Audio 9 Professional and later</span></span>
-   <span data-ttu-id="80cb3-126">Голосовая связь Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="80cb3-126">Windows Media Audio 9 Voice</span></span>

<span data-ttu-id="80cb3-127">Для использования шаблонов соответствия устройств не нужно предпринимать никаких дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="80cb3-127">You do not need to take any special steps to use device conformance templates.</span></span> <span data-ttu-id="80cb3-128">Кодек автоматически записывает строку шаблона для каждого соответствующего потока в файле.</span><span class="sxs-lookup"><span data-stu-id="80cb3-128">The codec automatically writes a template string for each appropriate stream in the file.</span></span> <span data-ttu-id="80cb3-129">Кодек выбирает используемый шаблон на основе параметров конфигурации потока в профиле.</span><span class="sxs-lookup"><span data-stu-id="80cb3-129">The codec will decide which template to use, based on the stream configuration settings in the profile.</span></span> <span data-ttu-id="80cb3-130">Существует некоторое перекрытие параметров шаблона согласованности устройств, поэтому может потребоваться запрашивать определенный шаблон вместо того, чтобы позволить кодеку назначить его.</span><span class="sxs-lookup"><span data-stu-id="80cb3-130">There is some overlap in device conformance template parameters, so you may want to request a specific template instead of letting the codec assign one for you.</span></span> <span data-ttu-id="80cb3-131">Вы можете указать нужный шаблон, задав \_ свойство g всздекодеркомплекситирекуестед с помощью методов интерфейса [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) соответствующего объекта конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="80cb3-131">You can specify which template you want by setting the g\_wszDecoderComplexityRequested property with the methods of the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the appropriate stream configuration object.</span></span>

<span data-ttu-id="80cb3-132">При записи ASF-файла фактический шаблон соответствия устройств для каждого потока устанавливается в значение, передаваемое в модуль записи кодеком.</span><span class="sxs-lookup"><span data-stu-id="80cb3-132">When an ASF file is written, the actual device conformance template for each stream is set to the value passed to the writer by the codec.</span></span> <span data-ttu-id="80cb3-133">При открытии файла для чтения можно узнать, какой шаблон соответствуют потокам файла, с помощью методов интерфейса [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) , чтобы получить \_ атрибут g всздевицеконформанцетемплате уровня потока.</span><span class="sxs-lookup"><span data-stu-id="80cb3-133">When opening a file for reading, you can find out which template the streams of the file conform to by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface to retrieve the g\_wszDeviceConformanceTemplate stream-level attribute.</span></span> <span data-ttu-id="80cb3-134">Дополнительные сведения об атрибутах см. [в разделе Работа с метаданными](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="80cb3-134">For more information about attributes, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80cb3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="80cb3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80cb3-136">**Проектирование профилей**</span><span class="sxs-lookup"><span data-stu-id="80cb3-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="80cb3-137">**Параметры шаблона соответствия устройств**</span><span class="sxs-lookup"><span data-stu-id="80cb3-137">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> </dl>

 

 




