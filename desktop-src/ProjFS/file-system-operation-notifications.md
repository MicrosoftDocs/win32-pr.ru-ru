---
title: Уведомления операций файловой системы
description: Описывает, как поставщик может получать уведомления об операциях файловой системы.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792006"
---
# <a name="file-system-operation-notifications"></a><span data-ttu-id="067f7-103">Уведомления операций файловой системы</span><span class="sxs-lookup"><span data-stu-id="067f7-103">File System Operation Notifications</span></span>

<span data-ttu-id="067f7-104">Помимо обязательных обратных вызовов для обработки перечисления, возврата метаданных файлов и содержимого файлов поставщик может дополнительно зарегистрировать обратный вызов **[PRJ_NOTIFICATION_CB]()** в своем вызове **[пржстартвиртуализинг]()**.</span><span class="sxs-lookup"><span data-stu-id="067f7-104">In addition to required callbacks for handling enumeration, returning file metadata, and file contents, a provider may optionally register a **[PRJ_NOTIFICATION_CB]()** callback in its call to **[PrjStartVirtualizing]()**.</span></span>  <span data-ttu-id="067f7-105">Этот обратный вызов получает уведомления об операциях файловой системы, выполняемых с файлами и каталогами, которые находятся под корнем виртуализации экземпляра.</span><span class="sxs-lookup"><span data-stu-id="067f7-105">This callback receives notifications of file system operations performed on files and directories beneath the instance's virtualization root.</span></span>  <span data-ttu-id="067f7-106">Некоторые уведомления являются уведомлениями, выполняемыми после операции, которые сообщают поставщику о том, что операция только что завершена.</span><span class="sxs-lookup"><span data-stu-id="067f7-106">Some of the notifications are "post-operation" notifications, which tell the provider that an operation has just completed.</span></span>  <span data-ttu-id="067f7-107">Другие уведомления — это уведомления о выполнении предварительной операции. Это означает, что поставщик получает уведомление перед выполнением операции.</span><span class="sxs-lookup"><span data-stu-id="067f7-107">The other notifications are "pre-operation" notifications, meaning that the provider is notified before the operation happens.</span></span>  <span data-ttu-id="067f7-108">В уведомлении о предварительной операции поставщик может отменять операцию, возвращая код ошибки из обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="067f7-108">In a pre-operation notification the provider can veto the operation by returning an error code from the callback.</span></span>  <span data-ttu-id="067f7-109">Это приводит к сбою операции с возвращенным кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="067f7-109">This causes the operation to fail with the returned error code.</span></span>

## <a name="how-to-specify-notifications-to-receive"></a><span data-ttu-id="067f7-110">Как указать уведомления для получения</span><span class="sxs-lookup"><span data-stu-id="067f7-110">How to Specify Notifications to Receive</span></span>

