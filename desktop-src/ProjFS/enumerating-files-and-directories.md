---
title: Перечисление файлов и каталогов
description: Описывает, как поставщик Прожфс участвует в перечислении каталогов.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "103789139"
---
# <a name="enumerating-files-and-directories"></a><span data-ttu-id="6c5dc-103">Перечисление файлов и каталогов</span><span class="sxs-lookup"><span data-stu-id="6c5dc-103">Enumerating Files and Directories</span></span>

<span data-ttu-id="6c5dc-104">Когда поставщик сначала создает корень виртуализации, он пуст в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-104">When a provider first creates a virtualization root it is empty on the local system.</span></span>  <span data-ttu-id="6c5dc-105">То есть ни один из элементов хранилища резервных данных еще не был кэширован на диск.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span>  <span data-ttu-id="6c5dc-106">При открытии каждый элемент кэшируется, но пока элемент не будет открыт, он существует только в хранилище резервных данных.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-106">As each item is opened it is cached, but until an item is opened it only exists in the backing data store.</span></span>

<span data-ttu-id="6c5dc-107">Поскольку неоткрытые элементы не имеют локального присутствия, обычное перечисление каталогов не покажет их существование пользователю.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-107">Since unopened items have no local presence, normal directory enumeration would not reveal their existence to the user.</span></span>  <span data-ttu-id="6c5dc-108">Поэтому поставщик должен участвовать в перечислении каталогов, возвращая сведения Прожфс о элементах в резервном хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-108">Therefore the provider must participate in directory enumeration by returning information to ProjFS about items in its backing data store.</span></span>  <span data-ttu-id="6c5dc-109">Прожфс объединяет сведения от поставщика с тем, что находится в локальной файловой системе, чтобы предоставить пользователю унифицированный список содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-109">ProjFS merges the information from the provider with what is on the local file system to present to the user a unified list of the contents of a directory.</span></span>

## <a name="directory-enumeration-callbacks"></a><span data-ttu-id="6c5dc-110">Обратные вызовы перечисления каталогов</span><span class="sxs-lookup"><span data-stu-id="6c5dc-110">Directory Enumeration Callbacks</span></span>

<span data-ttu-id="6c5dc-111">Для участия в перечислении каталогов поставщик должен реализовать **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** и обратные вызовы **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .</span><span class="sxs-lookup"><span data-stu-id="6c5dc-111">To participate in directory enumeration the provider must implement the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)**, and **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callbacks.</span></span>  <span data-ttu-id="6c5dc-112">При перечислении каталога в корне виртуализации поставщика Прожфс выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6c5dc-112">When a directory under the provider's virtualization root gets enumerated, ProjFS performs the following actions:</span></span>

1. <span data-ttu-id="6c5dc-113">Прожфс вызывает обратный вызов **PRJ_START_DIRECTORY_ENUMERATION_CB** поставщика для запуска сеанса перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-113">ProjFS calls the provider's **PRJ_START_DIRECTORY_ENUMERATION_CB** callback to start an enumeration session.</span></span>

    <span data-ttu-id="6c5dc-114">В процессе обработки этого обратного вызова поставщик должен подготовиться к выполнению перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-114">As part of processing this callback the provider should prepare to perform the enumeration.</span></span>  <span data-ttu-id="6c5dc-115">Например, он должен выделить любую память, которой может потребоваться отслеживать ход перечисления в резервном хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-115">For example, it should allocate any memory it may need to track the progress of the enumeration in its backing data store.</span></span>

    <span data-ttu-id="6c5dc-116">Прожфс определяет каталог, перечисленный в члене **FilePathName** параметра _каллбаккдата_ обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-116">ProjFS identifies the directory being enumerated in the **FilePathName** member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="6c5dc-117">Он указывается в качестве пути относительно корня виртуализации.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-117">This is specified as a path relative to the virtualization root.</span></span>  <span data-ttu-id="6c5dc-118">Например, если корень виртуализации расположен в `C:\virtRoot` каталоге, а каталог перечисляется `C:\virtRoot\dir1\dir2` , то элемент **FilePathName** будет содержать `dir1\dir2` .</span><span class="sxs-lookup"><span data-stu-id="6c5dc-118">For example, if the virtualization root is located at `C:\virtRoot`, and the directory being enumerated is `C:\virtRoot\dir1\dir2`, the **FilePathName** member will contain `dir1\dir2`.</span></span>  <span data-ttu-id="6c5dc-119">Поставщик подготовится к перечислению этого пути в резервном хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-119">The provider will prepare to enumerate that path in its backing data store.</span></span>  <span data-ttu-id="6c5dc-120">В зависимости от возможностей резервного хранилища поставщика может иметь смысл выполнить перечисление резервного хранилища в ответном вызове **PRJ_START_DIRECTORY_ENUMERATION_CB** .</span><span class="sxs-lookup"><span data-stu-id="6c5dc-120">Depending on the capabilities of a provider's backing store it may make sense to perform the backing store enumeration in the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback.</span></span>

    <span data-ttu-id="6c5dc-121">Поскольку несколько перечислений могут выполняться параллельно в одном и том же каталоге, каждый обратный вызов перечисления имеет аргумент _енумератионид_ , позволяющий поставщику связать вызовы обратного вызова в одном сеансе перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-121">Because multiple enumerations may occur in parallel in the same directory, each enumeration callback has an _enumerationId_ argument to enable the provider to associate the callback invocations into a single enumeration session.</span></span>

    <span data-ttu-id="6c5dc-122">Если поставщик возвращает S_OK из обратного вызова **PRJ_START_DIRECTORY_ENUMERATION_CB** , он должен поддерживать все сведения о сеансе перечисления, пока прожфс вызывает обратный вызов **PRJ_END_DIRECTORY_ENUMERATION_CB** с тем же значением для _енумератионид_.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-122">If the provider returns S_OK from the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback, it must maintain any enumeration session information it has until ProjFS invokes the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback with the same value for _enumerationId_.</span></span>  <span data-ttu-id="6c5dc-123">Если поставщик возвращает ошибку из **PRJ_START_DIRECTORY_ENUMERATION_CB**, прожфс не будет вызывать обратный вызов **PRJ_END_DIRECTORY_ENUMERATION_CB** для этого _енумератионид_.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-123">If the provider returns an error from **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS will not invoke the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback for that _enumerationId_.</span></span>

