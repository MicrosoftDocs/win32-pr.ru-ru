---
title: Получение сведений о профиле при воспроизведении
description: Получение сведений о профиле при воспроизведении
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, профили
- Расширенный формат систем (ASF), профили
- ASF (Расширенный системный формат), профили
- Расширенный формат систем (ASF), взаимное исключение
- ASF (Расширенный системный формат), взаимное исключение
- Расширенный формат систем (ASF), совместное использование пропускной способности
- ASF (Расширенный системный формат), совместное использование пропускной способности
- потоки, получение сведений о профилях при воспроизведении
- профили, получение информации при воспроизведении
- взаимное исключение, получение сведений о профиле при воспроизведении
- Совместное использование пропускной способности, получение сведений о профиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133511"
---
# <a name="getting-profile-information-at-playback"></a><span data-ttu-id="578c4-114">Получение сведений о профиле при воспроизведении</span><span class="sxs-lookup"><span data-stu-id="578c4-114">Getting Profile Information at Playback</span></span>

<span data-ttu-id="578c4-115">Сведения из профиля, используемого для создания файла, хранятся в разделе заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="578c4-115">Information from the profile used to create a file is stored in the header section of the file.</span></span> <span data-ttu-id="578c4-116">Оба объекта чтения могут получить доступ к сведениям профиля из заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="578c4-116">Both reader objects can access the profile information from the file header.</span></span> <span data-ttu-id="578c4-117">Существует несколько причин, по которым может потребоваться доступ к данным профиля из средства чтения.</span><span class="sxs-lookup"><span data-stu-id="578c4-117">There are several reasons why you might want to access profile data from the reader.</span></span> <span data-ttu-id="578c4-118">Чаще всего необходимо получить сведения о потоках, взаимоисключающих объектах и пропускной способности объектов совместного использования.</span><span class="sxs-lookup"><span data-stu-id="578c4-118">Most commonly, you will need to retrieve information about streams, mutual exclusion objects, and bandwidth sharing objects.</span></span>

