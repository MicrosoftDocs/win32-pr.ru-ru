---
title: Включение быстрой потоковой передачи кэша от клиента
description: Включение быстрой потоковой передачи кэша от клиента
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Пакет Windows Media Format SDK, обеспечивающий быструю потоковую передачу кэша
- Windows Media Format SDK, Быстрая потоковая передача кэша
- Расширенный системный формат (ASF), обеспечивающий быструю потоковую передачу кэша
- ASF (Расширенный системный формат), включение быстрой потоковой передачи кэша
- Расширенный системный формат (ASF), Быстрая потоковая передача кэша
- ASF (Расширенный системный формат), Быстрая потоковая передача кэша
- потоки, включение быстрой потоковой передачи кэша
- Быстрая потоковая передача кэша, включение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412506"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a><span data-ttu-id="8021a-111">Включение быстрой потоковой передачи кэша от клиента</span><span class="sxs-lookup"><span data-stu-id="8021a-111">Enabling Fast Cache Streaming from the Client</span></span>

<span data-ttu-id="8021a-112">Быстрый кэш — это технология потоковой передачи, в которой сервер рационально потоковое содержимое с более высокой скоростью, чем требуется для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8021a-112">Fast Cache is a streaming technology in which the server opportunistically streams content at a higher bit rate than what is needed for playback.</span></span>

<span data-ttu-id="8021a-113">Если доступная пропускная способность выше скорости потока содержимого, потоки быстрого кэширования с более высокой скоростью и помещает содержимое в буфер.</span><span class="sxs-lookup"><span data-stu-id="8021a-113">If the available bandwidth is higher than the bit rate of the content, Fast Cache streams at the higher rate and buffers the content.</span></span> <span data-ttu-id="8021a-114">Это позволяет сократить перерывы позже, если сеть перестает быть перегруженной.</span><span class="sxs-lookup"><span data-stu-id="8021a-114">This helps to reduce interruptions later if the network becomes congested.</span></span> <span data-ttu-id="8021a-115">Если пропускная способность сети ниже скорости содержимого, то быстрый кэш кэширует часть данных перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8021a-115">If network bandwidth is lower than the bit rate of the content, Fast Cache buffers a portion of the data before playback starts.</span></span> <span data-ttu-id="8021a-116">Быстрый кэш рекомендуется для ненадежных сетей, таких как беспроводные сети или сети, которые испытывают большие колебания сетевого трафика, такие как кабельные модемы.</span><span class="sxs-lookup"><span data-stu-id="8021a-116">Fast Cache is recommended for unreliable networks, such as wireless networks, or networks that experience large fluctuations in network traffic, such as cable modems.</span></span> <span data-ttu-id="8021a-117">Также рекомендуется использовать содержимое с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="8021a-117">It is also recommended for variable bit rate (VBR) content.</span></span> <span data-ttu-id="8021a-118">Требования к пропускной способности для содержимого VBR не являются постоянными, а быстрый кэш позволяет модулю чтения буферизовать поток во время построчных пропорций.</span><span class="sxs-lookup"><span data-stu-id="8021a-118">The bandwidth requirements for VBR content are not constant, and Fast Cache enables the reader to buffer the stream during the lower-bit-rate portions.</span></span>

<span data-ttu-id="8021a-119">Быстрая потоковая передача кэша поддерживается только для содержимого по запросу.</span><span class="sxs-lookup"><span data-stu-id="8021a-119">Fast Cache streaming is supported only for on-demand content.</span></span> <span data-ttu-id="8021a-120">Кроме того, сервер должен быть настроен для использования потоковой передачи с быстрым кэшем.</span><span class="sxs-lookup"><span data-stu-id="8021a-120">In addition, the server must be configured to use Fast Cache streaming.</span></span>

