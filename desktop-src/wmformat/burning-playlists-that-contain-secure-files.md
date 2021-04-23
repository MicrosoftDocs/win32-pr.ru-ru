---
title: Запись на компакт-диск списков воспроизведения, содержащих защищенные файлы
description: Запись на компакт-диск списков воспроизведения, содержащих защищенные файлы
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, запись списков воспроизведения с защищенными файлами
- Windows Media Format SDK, списки воспроизведения с защищенными файлами
- Расширенный формат систем (ASF), запись списков воспроизведения с защищенными файлами
- ASF (Расширенный системный формат), запись списков воспроизведения с защищенными файлами
- Расширенный формат систем (ASF), списки воспроизведения с защищенными файлами
- ASF (Расширенный системный формат), списки воспроизведения с защищенными файлами
- Управление цифровыми правами (DRM), запись списков воспроизведения с защищенными файлами
- DRM (Управление цифровыми правами), запись списков воспроизведения с защищенными файлами
- Управление цифровыми правами (DRM), списки воспроизведения с защищенными файлами
- DRM (Управление цифровыми правами), списки воспроизведения с защищенными файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "105710251"
---
# <a name="burning-playlists-that-contain-secure-files"></a><span data-ttu-id="5e75b-113">Запись на компакт-диск списков воспроизведения, содержащих защищенные файлы</span><span class="sxs-lookup"><span data-stu-id="5e75b-113">Burning Playlists That Contain Secure Files</span></span>

<span data-ttu-id="5e75b-114">Лицензии, созданные с помощью объектов пакета SDK Windows Media Rights Manager 10, могут указать право на копирование файла на компакт-диск в составе списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5e75b-114">Licenses created by using the objects of the Windows Media Rights Manager 10 SDK can specify the right to copy a file to compact disc as part of a playlist.</span></span> <span data-ttu-id="5e75b-115">Эта функция, называемая записью списка воспроизведения, требует проверки лицензий всех файлов в списке воспроизведения перед началом копирования данных.</span><span class="sxs-lookup"><span data-stu-id="5e75b-115">This feature, called playlist burning, requires that you verify the licenses of all of the files in the playlist before starting to copy data.</span></span> <span data-ttu-id="5e75b-116">Пакет SDK для Windows Media Format предоставляет интерфейс [**ивмреадерплайлистбурн**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) для выполнения проверки файлов.</span><span class="sxs-lookup"><span data-stu-id="5e75b-116">The Windows Media Format SDK provides the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface to perform file verification for you.</span></span>

<span data-ttu-id="5e75b-117">Чтобы реализовать запись списка воспроизведения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5e75b-117">To implement playlist burning, perform the following steps:</span></span>

1.  <span data-ttu-id="5e75b-118">Создайте экземпляр объекта Reader или синхронный объект Reader.</span><span class="sxs-lookup"><span data-stu-id="5e75b-118">Create an instance of the reader object, or the synchronous reader object.</span></span> <span data-ttu-id="5e75b-119">Дополнительные сведения см. в разделе [чтение файлов ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="5e75b-119">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="5e75b-120">Вызовите метод **QueryInterface** интерфейса чтения ([**ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) или [**ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)), чтобы получить указатель на интерфейс [**ивмреадерплайлистбурн**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .</span><span class="sxs-lookup"><span data-stu-id="5e75b-120">Call the **QueryInterface** method of the reader interface ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) or [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) to obtain a pointer to the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface.</span></span>
3.  <span data-ttu-id="5e75b-121">Скопируйте имена файлов из списка воспроизведения в массив строк расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="5e75b-121">Copy the file names from the playlist into an array of wide-character strings.</span></span> <span data-ttu-id="5e75b-122">Имена файлов в массиве должны быть в том же порядке, в котором они отображаются в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5e75b-122">The file names in the array must be in the same order as they appear in the playlist.</span></span>
4.  <span data-ttu-id="5e75b-123">Вызовите метод [**ивмреадерплайлистбурн:: инитплайлистбурн**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , передав указатель на массив, созданный на шаге 3, для инициализации проверки лицензии для файлов.</span><span class="sxs-lookup"><span data-stu-id="5e75b-123">Call the [**IWMReaderPlaylistBurn::InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) method, passing in a pointer to the array created in step 3, to initialize the license verification for the files.</span></span>
5.  <span data-ttu-id="5e75b-124">После завершения проверки лицензии объект Reader отправляет \_ \_ сообщение о записи списка воспроизведения ВМТ init \_ в реализацию метода обратного вызова [**Ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="5e75b-124">When the license verification is completed, the reader object sends a WMT\_INIT\_PLAYLIST\_BURN message to your implementation of the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="5e75b-125">Когда ответный вызов получает это сообщение, вызовите метод [**ивмреадерплайлистбурн:: жетинитресултс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) , чтобы получить результаты проверки лицензии.</span><span class="sxs-lookup"><span data-stu-id="5e75b-125">When your callback receives this message, call the [**IWMReaderPlaylistBurn::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) method to get the results of the license check.</span></span> <span data-ttu-id="5e75b-126">Этот метод принимает массив переменных **HRESULT** , соответствующих именам файлов в массиве, переданном в **инитплайлистбурн**.</span><span class="sxs-lookup"><span data-stu-id="5e75b-126">This method takes an array of **HRESULT** variables that correspond to the file names in the array passed to **InitPlaylistBurn**.</span></span> <span data-ttu-id="5e75b-127">Если все значения в результирующем массиве равны S \_ , можно продолжить.</span><span class="sxs-lookup"><span data-stu-id="5e75b-127">If all of the values in the result array are equal to S\_OK, you can continue.</span></span> <span data-ttu-id="5e75b-128">Если какой-либо из результатов является кодом ошибки, список воспроизведения не должен быть скопирован.</span><span class="sxs-lookup"><span data-stu-id="5e75b-128">If any result is an error code, the playlist must not be copied.</span></span>
6.  <span data-ttu-id="5e75b-129">Используя тот же экземпляр модуля чтения, откройте и прочтите каждый файл.</span><span class="sxs-lookup"><span data-stu-id="5e75b-129">Using the same instance of the reader, open and read each file.</span></span> <span data-ttu-id="5e75b-130">Необходимо открыть файлы в том порядке, в котором имена файлов появлялись в массиве имен файлов, переданном в **инитплайлистбурн**.</span><span class="sxs-lookup"><span data-stu-id="5e75b-130">You must open the files in the order in which the file names appeared in the file name array passed to **InitPlaylistBurn**.</span></span>
7.  <span data-ttu-id="5e75b-131">После копирования всех файлов в список воспроизведения вызовите [**ивмреадерплайлистбурн:: ендплайлистбурн**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) , чтобы завершить процесс записи списка воспроизведения и освободить ресурсы, используемые модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="5e75b-131">When you have copied all of the files in the playlist, call the [**IWMReaderPlaylistBurn::EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) to complete the playlist burn process and free the resources used by the reader.</span></span>

> [!Note]  
> <span data-ttu-id="5e75b-132">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="5e75b-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5e75b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="5e75b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e75b-134">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="5e75b-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




