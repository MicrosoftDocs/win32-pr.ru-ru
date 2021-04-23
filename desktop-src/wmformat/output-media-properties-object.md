---
title: Объект свойств выходного носителя
description: Объект свойств выходного носителя
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Пакет SDK для формата Windows Media, объекты свойств выходных данных мультимедиа
- Расширенный системный формат (ASF), объекты свойств выходных данных мультимедиа
- ASF (Расширенный системный формат), объекты свойств выходных данных мультимедиа
- объекты, выходные объекты свойств медиа
- объекты свойств выходных данных мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069700"
---
# <a name="output-media-properties-object"></a><span data-ttu-id="ce72a-108">Объект свойств выходного носителя</span><span class="sxs-lookup"><span data-stu-id="ce72a-108">Output Media Properties Object</span></span>

<span data-ttu-id="ce72a-109">Объект свойств выходного носителя используется для извлечения и задания выходного свойства.</span><span class="sxs-lookup"><span data-stu-id="ce72a-109">An output media properties object is used to retrieve and set an output property.</span></span> <span data-ttu-id="ce72a-110">Объекты свойств выходных данных мультимедиа создаются для поддерживаемых выходных форматов потоков в файле, который загружается в объект модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="ce72a-110">Output media properties objects are created for supported output formats of streams in a file that is loaded into a reader object.</span></span> <span data-ttu-id="ce72a-111">Для сжатых потоков свойства вывода определяются возможными выходными данными для десжатого кодека.</span><span class="sxs-lookup"><span data-stu-id="ce72a-111">For compressed streams, the output properties are determined by the possible outputs of the decompressing codec.</span></span>

<span data-ttu-id="ce72a-112">Объект свойств выходного носителя создается с помощью [**ивмреадер:: жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) этот метод создает выходной объект свойств носителя, который содержит свойства выходного формата по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce72a-112">An output media properties object is created by [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) This method creates an output media properties object that contains the properties of the default output format.</span></span> <span data-ttu-id="ce72a-113">Для выходных данных могут поддерживаться и другие форматы.</span><span class="sxs-lookup"><span data-stu-id="ce72a-113">Other formats may be supported for an output.</span></span> <span data-ttu-id="ce72a-114">Чтобы получить дополнительные выходные форматы, можно вызвать [**ивмреадер:: жетаутпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) , чтобы получить количество поддерживаемых выходных форматов, а затем прокручивать их с помощью вызовов [**Ивмреадер:: жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span><span class="sxs-lookup"><span data-stu-id="ce72a-114">To obtain additional output formats, you can call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported output formats and then loop through them using calls to [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span></span> <span data-ttu-id="ce72a-115">**Жетаутпутформат** создает выходной объект свойств мультимедиа, заполненный данными для выбранного формата выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ce72a-115">**GetOutputFormat** creates an output media properties object populated with the data for the selected output format.</span></span>

<span data-ttu-id="ce72a-116">Объекты свойств выходных данных мультимедиа также можно создать с помощью синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="ce72a-116">Output media properties objects can also be created with the synchronous reader.</span></span> <span data-ttu-id="ce72a-117">Все имена методов идентичны параметрам в модуле чтения, и все они предоставляются интерфейсом [**ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="ce72a-117">All of the method names are identical to those in the reader and they are all exposed by the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

<span data-ttu-id="ce72a-118">**Жетаутпутпропс** и **жетаутпутформат** устанавливают указатель на интерфейс [**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) .</span><span class="sxs-lookup"><span data-stu-id="ce72a-118">**GetOutputProps** and **GetOutputFormat** both set a pointer to an [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface.</span></span> <span data-ttu-id="ce72a-119">Другие интерфейсы объекта выходных свойств мультимедиа можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="ce72a-119">The other interfaces of the output media properties object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="ce72a-120">Каждый объект свойств выходного носителя поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ce72a-120">The following interfaces are supported by every output media properties object.</span></span>



| <span data-ttu-id="ce72a-121">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ce72a-121">Interface</span></span>                                          | <span data-ttu-id="ce72a-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ce72a-122">Description</span></span>                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce72a-123">**ивммедиапропс**</span><span class="sxs-lookup"><span data-stu-id="ce72a-123">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | <span data-ttu-id="ce72a-124">Используется в качестве базового интерфейса для других интерфейсов свойств мультимедиа (входные, выходные и видео).</span><span class="sxs-lookup"><span data-stu-id="ce72a-124">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="ce72a-125">**ивмаутпутмедиапропс**</span><span class="sxs-lookup"><span data-stu-id="ce72a-125">**IWMOutputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | <span data-ttu-id="ce72a-126">Извлекает свойства выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ce72a-126">Retrieves the properties of an output.</span></span>                                                                     |
| [<span data-ttu-id="ce72a-127">**ивмвидеомедиапропс**</span><span class="sxs-lookup"><span data-stu-id="ce72a-127">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | <span data-ttu-id="ce72a-128">Управляет свойствами потока видео.</span><span class="sxs-lookup"><span data-stu-id="ce72a-128">Manages the properties of a video stream.</span></span> <span data-ttu-id="ce72a-129">Это необязательный интерфейс, доступный только для потоков видео.</span><span class="sxs-lookup"><span data-stu-id="ce72a-129">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ce72a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ce72a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce72a-131">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="ce72a-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="ce72a-132">**Объект модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="ce72a-132">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




