---
title: Использование маркеров
description: Использование маркеров
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, маркеры
- Расширенный формат систем (ASF), маркеры
- ASF (Расширенный системный формат), маркеры
- Расширенный системный формат (ASF), Поиск маркеров
- ASF (Расширенный системный формат), Поиск маркеров
- маркеры, сведения
- маркеры, добавление
- маркеры, удаление
- маркеры, извлечение
- маркеры, Поиск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789234"
---
# <a name="using-markers"></a><span data-ttu-id="40135-113">Использование маркеров</span><span class="sxs-lookup"><span data-stu-id="40135-113">Using Markers</span></span>

<span data-ttu-id="40135-114">*Маркер* — это именованная точка в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="40135-114">A *marker* is a named point within an ASF file.</span></span> <span data-ttu-id="40135-115">Каждый маркер состоит из имени и связанного времени, измеряемого как смещение от начала файла.</span><span class="sxs-lookup"><span data-stu-id="40135-115">Each marker consists of a name and an associated time, measured as an offset from the start of the file.</span></span> <span data-ttu-id="40135-116">Приложение может использовать маркеры для назначения имен различным точкам внутри содержимого, отображать эти имена пользователю, а затем искать позиции маркеров.</span><span class="sxs-lookup"><span data-stu-id="40135-116">An application can use markers to assign names to various points within the content, display those names to the user, and then seek to the marker positions.</span></span> <span data-ttu-id="40135-117">Приложение может добавлять или удалять маркеры из существующего файла ASF.</span><span class="sxs-lookup"><span data-stu-id="40135-117">An application can add or remove markers from an existing ASF file.</span></span>