<span data-ttu-id="578c4-119">Для интерфейса [**ивмпрофиле**](iwmprofile.md) можно запросить как асинхронный, так и синхронный объект Reader.</span><span class="sxs-lookup"><span data-stu-id="578c4-119">Both the asynchronous reader object and the synchronous reader object can be queried for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="578c4-120">Никакие изменения, внесенные в данные профиля, не могут повлиять на файл в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="578c4-120">No changes made to the profile information can have any affect on the file in the reader.</span></span> <span data-ttu-id="578c4-121">Дополнительные сведения о доступе к сведениям о профиле см. [в разделе Работа с профилями](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="578c4-121">For more information about accessing profile information, see [Working with Profiles](working-with-profiles.md).</span></span>

## <a name="stream-information"></a><span data-ttu-id="578c4-122">Сведения о потоке</span><span class="sxs-lookup"><span data-stu-id="578c4-122">Stream Information</span></span>

<span data-ttu-id="578c4-123">Иногда важно иметь представление о настройке потока.</span><span class="sxs-lookup"><span data-stu-id="578c4-123">It is sometimes important to know how a stream is configured.</span></span> <span data-ttu-id="578c4-124">При извлечении свойств мультимедиа из любого из объектов чтения вы получаете свойства выходов.</span><span class="sxs-lookup"><span data-stu-id="578c4-124">When you retrieve media properties from the either of the reader objects, you get the properties of the outputs.</span></span> <span data-ttu-id="578c4-125">Выходные свойства описывают, как несжатые данные из потока будут доставляться модулем чтения, а не как поток настраивается в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="578c4-125">Output properties describe how the uncompressed data from a stream is going to be delivered by the reader, not how the stream is configured within the ASF file.</span></span>

<span data-ttu-id="578c4-126">При получении несжатых образцов потока из любого объекта модуля чтения необходимо использовать сведения о профиле для задания формата сжатых данных.</span><span class="sxs-lookup"><span data-stu-id="578c4-126">When receiving uncompressed stream samples from either reader object, you must use the profile information to identify the format of the compressed data.</span></span> <span data-ttu-id="578c4-127">Это особенно важно, если вы собираетесь записать сжатый поток в другой ASF-файл.</span><span class="sxs-lookup"><span data-stu-id="578c4-127">This is particularly important if you are going to write the compressed stream to another ASF file.</span></span>

<span data-ttu-id="578c4-128">Кроме того, необходимо получить доступ к потоковой информации при использовании интеллектуального сжатия для перекодирования звукового потока на более низкую скорость.</span><span class="sxs-lookup"><span data-stu-id="578c4-128">You also need to access stream information when using smart recompression to transcode an audio stream to a lower bit rate.</span></span>

<span data-ttu-id="578c4-129">Может потребоваться определить, был ли поток записан с помощью кодирования с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="578c4-129">You may want to determine whether a stream was written using variable bit rate (VBR) encoding.</span></span> <span data-ttu-id="578c4-130">Доступ к сведениям о VBR из интерфейса **ивмпрофиле** любого объекта Reader невозможен.</span><span class="sxs-lookup"><span data-stu-id="578c4-130">You cannot access any VBR information from the **IWMProfile** interface of either reader object.</span></span> <span data-ttu-id="578c4-131">Это обусловлено тем, что сведения о VBR не хранятся в файле после кодирования.</span><span class="sxs-lookup"><span data-stu-id="578c4-131">This is because the VBR information is not stored in the file after encoding.</span></span> <span data-ttu-id="578c4-132">Чтобы определить, был ли поток создан с помощью кодирования VBR, можно получить указатель на интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) объекта Reader и вызвать [**Ивмхеадеринфо:: жетаттрибутебинаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="578c4-132">You can determine whether a stream was created using VBR encoding by obtaining a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface of the reader object and calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span> <span data-ttu-id="578c4-133">Необходимо указать номер потока и передать g \_ всзисвбр в качестве имени атрибута.</span><span class="sxs-lookup"><span data-stu-id="578c4-133">You must specify the stream number and pass g\_wszIsVBR as the attribute name.</span></span>

## <a name="mutual-exclusion-information"></a><span data-ttu-id="578c4-134">Сведения об взаимном исключении</span><span class="sxs-lookup"><span data-stu-id="578c4-134">Mutual Exclusion Information</span></span>

<span data-ttu-id="578c4-135">Если вы хотите создать приложение для чтения, использующее взаимное исключение, вам потребуется получить доступ к сведениям о любых взаимоисключающих объектах, включенных в профиль.</span><span class="sxs-lookup"><span data-stu-id="578c4-135">If you want to create a reading application that uses mutual exclusion, you will want to access the information about any mutual exclusion objects included in the profile.</span></span> <span data-ttu-id="578c4-136">Для всех взаимоисключающих типов, за исключением скорости битов, приложение чтения отвечает за любое требуемое переключение потоков.</span><span class="sxs-lookup"><span data-stu-id="578c4-136">For all mutual exclusion types except bit rate, the reading application is responsible for any stream switching that is required.</span></span> <span data-ttu-id="578c4-137">Чтобы переключить потоки, необходимо знать, какие потоки.</span><span class="sxs-lookup"><span data-stu-id="578c4-137">To switch streams, you need to know which streams are which.</span></span>

## <a name="bandwidth-sharing-information"></a><span data-ttu-id="578c4-138">Сведения о совместном использовании полосы пропускания</span><span class="sxs-lookup"><span data-stu-id="578c4-138">Bandwidth Sharing Information</span></span>

<span data-ttu-id="578c4-139">Объекты, совместно использующие пропускную способность, которые включены в профиль, включаются только в информационных целях.</span><span class="sxs-lookup"><span data-stu-id="578c4-139">Bandwidth sharing objects that are included in a profile are included only for informational purposes.</span></span> <span data-ttu-id="578c4-140">Ни объект модуля записи, ни ни один из объектов чтения не принимают никаких действий в результате предоставления данных о пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="578c4-140">Neither the writer object nor either of the reader objects takes any action as a result of bandwidth sharing data.</span></span> <span data-ttu-id="578c4-141">Если вы хотите использовать совместное использование пропускной способности в приложении чтения, необходимо получить доступ к сведениям о совместном использовании пропускной способности из данных профиля.</span><span class="sxs-lookup"><span data-stu-id="578c4-141">If you want to use bandwidth sharing in your reading application, you must access the bandwidth sharing information from the profile data.</span></span>

> [!Note]  
> <span data-ttu-id="578c4-142">Не все сведения из профиля, используемого для создания файла, содержатся в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="578c4-142">Not all of the information from the profile used to create a file is present in the file header.</span></span> <span data-ttu-id="578c4-143">Как правило, данные, используемые только во время кодирования, не сохраняются в файле.</span><span class="sxs-lookup"><span data-stu-id="578c4-143">As a general rule, data that is used only at the time of encoding is not persisted in the file.</span></span> <span data-ttu-id="578c4-144">Сюда входят параметры ввода, заданные с помощью метода [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , а также свойства, заданные с помощью метода [**Ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="578c4-144">This includes input settings that were set using the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method, as well as properties set using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="578c4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="578c4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="578c4-146">**Интерфейс Ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="578c4-146">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="578c4-147">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="578c4-147">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




