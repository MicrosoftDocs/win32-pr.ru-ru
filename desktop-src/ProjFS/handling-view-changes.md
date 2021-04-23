---
title: Обработка изменений представления
description: Описывает, как обновить клиентское представление резервного хранилища поставщика.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 1d5a709752f92b7449d2ccc38f67c4417edf8d62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070123"
---
# <a name="handling-view-changes"></a><span data-ttu-id="6b2c3-103">Обработка изменений представления</span><span class="sxs-lookup"><span data-stu-id="6b2c3-103">Handling View Changes</span></span>

<span data-ttu-id="6b2c3-104">По мере открытия файлов и каталогов в корне виртуализации поставщик создает заполнители на диске, а файлы считываются заполнители с содержимым.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-104">As files and directories under the virtualization root are opened, the provider creates placeholders on disk, and as files are read the placeholders are hydrated with contents.</span></span>  <span data-ttu-id="6b2c3-105">Эти заполнители представляют состояние резервного хранилища на момент создания.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-105">These placeholders represent the state of the backing store at the time they were created.</span></span>  <span data-ttu-id="6b2c3-106">Эти кэшированные элементы в сочетании с элементами, проецируемыми поставщиком в перечислениях, составляют представление резервного хранилища клиента.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-106">These cached items, combined with the items projected by the provider in enumerations, constitute the client's "view" of the backing store.</span></span>  <span data-ttu-id="6b2c3-107">Время от времени поставщику может потребоваться обновить представление клиента, будь это из-за изменений в резервном хранилище или из-за явного действия, предпринимаемого пользователем для изменения их представления.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-107">From time to time the provider may wish to update the client's view, whether because of changes in the backing store, or because of explicit action taken by the user to change their view.</span></span>

> <span data-ttu-id="6b2c3-108">Если поставщик обновляет представление заранее при изменении резервного хранилища, рекомендуется, чтобы изменения в представлении были довольно редки.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-108">If the provider updates the view proactively, as the backing store changes, it is recommended that view changes be relatively infrequent.</span></span>  <span data-ttu-id="6b2c3-109">Это связано с тем, что при изменении представления элемента, который был открыт, и, таким образом, на диске был создан заполнитель, необходимо обновить или удалить элемент на диске, чтобы отразить изменение представления.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-109">This is because a view change to an item that has been opened, and therefore had a placeholder created on disk, requires that the on-disk item be either updated or deleted to reflect the view change.</span></span>  <span data-ttu-id="6b2c3-110">Частые обновления могут привести к дополнительным действиям с диском, которые могут негативно сказаться на производительности системы.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-110">Frequent updates may result in extra disk activity that can negatively impact system performance.</span></span>

## <a name="item-versioning"></a><span data-ttu-id="6b2c3-111">Управление версиями элементов</span><span class="sxs-lookup"><span data-stu-id="6b2c3-111">Item Versioning</span></span>

