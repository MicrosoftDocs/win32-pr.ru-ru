---
title: Поддержка нескольких языков
description: Поддержка нескольких языков
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Пакет Windows Media Format SDK, поддерживающий несколько языков
- Пакет SDK для Windows Media Format, поддержка нескольких языков
- Windows Media Format SDK, языковая поддержка
- Расширенный формат систем (ASF), поддерживающий несколько языков
- ASF (Расширенный системный формат), поддержка нескольких языков
- Расширенный формат систем (ASF), поддержка нескольких языков
- ASF (Расширенный системный формат), поддержка нескольких языков
- Расширенный системный формат (ASF), поддержка языков
- ASF (Расширенный системный формат), поддержка языков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103987272"
---
# <a name="to-support-multiple-languages"></a><span data-ttu-id="16879-112">Поддержка нескольких языков</span><span class="sxs-lookup"><span data-stu-id="16879-112">To Support Multiple Languages</span></span>

<span data-ttu-id="16879-113">Можно поддерживать несколько языков в потоках и в метаданных.</span><span class="sxs-lookup"><span data-stu-id="16879-113">You can support multiple languages both in streams and in metadata.</span></span> <span data-ttu-id="16879-114">Основой поддержки нескольких языков в пакете SDK для Windows Media Format является интерфейс [**ивмлангуажелист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , который поддерживает список поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="16879-114">The core of multiple language support in the Windows Media Format SDK is the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface, which maintains a list of the languages supported.</span></span> <span data-ttu-id="16879-115">Список языков предоставляет каждому поддерживаемому языку индекс, который используется в различных объектах пакета SDK при работе с несколькими языками.</span><span class="sxs-lookup"><span data-stu-id="16879-115">The language list gives each supported language an index, which is used in various objects in the SDK when dealing with the multiple languages.</span></span>

<span data-ttu-id="16879-116">Метод [**ивмлангуажелист:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) добавляет язык в список.</span><span class="sxs-lookup"><span data-stu-id="16879-116">The [**IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) method adds a language to the list.</span></span> <span data-ttu-id="16879-117">Вы можете узнать, какие языки уже находятся в списке, получая общее число языков с помощью [**ивмлангуажелист:: жетлангуажекаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) , а затем прокручивать языки, вызывающие [**Ивмлангуажелист:: жетлангуажедетаилс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) для каждого.</span><span class="sxs-lookup"><span data-stu-id="16879-117">You can identify the languages already in the list by obtaining the total number of languages with [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) and then looping through the languages calling [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) for each.</span></span> <span data-ttu-id="16879-118">Индекс языка отсчитывается от нуля.</span><span class="sxs-lookup"><span data-stu-id="16879-118">The language index is zero based.</span></span>

## <a name="to-configure-mutual-exclusion-by-language"></a><span data-ttu-id="16879-119">Настройка взаимного исключения по языку</span><span class="sxs-lookup"><span data-stu-id="16879-119">To Configure Mutual Exclusion by Language</span></span>

<span data-ttu-id="16879-120">Настройка простого взаимоисключающего объекта по языку очень проста.</span><span class="sxs-lookup"><span data-stu-id="16879-120">Configuring a simple mutual exclusion object by language is very simple.</span></span> <span data-ttu-id="16879-121">Теперь каждый поток связан с языком.</span><span class="sxs-lookup"><span data-stu-id="16879-121">Each stream is now associated with a language.</span></span> <span data-ttu-id="16879-122">Язык, связанный с потоком, можно задать с помощью [**IWMStreamConfig3:: сетлангуаже**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span><span class="sxs-lookup"><span data-stu-id="16879-122">The language associated with a stream can be set using [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span></span> <span data-ttu-id="16879-123">После настройки всех взаимоисключающих потоков просто создайте объект взаимного исключения, как для любого другого типа.</span><span class="sxs-lookup"><span data-stu-id="16879-123">After all of the mutually exclusive streams are configured, simply create a mutual exclusion object as you would for any other type.</span></span> <span data-ttu-id="16879-124">Затем вызовите [**ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) \_ , передав язык CLSID вммутекс \_ для типа.</span><span class="sxs-lookup"><span data-stu-id="16879-124">Then call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passing CLSID\_WMMUTEX\_Language for the type.</span></span>

<span data-ttu-id="16879-125">Потоки, которые являются взаимоисключающими по языку, становятся более сложными, когда эксклюзивные потоки также взаимоисключающи по скорости потока.</span><span class="sxs-lookup"><span data-stu-id="16879-125">Streams that are mutually exclusive by language become more complicated when the exclusive streams are also mutually exclusive by bit rate.</span></span> <span data-ttu-id="16879-126">В этом случае необходимо использовать взаимоисключающие записи, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="16879-126">In this case you must use mutually exclusive records, by performing the following steps:</span></span>

1.  <span data-ttu-id="16879-127">Создайте объект взаимного исключения для потоков с разными скоростями разрядов на каждом языке.</span><span class="sxs-lookup"><span data-stu-id="16879-127">Create a mutual exclusion object for the streams of differing bit rates in each language.</span></span> <span data-ttu-id="16879-128">Дополнительные сведения о создании взаимоисключающего объекта по скорости потока см. в разделе Использование нескольких взаимоисключающих [исключений с несколькими битовыми частотами](using-multiple-bit-rate-mutual-exclusion.md).</span><span class="sxs-lookup"><span data-stu-id="16879-128">For more information about creating a mutual exclusion object by bit rate, see [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).</span></span>
2.  <span data-ttu-id="16879-129">Создайте объект взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="16879-129">Create a mutual exclusion object.</span></span> <span data-ttu-id="16879-130">Вызовите [**ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) и передайте \_ язык CLSID вммутекс, \_ чтобы указать исключительные права по языку.</span><span class="sxs-lookup"><span data-stu-id="16879-130">Call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) and pass CLSID\_WMMUTEX\_Language to specify exclusivity by language.</span></span>
3.  <span data-ttu-id="16879-131">Получите указатель на интерфейс [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) объекта взаимного исключения, созданного на шаге 2, вызвав метод **QueryInterface** [**ивммутуалексклусион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="16879-131">Obtain a pointer to the [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) interface of the mutual exclusion object created in step 2 by calling the **QueryInterface** method of [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span></span>
4.  <span data-ttu-id="16879-132">Вызовите метод [**IWMMutualExclusion2:: аддрекорд**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) один раз для каждого языка, чтобы создать записи потока, которые будут взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="16879-132">Call the [**IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) method once for each language, to create stream records that will be mutually exclusive.</span></span>
5.  <span data-ttu-id="16879-133">Для каждой записи, созданной на шаге 4, добавьте потоки соответствующего языка с вызовами метода [**IWMMutualExclusion2:: аддстреамфоррекорд**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span><span class="sxs-lookup"><span data-stu-id="16879-133">For each record created in step 4, add the streams of the appropriate language with calls to [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span></span>

## <a name="to-read-files-with-multiple-languages"></a><span data-ttu-id="16879-134">Чтение файлов с несколькими языками</span><span class="sxs-lookup"><span data-stu-id="16879-134">To Read Files with Multiple Languages</span></span>

<span data-ttu-id="16879-135">Объект "читатель" предоставляет методы для обнаружения доступных языков потоков в файле.</span><span class="sxs-lookup"><span data-stu-id="16879-135">The reader object provides methods to identify the available languages of streams in a file.</span></span> <span data-ttu-id="16879-136">Число поддерживаемых языков для выходных данных можно получить, вызвав [**IWMReaderAdvanced4:: жетлангуажекаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span><span class="sxs-lookup"><span data-stu-id="16879-136">You can retrieve the number of supported languages for an output by calling [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span></span> <span data-ttu-id="16879-137">Затем можно получить сведения о каждом языке с вызовами [**IWMReaderAdvanced4:: onlanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span><span class="sxs-lookup"><span data-stu-id="16879-137">You can then retrieve details about each language with calls to [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span></span>

<span data-ttu-id="16879-138">Можно указать язык для воспроизведения, передав индекс этого языка в средство чтения с помощью вызова [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="16879-138">You can specify the language to play by passing the index of that language to the reader with a call to [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span> <span data-ttu-id="16879-139">Это позволит выбрать указанный язык при сохранении автоматического выбора потоков для любых других взаимоисключающих объектов в файле.</span><span class="sxs-lookup"><span data-stu-id="16879-139">This will select the specified language while maintaining automatic stream selection for any other mutual exclusion objects in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16879-140">См. также</span><span class="sxs-lookup"><span data-stu-id="16879-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16879-141">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="16879-141">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="16879-142">**Интерфейс Ивмлангуажелист**</span><span class="sxs-lookup"><span data-stu-id="16879-142">**IWMLanguageList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[<span data-ttu-id="16879-143">**Интерфейс Ивммутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="16879-143">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="16879-144">**Интерфейс IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="16879-144">**IWMMutualExclusion2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[<span data-ttu-id="16879-145">**Интерфейс IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="16879-145">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="16879-146">**Интерфейс IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="16879-146">**IWMReaderAdvanced4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[<span data-ttu-id="16879-147">**Интерфейс IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="16879-147">**IWMStreamConfig3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