<span data-ttu-id="067f7-111">Если поставщик предоставляет реализацию **PRJ_NOTIFICATION_CB** при запуске экземпляра виртуализации, он также должен указать, какие уведомления он хочет получить.</span><span class="sxs-lookup"><span data-stu-id="067f7-111">If the provider supplies an implementation of **PRJ_NOTIFICATION_CB** when it starts a virtualization instance, it should also specify which notifications it wishes to receive.</span></span>  <span data-ttu-id="067f7-112">Уведомления, для которых может быть зарегистрирован поставщик, определяются в перечислении [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) .</span><span class="sxs-lookup"><span data-stu-id="067f7-112">The notifications for which the provider can register are defined in the [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span></span>

<span data-ttu-id="067f7-113">Когда поставщик задает уведомления, которые он хочет получить, он использует массив из одной или нескольких структур [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) .</span><span class="sxs-lookup"><span data-stu-id="067f7-113">When the provider specifies the notifications it wishes to receive, it does so using an array of one or more [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) structures.</span></span>  <span data-ttu-id="067f7-114">Они определяют "сопоставления уведомлений".</span><span class="sxs-lookup"><span data-stu-id="067f7-114">These define "notification mappings".</span></span>  <span data-ttu-id="067f7-115">Сопоставление уведомлений — это пара между каталогом, называемая "корневым элементом уведомлений", и набором уведомлений, выраженный в виде битовой маски, который Прожфс должен отправить для этого каталога и его потомков.</span><span class="sxs-lookup"><span data-stu-id="067f7-115">A notification mapping is a pairing between a directory, referred to as a "notification root", and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants.</span></span>  <span data-ttu-id="067f7-116">Сопоставление уведомлений также можно установить для одного файла.</span><span class="sxs-lookup"><span data-stu-id="067f7-116">A notification mapping can also be established for a single file.</span></span>  <span data-ttu-id="067f7-117">Файл или каталог, указанный в сопоставлении уведомлений, не обязательно должен существовать в момент, когда поставщик вызывает **пржстартвиртуализинг**, поставщик может указать любой путь, и сопоставление будет применено к нему, если оно когда-либо создано.</span><span class="sxs-lookup"><span data-stu-id="067f7-117">A file or directory specified in a notification mapping does not have to exist already at the time the provider calls **PrjStartVirtualizing**, the provider can specify any path and the mapping will apply to it if it is ever created.</span></span>

<span data-ttu-id="067f7-118">Если поставщик указывает несколько сопоставлений уведомлений, а некоторые являются потомками других, сопоставления должны быть указаны в убывающей глубине.</span><span class="sxs-lookup"><span data-stu-id="067f7-118">If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth.</span></span>  <span data-ttu-id="067f7-119">Сопоставления уведомлений на более глубоких уровнях переопределяют уровни более высокого уровня для своих потомков.</span><span class="sxs-lookup"><span data-stu-id="067f7-119">Notification mappings at deeper levels override higher-level ones for their descendants.</span></span>

<span data-ttu-id="067f7-120">Если поставщик не указал набор сопоставлений уведомлений, Прожфс будет по умолчанию отправлять его PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED и PRJ_NOTIFY_FILE_OVERWRITTEN для всех файлов и каталогов, расположенных под корнем виртуализации.</span><span class="sxs-lookup"><span data-stu-id="067f7-120">If the provider does not specify a set of notification mappings, ProjFS will default to sending it PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED, and PRJ_NOTIFY_FILE_OVERWRITTEN for all files and directories beneath the virtualization root.</span></span>

<span data-ttu-id="067f7-121">В следующем фрагменте кода показано, как зарегистрировать набор уведомлений при запуске экземпляра виртуализации.</span><span class="sxs-lookup"><span data-stu-id="067f7-121">The following code snippet illustrates how to register a set of notifications when starting a virtualization instance.</span></span>

```C++
PRJ_CALLBACKS callbackTable;

// Supply required callbacks.
callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
callbackTable.GetFileDataCallback = MyGetFileDataCallback;

// The rest of the callbacks are optional.  We want notifications, so specify
// our notification callback.
callbackTable.QueryFileNameCallback = nullptr;
callbackTable.NotificationCallback = MyNotificationCallback;
callbackTable.CancelCommandCallback = nullptr;

// Assume the provider has created a new virtualization root at C:\VirtRoot and
// initialized it with this layout:
//
//     C:\VirtRoot
//     +--- baz
//     \--- foo
//          +--- subdir1
//          \--- subdir2
//
// The provider wants these notifications:
// * Notification of new file/directory creates for all locations within the
//   virtualization root that are not subject to one of the following more
//   specific notification mappings.
// * Notification of new file/directory creates, file opens, post-renames, and
//   pre- and post-deletes for C:\VirtRoot\foo
// * No notifications for C:\VirtRoot\foo\subdir1
PRJ_STARTVIRTUALIZING_OPTIONS startOpts = {};
PRJ_VIRTUALIZATION_MAPPING notificationMappings[3];

// Configure default notifications - notify of new files for most of the tree.
notificationMappings[0].NotificationRoot = L"";
notificationMappings[0].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED;

// Override default notifications - notify of new files, opened files, and file
// deletes for C:\VirtRoot\foo and its descendants.
notificationMappings[1].NotificationRoot = L"foo";
notificationMappings[1].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED |
                                              PRJ_NOTIFY_FILE_OPENED |
                                              PRJ_NOTIFY_PRE_DELETE |
                                              PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |
                                              PRJ_NOTIFY_FILE_RENAMED;

// Override all notifications for C:\VirtRoot\foo\subdir1 and its descendants.
notificationMappings[2].NotificationRoot = L"foo\\subdir1";
notificationMappings[2].NotificationBitMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;

startOpts.NotificationMappings = notificationMappings;
startOpts.NotificationMappingsCount = ARRAYSIZE(notificationMapping);

// Start the instance and provide our notification mappings.
HRESULT hr;
PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
hr = PrjStartVirtualizing(rootName,
                          &callbackTable,
                          nullptr,
                          &startOpts,
                          &instanceHandle);
if (FAILED(hr))
{
    wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
    return;
}
```

## <a name="receiving-notifications"></a><span data-ttu-id="067f7-122">Получение уведомлений</span><span class="sxs-lookup"><span data-stu-id="067f7-122">Receiving Notifications</span></span>

<span data-ttu-id="067f7-123">Прожфс отправляет уведомления об операциях файловой системы, вызывая обратный вызов **PRJ_NOTIFICATION_CB** поставщика.</span><span class="sxs-lookup"><span data-stu-id="067f7-123">ProjFS sends notifications of file system operations by calling the provider's **PRJ_NOTIFICATION_CB** callback.</span></span>  <span data-ttu-id="067f7-124">Это делается для каждой операции, зарегистрированной в поставщике.</span><span class="sxs-lookup"><span data-stu-id="067f7-124">It does this for each operation the provider has registered for.</span></span>  <span data-ttu-id="067f7-125">Если, как в приведенном выше примере, поставщик, зарегистрированный для PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED и приложение создало новый файл в корневом каталоге уведомлений, Прожфс вызовет обратный вызов **PRJ_NOTIFICATION_CB** с новым именем пути к файлу, а параметр _уведомления_ имеет значение PRJ_NOTIFICATION_NEW_FILE_CREATED.</span><span class="sxs-lookup"><span data-stu-id="067f7-125">If, as in the above example, the provider registered for PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, and an application created a new file in the notification root, ProjFS would call the **PRJ_NOTIFICATION_CB** callback with the new file's path name and the _notification_ parameter set to PRJ_NOTIFICATION_NEW_FILE_CREATED.</span></span>

<span data-ttu-id="067f7-126">Прожфс отправляет уведомления в следующем списке перед выполнением соответствующей операции файловой системы.</span><span class="sxs-lookup"><span data-stu-id="067f7-126">ProjFS sends the notifications in the following list before the associated file system operation takes place.</span></span>  <span data-ttu-id="067f7-127">Если поставщик возвращает код ошибки из обратного вызова **PRJ_NOTIFICATION_CB** , операция файловой системы завершится ошибкой и возвратит код ошибки, указанный поставщиком.</span><span class="sxs-lookup"><span data-stu-id="067f7-127">If the provider returns a failure code from the **PRJ_NOTIFICATION_CB** callback, the file system operation will fail and return the failure code the provider specified.</span></span>

* <span data-ttu-id="067f7-128">PRJ_NOTIFICATION_PRE_DELETE — файл будет удален.</span><span class="sxs-lookup"><span data-stu-id="067f7-128">PRJ_NOTIFICATION_PRE_DELETE - The file is about to be deleted.</span></span>
* <span data-ttu-id="067f7-129">PRJ_NOTIFICATION_PRE_RENAME — файл будет переименован.</span><span class="sxs-lookup"><span data-stu-id="067f7-129">PRJ_NOTIFICATION_PRE_RENAME - The file is about to be renamed.</span></span>
* <span data-ttu-id="067f7-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK — для файла будет создана жесткая связь.</span><span class="sxs-lookup"><span data-stu-id="067f7-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK - A hard link is about to be created for the file.</span></span>
* <span data-ttu-id="067f7-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL — файл будет распакован из заполнителя в полный файл, что означает, что его содержимое, скорее всего, будет изменено.</span><span class="sxs-lookup"><span data-stu-id="067f7-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - A file is about to be expanded from a placeholder to a full file, which indicates its contents are likely to be modified.</span></span>

<span data-ttu-id="067f7-132">Прожфс отправляет уведомления в следующем списке после завершения соответствующей операции файловой системы.</span><span class="sxs-lookup"><span data-stu-id="067f7-132">ProjFS sends the notifications in the following list after the associated file system operation has completed.</span></span>

* <span data-ttu-id="067f7-133">PRJ_NOTIFICATION_FILE_OPENED — уже открыт существующий файл.</span><span class="sxs-lookup"><span data-stu-id="067f7-133">PRJ_NOTIFICATION_FILE_OPENED - An existing file has been opened.</span></span>
  * <span data-ttu-id="067f7-134">Несмотря на то, что это уведомление отправляется после открытия файла, поставщик может вернуть код ошибки.</span><span class="sxs-lookup"><span data-stu-id="067f7-134">Even though this notification is sent after the file has been opened, the provider can return a failure code.</span></span>  <span data-ttu-id="067f7-135">В ответе Прожфс отменяет открытость и возвращает ошибку вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="067f7-135">In response, ProjFS will cancel the open and return the failure to the caller.</span></span>
* <span data-ttu-id="067f7-136">PRJ_NOTIFICATION_NEW_FILE_CREATED — создан новый файл.</span><span class="sxs-lookup"><span data-stu-id="067f7-136">PRJ_NOTIFICATION_NEW_FILE_CREATED - A new file has been created.</span></span>
* <span data-ttu-id="067f7-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN — существующий файл был перезаписан, например путем вызова [креатефилев](/windows/desktop/api/fileapi/nf-fileapi-createfilew) с флагом **CREATE_ALWAYS** _двкреатиондиспоситион_ .</span><span class="sxs-lookup"><span data-stu-id="067f7-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN - An existing file has been overwritten, for example by calling [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) with the **CREATE_ALWAYS** _dwCreationDisposition_ flag.</span></span>
* <span data-ttu-id="067f7-138">PRJ_NOTIFICATION_FILE_RENAMED — файл переименован.</span><span class="sxs-lookup"><span data-stu-id="067f7-138">PRJ_NOTIFICATION_FILE_RENAMED - A file has been renamed.</span></span>
* <span data-ttu-id="067f7-139">PRJ_NOTIFICATION_HARDLINK_CREATED — для файла была создана [жесткая связь](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) .</span><span class="sxs-lookup"><span data-stu-id="067f7-139">PRJ_NOTIFICATION_HARDLINK_CREATED - A [hard link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) has been created for a file.</span></span>
* <span data-ttu-id="067f7-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION — файл был закрыт, а содержимое файла не было изменено, а файл не был удален.</span><span class="sxs-lookup"><span data-stu-id="067f7-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - A file handle has been closed, and the file's content was not modified, nor was the file deleted.</span></span>
* <span data-ttu-id="067f7-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED — файл был закрыт, а содержимое файла было изменено.</span><span class="sxs-lookup"><span data-stu-id="067f7-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - A file handle has been closed, and the file's content has been modified.</span></span>
* <span data-ttu-id="067f7-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED — файл был закрыт, а сам файл был удален в процессе закрытия маркера.</span><span class="sxs-lookup"><span data-stu-id="067f7-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - A file handle has been closed, and the file was deleted as part of closing the handle.</span></span>

<span data-ttu-id="067f7-143">Дополнительные сведения о каждом уведомлении см. в документации по **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span><span class="sxs-lookup"><span data-stu-id="067f7-143">For more details on each notification refer to the documentation for **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span></span>

<span data-ttu-id="067f7-144">Параметр _нотификатионпараметерс_ обратного вызова **PRJ_NOTIFICATION_CB** указывает дополнительные параметры для некоторых уведомлений.</span><span class="sxs-lookup"><span data-stu-id="067f7-144">The **PRJ_NOTIFICATION_CB** callback's _notificationParameters_ parameter specifies extra parameters for certain notifications.</span></span>  <span data-ttu-id="067f7-145">Если поставщик получает PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED или PRJ_NOTIFICATION_FILE_OVERWRITTEN или PRJ_NOTIFICATION_FILE_RENAMED уведомление, поставщик может указать новый набор уведомлений для получения файла.</span><span class="sxs-lookup"><span data-stu-id="067f7-145">If a provider receives a PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, or PRJ_NOTIFICATION_FILE_OVERWRITTEN, or PRJ_NOTIFICATION_FILE_RENAMED notification, the provider can specify a new set of notifications to receive for the file.</span></span> <span data-ttu-id="067f7-146">Дополнительные сведения см. в документации по **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span><span class="sxs-lookup"><span data-stu-id="067f7-146">For further details, refer to the documentation for **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span></span>

<span data-ttu-id="067f7-147">В следующем примере показаны простые примеры того, как поставщик может обработать уведомления, зарегистрированные для, в приведенном выше фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="067f7-147">The following sample shows simple examples of how a provider might process the notifications it registered for in the code snippet above.</span></span>

```C++
#include <windows.h>

HRESULT
MyNotificationCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ BOOLEAN isDirectory,
    _In_ PRJ_NOTIFICATION notification,
    _In_opt_z_ PCWSTR destinationFileName,
    _Inout_ PRJ_NOTIFICATION_PARAMETERS* operationParameters
    )
{
    HRESULT hr = S_OK;

    switch (notification)
    {
    case PRJ_NOTIFY_NEW_FILE_CREATED:

        wprintf(L"A new %ls was created at [%ls].\n",
                isDirectory ? L"directory" : L"file",
                callbackData->FilePathName);

        // Let's stop getting notifications inside newly-created directories.
        if (isDirectory)
        {
            operationParameters->PostCreate.NotificationMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;
        }
        break;

    case PRJ_NOTIFY_FILE_OPENED:

        wprintf(L"Handle opened to %ls [%ls].\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_PRE_DELETE:

        wprintf(L"Attempt to delete %ls [%ls]: ",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);

        // MyAllowDelete is a routine the provider might implement to decide
        // whether to allow a given file/directory to be deleted.
        if (!MyAllowDelete(callbackData->FilePathName, isDirectory))
        {
            wprintf(L"DENIED\n");
            hr = HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED);
        }
        else
        {
            wprintf(L"ALLOWED\n");
        }
        break;

    case PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:

        wprintf(L"The %ls [%ls] was deleted.\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_FILE_RENAMED:

        if (wcslen(callbackData->FilePathName) == 0)
        {
            // If callbackData->FilePathName is an empty string, then the item
            // that was renamed was originally in a location not under the
            // virtualization root.
            wprintf(L"A %ls was renamed into the virtualization root,\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its new location is [%ls].\n",
                    destinationFileName);
        }
        else if (wcslen(destinationFileName) == 0)
        {
            // If destinationFileName is an empty string, then the item that was
            // renamed is now in a location not under the virtualization root.
            wprintf(L"A %ls was renamed out of the virtualization root.\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its original location was [%ls].\n",
                    callbackData->FilePathName);
        }
        else
        {
            // If both names are specified, both the new and old names are under
            // the virtualization root (it is never the case that nether name is
            // specified).
            wprintf(L"A %ls [%ls] was renamed.\n",
                    isDirectory ? L"directory": L"file",
                    callbackData->FilePathName);
            wprintf(L"Its new name is [%ls].\n", destinationFileName);
        }
        break;

    default:
        wprintf(L"Unrecognized notification: 0x%08x");
    }

    // Note that this may be a failure code from MyAllowDelete().
    return hr;
}
```