---
title: Запись образа диска
description: Основное (запись диска) с помощью IMAPI состоит из следующих этапов создания образа файловой системы, содержащего каталоги и файлы для записи на диск. Настройте устройство записи дисков для взаимодействия с оптическим устройством. Создайте модуль записи данных и запишите образ на диск.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337193"
---
# <a name="burning-a-disc-image"></a><span data-ttu-id="f1c34-103">Запись образа диска</span><span class="sxs-lookup"><span data-stu-id="f1c34-103">Burning a Disc Image</span></span>

<span data-ttu-id="f1c34-104">Основной процесс (запись диска) с помощью IMAPI состоит из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="f1c34-104">Mastering (burning a disc) using IMAPI consists of the following steps:</span></span>

1.  <span data-ttu-id="f1c34-105">Создайте образ файловой системы, содержащий каталоги и файлы для записи на диск.</span><span class="sxs-lookup"><span data-stu-id="f1c34-105">Construct a file system image that contains the directories and files to write disc.</span></span>
2.  <span data-ttu-id="f1c34-106">[Настройте устройство записи дисков](#set-up-a-disc-recorder) для взаимодействия с оптическим устройством.</span><span class="sxs-lookup"><span data-stu-id="f1c34-106">[Set up a disc recorder](#set-up-a-disc-recorder) to communicate with the optical device.</span></span>
3.  <span data-ttu-id="f1c34-107">[Создайте модуль записи данных](#create-a-data-writer-and-write-the-burn-image) и запишите образ на диск.</span><span class="sxs-lookup"><span data-stu-id="f1c34-107">[Create a data writer](#create-a-data-writer-and-write-the-burn-image) and burn the image to disc.</span></span>

<span data-ttu-id="f1c34-108">Пример, в котором записывается образ диска, см. в разделе [пример на языке VBScript](#vbscript-example).</span><span class="sxs-lookup"><span data-stu-id="f1c34-108">For an example that burns a disc image, see [VBScript example](#vbscript-example).</span></span>

## <a name="construct-a-burn-image"></a><span data-ttu-id="f1c34-109">Создание образа записи</span><span class="sxs-lookup"><span data-stu-id="f1c34-109">Construct a burn image</span></span>

<span data-ttu-id="f1c34-110">Образ записи — это поток данных, готовый для записи на оптические носители.</span><span class="sxs-lookup"><span data-stu-id="f1c34-110">A burn image is a data stream that is ready to be written to optical media.</span></span> <span data-ttu-id="f1c34-111">Образ записи для форматов ISO9660, Жолиет и UDF состоит из файловой системы отдельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="f1c34-111">The burn image for ISO9660, Joliet and UDF formats consists of a file system of individual files and directories.</span></span> <span data-ttu-id="f1c34-112">Объект **кфилесистемимаже** — это объект файловой системы, содержащий файлы и каталоги для размещения на оптическом носителе.</span><span class="sxs-lookup"><span data-stu-id="f1c34-112">The **CFileSystemImage** object is the file system object that holds the files and directories to place on the optical media.</span></span> <span data-ttu-id="f1c34-113">Интерфейс [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) предоставляет доступ к объекту и параметрам файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f1c34-113">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>

<span data-ttu-id="f1c34-114">После создания объекта файловой системы вызовите методы [**ифилесистемимаже:: креатефилеитем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) и [**Ифилесистемимаже:: креатедиректоритем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) для создания объектов File и Directory соответственно.</span><span class="sxs-lookup"><span data-stu-id="f1c34-114">After creating the file system object, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create the file and directory objects, respectively.</span></span> <span data-ttu-id="f1c34-115">Объекты File и Directory можно использовать для предоставления конкретных сведений о файле и каталоге.</span><span class="sxs-lookup"><span data-stu-id="f1c34-115">The file and directory objects can be used to provide specific details about the file and directory.</span></span> <span data-ttu-id="f1c34-116">Методы обработчика событий, доступные для [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) , могут определять текущий файл, добавляемый в образ файловой системы, число уже скопированных секторов и общее число секторов, которые будут скопированы.</span><span class="sxs-lookup"><span data-stu-id="f1c34-116">The event handler methods available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) can identify the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="f1c34-117">При необходимости загрузочный образ можно подключить к файловой системе с помощью свойства [**ифилесистемимаже::p UT \_ бутимажеоптионс**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) .</span><span class="sxs-lookup"><span data-stu-id="f1c34-117">Optionally, a boot image can be attached to the file system using the [**IFileSystemImage::put\_BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) property.</span></span> <span data-ttu-id="f1c34-118">Пример см. в разделе [Добавление загрузочного образа](adding-a-boot-image.md).</span><span class="sxs-lookup"><span data-stu-id="f1c34-118">For an example, see [Adding a Boot Image](adding-a-boot-image.md).</span></span>

<span data-ttu-id="f1c34-119">Наконец, вызовите [**ифилесистемимаже:: креатересултимаже**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) , чтобы создать поток данных и предоставить доступ через [**ифилесистемимажересулт**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span><span class="sxs-lookup"><span data-stu-id="f1c34-119">Finally, call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream and provides access through [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span></span> <span data-ttu-id="f1c34-120">Затем новый поток данных может быть предоставлен непосредственно методу [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) или сохранен в файл для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="f1c34-120">The new data stream can then be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>

## <a name="set-up-a-disc-recorder"></a><span data-ttu-id="f1c34-121">Настройка средства записи дисков</span><span class="sxs-lookup"><span data-stu-id="f1c34-121">Set up a disc recorder</span></span>

<span data-ttu-id="f1c34-122">Объект **MsftDiscMaster2** предоставляет перечисление оптических устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="f1c34-122">The **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="f1c34-123">Интерфейс [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) предоставляет доступ к результирующему перечислению устройств.</span><span class="sxs-lookup"><span data-stu-id="f1c34-123">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to the resultant device enumeration.</span></span> <span data-ttu-id="f1c34-124">Прохождение перечислений для нахождения соответствующего устройства записи.</span><span class="sxs-lookup"><span data-stu-id="f1c34-124">Traverse the enumerations to locate an appropriate recording device.</span></span> <span data-ttu-id="f1c34-125">Объект **MsftDiscMaster2** также предоставляет уведомления о событиях при добавлении или удалении оптических устройств с компьютера.</span><span class="sxs-lookup"><span data-stu-id="f1c34-125">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or deleted from a computer.</span></span>

<span data-ttu-id="f1c34-126">После нахождения оптического устройства записи и получения его идентификатора создайте объект **MsftDiscRecorder2** и инициализируйте средство записи с помощью идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="f1c34-126">After finding an optical recorder and retrieving its ID, create an **MsftDiscRecorder2** object and initialize the recorder using the device ID.</span></span> <span data-ttu-id="f1c34-127">Интерфейс [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) предоставляет доступ к объекту средства записи, а также к некоторым основным сведениям об устройстве, таким как идентификатор поставщика, идентификатор продукта, версия продукта и методы для извлечения носителя и закрытия области.</span><span class="sxs-lookup"><span data-stu-id="f1c34-127">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to the recorder object as well as some basic device information such as vendor ID, product ID, product revision, and methods to eject the media and close the tray.</span></span>

## <a name="create-a-data-writer-and-write-the-burn-image"></a><span data-ttu-id="f1c34-128">Создание модуля записи данных и запись образа записи</span><span class="sxs-lookup"><span data-stu-id="f1c34-128">Create a data writer and write the burn image</span></span>

<span data-ttu-id="f1c34-129">Объект **MsftDiscFormat2Data** предоставляет метод записи, свойства функции записи и свойства, относящиеся к носителю.</span><span class="sxs-lookup"><span data-stu-id="f1c34-129">The **MsftDiscFormat2Data** object provides the writing method, the properties about the write function and media-specific properties.</span></span> <span data-ttu-id="f1c34-130">Интерфейс [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) предоставляет доступ к объекту **MsftDiscFormat2Data** .</span><span class="sxs-lookup"><span data-stu-id="f1c34-130">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to the **MsftDiscFormat2Data** object.</span></span>

<span data-ttu-id="f1c34-131">Устройство записи дисков связывается с модулем записи формата с помощью свойства [**IDiscFormat2Data::p UT \_ Record**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="f1c34-131">The disc recorder links to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="f1c34-132">После привязки средства записи к модулю записи формата можно выполнять запросы к носителю и обновлять свойства, связанные с записью, перед записью полученного образа на диск с помощью метода [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="f1c34-132">After the recorder is bound to the format writer, you can perform queries regarding the media and update write-specific properties before writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

<span data-ttu-id="f1c34-133">Другие интерфейсы записи формата, предоставляемые IMAPI, работают аналогично. к дополнительным интерфейсам записи формата относятся:</span><span class="sxs-lookup"><span data-stu-id="f1c34-133">Other format writing interfaces provided by IMAPI work similarly; additional format writing interfaces include:</span></span>

-   <span data-ttu-id="f1c34-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) удаляет перезаписываемый оптический носитель.</span><span class="sxs-lookup"><span data-stu-id="f1c34-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) erases rewritable optical media.</span></span>
-   <span data-ttu-id="f1c34-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) записывает необработанный образ на оптический носитель.</span><span class="sxs-lookup"><span data-stu-id="f1c34-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) writes a raw image to optical media.</span></span>
-   <span data-ttu-id="f1c34-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) записывает звуковые дорожки на оптические носители.</span><span class="sxs-lookup"><span data-stu-id="f1c34-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) writes audio tracks to optical media.</span></span>

> [!Note]  
> <span data-ttu-id="f1c34-137">Переход в состояние электропитания может происходить во время операции записи (т. е. выход пользователя из системы или приостановки работы систем), что приводит к прерыванию процесса записи и возможной потери данных.</span><span class="sxs-lookup"><span data-stu-id="f1c34-137">It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the interruption of the burn process and possible data loss.</span></span> <span data-ttu-id="f1c34-138">Рекомендации по программированию см. [в статье предотвращение выхода из системы или приостановка выполнения во время записи](preventing-logoff-or-suspend-during-a-burn.md).</span><span class="sxs-lookup"><span data-stu-id="f1c34-138">For programming considerations, see [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="f1c34-139">Пример на языке VBScript</span><span class="sxs-lookup"><span data-stu-id="f1c34-139">VBScript example</span></span>

<span data-ttu-id="f1c34-140">В этом примере сценария показано, как использовать объекты IMAPI для записи оптического носителя. в частности, следует записать каталог на чистый диск. Код не содержит проверки на ошибки и предполагает следующее:</span><span class="sxs-lookup"><span data-stu-id="f1c34-140">This script example shows how to use the IMAPI objects to burn optical media; more specifically, write a directory to a blank disc. The code contains no error checking, and assumes the following:</span></span>

-   <span data-ttu-id="f1c34-141">В системе установлено совместимое устройство чтения.</span><span class="sxs-lookup"><span data-stu-id="f1c34-141">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="f1c34-142">Дисковое устройство является вторым диском в системе.</span><span class="sxs-lookup"><span data-stu-id="f1c34-142">The disc device is the second drive on the system.</span></span>
-   <span data-ttu-id="f1c34-143">В устройство вставляется совместимый диск.</span><span class="sxs-lookup"><span data-stu-id="f1c34-143">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="f1c34-144">Диск пуст.</span><span class="sxs-lookup"><span data-stu-id="f1c34-144">The disc is blank.</span></span>
-   <span data-ttu-id="f1c34-145">Файлы для записи на диск находятся в папке "g: \\ бурндир".</span><span class="sxs-lookup"><span data-stu-id="f1c34-145">Files to write to disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="f1c34-146">В этот сценарий можно добавить дополнительные функции, такие как проверка ошибок, совместимость устройств и носителей, уведомление о событиях и вычисление свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="f1c34-146">Additional functionality such as error checking, device and media compatibility, event notification, and calculating free space on the disc can be added to this script.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="f1c34-147">См. также</span><span class="sxs-lookup"><span data-stu-id="f1c34-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c34-148">Использование IMAPI</span><span class="sxs-lookup"><span data-stu-id="f1c34-148">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="f1c34-149">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="f1c34-149">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="f1c34-150">**IDiscFormat2Erase**</span><span class="sxs-lookup"><span data-stu-id="f1c34-150">**IDiscFormat2Erase**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[<span data-ttu-id="f1c34-151">**IDiscFormat2RawCD**</span><span class="sxs-lookup"><span data-stu-id="f1c34-151">**IDiscFormat2RawCD**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[<span data-ttu-id="f1c34-152">**IDiscFormat2TrackAtOnce**</span><span class="sxs-lookup"><span data-stu-id="f1c34-152">**IDiscFormat2TrackAtOnce**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[<span data-ttu-id="f1c34-153">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="f1c34-153">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="f1c34-154">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="f1c34-154">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="f1c34-155">**ифилесистемимаже**</span><span class="sxs-lookup"><span data-stu-id="f1c34-155">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[<span data-ttu-id="f1c34-156">**IStream**</span><span class="sxs-lookup"><span data-stu-id="f1c34-156">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 