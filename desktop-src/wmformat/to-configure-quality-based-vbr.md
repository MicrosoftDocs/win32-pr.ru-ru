---
title: Настройка Quality-Based VBR
description: Настройка Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- потоки, Настройка потоков VBR
- потоки, переменная скорость (VBR)
- Переменная скорость (VBR), потоки
- VBR (переменная скорость), потоки
- потоки, Настройка VBR на основе качества
- Переменная скорость (VBR), Настройка на основе качества
- VBR (переменная скорость), Настройка на основе качества
- профили, Настройка VBR на основе качества
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103987270"
---
# <a name="to-configure-quality-based-vbr"></a><span data-ttu-id="1f465-111">Настройка Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="1f465-111">To Configure Quality-Based VBR</span></span>

<span data-ttu-id="1f465-112">Для указания уровня качества, который будет поддерживаться для всего потока, независимо от требований к битовой скорости, в потоке можно использовать кодировку переменной на основе качества (VBR).</span><span class="sxs-lookup"><span data-stu-id="1f465-112">You can use quality-based variable bit rate (VBR) encoding on a stream to specify a quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>

<span data-ttu-id="1f465-113">Для видеопотоков с поддержкой VBR необходимо указать уровень качества от 1 до 100, при этом 100 представляет наивысшее качество.</span><span class="sxs-lookup"><span data-stu-id="1f465-113">For quality-based VBR video streams, you must specify a quality level from 1 to 100, with 100 representing the highest quality.</span></span> <span data-ttu-id="1f465-114">В настоящее время существует только 30 дискретных параметров качества.</span><span class="sxs-lookup"><span data-stu-id="1f465-114">At present there are only 30 discrete quality settings.</span></span> <span data-ttu-id="1f465-115">Следующие уровни качества эквивалентны дискретным параметрам качества: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span><span class="sxs-lookup"><span data-stu-id="1f465-115">The following quality levels equate to discrete quality settings: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span></span> <span data-ttu-id="1f465-116">Числа между двумя последовательными значениями в приведенном выше списке приравниваются к тому же параметру качества, что и меньшее число.</span><span class="sxs-lookup"><span data-stu-id="1f465-116">Numbers between two consecutive values in the preceding list equate to the same quality setting as the lower number.</span></span> <span data-ttu-id="1f465-117">Например, указаны значения 1 и 4, поэтому 2 и 3 приводят к тому же параметру качества, что и 1.</span><span class="sxs-lookup"><span data-stu-id="1f465-117">For example, 1 and 4 are listed, so 2 and 3 both result in the same quality setting as 1.</span></span>

<span data-ttu-id="1f465-118">Для звуковых потоков можно перечислить доступные режимы и получить объект конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="1f465-118">For audio streams, you can enumerate the available modes and retrieve a stream configuration object.</span></span> <span data-ttu-id="1f465-119">Дополнительные сведения см. [в разделе перечисление форматов кодеков](to-enumerate-codec-formats.md).</span><span class="sxs-lookup"><span data-stu-id="1f465-119">For more information, see [To Enumerate Codec Formats](to-enumerate-codec-formats.md).</span></span>

<span data-ttu-id="1f465-120">При использовании видео VBR на основе качества необходимо задать положительное значение для элемента **двбитрате** структуры [**вмвидеоинфохеадер**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="1f465-120">When using quality-based VBR video, you must set the **dwBitrate** member of the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to a positive value.</span></span> <span data-ttu-id="1f465-121">Это значение не используется модулем записи, но передача нуля или отрицательное число может вызвать ошибки при записи.</span><span class="sxs-lookup"><span data-stu-id="1f465-121">This value is not used by the writer, but passing zero or a negative number can cause errors when writing.</span></span>

<span data-ttu-id="1f465-122">Чтобы настроить поток в профиле для кодирования с VBR на основе качества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1f465-122">To configure a stream in a profile to be encoded with quality-based VBR, perform the following steps.</span></span>

1.  <span data-ttu-id="1f465-123">Создайте объект диспетчера профилей, вызвав функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="1f465-123">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="1f465-124">Откройте существующий профиль, в который требуется добавить поддержку VBR.</span><span class="sxs-lookup"><span data-stu-id="1f465-124">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="1f465-125">Дополнительные сведения об открытии профилей см. [в разделе Работа с профилями](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1f465-125">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="1f465-126">Получите объект конфигурации потока для потока, который вы хотите использовать, вызвав либо [**ивмпрофиле::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) GetObject, либо [**Ивмпрофиле:: жетстреамбинумбер**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="1f465-126">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="1f465-127">Получите указатель на интерфейс [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="1f465-127">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="1f465-128">Включите VBR для потока, вызвав метод [**ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) для свойства **g \_ всзвбренаблед** .</span><span class="sxs-lookup"><span data-stu-id="1f465-128">Enable VBR for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="1f465-129">Задайте уровень качества для потока VBR, вызвав метод **ивмпропертиваулт:: SetProperty** для свойства **g \_ всзвбркуалити** .</span><span class="sxs-lookup"><span data-stu-id="1f465-129">Set the quality level for the VBR stream by calling **IWMPropertyVault::SetProperty** for the **g\_wszVBRQuality** property.</span></span>
7.  <span data-ttu-id="1f465-130">Задайте для параметра **g \_ всзвбрбитратемакс** и **g \_ Всзвбрбуффервиндовмакс** значение 0 с помощью **ивмпропертиваулт:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="1f465-130">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
8.  <span data-ttu-id="1f465-131">Сохраните изменения, внесенные в поток, вызвав [**ивмпрофиле:: реконфигстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="1f465-131">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
9.  <span data-ttu-id="1f465-132">Сохраните профиль или передайте его в объект Writer и начните писать.</span><span class="sxs-lookup"><span data-stu-id="1f465-132">Save the profile, or pass it to the writer object and start writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f465-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1f465-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f465-134">**Настройка потоков с VBR**</span><span class="sxs-lookup"><span data-stu-id="1f465-134">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