<span data-ttu-id="40135-118">Интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) содержит методы для работы с маркерами.</span><span class="sxs-lookup"><span data-stu-id="40135-118">The [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface contains methods for working with markers.</span></span> <span data-ttu-id="40135-119">Объект редактора метаданных поддерживает добавление и удаление маркеров.</span><span class="sxs-lookup"><span data-stu-id="40135-119">The metadata editor object supports adding and removing markers.</span></span> <span data-ttu-id="40135-120">Объекты Writer и Reader могут извлекать маркеры, но не могут добавлять или удалять маркеры.</span><span class="sxs-lookup"><span data-stu-id="40135-120">The writer and reader objects can retrieve markers but cannot add or remove markers.</span></span>

## <a name="adding-markers"></a><span data-ttu-id="40135-121">Добавление маркеров</span><span class="sxs-lookup"><span data-stu-id="40135-121">Adding Markers</span></span>

<span data-ttu-id="40135-122">Чтобы добавить маркер, запросите редактор метаданных для интерфейса **ивмхеадеринфо** .</span><span class="sxs-lookup"><span data-stu-id="40135-122">To add a marker, query the metadata editor for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="40135-123">Затем вызовите метод [**ивмхеадеринфо:: аддмаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , указав имя маркера в виде строки расширенных символов и время в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="40135-123">Then call the [**IWMHeaderInfo::AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) method, specifying the marker name as a wide-character string and the time in 100-nanosecond units.</span></span> <span data-ttu-id="40135-124">Время не должно превышать длительность файла.</span><span class="sxs-lookup"><span data-stu-id="40135-124">The time must not exceed the file duration.</span></span> <span data-ttu-id="40135-125">Два маркера могут иметь одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="40135-125">Two markers can have the same time.</span></span>

<span data-ttu-id="40135-126">В следующем примере в файл добавляется несколько маркеров:</span><span class="sxs-lookup"><span data-stu-id="40135-126">The following example adds several markers to a file:</span></span>


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a><span data-ttu-id="40135-127">Удаление маркеров</span><span class="sxs-lookup"><span data-stu-id="40135-127">Removing Markers</span></span>

<span data-ttu-id="40135-128">Чтобы удалить маркер, вызовите [**ивмхеадеринфо:: ремовемаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), указав индекс удаляемого маркера.</span><span class="sxs-lookup"><span data-stu-id="40135-128">To remove a marker, call [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specifying the index of the marker to remove.</span></span> <span data-ttu-id="40135-129">Маркеры автоматически сортируются в порядке возрастания времени, поэтому индекс 0 всегда является первым маркером.</span><span class="sxs-lookup"><span data-stu-id="40135-129">Markers are automatically sorted in increasing time order, so index 0 is always the first marker.</span></span> <span data-ttu-id="40135-130">Обратите внимание, что вызов **ремовемаркер** изменяет номера индексов следующих маркеров.</span><span class="sxs-lookup"><span data-stu-id="40135-130">Note that calling **RemoveMarker** changes the index numbers of any markers that follow.</span></span> <span data-ttu-id="40135-131">Следующий код, где *пинфо* — это указатель на интерфейс **ивмхеадеринфо** , удаляет все маркеры из файла:</span><span class="sxs-lookup"><span data-stu-id="40135-131">The following code, where *pInfo* is a pointer to an **IWMHeaderInfo** interface, removes all the markers from a file:</span></span>


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a><span data-ttu-id="40135-132">Получение маркеров</span><span class="sxs-lookup"><span data-stu-id="40135-132">Retrieving Markers</span></span>

<span data-ttu-id="40135-133">Чтобы получить имя и время маркера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40135-133">To retrieve the name and time of a marker, perform the following steps:</span></span>

1.  <span data-ttu-id="40135-134">Вызовите метод [**ивмхеадеринфо:: жетмаркеркаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) , чтобы определить, сколько маркеров содержит файл.</span><span class="sxs-lookup"><span data-stu-id="40135-134">Call the [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) method to determine how many markers the file contains.</span></span>
2.  <span data-ttu-id="40135-135">Получение размера строки, необходимой для хранения имени маркера.</span><span class="sxs-lookup"><span data-stu-id="40135-135">Retrieve the size of the string needed to contain the marker name.</span></span> <span data-ttu-id="40135-136">Чтобы сделать это, вызовите метод [**ивмхеадеринфо:: @ Mark**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) .</span><span class="sxs-lookup"><span data-stu-id="40135-136">To do so, call the [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) method.</span></span> <span data-ttu-id="40135-137">Укажите индекс извлекаемого маркера и **значение NULL** для буфера строки (параметр *пвсзмаркернаме* ).</span><span class="sxs-lookup"><span data-stu-id="40135-137">Specify the index of the marker to retrieve, and **NULL** for the string buffer (the *pwszMarkerName* parameter).</span></span> <span data-ttu-id="40135-138">Метод возвращает длину строки, включая завершающий \\ символ "0", в параметре *пкчмаркернамелен* .</span><span class="sxs-lookup"><span data-stu-id="40135-138">The method returns the length of the string, including the terminating '\\0' character, in the *pcchMarkerNameLen* parameter.</span></span>
3.  <span data-ttu-id="40135-139">Выделить строку расширенных символов для получения имени.</span><span class="sxs-lookup"><span data-stu-id="40135-139">Allocate a wide-character string to receive the name.</span></span>
4.  <span data-ttu-id="40135-140">Снова  вызовите метод GetString, но в это время передайте адрес строки в параметре *пвсзмаркернаме* .</span><span class="sxs-lookup"><span data-stu-id="40135-140">Call **GetMarker** again, but this time pass the address of the string in the *pwszMarkerName* parameter.</span></span> <span data-ttu-id="40135-141">Метод записывает имя маркера в строку и возвращает время метки в параметре *пкнсмаркертиме* .</span><span class="sxs-lookup"><span data-stu-id="40135-141">The method writes the marker name into the string, and returns the marker time in the *pcnsMarkerTime* parameter.</span></span>

<span data-ttu-id="40135-142">В следующем коде каждый маркер перебирается по порядку и получает имя и время:</span><span class="sxs-lookup"><span data-stu-id="40135-142">The following code loops through every marker in order and retrieves the name and time:</span></span>


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a><span data-ttu-id="40135-143">Поиск маркера</span><span class="sxs-lookup"><span data-stu-id="40135-143">Seeking to a Marker</span></span>

<span data-ttu-id="40135-144">Чтобы начать воспроизведение из расположения маркера, вызовите метод [**IWMReaderAdvanced2:: стартатмаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) объекта Reader, указав индекс маркера.</span><span class="sxs-lookup"><span data-stu-id="40135-144">To start playback from a marker location, call the reader object's [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) method, specifying the index of the marker.</span></span> <span data-ttu-id="40135-145">Остальные параметры идентичны параметрам метода [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) .</span><span class="sxs-lookup"><span data-stu-id="40135-145">The remaining parameters are identical to those for the [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) method.</span></span> <span data-ttu-id="40135-146">В следующем примере производится запрос к модулю чтения для интерфейса [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) и осуществляется поиск первого маркера.</span><span class="sxs-lookup"><span data-stu-id="40135-146">The following example queries the reader for the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface and seeks to the first marker.</span></span>


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="40135-147">См. также</span><span class="sxs-lookup"><span data-stu-id="40135-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40135-148">**Интерфейс Ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="40135-148">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="40135-149">**IWMReaderAdvanced2:: Стартатмаркер**</span><span class="sxs-lookup"><span data-stu-id="40135-149">**IWMReaderAdvanced2::StartAtMarker**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[<span data-ttu-id="40135-150">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="40135-150">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