<span data-ttu-id="8021a-121">Чтобы включить быстрый кэш в объекте Reader, вызовите методы [**IWMReaderNetworkConfig2:: сетенаблеконтенткачинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) и [**IWMReaderNetworkConfig2:: Сетенаблефасткаче**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="8021a-121">To enable Fast Cache in the reader object, call the [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) and [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) methods with the value **TRUE**.</span></span> <span data-ttu-id="8021a-122">Первый метод позволяет модулю чтения кэшировать потоковое содержимое.</span><span class="sxs-lookup"><span data-stu-id="8021a-122">The first method enables the reader to cache streamed content.</span></span> <span data-ttu-id="8021a-123">Второй позволяет использовать быстрый кэш в частности.</span><span class="sxs-lookup"><span data-stu-id="8021a-123">The second enables the use of Fast Cache in particular.</span></span>

<span data-ttu-id="8021a-124">С помощью этих параметров модуль чтения активирует быстрый кэш по умолчанию, если пропускная способность сети значительно выше или ниже, чем скорость содержимого, и если сервер поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="8021a-124">With these settings, the reader will activate Fast Cache by default if the network bandwidth is significantly higher or lower than the bit rate of the content, and if the server supports it.</span></span> <span data-ttu-id="8021a-125">Пользователь также может управлять тем, использует ли объект чтения быстрый кэш, добавляя к URL-адресу один или несколько из следующих модификаторов.</span><span class="sxs-lookup"><span data-stu-id="8021a-125">The user can also control whether the reader object uses Fast Cache by adding one or more of the following modifiers to the URL.</span></span>



| <span data-ttu-id="8021a-126">Модификатор</span><span class="sxs-lookup"><span data-stu-id="8021a-126">Modifier</span></span>         | <span data-ttu-id="8021a-127">Описание</span><span class="sxs-lookup"><span data-stu-id="8021a-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8021a-128">вмкаче</span><span class="sxs-lookup"><span data-stu-id="8021a-128">WMCache</span></span>          | <span data-ttu-id="8021a-129">Если этот модификатор имеется, значение "0" явно отключает быстрый кэш, а значение "1" явно включает его.</span><span class="sxs-lookup"><span data-stu-id="8021a-129">If this modifier is present, the value '0' explicitly disables Fast Cache, while the value '1' explicitly enables it.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="8021a-130">вмбитрате</span><span class="sxs-lookup"><span data-stu-id="8021a-130">WMBitrate</span></span>        | <span data-ttu-id="8021a-131">Этот модификатор задает максимальную скорость передачи с сервера.</span><span class="sxs-lookup"><span data-stu-id="8021a-131">This modifier specifies the maximum bit rate from the server.</span></span> <span data-ttu-id="8021a-132">Этот модификатор можно использовать для ограничения быстрого кэширования на определенный предел пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="8021a-132">This modifier can be used to restrict Fast Cache to a certain bandwidth limit.</span></span> <span data-ttu-id="8021a-133">Этот модификатор игнорируется, если для явной пропускной способности соединения уже задан вызов [**ивмреадернетворкконфиг:: сетконнектионбандвидс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span><span class="sxs-lookup"><span data-stu-id="8021a-133">This modifier is ignored if an explicit connection bandwidth is already set with a call to [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span></span> |
| <span data-ttu-id="8021a-134">вмконтентбитрате</span><span class="sxs-lookup"><span data-stu-id="8021a-134">WMContentBitrate</span></span> | <span data-ttu-id="8021a-135">Этот модификатор задает скорость потока для содержимого.</span><span class="sxs-lookup"><span data-stu-id="8021a-135">This modifier specifies the bit rate for the content.</span></span> <span data-ttu-id="8021a-136">Модуль чтения использует этот модификатор, если он есть, при выборе потоков из файла с несколькими битовыми скоростями (MBR).</span><span class="sxs-lookup"><span data-stu-id="8021a-136">The reader uses this modifier, if present, when it selects streams from a multiple bit rate (MBR) file.</span></span> <span data-ttu-id="8021a-137">Это может привести к тому, что читатель сможет получить содержимое с высокой скоростью передачи данных через медленное подключение, что приводит к очень длительному времени буферизации и задержкам.</span><span class="sxs-lookup"><span data-stu-id="8021a-137">This can cause the reader to receive high bit rate content over a slow connection, which results in very long buffering times and delays.</span></span>                                          |



 

<span data-ttu-id="8021a-138">Модификатор Вмкаче = 1 заставляет средство чтения использовать потоковую передачу с быстрым кэшем независимо от пропускной способности сети или скорости потока содержимого и вне зависимости от предыдущих вызовов **сетенаблефасткаче**.</span><span class="sxs-lookup"><span data-stu-id="8021a-138">The modifier WMCache=1 forces the reader to use Fast Cache streaming, regardless of the network bandwith or the bit rate of the content and regardless of any previous calls to **SetEnableFastCache**.</span></span> <span data-ttu-id="8021a-139">Однако он не переопределяет параметр **сетенаблеконтенткачинг** в модуле чтения. и не переопределяет конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="8021a-139">However, it does not override the **SetEnableContentCaching** setting on the reader; nor does it override the server configuration.</span></span>

<span data-ttu-id="8021a-140">Модификаторы URL-адреса имеют следующую форму:</span><span class="sxs-lookup"><span data-stu-id="8021a-140">URL modifiers have the following form:</span></span>

<span data-ttu-id="8021a-141">*URL-адрес*? *Модификатор* = *значение*</span><span class="sxs-lookup"><span data-stu-id="8021a-141">*url*?*modifier*=*value*</span></span>

<span data-ttu-id="8021a-142">Пример:</span><span class="sxs-lookup"><span data-stu-id="8021a-142">For example:</span></span>

<span data-ttu-id="8021a-143">mms://MyServer/MyVideo.wmv? Вмкаче = 1</span><span class="sxs-lookup"><span data-stu-id="8021a-143">mms://MyServer/MyVideo.wmv?WMCache=1</span></span>

<span data-ttu-id="8021a-144">Можно указать более одного модификатора; чтобы разделить их, используйте амперсанд (&):</span><span class="sxs-lookup"><span data-stu-id="8021a-144">More than one modifier can specified; use an ampersand (&) to separate them:</span></span>

<span data-ttu-id="8021a-145">mms://MyServer/MyVideo.wmv? Вмкаче = 1&Вмконтентбитрате = 56000</span><span class="sxs-lookup"><span data-stu-id="8021a-145">mms://MyServer/MyVideo.wmv?WMCache=1&WMContentBitrate=56000</span></span>

 

 




