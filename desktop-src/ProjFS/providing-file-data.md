---
title: Предоставление данных файлов
description: Описывает, как поставщик предоставляет сведения о заполнителе и данные файлов.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413333"
---
# <a name="providing-file-data"></a><span data-ttu-id="63126-103">Предоставление данных файлов</span><span class="sxs-lookup"><span data-stu-id="63126-103">Providing File Data</span></span>

<span data-ttu-id="63126-104">Когда поставщик сначала создает корень виртуализации, он пуст в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="63126-104">When a provider first creates a virtualization root it is empty on the local system.</span></span> <span data-ttu-id="63126-105">То есть ни один из элементов хранилища резервных данных еще не был кэширован на диск.</span><span class="sxs-lookup"><span data-stu-id="63126-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span> <span data-ttu-id="63126-106">При открытии элементов Прожфс запрашивает сведения от поставщика, чтобы разрешить создание заполнителей для этих элементов в локальной файловой системе.</span><span class="sxs-lookup"><span data-stu-id="63126-106">As items are opened, ProjFS requests information from the provider to allow placeholders for those items to be created in the local file system.</span></span>  <span data-ttu-id="63126-107">При доступе к содержимому элемента Прожфс запрашивает это содержимое от поставщика.</span><span class="sxs-lookup"><span data-stu-id="63126-107">As item contents are accessed, ProjFS requests those contents from the provider.</span></span>  <span data-ttu-id="63126-108">Результат заключается в том, что с точки зрения пользователя виртуализированные файлы и каталоги похожи на обычные файлы и каталоги, которые уже находятся в локальной файловой системе.</span><span class="sxs-lookup"><span data-stu-id="63126-108">The result is that from the user's perspective, virtualized files and directories appear similar to normal files and directories that already reside on the local file system.</span></span>

## <a name="placeholder-creation"></a><span data-ttu-id="63126-109">Создание заполнителя</span><span class="sxs-lookup"><span data-stu-id="63126-109">Placeholder Creation</span></span>

<span data-ttu-id="63126-110">Когда приложение пытается открыть обработчик для виртуализированного файла, Прожфс вызывает обратный вызов **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** для каждого элемента пути, который еще не существует на диске.</span><span class="sxs-lookup"><span data-stu-id="63126-110">When an application attempts to open a handle to a virtualized file, ProjFS calls the **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** callback for each item of the path that does not yet exist on disk.</span></span>  <span data-ttu-id="63126-111">Например, если приложение пытается открыть `C:\virtRoot\dir1\dir2\file.txt` , но `C:\virtRoot\dir1` на диске существует только путь, то поставщик получит обратный вызов для `C:\virtRoot\dir1\dir2` , а затем для `C:\virtRoot\dir1\dir2\file.txt` .</span><span class="sxs-lookup"><span data-stu-id="63126-111">For example, if an application tries to open `C:\virtRoot\dir1\dir2\file.txt`, but only the path `C:\virtRoot\dir1` exists on disk, then the provider will receive a callback for `C:\virtRoot\dir1\dir2`, then for `C:\virtRoot\dir1\dir2\file.txt`.</span></span>

<span data-ttu-id="63126-112">Когда Прожфс вызывает обратный вызов **PRJ_GET_PLACEHOLDER_INFO_CB** поставщика, поставщик выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="63126-112">When ProjFS calls the provider's **PRJ_GET_PLACEHOLDER_INFO_CB** callback, the provider performs the following actions:</span></span>

1. <span data-ttu-id="63126-113">Поставщик определяет, существует ли запрошенное имя в резервном хранилище.</span><span class="sxs-lookup"><span data-stu-id="63126-113">The provider determines whether the requested name exists in its backing store.</span></span>  <span data-ttu-id="63126-114">Поставщик должен использовать **[пржфиленамекомпаре](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** в качестве подпрограммы сравнения при поиске в резервном хранилище, чтобы определить, существует ли запрошенное имя в резервном хранилище.</span><span class="sxs-lookup"><span data-stu-id="63126-114">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** as the comparison routine when searching its backing store to determine whether the requested name exists in the backing store.</span></span>  <span data-ttu-id="63126-115">В противном случае поставщик возвращает HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="63126-115">If it does not, the provider returns HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) from the callback.</span></span>

