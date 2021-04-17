---
title: Создание многосеансового диска
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'Дополнительные сведения: создание многосеансового диска'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497829"
---
# <a name="creating-a-multisession-disc"></a><span data-ttu-id="c6882-103">Создание многосеансового диска</span><span class="sxs-lookup"><span data-stu-id="c6882-103">Creating a Multisession Disc</span></span>

<span data-ttu-id="c6882-104">API-интерфейс для работы с [образами](about-imapi.md) (IMAPI) поддерживает добавление и удаление файлов на следующих типах многосеансовых дисков:</span><span class="sxs-lookup"><span data-stu-id="c6882-104">The [Image Mastering API](about-imapi.md) (IMAPI) supports the addition and removal of files to, or from, the following multisession disc types:</span></span>

-   <span data-ttu-id="c6882-105">CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="c6882-105">CD-R/CD-RW</span></span>
-   <span data-ttu-id="c6882-106">Single-Layer DVD + R/DVD-R</span><span class="sxs-lookup"><span data-stu-id="c6882-106">Single-Layer DVD+R/DVD-R</span></span>
-   <span data-ttu-id="c6882-107">Двойной слой DVD + R</span><span class="sxs-lookup"><span data-stu-id="c6882-107">DVD+R Dual Layer</span></span>
-   <span data-ttu-id="c6882-108">BD-R</span><span class="sxs-lookup"><span data-stu-id="c6882-108">BD-R</span></span>
-   <span data-ttu-id="c6882-109">DVD-RW/DVD + RW (**только Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="c6882-109">DVD-RW/DVD+RW (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="c6882-110">DVD-RAM (**только Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="c6882-110">DVD-RAM (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="c6882-111">BD-RE (**только Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="c6882-111">BD-RE (**Windows 7 Only**)</span></span>

<span data-ttu-id="c6882-112">Создание многосеансового диска с помощью IMAPI состоит из следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="c6882-112">Creation of a multisession disc using IMAPI consists of the following steps.</span></span> <span data-ttu-id="c6882-113">Каждый из описанных шагов содержит соответствующую часть полного примера сценария Visual Basic, приведенного в последнем разделе.</span><span class="sxs-lookup"><span data-stu-id="c6882-113">Each of these documented steps contains the relevant portion of the complete Visual Basic script example provided in the final section.</span></span>

## <a name="initializing-the-disc-recorder"></a><span data-ttu-id="c6882-114">Инициализация записи на диск</span><span class="sxs-lookup"><span data-stu-id="c6882-114">Initializing the Disc Recorder</span></span>

<span data-ttu-id="c6882-115">Перед инициализацией устройства объект **MsftDiscMaster2** предоставляет перечисление оптических устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="c6882-115">Prior to device initialization, the **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="c6882-116">Интерфейс [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) предоставляет доступ к этому перечислению устройств, чтобы упростить расположение соответствующего устройства записи.</span><span class="sxs-lookup"><span data-stu-id="c6882-116">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to this device enumeration to facilitate the location of the appropriate recording device.</span></span> <span data-ttu-id="c6882-117">Объект **MsftDiscMaster2** также предоставляет уведомления о событиях при добавлении или удалении оптических устройств с компьютера.</span><span class="sxs-lookup"><span data-stu-id="c6882-117">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or removed from a machine.</span></span>

<span data-ttu-id="c6882-118">После обнаружения оптического устройства записи и получения назначенного ему идентификатора создайте новый объект **MsftDiscMaster2** и инициализируйте средство записи, используя конкретный идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="c6882-118">After locating an optical recorder and retrieving the ID assigned to it, create a new **MsftDiscMaster2** object and initialize the recorder using the specific device ID.</span></span>

<span data-ttu-id="c6882-119">Интерфейс [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) предоставляет доступ к основным сведениям об устройстве, таким как идентификатор поставщика, идентификатор продукта, версия продукта, а также методы извлечения носителя или закрытия лотка.</span><span class="sxs-lookup"><span data-stu-id="c6882-119">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to basic device information such as vendor ID, product ID, product revision, as well as the methods to eject media or close the tray.</span></span>

> [!Note]  
> <span data-ttu-id="c6882-120">Дополнительные константы и измерения, объявленные в следующем примере, используются далее в полном примере сценария, расположенном в последнем разделе этого документа.</span><span class="sxs-lookup"><span data-stu-id="c6882-120">The additional constants and dimensions declared in the following sample are used later in the complete sample script located in the final section of this document.</span></span> <span data-ttu-id="c6882-121">Эти элементы не являются обязательными для инициализации устройства записи дисков.</span><span class="sxs-lookup"><span data-stu-id="c6882-121">These elements are not required for the act of initializing a disc recorder.</span></span>

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a><span data-ttu-id="c6882-122">Создание модуля записи данных</span><span class="sxs-lookup"><span data-stu-id="c6882-122">Creating a Data Writer</span></span>

<span data-ttu-id="c6882-123">Объект _ *MsftDiscFormat2Data*\* предоставляет метод записи, его свойства, а также свойства, относящиеся к носителю.</span><span class="sxs-lookup"><span data-stu-id="c6882-123">The _ *MsftDiscFormat2Data*\* object provides the writing method, its properties, as well as the media-specific properties.</span></span> <span data-ttu-id="c6882-124">Интерфейс [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) предоставляет доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="c6882-124">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to this object.</span></span>

<span data-ttu-id="c6882-125">Устройство записи дисков привязывается к модулю записи формата с помощью свойства [**IDiscFormat2Data::p UT \_ Record**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="c6882-125">The disc recorder binds to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="c6882-126">После привязки модуля записи к модулю записи формата для записи образа на диск с помощью метода [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) можно выполнить запросы свойств мультимедиа и записи.</span><span class="sxs-lookup"><span data-stu-id="c6882-126">After the recorder is bound to the format writer, media and write-specific property queries can be performed prior to writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

> [!Note]  
> <span data-ttu-id="c6882-127">Строка имени клиента, указанная в приведенном ниже образце кода, должна быть скорректирована соответствующим образом для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="c6882-127">The client name string specified in the sample code below should be adjusted as appropriate for the specific application.</span></span>

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a><span data-ttu-id="c6882-128">Создание объекта файловой системы</span><span class="sxs-lookup"><span data-stu-id="c6882-128">Creating the File System Object</span></span>

<span data-ttu-id="c6882-129">Чтобы записать новый сеанс, сначала необходимо создать образ записи.</span><span class="sxs-lookup"><span data-stu-id="c6882-129">In order to record a new session, a burn image must be generated for it first.</span></span> <span data-ttu-id="c6882-130">Образ записи для форматов **ISO9660**, **Жолиет** и **UDF** состоит из файловых систем отдельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="c6882-130">A burn image for **ISO9660**, **Joliet** and **UDF** formats consist of file systems of individual files and directories.</span></span> <span data-ttu-id="c6882-131">Объект **мсфтфилесистемимаже** — это объект файловой системы, содержащий файлы и каталоги, которые будут размещены на оптическом носителе.</span><span class="sxs-lookup"><span data-stu-id="c6882-131">The **MsftFileSystemImage** object is the file system object that contains the files and directories to be placed on the optical media.</span></span> <span data-ttu-id="c6882-132">Интерфейс [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) предоставляет доступ к объекту и параметрам файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c6882-132">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a><span data-ttu-id="c6882-133">Импорт файловой системы</span><span class="sxs-lookup"><span data-stu-id="c6882-133">Importing a File System</span></span>

<span data-ttu-id="c6882-134">Прежде чем продолжать, убедитесь, что диск не пуст, проверив свойство [**IDiscFormat2:: Get \_ медиахеуристикаллибланк**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .</span><span class="sxs-lookup"><span data-stu-id="c6882-134">Before proceeding, ensure that the disc is not blank by checking the [**IDiscFormat2::get\_MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) property.</span></span>

<span data-ttu-id="c6882-135">После создания объекта **мсфтфилесистемимаже** свойство [**ифилесистемимаже::p UT \_ мултисессионинтерфацес**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) должно быть инициализировано до вызова метода [**ифилесистемимаже:: импортфилесистем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) или [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) для импорта файловой системы из последнего записанного сеанса.</span><span class="sxs-lookup"><span data-stu-id="c6882-135">After creating the **MsftFileSystemImage** object, the [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property should be initialized prior to a call to either the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) or [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method to import the file system from the last recorded session.</span></span> <span data-ttu-id="c6882-136">Эти методы будут автоматически заполнять объект **мсфтфилесистемимаже** сведениями, описывающими ранее записанные файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="c6882-136">These methods will automatically populate the **MsftFileSystemImage** object with information describing the previously recorded files and directories.</span></span>

> [!Note]  
> <span data-ttu-id="c6882-137">Свойство [**ифилесистемимаже::p UT \_ мултисессионинтерфацес**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) обычно инициализируется с помощью многосеансовых интерфейсов, предоставляемых модулем записи данных через свойство [**IDiscFormat2Data:: Get \_ мултисессионинтерфацес**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .</span><span class="sxs-lookup"><span data-stu-id="c6882-137">The [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property is typically initialized with the multisession interfaces provided by the data writer via the [**IDiscFormat2Data::get\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) property.</span></span>

 

<span data-ttu-id="c6882-138">Попытка установить свойство **ифилесистемимаже::p UT \_ мултисессионинтерфацес** завершится ошибкой, если IMAPI не поддерживает многосеансовую поддержку для вставленного носителя, или не удается добавить носитель по какой-либо другой причине (например, потому, что он закрыт).</span><span class="sxs-lookup"><span data-stu-id="c6882-138">Attempts to set the **IFileSystemImage::put\_MultisessionInterfaces** property will fail if IMAPI does not support multisession for the currently inserted media or the media cannot be appended for some other reason (e.g. because it is closed).</span></span>

<span data-ttu-id="c6882-139">Если предыдущий сеанс записи содержал более одного типа файловой системы, метод [**ифилесистемимаже:: импортфилесистем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) будет импортировать данные из наиболее расширенного типа файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c6882-139">If the previous burn session contained more than one file system type, the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method will import information from the most advanced file system type present.</span></span> <span data-ttu-id="c6882-140">Например, в примере, приведенном в этом разделе, UDF — это импортированная файловая система.</span><span class="sxs-lookup"><span data-stu-id="c6882-140">For example, in the example provided in this topic, UDF is the imported file system.</span></span> <span data-ttu-id="c6882-141">Однако использование метода [**ифилесистемимаже:: импортспеЦификфилесистем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) позволяет импортировать определенную файловую систему.</span><span class="sxs-lookup"><span data-stu-id="c6882-141">However, use of the [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method allows the specific selection of the file system to import.</span></span>

> [!Note]  
> <span data-ttu-id="c6882-142">Метод [**ифилесистемимаже:: идентифифилесистемсондиск**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) можно использовать для определения того, какие файловые системы доступны на диске.</span><span class="sxs-lookup"><span data-stu-id="c6882-142">The [**IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) method can be used to determine which file systems are available on the disc.</span></span>

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a><span data-ttu-id="c6882-143">Добавление или удаление файлов в файловой системе</span><span class="sxs-lookup"><span data-stu-id="c6882-143">Adding or Removing Files to the File System</span></span>

<span data-ttu-id="c6882-144">После создания объекта файловой системы и импорта файловой системы из предыдущего сеанса вызовите методы [**ифилесистемимаже:: креатефилеитем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) и [**Ифилесистемимаже:: креатедиректоритем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) , чтобы создать новые объекты File и Directory соответственно.</span><span class="sxs-lookup"><span data-stu-id="c6882-144">After creating the file system object and importing the file system from the previous session, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create new file and directory objects, respectively.</span></span> <span data-ttu-id="c6882-145">Объекты File и Directory содержат конкретные сведения о файлах и каталогах.</span><span class="sxs-lookup"><span data-stu-id="c6882-145">The file and directory objects provide specific details about the files and directories.</span></span> <span data-ttu-id="c6882-146">Кроме того, метод [**ифсидиректоритем:: аддтри**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) объекта каталога, представленного через интерфейс [**ифсидиректоритем**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , можно использовать для добавления существующих файлов и каталогов с другого устройства хранения (т. е. жесткого диска).</span><span class="sxs-lookup"><span data-stu-id="c6882-146">Alternatively, the [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) method of a directory object, represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface, can be used to add existing files and directories from another storage device (i.e. a hard drive).</span></span>

<span data-ttu-id="c6882-147">Метод обновления обработчика событий, доступный для [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) , определяет текущий файл, добавляемый в образ файловой системы, число уже скопированных секторов и общее число секторов для копирования.</span><span class="sxs-lookup"><span data-stu-id="c6882-147">The event handler update method available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifies the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="c6882-148">Чтобы удалить существующие файлы и каталоги из файловой системы, используйте методы [**ифсидиректоритем:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) и [**Ифсидиректоритем:: ремоветри**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) объектов каталога, представленных через интерфейс [**ифсидиректоритем**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) .</span><span class="sxs-lookup"><span data-stu-id="c6882-148">To remove existing files and directories from the file system, use the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods of the directory objects represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface.</span></span> <span data-ttu-id="c6882-149">Свойство [**ифилесистемимаже:: Get \_ root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) используется для получения указателя на корневой каталог файловой системы и интерфейса **ифсидиректоритем** для прохода по дереву каталогов.</span><span class="sxs-lookup"><span data-stu-id="c6882-149">The [**IFileSystemImage::get\_Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) property is used to get a pointer to the root directory of the file system and the **IFsiDirectoryItem** interface to traverse through the directory tree.</span></span>

> [!Note]  
> <span data-ttu-id="c6882-150">Файлы и каталоги, удаленные с помощью методов [**ифсидиректоритем:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) и [**Ифсидиректоритем:: ремоветри**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) , физически не удаляются с диска, а расширенное программное обеспечение может легко восстановить удаленные данные.</span><span class="sxs-lookup"><span data-stu-id="c6882-150">Files and directories removed via the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods are not physically removed from the disc, and advanced software can easily recover the deleted information.</span></span>

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a><span data-ttu-id="c6882-151">Создание образа файловой системы</span><span class="sxs-lookup"><span data-stu-id="c6882-151">Constructing a File System Image</span></span>

<span data-ttu-id="c6882-152">Последним шагом является вызов [**ифилесистемимаже:: креатересултимаже**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) для создания потока данных для образа записи и предоставления доступа к нему через интерфейс [**ифилесистемимажересулт**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) .</span><span class="sxs-lookup"><span data-stu-id="c6882-152">The final step is to call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream for the burn image and provide access to it through the [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) interface.</span></span> <span data-ttu-id="c6882-153">Этот поток данных может быть предоставлен непосредственно методу [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) или сохранен в файл для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="c6882-153">This data stream can either be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a><span data-ttu-id="c6882-154">Пример сводки</span><span class="sxs-lookup"><span data-stu-id="c6882-154">Example Summary</span></span>

<span data-ttu-id="c6882-155">В следующем примере скрипта Visual Basic показано, как использовать объекты IMAPI для создания многосеансовых дисков.</span><span class="sxs-lookup"><span data-stu-id="c6882-155">The following Visual Basic script example shows how to use IMAPI objects to create multisession discs.</span></span> <span data-ttu-id="c6882-156">В этом примере создается новый сеанс и добавляется каталог на диск. В целях простоты код не выполняет расширенную проверку на наличие ошибок и предполагает следующее:</span><span class="sxs-lookup"><span data-stu-id="c6882-156">The example creates a new session and adds a directory to the disc. For the sake of simplicity, the code does not perform extensive error checking, and assumes the following:</span></span>

-   <span data-ttu-id="c6882-157">В системе установлено совместимое устройство чтения.</span><span class="sxs-lookup"><span data-stu-id="c6882-157">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="c6882-158">Устройство является первым диском в системе.</span><span class="sxs-lookup"><span data-stu-id="c6882-158">The disc device is the first drive on the system.</span></span>
-   <span data-ttu-id="c6882-159">В устройство вставляется совместимый диск.</span><span class="sxs-lookup"><span data-stu-id="c6882-159">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="c6882-160">Файлы, добавляемые на диск, находятся в папке "g: \\ бурндир".</span><span class="sxs-lookup"><span data-stu-id="c6882-160">Files to add to the disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="c6882-161">Дополнительные функции, такие как обширная проверка ошибок, совместимость с устройствами и носителями, уведомление о событиях и вычисление свободного места на диске, можно добавить в скрипт.</span><span class="sxs-lookup"><span data-stu-id="c6882-161">Additional functionality such as extensive error checking, device and media compatibility, event notification, and calculation of free space on the disc can be added to the script.</span></span>


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="c6882-162">См. также</span><span class="sxs-lookup"><span data-stu-id="c6882-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6882-163">Использование IMAPI</span><span class="sxs-lookup"><span data-stu-id="c6882-163">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="c6882-164">_ *IStream*\*</span><span class="sxs-lookup"><span data-stu-id="c6882-164">_ *IStream*\*</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="c6882-165">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="c6882-165">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="c6882-166">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="c6882-166">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="c6882-167">**ифилесистемимаже**</span><span class="sxs-lookup"><span data-stu-id="c6882-167">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
