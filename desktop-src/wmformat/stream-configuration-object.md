---
title: Объект конфигурации потока
description: Объект конфигурации потока
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media Format SDK, объекты конфигурации потока
- Расширенный системный формат (ASF), объекты конфигурации потока
- ASF (Расширенный системный формат), объекты конфигурации потока
- объекты, объекты конфигурации Stream
- объекты конфигурации потока
- потоки, объекты конфигурации потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133582"
---
# <a name="stream-configuration-object"></a><span data-ttu-id="1141e-109">Объект конфигурации потока</span><span class="sxs-lookup"><span data-stu-id="1141e-109">Stream Configuration Object</span></span>

<span data-ttu-id="1141e-110">Объект конфигурации потока используется для указания свойств потока мультимедиа в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="1141e-110">A stream configuration object is used to specify the properties of a media stream in an ASF file.</span></span> <span data-ttu-id="1141e-111">Объекты конфигурации потока могут быть созданы для существующих потоков в профиле или могут быть созданы пустыми и готовы к получению новых данных.</span><span class="sxs-lookup"><span data-stu-id="1141e-111">Stream configuration objects can be created for existing streams in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="1141e-112">Объекты конфигурации потока не могут существовать независимо от объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="1141e-112">Stream configuration objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="1141e-113">Чтобы сохранить содержимое объекта конфигурации потока, необходимо вызвать метод [**ивмпрофиле:: аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) , чтобы добавить новый поток или [**Ивмпрофиле:: реконфигстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) для сохранения изменений, внесенных в существующий поток.</span><span class="sxs-lookup"><span data-stu-id="1141e-113">To save the contents of a stream configuration object, you must call either [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add a new stream or [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to save changes made to an existing stream.</span></span>

<span data-ttu-id="1141e-114">Чтобы создать объект конфигурации потока, используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="1141e-114">To create a stream configuration object, use one of the following methods.</span></span>



| <span data-ttu-id="1141e-115">Метод</span><span class="sxs-lookup"><span data-stu-id="1141e-115">Method</span></span>                                                                | <span data-ttu-id="1141e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1141e-116">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1141e-117">**Ивмпрофиле:: Креатеневстреам**</span><span class="sxs-lookup"><span data-stu-id="1141e-117">**IWMProfile::CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | <span data-ttu-id="1141e-118">Создает объект конфигурации потока без каких-либо данных.</span><span class="sxs-lookup"><span data-stu-id="1141e-118">Creates a stream configuration object without any data.</span></span>                                                                          |
| [<span data-ttu-id="1141e-119">**Ивмпрофиле:: Stream**</span><span class="sxs-lookup"><span data-stu-id="1141e-119">**IWMProfile::GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | <span data-ttu-id="1141e-120">Создает объект конфигурации потока, заполненный данными из профиля.</span><span class="sxs-lookup"><span data-stu-id="1141e-120">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="1141e-121">Использует индекс потока для задания нужного потока.</span><span class="sxs-lookup"><span data-stu-id="1141e-121">Uses the stream index to identify the desired stream.</span></span>  |
| [<span data-ttu-id="1141e-122">**Ивмпрофиле:: Жетстреамбинумбер**</span><span class="sxs-lookup"><span data-stu-id="1141e-122">**IWMProfile::GetStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | <span data-ttu-id="1141e-123">Создает объект конфигурации потока, заполненный данными из профиля.</span><span class="sxs-lookup"><span data-stu-id="1141e-123">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="1141e-124">Использует номер потока для задания нужного потока.</span><span class="sxs-lookup"><span data-stu-id="1141e-124">Uses the stream number to identify the desired stream.</span></span> |



 

<span data-ttu-id="1141e-125">Все методы в приведенной выше таблице устанавливают указатель на интерфейс **ивмстреамконфиг** .</span><span class="sxs-lookup"><span data-stu-id="1141e-125">All of the methods in the preceding table set a pointer to an **IWMStreamConfig** interface.</span></span> <span data-ttu-id="1141e-126">Другие интерфейсы объекта конфигурации потока можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="1141e-126">The other interfaces of the stream configuration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="1141e-127">Объект конфигурации Stream поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1141e-127">The following interfaces are supported by the stream configuration object.</span></span>



| <span data-ttu-id="1141e-128">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="1141e-128">Interface</span></span>                                        | <span data-ttu-id="1141e-129">Описание</span><span class="sxs-lookup"><span data-stu-id="1141e-129">Description</span></span>                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1141e-130">**ивммедиапропс**</span><span class="sxs-lookup"><span data-stu-id="1141e-130">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="1141e-131">Задает и получает структуру [**\_ \_ типа WM Media**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для потока.</span><span class="sxs-lookup"><span data-stu-id="1141e-131">Sets and retrieves the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream.</span></span>                                    |
| [<span data-ttu-id="1141e-132">**ивмпропертиваулт**</span><span class="sxs-lookup"><span data-stu-id="1141e-132">**IWMPropertyVault**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | <span data-ttu-id="1141e-133">Задает и получает свойства, которые не требуются для всех потоков, например для параметров переменной скорости (VBR).</span><span class="sxs-lookup"><span data-stu-id="1141e-133">Sets and retrieves properties that are not required for all streams, like variable bit rate (VBR) settings.</span></span>                  |
| [<span data-ttu-id="1141e-134">**ивмстреамконфиг**</span><span class="sxs-lookup"><span data-stu-id="1141e-134">**IWMStreamConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | <span data-ttu-id="1141e-135">Задает и извлекает все основные сведения о потоке.</span><span class="sxs-lookup"><span data-stu-id="1141e-135">Sets and retrieves all of the basic information about a stream.</span></span>                                                              |
| [<span data-ttu-id="1141e-136">**IWMStreamConfig2**</span><span class="sxs-lookup"><span data-stu-id="1141e-136">**IWMStreamConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | <span data-ttu-id="1141e-137">Настраивает типы модулей обработки данных, связанных с потоком.</span><span class="sxs-lookup"><span data-stu-id="1141e-137">Configures the types of data unit extensions associated with the stream.</span></span> <span data-ttu-id="1141e-138">Наследует все методы **ивмстреамконфиг**.</span><span class="sxs-lookup"><span data-stu-id="1141e-138">Inherits all of the methods of **IWMStreamConfig**.</span></span> |
| [<span data-ttu-id="1141e-139">**IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="1141e-139">**IWMStreamConfig3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | <span data-ttu-id="1141e-140">Задает и получает язык для потока.</span><span class="sxs-lookup"><span data-stu-id="1141e-140">Sets and retrieves the language for the stream.</span></span> <span data-ttu-id="1141e-141">Наследует все методы **ивмстреамконфиг** и **IWMStreamConfig2**.</span><span class="sxs-lookup"><span data-stu-id="1141e-141">Inherits all of the methods of **IWMStreamConfig** and **IWMStreamConfig2**.</span></span> |
| [<span data-ttu-id="1141e-142">**ивмвидеомедиапропс**</span><span class="sxs-lookup"><span data-stu-id="1141e-142">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="1141e-143">Управляет свойствами потока видео.</span><span class="sxs-lookup"><span data-stu-id="1141e-143">Manages the properties of a video stream.</span></span> <span data-ttu-id="1141e-144">Это необязательный интерфейс, который доступен только для потоков видео.</span><span class="sxs-lookup"><span data-stu-id="1141e-144">This is an optional interface, and is available only for video streams.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="1141e-145">См. также</span><span class="sxs-lookup"><span data-stu-id="1141e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1141e-146">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="1141e-146">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="1141e-147">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="1141e-147">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="1141e-148">**Объект диспетчера профилей**</span><span class="sxs-lookup"><span data-stu-id="1141e-148">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