<span data-ttu-id="6b2c3-112">Для поддержки обслуживания нескольких представлений Прожфс предоставляет **[PRJ_PLACEHOLDER_VERSION_INFOную](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** структуру.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-112">To support maintaining multiple views, ProjFS provides the **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span></span>  <span data-ttu-id="6b2c3-113">Поставщик использует эту структуру автономно в вызовах **[пржмаркдиректорясплацехолдер](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** и внедряется в структуры **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** и **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .</span><span class="sxs-lookup"><span data-stu-id="6b2c3-113">A provider uses this struct standalone in calls to **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, and it is embedded in the **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** and **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.</span></span>  <span data-ttu-id="6b2c3-114">**PRJ_PLACEHOLDER_VERSION_INFO**. В поле ContentID поставщик хранит до 128 байт сведений о версии для файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-114">The **PRJ_PLACEHOLDER_VERSION_INFO**.ContentID field is where the provider stores up to 128 bytes of version information for a file or directory.</span></span>  <span data-ttu-id="6b2c3-115">Поставщик может внутренне связать это значение с некоторым значением, определяющим конкретное представление.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-115">The provider may then internally associate this value to some value that identifies a particular view.</span></span>

<span data-ttu-id="6b2c3-116">Например, поставщик, выполняющий виртуализацию репозитория системы управления версиями, может использовать хэш содержимого файла для использования в качестве идентификатора ContentID и может использовать метки времени для обнаружения представлений репозитория в разные моменты времени.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-116">For example, a provider that virtualizes a source control repository might choose to use a hash of a file's contents to serve as the ContentID, and it might use timestamps to identify views of the repository at various points in time.</span></span>  <span data-ttu-id="6b2c3-117">Метки времени могут быть временем выполнения фиксации в репозитории.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-117">The timestamps might be the times that commits to the repository were performed.</span></span>

<span data-ttu-id="6b2c3-118">Используя пример репозитория с отметкой времени, типичным потоком для использования ContentID элемента может быть:</span><span class="sxs-lookup"><span data-stu-id="6b2c3-118">Using the example of a timestamp-indexed repository, a typical flow for using an item's ContentID might be:</span></span>

1. <span data-ttu-id="6b2c3-119">Клиент устанавливает представление, указывая отметку времени, в которой будет представлено содержимое репозитория.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-119">The client establishes a view by specifying the timestamp at which to present the repository contents.</span></span>  <span data-ttu-id="6b2c3-120">Это можно сделать через некоторый интерфейс, реализованный поставщиком, а не через API Прожфс.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-120">This would be done through some interface implemented by the provider, not via a ProjFS API.</span></span>  <span data-ttu-id="6b2c3-121">Например, поставщик может иметь программу командной строки, которую можно использовать, чтобы сообщить поставщику о необходимости просмотра.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-121">For example, the provider may have a command-line tool that could be used to tell the provider which view the user desires.</span></span>
1. <span data-ttu-id="6b2c3-122">Когда клиент создает маркер для виртуализированного файла или каталога, поставщик создает для него заполнитель, используя метаданные файловой системы из резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-122">When the client creates a handle to a virtualized file or directory, the provider creates a placeholder for it, using file system metadata from the backing store.</span></span>  <span data-ttu-id="6b2c3-123">Конкретный набор метаданных, который он использует, определяется значением ContentID, связанным с меткой времени нужного представления.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-123">The particular set of metadata it uses is identified by the ContentID value associated with the timestamp of the desired view.</span></span>  <span data-ttu-id="6b2c3-124">Когда поставщик вызывает **[пржвритеплацехолдеринфо](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** для записи сведений заполнителя, он предоставляет идентификатор ContentID в члене versionInfo аргумента _плацехолдеринфо_ .</span><span class="sxs-lookup"><span data-stu-id="6b2c3-124">When the provider calls **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to write the placeholder information, it supplies the ContentID in the VersionInfo member of the _placeholderInfo_ argument.</span></span>  <span data-ttu-id="6b2c3-125">Затем поставщик должен записать заполнитель для этого файла или каталога, созданный в этом представлении.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-125">The provider should then record that a placeholder for that file or directory was created in this view.</span></span>
1. <span data-ttu-id="6b2c3-126">Когда клиент считывает данные из заполнителя, вызывается обратный вызов **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** поставщика.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-126">When the client reads from a placeholder, the provider's **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback is invoked.</span></span>  <span data-ttu-id="6b2c3-127">Элемент VersionInfo в параметре _каллбаккдата_ содержит идентификатор объекта ContentID, указанный в **пржвритеплацехолдеринфо** при создании заполнителя файла.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-127">The _callbackData_ parameter's VersionInfo member contains the ContentID the provider specified in **PrjWritePlaceholderInfo** when it created the file placeholder.</span></span>  <span data-ttu-id="6b2c3-128">Поставщик использует объект ContentID для получения правильного содержимого файла из резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-128">The provider uses that ContentID to retrieve the correct contents of the file from its backing store.</span></span>
1. <span data-ttu-id="6b2c3-129">Клиент запрашивает изменение представления, указывая новую метку времени.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-129">The client requests a view change by specifying a new timestamp.</span></span>  <span data-ttu-id="6b2c3-130">Для каждого заполнитель поставщика, созданного в предыдущем представлении, если в новом представлении существует другая версия этого файла, поставщик может заменить заполнитель на диске обновленным, идентификатором ContentID которого связан с новой меткой времени, вызвав **[пржупдатефилеифнидед](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-130">For each placeholder the provider created in the previous view, if a different version of that file exists in the new view the provider may replace the placeholder on disk with an updated one whose ContentID is associated with the new timestamp by calling **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span></span>  <span data-ttu-id="6b2c3-131">Кроме того, поставщик может удалить заполнитель, вызвав **[пржделетефиле](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** , чтобы новое представление файла было проецировано в перечислениях.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-131">Alternatively, the provider may delete the placeholder by calling **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** so that the new view of the file will be projected in enumerations.</span></span>  <span data-ttu-id="6b2c3-132">Если файл не существует в новом представлении, поставщик должен удалить его, вызвав **пржделетефиле**.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-132">If the file does not exist in the new view, the provider must delete it by calling **PrjDeleteFile**.</span></span>

<span data-ttu-id="6b2c3-133">Обратите внимание, что поставщик должен гарантировать, что когда клиент перечислит каталог, поставщик предоставит содержимое, соответствующее представлению клиента.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-133">Note that the provider must ensure that when the client enumerates a directory, the provider will supply the contents that correspond to the client's view.</span></span>  <span data-ttu-id="6b2c3-134">Например, поставщик может использовать член VersionInfo параметра _каллбаккдата_ **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** и **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** обратные вызовы для получения содержимого каталога в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-134">For example, the provider could use the VersionInfo member of the _callbackData_ parameter of the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** and **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** callbacks to retrieve directory contents on the fly.</span></span>  <span data-ttu-id="6b2c3-135">Кроме того, можно создать структуру каталогов для этого представления в резервном хранилище в процессе создания представления, а затем просто перечислить эту структуру.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-135">Alternatively it could build a directory structure for that view in its backing store as part of establishing the view, and then simply enumerate that structure.</span></span>

> <span data-ttu-id="6b2c3-136">При вызове обратного вызова поставщика для заполнителя или частичного файла сведения о версии, указанные поставщиком при создании элемента, предоставляются в элементе VersionInfo в параметре _каллбаккдата_ обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-136">Whenever a provider callback is invoked for a placeholder or partial file, the version information the provider specified when creating the item is provided in the VersionInfo member of the callback's _callbackData_ parameter.</span></span>

## <a name="updating-the-view"></a><span data-ttu-id="6b2c3-137">Обновление представления</span><span class="sxs-lookup"><span data-stu-id="6b2c3-137">Updating the View</span></span>

<span data-ttu-id="6b2c3-138">Ниже приведен пример функции, показывающей, как поставщик может обновлять локальное представление, когда пользователь указывает новую метку времени.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-138">Below is a sample function illustrating how a provider might update the local view when the user specifies a new timestamp.</span></span>  <span data-ttu-id="6b2c3-139">Функция получает список заполнителей поставщика, созданного для представления, измененного пользователем, и обновляет локальное состояние кэша на основе состояния каждого заполнителя в новом представлении.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-139">The function retrieves a list of the placeholders the provider created for the view the user has just changed from, and updates the local cache state based on each placeholder's state in the new view.</span></span>  <span data-ttu-id="6b2c3-140">Для ясности эта подпрограммы не имеет определенных сложностей, связанных с файловой системой.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-140">For clarity, this routine omits certain complexities of dealing with the file system.</span></span>  <span data-ttu-id="6b2c3-141">Например, в старом представлении указанный каталог может существовать с некоторыми файлами или каталогами, но в новом представлении этот каталог (и его содержимое) больше не может существовать.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-141">For example, in the old view a given directory may have existed with some files or directories in it, but in the new view that directory (and its contents) may no longer exist.</span></span>  <span data-ttu-id="6b2c3-142">Чтобы избежать ошибок в такой ситуации, поставщик должен обновить состояние файла и каталогов под корнем виртуализации в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-142">To avoid encountering errors in such a situation the provider should update the state of the file and directories beneath the virtualization root in a depth-first fashion.</span></span>

```C++
typedef struct MY_ON_DISK_PLACEHOLDER MY_ON_DISK_PLACEHOLDER;

typedef struct MY_ON_DISK_PLACEHOLDER {
    MY_ON_DISK_PLACEHOLDER* Next;
    PWSTR RelativePath;
} MY_ON_DISK_PLACEHOLDER;

HRESULT
MyViewUpdater(
    _In_ PRJ_CALLBACK_DATA callbackData,
    _In_ time_t newViewTime
    )
{
    HRESULT hr = S_OK;

    // MyGetOnDiskPlaceholders is a routine the provider might implement to produce
    // a pointer to a list of the placeholders the provider has created in the view.
    MY_ON_DISK_PLACEHOLDER* placeholder = MyGetOnDiskPlaceholders();
    while (placeholder != NULL)
    {
        // MyGetProjectedFileInfo is a routine the provider might implement to
        // determine whether a given file exists in its backing store at a
        // particular timestamp.  If it does, the routine returns a pointer to
        // a PRJ_PLACEHOLDER_INFO struct populated with information about the
        // file.
        PRJ_PLACEHOLDER_INFO* newViewPlaceholderInfo = NULL;
        UINT32 newViewPlaceholderInfoSize = 0;

        newViewPlaceholderInfo = MyGetProjectedFileInfo(placeholder->RelativePath,
                                                 newViewTime,
                                                 &newViewPlaceholderInfoSize);
        if (newViewPlaceholderInfo == NULL)
        {
            // The file no longer exists in the new view.  We want to remove its
            // placeholder from the local cache.
            PRJ_UPDATE_FAILURE_CAUSES deleteFailureReason;
            hr = PrjDeleteFile(callbackData->NamespaceVirtualizationContext,
                               placeholder->RelativePath,
                               PRJ_UPDATE_ALLOW_DIRTY_METADATA
                               | PRJ_UPDATE_ALLOW_DIRTY_DATA
                               | PRJ_UPDATE_ALLOW_TOMBSTONE,
                               &deleteFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not delete [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", deleteFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error deleting [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyRemovePlaceholderData is a routine the provider might implement
            // to remove an item from its list of placeholders it has created in
            // the view.
            MyRemovePlaceholderData(placeholder);
        }
        else
        {
            // The file exists in the new view.  Its local cache state may need
            // to be updated, for example if its content is different in this view.
            // As an optimization, the provider may compare the file's ContentID
            // in the new view (stored in newViewPlaceholderInfo->ContentId) with
            // the ContentID it had in the old view.  If they are the same, calling
            // PrjUpdateFileIfNeeded would not be needed.
            PRJ_UPDATE_FAILURE_CAUSES updateFailureReason;
            hr = PrjUpdateFileIfNeeded(callbackData->NamespaceVirtualizationContext,
                                       placeholder->RelativePath,
                                       newViewPlaceholderInfo,
                                       newViewPlaceholderInfoSize,
                                       PRJ_UPDATE_ALLOW_DIRTY_METADATA
                                       | PRJ_UPDATE_ALLOW_DIRTY_DATA
                                       | PRJ_UPDATE_ALLOW_TOMBSTONE,
                                       &updateFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not update [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", updateFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error updating [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyUpdatePlaceholderData is a routine the provider might implement
            // to update information about a placeholder it has created in the view.
            MyUpdatePlaceholderData(placeholder, newViewPlaceholderInfo);
        }

        placeholder = placeholder->Next;
    }

    return hr;
}
```