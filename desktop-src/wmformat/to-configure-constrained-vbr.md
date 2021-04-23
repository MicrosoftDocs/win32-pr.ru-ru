---
title: Настройка ограниченного VBR
description: Настройка ограниченного VBR
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- потоки, Настройка потоков VBR
- потоки, переменная скорость (VBR)
- Переменная скорость (VBR), потоки
- VBR (переменная скорость), потоки
- потоки, Настройка ограниченного VBR
- Переменная скорость (VBR), Настройка ограничена
- VBR (переменная скорость), Настройка ограничена
- профили, Настройка ограниченного VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069692"
---
# <a name="to-configure-constrained-vbr"></a><span data-ttu-id="1e323-111">Настройка ограниченного VBR</span><span class="sxs-lookup"><span data-stu-id="1e323-111">To Configure Constrained VBR</span></span>

<span data-ttu-id="1e323-112">В потоке можно использовать кодирование с ограничением переменной скорости (VBR) для указания средней скорости потока, которая будет поддерживаться в кодированном содержимом.</span><span class="sxs-lookup"><span data-stu-id="1e323-112">You can use constrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="1e323-113">Вы также указываете максимальную скорость потока и максимально необходимое окно буфера.</span><span class="sxs-lookup"><span data-stu-id="1e323-113">You also specify the maximum bit rate of the stream and the maximum required buffer window.</span></span>

<span data-ttu-id="1e323-114">Вы не можете узнать, какая средняя скорость будет использоваться для потока с ограничением VBR перед кодированием, но можно использовать приблизительную оценку.</span><span class="sxs-lookup"><span data-stu-id="1e323-114">You cannot know what the average bit rate will be for a constrained VBR stream before encoding, but you can use a rough estimate.</span></span> <span data-ttu-id="1e323-115">Как правило, максимальная скорость, которую вы задаете, составляет от двух до трех раз средней скорости.</span><span class="sxs-lookup"><span data-stu-id="1e323-115">As a general rule, the maximum bit rate you specify will end up being two to three times the average bit rate.</span></span>

<span data-ttu-id="1e323-116">В сочетании с двумя проходными кодировками необходимо использовать ограниченные VBR.</span><span class="sxs-lookup"><span data-stu-id="1e323-116">Constrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="1e323-117">В профиле не задано двустороннее кодирование.</span><span class="sxs-lookup"><span data-stu-id="1e323-117">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="1e323-118">Перед записью потока необходимо настроить модуль записи для выполнения этапа предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="1e323-118">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="1e323-119">Дополнительные сведения об использовании двусторонней кодировки см. [в разделе использование Two-Pass Encoding](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="1e323-119">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="1e323-120">Чтобы настроить поток в профиле для использования ограниченного кодирования VBR, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e323-120">To configure a stream in a profile to use constrained VBR encoding, perform the following steps.</span></span>

1.  <span data-ttu-id="1e323-121">Создайте объект диспетчера профилей, вызвав функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="1e323-121">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="1e323-122">Откройте существующий профиль, в который требуется добавить поддержку VBR.</span><span class="sxs-lookup"><span data-stu-id="1e323-122">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="1e323-123">Дополнительные сведения об открытии профилей см. [в разделе Работа с профилями](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1e323-123">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="1e323-124">Получите объект конфигурации потока для потока, который вы хотите использовать, вызвав либо [**ивмпрофиле::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) GetObject, либо [**Ивмпрофиле:: жетстреамбинумбер**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="1e323-124">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="1e323-125">Получите указатель на интерфейс [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="1e323-125">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="1e323-126">Включите кодирование VBR для потока, вызвав метод [**ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) для свойства **g \_ всзвбренаблед** .</span><span class="sxs-lookup"><span data-stu-id="1e323-126">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="1e323-127">Используйте вызовы метода **ивмпропертиваулт:: SetProperty** , чтобы задать требуемые максимальные значения для свойств **g \_ всзвбрбитратемакс** и **g \_ всзвбрбуффервиндовмакс** .</span><span class="sxs-lookup"><span data-stu-id="1e323-127">Use calls to **IWMPropertyVault::SetProperty** to set the desired maximum values for the **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** properties.</span></span>
7.  <span data-ttu-id="1e323-128">Сохраните изменения, внесенные в поток, вызвав [**ивмпрофиле:: реконфигстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="1e323-128">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="1e323-129">Сохраните профиль или передайте его в объект модуля записи.</span><span class="sxs-lookup"><span data-stu-id="1e323-129">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="1e323-130">Настройте модуль записи для выполнения этапа предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="1e323-130">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e323-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1e323-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e323-132">**Настройка потоков с VBR**</span><span class="sxs-lookup"><span data-stu-id="1e323-132">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