1. <span data-ttu-id="6c5dc-124">Прожфс вызывает обратный вызов **PRJ_GET_DIRECTORY_ENUMERATION_CB** поставщика один или несколько раз, чтобы получить содержимое каталога от поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-124">ProjFS calls the provider's **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback one or more times to get the directory contents from the provider.</span></span>

    <span data-ttu-id="6c5dc-125">В ответ на этот обратный вызов поставщик возвращает отсортированный список элементов из резервного хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-125">In response to this callback the provider returns a sorted list of items from its backing data store.</span></span>

    <span data-ttu-id="6c5dc-126">Обратный вызов может предоставить выражение поиска в своем параметре _сеарчекспрессион_ , который используется поставщиком для определения области результатов перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-126">The callback may provide a search expression in its _searchExpression_ parameter that the provider uses to scope the results of the enumeration.</span></span>  <span data-ttu-id="6c5dc-127">Если _сеарчекспрессион_ имеет значение null, поставщик возвращает все записи в каталоге, для которого выполняется перечисление.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-127">If _searchExpression_ is NULL, the provider returns all the entries in the directory being enumerated.</span></span>  <span data-ttu-id="6c5dc-128">Если значение не равно NULL, поставщик может использовать **[прждоеснамеконтаинвилдкардс](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** , чтобы определить, есть ли в выражении подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-128">If it is non-NULL, the provider can use **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** to determine whether there are wildcards in the expression.</span></span>  <span data-ttu-id="6c5dc-129">Если это так, поставщик использует **[пржфиленамематч](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** , чтобы определить, соответствует ли запись в каталоге поисковому выражению.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-129">If there are, the provider uses **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** to determine whether an entry in the directory matches the search expression.</span></span>

    <span data-ttu-id="6c5dc-130">Поставщик должен записать значение _сеарчекспрессион_ при первом вызове этого обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-130">The provider should capture the value of _searchExpression_ on the first invocation of this callback.</span></span>  <span data-ttu-id="6c5dc-131">Он использует захваченное значение при каждом последующем вызове обратного вызова в том же сеансе перечисления, если только PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN не задан в поле **flags** параметра _каллбаккдата_ обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-131">It uses the captured value on any subsequent invocation of the callback in the same enumeration session, unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is set in the **Flags** field of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="6c5dc-132">В этом случае необходимо перехватить значение _сеарчекспрессион_.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-132">In that case it should recapture the value of _searchExpression_.</span></span>

    <span data-ttu-id="6c5dc-133">Если в резервном хранилище нет совпадающих записей, поставщик просто возвращает S_OK из обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-133">If there are no matching entries in its backing store, the provider simply returns S_OK from the callback.</span></span>  <span data-ttu-id="6c5dc-134">В противном случае поставщик форматирует каждую соответствующую запись из своего резервного хранилища в структуру **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** , а затем использует **[пржфиллдирентрибуффер](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** для заполнения буфера, предоставленного параметром _дирентрибуфферхандле_ обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-134">Otherwise the provider formats each matching entry from its backing store into a **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** structure, and then uses **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="6c5dc-135">Поставщик сохраняет Добавление записей до тех пор, пока не добавит их все или до тех пор, пока **пржфиллдирентрибуффер** не возвратит HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).</span><span class="sxs-lookup"><span data-stu-id="6c5dc-135">The provider keeps adding entries until it has added them all or until **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).</span></span>  <span data-ttu-id="6c5dc-136">Затем поставщик возвращает S_OK обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-136">Then the provider returns S_OK from the callback.</span></span>  <span data-ttu-id="6c5dc-137">Обратите внимание, что поставщик должен добавить записи в буфер _дирентрибуфферхандле_ в правильном порядке сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-137">Note that the provider must add the entries to the _dirEntryBufferHandle_ buffer in the correct sort order.</span></span>  <span data-ttu-id="6c5dc-138">Поставщик должен использовать **[пржфиленамекомпаре](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** для определения правильного порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-138">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** to determine the correct sort order.</span></span>

    > <span data-ttu-id="6c5dc-139">Поставщик должен предоставить значение для элемента **datadirectory** **PRJ_FILE_BASIC_INFO**.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-139">The provider must supply a value for the **IsDirectory** member of **PRJ_FILE_BASIC_INFO**.</span></span>  <span data-ttu-id="6c5dc-140">Если параметру **DataDirectory** присвоено значение false, поставщик также должен предоставить значение для элемента **Размер файла** .</span><span class="sxs-lookup"><span data-stu-id="6c5dc-140">If **IsDirectory** is FALSE, the provider must also supply a value for the **FileSize** member.</span></span>
    >
    > <span data-ttu-id="6c5dc-141">Если поставщик не предоставил значения для членов **CreationTime**, **lastAccessTime**, **LastWriteTime** и **чанжетиме** , прожфс будет использовать текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-141">If the provider does not supply values for the **CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime** members, ProjFS will use the current system time.</span></span>
    >
    > <span data-ttu-id="6c5dc-142">Прожфс будет использовать любые FILE_ATTRIBUTEные Флаги наборов поставщиков в члене **FileAttributes** , за исключением FILE_ATTRIBUTE_DIRECTORY; будет задано правильное значение для FILE_ATTRIBUTE_DIRECTORY в элементе **FileAttributes** в соответствии с предоставленным значением элемента **DataDirectory** .</span><span class="sxs-lookup"><span data-stu-id="6c5dc-142">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileAttributes** member except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileAttributes** member according to the supplied value of the **IsDirectory** member.</span></span>

    <span data-ttu-id="6c5dc-143">Если **пржфиллдирентрибуффер** возвращает HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) до того, как Поставщик исчерпал записи для добавления, поставщик должен отследить запись, которую он пытался добавить при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-143">If **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) before the provider runs out of entries to add to it, the provider must keep track of the entry it was trying to add when it received the error.</span></span>  <span data-ttu-id="6c5dc-144">В следующий раз, когда Прожфс вызывает обратный вызов **PRJ_GET_DIRECTORY_ENUMERATION_CB** для того же сеанса перечисления, поставщик должен возобновить добавление записей в буфер _дирентрибуфферхандле_ с записью, которую он пытался добавить.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-144">The next time ProjFS calls the **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback for the same enumeration session, the provider must resume adding entries to the _dirEntryBufferHandle_ buffer with the entry it was trying to add.</span></span>

    > <span data-ttu-id="6c5dc-145">Если резервное хранилище поддерживает символьные ссылки, поставщик должен использовать **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** для заполнения буфера, предоставленного параметром _дирентрибуфферхандле_ обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-145">If the backing store supports symbolic links, the provider must use **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="6c5dc-146">**PrjFillDirEntryBuffer2** поддерживает дополнительные входные данные буфера, позволяющие поставщику указать, что запись перечисления является символьной ссылкой и что ее целью является.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-146">**PrjFillDirEntryBuffer2** supports an extra buffer input that allows the provider to specify that the enumeration entry is a symbolic link and what its target is.</span></span>  <span data-ttu-id="6c5dc-147">В противном случае он ведет себя так, как описано выше, для **пржфиллдирентрибуффер**.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-147">It otherwise behaves as described above for **PrjFillDirEntryBuffer**.</span></span>  <span data-ttu-id="6c5dc-148">В следующем примере используется **PrjFillDirEntryBuffer2** для демонстрации поддержки символьных ссылок.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-148">The following sample uses **PrjFillDirEntryBuffer2** to illustrate support for symbolic links.</span></span>
    >
    > <span data-ttu-id="6c5dc-149">Обратите внимание, что **PrjFillDirEntryBuffer2** поддерживается в Windows 10, версия 2004.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-149">Note that **PrjFillDirEntryBuffer2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="6c5dc-150">Поставщик должен проверять наличие **PrjFillDirEntryBuffer2**, например, с помощью **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-150">A provider should probe for the existence of **PrjFillDirEntryBuffer2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. <span data-ttu-id="6c5dc-151">Прожфс вызывает обратный вызов **PRJ_END_DIRECTORY_ENUMERATION_CB** поставщика для завершения сеанса перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-151">ProjFS calls the provider's **PRJ_END_DIRECTORY_ENUMERATION_CB** callback to end the enumeration session.</span></span>

    <span data-ttu-id="6c5dc-152">Поставщик должен выполнить очистку, которую необходимо выполнить для завершения сеанса перечисления, например освободить память, выделенную в процессе обработки **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span><span class="sxs-lookup"><span data-stu-id="6c5dc-152">The provider should perform any cleanup it needs to do to end the enumeration session, such as deallocate memory allocated as part of processing **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span></span>