1. <span data-ttu-id="63126-116">Если запрошенное имя существует в резервном хранилище, поставщик заполняет структуру [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) с помощью метаданных файловой системы элемента и вызывает **[пржвритеплацехолдеринфо](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** для отправки данных в прожфс.</span><span class="sxs-lookup"><span data-stu-id="63126-116">If the requested name does exist in the backing store, the provider populates a [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) structure with the item's file system metadata and calls **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to send the data to ProjFS.</span></span>  <span data-ttu-id="63126-117">Прожфс будет использовать эти сведения для создания заполнителя в локальной файловой системе для элемента.</span><span class="sxs-lookup"><span data-stu-id="63126-117">ProjFS will use that information to create a placeholder in the local file system for the item.</span></span>

    > <span data-ttu-id="63126-118">Прожфс будет использовать любые FILE_ATTRIBUTE Флаги наборов поставщиков в PRJ_PLACEHOLDER_INFO члене **филебасиЦинфо. FileAttributes** , кроме FILE_ATTRIBUTE_DIRECTORY; будет задано правильное значение для FILE_ATTRIBUTE_DIRECTORY в элементе **филебасиЦинфо. FileAttributes** в соответствии с предоставленным значением элемента **филебасиЦинфо. DataDirectory** .</span><span class="sxs-lookup"><span data-stu-id="63126-118">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileBasicInfo.FileAttributes** member of PRJ_PLACEHOLDER_INFO except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileBasicInfo.FileAttributes** member according to the supplied value of the **FileBasicInfo.IsDirectory** member.</span></span>

    > <span data-ttu-id="63126-119">Если резервное хранилище поддерживает символьные ссылки, поставщик должен использовать **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** для отправки данных заполнителя в прожфс.</span><span class="sxs-lookup"><span data-stu-id="63126-119">If the backing store supports symbolic links, the provider must use **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** to send the placeholder data to ProjFS.</span></span>  <span data-ttu-id="63126-120">**PrjWritePlaceholderInfo2** поддерживает дополнительные входные данные буфера, позволяющие поставщику указать, что заполнитель является символьной ссылкой, и ее целью является.</span><span class="sxs-lookup"><span data-stu-id="63126-120">**PrjWritePlaceholderInfo2** supports an extra buffer input that allows the provider to specify that the placeholder is a symbolic link and what its target is.</span></span>  <span data-ttu-id="63126-121">В противном случае он ведет себя так, как описано выше, для **пржвритеплацехолдеринфо**.</span><span class="sxs-lookup"><span data-stu-id="63126-121">It otherwise behaves as described above for **PrjWritePlaceholderInfo**.</span></span>  <span data-ttu-id="63126-122">В следующем примере показано, как использовать **PrjWritePlaceholderInfo2** для предоставления поддержки символьных ссылок.</span><span class="sxs-lookup"><span data-stu-id="63126-122">The following sample illustrates how to use **PrjWritePlaceholderInfo2** to provide support for symbolic links.</span></span>
    >
    > <span data-ttu-id="63126-123">Обратите внимание, что **PrjWritePlaceholderInfo2** поддерживается в Windows 10, версия 2004.</span><span class="sxs-lookup"><span data-stu-id="63126-123">Note that **PrjWritePlaceholderInfo2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="63126-124">Поставщик должен проверять наличие **PrjWritePlaceholderInfo2**, например, с помощью **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="63126-124">A provider should probe for the existence of **PrjWritePlaceholderInfo2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a><span data-ttu-id="63126-125">Предоставление содержимого файлов</span><span class="sxs-lookup"><span data-stu-id="63126-125">Providing File Contents</span></span>

<span data-ttu-id="63126-126">Когда Прожфс необходимо обеспечить, чтобы виртуализированный файл содержал данные, например, когда приложение пытается выполнить чтение из файла, Прожфс вызывает обратный вызов **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** для этого элемента, чтобы запросить, что поставщик предоставил содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="63126-126">When ProjFS needs to ensure that a virtualized file contains data, such as when an application attempts to read from the file, ProjFS calls the **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback for that item to request that the provider supply the file's contents.</span></span>  <span data-ttu-id="63126-127">Поставщик получает данные файла из резервного хранилища и использует **[пржвритефиледата](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** для отправки данных в локальную файловую систему.</span><span class="sxs-lookup"><span data-stu-id="63126-127">The provider retrieves the file's data from its backing store and uses **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** to send the data to the local file system.</span></span>

> <span data-ttu-id="63126-128">Когда Прожфс вызывает этот обратный вызов, член **FilePathName** параметра _каллбаккдата_ предоставляет имя, которое файл имел при создании его заполнителя.</span><span class="sxs-lookup"><span data-stu-id="63126-128">When ProjFS calls this callback, the **FilePathName** member of the _callbackData_ parameter supplies the name the file had when its placeholder was created.</span></span>  <span data-ttu-id="63126-129">То есть, если файл был переименован с момента создания заполнителя, обратный вызов предоставляет исходное имя (pre-Rename), а не текущее имя (после переименования).</span><span class="sxs-lookup"><span data-stu-id="63126-129">That is, if the file has been renamed since its placeholder was created, the callback supplies the original (pre-rename) name, not the current (post-rename) name.</span></span>  <span data-ttu-id="63126-130">При необходимости поставщик может использовать член **versionInfo** параметра _каллбаккдата_ для определения того, какие данные запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="63126-130">If necessary, the provider can use the **VersionInfo** member of the _callbackData_ parameter to determine which file's data is being requested.</span></span>
>
> <span data-ttu-id="63126-131">Дополнительные сведения о том, как можно использовать член **VersionInfo** PRJ_CALLBACK_DATA, см. в документации по [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) и разделу [Обработка изменений в представлении](handling-view-changes.md) .</span><span class="sxs-lookup"><span data-stu-id="63126-131">For more information on how the **VersionInfo** member of PRJ_CALLBACK_DATA may be used, see the documentation for [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) and the [Handling View Changes](handling-view-changes.md) topic.</span></span>

<span data-ttu-id="63126-132">Поставщику разрешено разбивать диапазон данных, запрошенных в **PRJ_GET_FILE_DATA_CB** обратном вызове, на несколько вызовов **пржвритефиледата**, каждый из которых предоставляет часть запрошенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="63126-132">The provider is allowed to split the range of data requested in the **PRJ_GET_FILE_DATA_CB** callback into multiple calls to **PrjWriteFileData**, each supplying a portion of the requested range.</span></span>  <span data-ttu-id="63126-133">Однако перед завершением обратного вызова поставщик должен предоставить весь запрошенный диапазон.</span><span class="sxs-lookup"><span data-stu-id="63126-133">However, the provider must supply the entire requested range before completing the callback.</span></span>  <span data-ttu-id="63126-134">Например, если обратный вызов запрашивает 10 МБ данных от _byteOffset_ 0 для _длины_ 10 485 760, поставщик может указать данные в 10 вызовах **пржвритефиледата**, каждая из которых отправляет 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="63126-134">For example, if the callback requests 10 MB of data from _byteOffset_ 0 for _length_ 10,485,760, the provider may choose to supply the data in 10 calls to **PrjWriteFileData**, each sending 1 MB.</span></span>

<span data-ttu-id="63126-135">Поставщик также может предоставить больше запрошенного диапазона, вплоть до длины файла.</span><span class="sxs-lookup"><span data-stu-id="63126-135">The provider is also free to supply more than the requested range, up to the length of the file.</span></span>  <span data-ttu-id="63126-136">Диапазон, предоставляемый поставщиком, должен охватывать запрошенный диапазон.</span><span class="sxs-lookup"><span data-stu-id="63126-136">The range the provider supplies must cover the requested range.</span></span>  <span data-ttu-id="63126-137">Например, если обратный вызов запрашивает 1 МБ данных из _byteOffset_ 4096 для _длины_ 1 052 672 и файл имеет общий размер 10 МБ, поставщик может вернуть 2 МБ данных, начиная со смещения 0.</span><span class="sxs-lookup"><span data-stu-id="63126-137">For example, if the callback requests 1 MB of data from _byteOffset_ 4096 for _length_ 1,052,672, and the file has a total size of 10 MB, the provider could choose to return 2 MB of data starting at offset 0.</span></span>

### <a name="buffer-alignment-considerations"></a><span data-ttu-id="63126-138">Рекомендации по выравниванию буфера</span><span class="sxs-lookup"><span data-stu-id="63126-138">Buffer Alignment Considerations</span></span>

<span data-ttu-id="63126-139">Прожфс использует [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) от вызывающего объекта, которому требуются данные для записи данных в локальную файловую систему.</span><span class="sxs-lookup"><span data-stu-id="63126-139">ProjFS uses the [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) from the caller who requires the data to write the data to the local file system.</span></span>  <span data-ttu-id="63126-140">Однако Прожфс не может контролировать, открыт ли FILE_OBJECT для буферизованной или небуферизованной операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="63126-140">However ProjFS cannot control whether that FILE_OBJECT was opened for buffered or unbuffered I/O.</span></span>  <span data-ttu-id="63126-141">Если FILE_OBJECT был открыт для операций ввода-вывода без буферизации, операции чтения и записи в файл должны соответствовать определенным требованиям к выравниванию.</span><span class="sxs-lookup"><span data-stu-id="63126-141">If the FILE_OBJECT was opened for unbuffered I/O, reads and writes to the file must adhere to certain alignment requirements.</span></span>  <span data-ttu-id="63126-142">Поставщик может удовлетворять этим требованиям по выравниванию, выполняя два действия:</span><span class="sxs-lookup"><span data-stu-id="63126-142">The provider can meet those alignment requirements by doing two things:</span></span>

1. <span data-ttu-id="63126-143">Используйте **[пржаллокатеалигнедбуффер](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** , чтобы выделить буфер для передачи в параметр _буфера_ **пржвритефиледата**.</span><span class="sxs-lookup"><span data-stu-id="63126-143">Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** to allocate the buffer to pass in **PrjWriteFileData**'s _buffer_ parameter.</span></span>
1. <span data-ttu-id="63126-144">Убедитесь, что параметры _byteOffset_ и _length_ параметра **пржвритефиледата** являются целыми числами, кратными требованиям к выравниванию устройства хранения (Обратите внимание, что параметр _длины_ не должен соответствовать этому требованию, если _byteOffset_  +  _Длина_ равна концу файла).</span><span class="sxs-lookup"><span data-stu-id="63126-144">Ensure that the _byteOffset_ and _length_ parameters of **PrjWriteFileData** are integer multiples of the storage device's alignment requirement (note that the _length_ parameter does not have to meet this requirement if _byteOffset_ + _length_ is equal to the end of the file).</span></span>  <span data-ttu-id="63126-145">Поставщик может использовать **[пржжетвиртуализатионинстанцеинфо](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** для получения требования к выравниванию устройства хранения.</span><span class="sxs-lookup"><span data-stu-id="63126-145">The provider can use **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** to retrieve the storage device's alignment requirement.</span></span>

<span data-ttu-id="63126-146">Прожфс оставляет его поставщику для вычисления правильного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="63126-146">ProjFS leaves it up to the provider to calculate proper alignment.</span></span>  <span data-ttu-id="63126-147">Это обусловлено тем, что при обработке **PRJ_GET_FILE_DATA_CBного** обратного вызова поставщик может вернуть запрошенные данные между несколькими вызовами **пржвритефиледата** , каждый из которых возвращает часть общих запрошенных данных перед завершением обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="63126-147">This is because when processing a **PRJ_GET_FILE_DATA_CB** callback the provider may opt to return the requested data across multiple **PrjWriteFileData** calls, each returning part of the total requested data, before completing the callback.</span></span>

> <span data-ttu-id="63126-148">Если поставщик будет использовать один вызов **пржвритефиледата** для записи всего файла, т. е. от _byteOffset_ = 0 до _length_ = размера файла или для возврата точного диапазона, запрошенного в ответном вызове **PRJ_GET_FILE_DATA_CB** , поставщику не нужно выполнять вычисления выравнивания.</span><span class="sxs-lookup"><span data-stu-id="63126-148">If the provider is going to use a single call to **PrjWriteFileData** to either write the entire file, i.e. from _byteOffset_ = 0 to _length_ = size of the file, or to return the exact range requested in the **PRJ_GET_FILE_DATA_CB** callback, the provider does not have to do any alignment calculations.</span></span>  <span data-ttu-id="63126-149">Однако он по-прежнему должен использовать **пржаллокатеалигнедбуффер** , чтобы обеспечить соответствие _буфера_ требованиям к выравниванию устройства хранения.</span><span class="sxs-lookup"><span data-stu-id="63126-149">However, it must still use **PrjAllocateAlignedBuffer** to ensure that _buffer_ meets the storage device’s alignment requirements.</span></span>

<span data-ttu-id="63126-150">Дополнительные сведения о буферизованном и небуферизованном вводе-выводе см. в разделе [буферизация файлов](/windows/desktop/FileIO/file-buffering) разделов.</span><span class="sxs-lookup"><span data-stu-id="63126-150">See the topic [File Buffering](/windows/desktop/FileIO/file-buffering) for more information on buffered vs. unbuffered I/O.</span></span>

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```