---
title: Сохранение содержимого
description: Сохранение содержимого
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, сохранение содержимого
- Windows Media Format SDK, Быстрая потоковая передача кэша
- Расширенный формат систем (ASF), сохранение содержимого
- ASF (Расширенный системный формат), сохранение содержимого
- Расширенный системный формат (ASF), Быстрая потоковая передача кэша
- ASF (Расширенный системный формат), Быстрая потоковая передача кэша
- потоки, сохранение содержимого
- Быстрая потоковая передача кэша, сохранение содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789210"
---
# <a name="saving-content"></a><span data-ttu-id="c48ab-111">Сохранение содержимого</span><span class="sxs-lookup"><span data-stu-id="c48ab-111">Saving Content</span></span>

<span data-ttu-id="c48ab-112">С помощью этого пакета SDK приложение может сохранить загруженное или потоковое содержимое на локальном компьютере пользователя, вызвав метод [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="c48ab-112">By using this SDK, an application can save downloaded or streamed content to the user's local computer, by calling the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) method on the reader object.</span></span> <span data-ttu-id="c48ab-113">Для потокового содержимого сервер должен использовать быструю потоковую передачу кэша, как описано в разделе [Включение быстрой потоковой передачи кэша от клиента](enabling-fast-cache-streaming-from-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="c48ab-113">For streamed content, the server must be using Fast Cache streaming, which is described in the section [Enabling Fast Cache Streaming from the Client](enabling-fast-cache-streaming-from-the-client.md).</span></span> <span data-ttu-id="c48ab-114">Для потокового содержимого метод **SaveFileAs** создает ASX файл, указывающий на ASF файл, содержащий сохраненное содержимое.</span><span class="sxs-lookup"><span data-stu-id="c48ab-114">For streamed content, the **SaveFileAs** method creates an ASX file that points to an ASF file containing the saved content.</span></span> <span data-ttu-id="c48ab-115">Если объект модуля чтения потоковой передачи списка воспроизведения на стороне сервера, каждая запись сохраняется в виде отдельного ASF-файла, а файл ASX указывает на каждый из файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="c48ab-115">If the reader object is streaming a server-side playlist, each entry is saved as a separate ASF file, and the ASX file points to each of the ASF files.</span></span> <span data-ttu-id="c48ab-116">Для загруженного содержимого метод **SaveFileAs** просто создает файл ASF.</span><span class="sxs-lookup"><span data-stu-id="c48ab-116">For downloaded content, the **SaveFileAs** method simply creates an ASF file.</span></span>

<span data-ttu-id="c48ab-117">Чтобы сохранить содержимое в локальном файле, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c48ab-117">To save content to a local file, do the following:</span></span>

1.  <span data-ttu-id="c48ab-118">Вызовите [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="c48ab-118">Call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) with the URL.</span></span> <span data-ttu-id="c48ab-119">**Open** является асинхронным вызовом и возвращается немедленно.</span><span class="sxs-lookup"><span data-stu-id="c48ab-119">**Open** is an asynchronous call, and returns immediately.</span></span> <span data-ttu-id="c48ab-120">Дождитесь завершения операции, как описано в разделе [Создание читателя и открытие файла](to-create-a-reader-and-open-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="c48ab-120">Wait for the operation to complete, as described in [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md).</span></span>
2.  <span data-ttu-id="c48ab-121">Запросите объект модуля чтения для интерфейса [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .</span><span class="sxs-lookup"><span data-stu-id="c48ab-121">Query the reader object for the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface.</span></span>
3.  <span data-ttu-id="c48ab-122">Проверьте, можно ли сохранить содержимое, вызвав метод [**IWMReaderAdvanced4:: кансавефилеас**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) .</span><span class="sxs-lookup"><span data-stu-id="c48ab-122">Check whether the content can be saved by calling the [**IWMReaderAdvanced4::CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) method.</span></span> <span data-ttu-id="c48ab-123">Если метод возвращает значение false, содержимое не может быть сохранено локально.</span><span class="sxs-lookup"><span data-stu-id="c48ab-123">If the method returns False, the content cannot be saved locally.</span></span> <span data-ttu-id="c48ab-124">В противном случае перейдите к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="c48ab-124">Otherwise, proceed to step 4.</span></span>
4.  <span data-ttu-id="c48ab-125">Вызовите метод [**IWMReaderAdvanced4:: исусингфасткаче**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) , чтобы определить, использует ли сервер быструю потоковую передачу кэша.</span><span class="sxs-lookup"><span data-stu-id="c48ab-125">Call the [**IWMReaderAdvanced4::IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) method to determine whether the server is using Fast Cache streaming.</span></span>
5.  <span data-ttu-id="c48ab-126">Вызовите [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) с именем файла для локального файла.</span><span class="sxs-lookup"><span data-stu-id="c48ab-126">Call the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) with a file name for the local file.</span></span> <span data-ttu-id="c48ab-127">Если метод **исусингфасткаче** возвращает значение true, присвойте файлу расширение ASX.</span><span class="sxs-lookup"><span data-stu-id="c48ab-127">If the **IsUsingFastCache** method returned True, give the file name an .asx extension.</span></span> <span data-ttu-id="c48ab-128">В противном случае укажите имя файла с расширением ASF, WMA или WMV.</span><span class="sxs-lookup"><span data-stu-id="c48ab-128">Otherwise, give the file name an .asf, .wma, or .wmv extension.</span></span>

<span data-ttu-id="c48ab-129">Приложение может отменить операцию сохранения во время выполнения, вызвав метод [**IWMReaderAdvanced4:: канцелсавефилеас**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .</span><span class="sxs-lookup"><span data-stu-id="c48ab-129">The application can cancel the save operation while it is in progress, by calling the [**IWMReaderAdvanced4::CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) method.</span></span>

<span data-ttu-id="c48ab-130">Сохраненное содержимое может быть защищено с помощью DRM, поэтому может оказаться невозможным воспроизведение файла на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="c48ab-130">The saved content might be protected with DRM, so it may not be possible to play the file on another computer.</span></span> <span data-ttu-id="c48ab-131">Дополнительные сведения о защите содержимого см. в статье [функции цифрового Rights Management](digital-rights-management-features.md).</span><span class="sxs-lookup"><span data-stu-id="c48ab-131">For more information on content protection, see [Digital Rights Management Features](digital-rights-management-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c48ab-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c48ab-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c48ab-133">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="c48ab-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="c48ab-134">**Интерфейс IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="c48ab-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




