---
title: Настройка неограниченных VBR
description: Настройка неограниченных VBR
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- потоки, Настройка потоков VBR
- потоки, переменная скорость (VBR)
- Переменная скорость (VBR), потоки
- VBR (переменная скорость), потоки
- потоки, Настройка неограниченных VBR
- Переменная скорость (VBR), настройка не ограничена
- VBR (переменная скорость), Настройка неограниченного
- профили, Настройка неограниченных VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133574"
---
# <a name="to-configure-unconstrained-vbr"></a><span data-ttu-id="864c9-111">Настройка неограниченных VBR</span><span class="sxs-lookup"><span data-stu-id="864c9-111">To Configure Unconstrained VBR</span></span>

<span data-ttu-id="864c9-112">В потоке можно использовать кодирование с переменной скоростью без ограничений (VBR), чтобы указать среднюю скорость потока, которая будет поддерживаться в кодированном содержимом.</span><span class="sxs-lookup"><span data-stu-id="864c9-112">You can use unconstrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="864c9-113">Неограниченная VBR отличается от обычного CBR в том, что дисперсия по скорости потока может быть выше.</span><span class="sxs-lookup"><span data-stu-id="864c9-113">Unconstrained VBR differs from normal CBR in that the variance in bit rate throughout the stream can be greater.</span></span>

<span data-ttu-id="864c9-114">Скорость потока, заданная с помощью [**ивмстреамконфиг:: сетбитрате**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), используется в качестве нужной средней битовой скорости.</span><span class="sxs-lookup"><span data-stu-id="864c9-114">The bit rate of the stream, set with [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), is used as the desired average bit rate.</span></span> <span data-ttu-id="864c9-115">После завершения кодирования потока можно использовать [**ивмпропертиваулт:: жетпропертибинаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) для получения двух дополнительных свойств: **g \_ всзвбрпеак** и **g \_ всзбуфферавераже**.</span><span class="sxs-lookup"><span data-stu-id="864c9-115">When encoding of the stream is complete, you can use [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) to retrieve two additional properties: **g\_wszVBRPeak** and **g\_wszBufferAverage**.</span></span> <span data-ttu-id="864c9-116">Эти свойства описывают пиковую скорость потока в кодированном содержимом и среднее окно буфера содержимого соответственно.</span><span class="sxs-lookup"><span data-stu-id="864c9-116">These properties describe the peak bit rate of the encoded content and the average buffer window of the content, respectively.</span></span>

<span data-ttu-id="864c9-117">В сочетании с двумя проходными кодировками необходимо использовать неограниченные VBR.</span><span class="sxs-lookup"><span data-stu-id="864c9-117">Unconstrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="864c9-118">В профиле не задано двустороннее кодирование.</span><span class="sxs-lookup"><span data-stu-id="864c9-118">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="864c9-119">Перед записью потока необходимо настроить модуль записи для выполнения этапа предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="864c9-119">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="864c9-120">Дополнительные сведения об использовании двусторонней кодировки см. [в разделе использование Two-Pass Encoding](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="864c9-120">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="864c9-121">Чтобы настроить поток в профиле для кодирования с неограниченными VBR, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="864c9-121">To configure a stream in a profile to be encoded with unconstrained VBR, perform the following steps:</span></span>

1.  <span data-ttu-id="864c9-122">Создайте объект диспетчера профилей, вызвав функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="864c9-122">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="864c9-123">Откройте существующий профиль, в который требуется добавить поддержку VBR.</span><span class="sxs-lookup"><span data-stu-id="864c9-123">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="864c9-124">Дополнительные сведения об открытии профилей см. [в разделе Работа с профилями](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="864c9-124">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="864c9-125">Получите объект конфигурации потока для потока, который вы хотите использовать, вызвав либо [**ивмпрофиле::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) GetObject, либо [**Ивмпрофиле:: жетстреамбинумбер**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="864c9-125">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="864c9-126">Получите указатель на интерфейс [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="864c9-126">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="864c9-127">Включите кодирование VBR для потока, вызвав метод [**ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) для свойства **g \_ всзвбренаблед** .</span><span class="sxs-lookup"><span data-stu-id="864c9-127">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="864c9-128">Задайте для параметра **g \_ всзвбрбитратемакс** и **g \_ Всзвбрбуффервиндовмакс** значение 0 с помощью **ивмпропертиваулт:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="864c9-128">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
7.  <span data-ttu-id="864c9-129">Сохраните изменения, внесенные в поток, вызвав [**ивмпрофиле:: реконфигстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="864c9-129">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="864c9-130">Сохраните профиль или передайте его в объект модуля записи.</span><span class="sxs-lookup"><span data-stu-id="864c9-130">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="864c9-131">Настройте модуль записи для выполнения этапа предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="864c9-131">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="864c9-132">См. также</span><span class="sxs-lookup"><span data-stu-id="864c9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="864c9-133">**Настройка потоков с VBR**</span><span class="sxs-lookup"><span data-stu-id="864c9-133">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




