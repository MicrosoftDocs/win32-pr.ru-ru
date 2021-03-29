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
# <a name="file-system-operation-notifications"></a>Уведомления операций файловой системы

Помимо обязательных обратных вызовов для обработки перечисления, возврата метаданных файлов и содержимого файлов поставщик может дополнительно зарегистрировать обратный вызов **[PRJ_NOTIFICATION_CB]()** в своем вызове **[пржстартвиртуализинг]()**.  Этот обратный вызов получает уведомления об операциях файловой системы, выполняемых с файлами и каталогами, которые находятся под корнем виртуализации экземпляра.  Некоторые уведомления являются уведомлениями, выполняемыми после операции, которые сообщают поставщику о том, что операция только что завершена.  Другие уведомления — это уведомления о выполнении предварительной операции. Это означает, что поставщик получает уведомление перед выполнением операции.  В уведомлении о предварительной операции поставщик может отменять операцию, возвращая код ошибки из обратного вызова.  Это приводит к сбою операции с возвращенным кодом ошибки.

## <a name="how-to-specify-notifications-to-receive"></a>Как указать уведомления для получения

Если поставщик предоставляет реализацию **PRJ_NOTIFICATION_CB** при запуске экземпляра виртуализации, он также должен указать, какие уведомления он хочет получить.  Уведомления, для которых может быть зарегистрирован поставщик, определяются в перечислении [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) .

Когда поставщик задает уведомления, которые он хочет получить, он использует массив из одной или нескольких структур [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) .  Они определяют "сопоставления уведомлений".  Сопоставление уведомлений — это пара между каталогом, называемая "корневым элементом уведомлений", и набором уведомлений, выраженный в виде битовой маски, который Прожфс должен отправить для этого каталога и его потомков.  Сопоставление уведомлений также можно установить для одного файла.  Файл или каталог, указанный в сопоставлении уведомлений, не обязательно должен существовать в момент, когда поставщик вызывает **пржстартвиртуализинг**, поставщик может указать любой путь, и сопоставление будет применено к нему, если оно когда-либо создано.

Если поставщик указывает несколько сопоставлений уведомлений, а некоторые являются потомками других, сопоставления должны быть указаны в убывающей глубине.  Сопоставления уведомлений на более глубоких уровнях переопределяют уровни более высокого уровня для своих потомков.

Если поставщик не указал набор сопоставлений уведомлений, Прожфс будет по умолчанию отправлять его PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED и PRJ_NOTIFY_FILE_OVERWRITTEN для всех файлов и каталогов, расположенных под корнем виртуализации.

В следующем фрагменте кода показано, как зарегистрировать набор уведомлений при запуске экземпляра виртуализации.

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

## <a name="receiving-notifications"></a>Получение уведомлений

Прожфс отправляет уведомления об операциях файловой системы, вызывая обратный вызов **PRJ_NOTIFICATION_CB** поставщика.  Это делается для каждой операции, зарегистрированной в поставщике.  Если, как в приведенном выше примере, поставщик, зарегистрированный для PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED и приложение создало новый файл в корневом каталоге уведомлений, Прожфс вызовет обратный вызов **PRJ_NOTIFICATION_CB** с новым именем пути к файлу, а параметр _уведомления_ имеет значение PRJ_NOTIFICATION_NEW_FILE_CREATED.

Прожфс отправляет уведомления в следующем списке перед выполнением соответствующей операции файловой системы.  Если поставщик возвращает код ошибки из обратного вызова **PRJ_NOTIFICATION_CB** , операция файловой системы завершится ошибкой и возвратит код ошибки, указанный поставщиком.

* PRJ_NOTIFICATION_PRE_DELETE — файл будет удален.
* PRJ_NOTIFICATION_PRE_RENAME — файл будет переименован.
* PRJ_NOTIFICATION_PRE_SET_HARDLINK — для файла будет создана жесткая связь.
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL — файл будет распакован из заполнителя в полный файл, что означает, что его содержимое, скорее всего, будет изменено.

Прожфс отправляет уведомления в следующем списке после завершения соответствующей операции файловой системы.

* PRJ_NOTIFICATION_FILE_OPENED — уже открыт существующий файл.
  * Несмотря на то, что это уведомление отправляется после открытия файла, поставщик может вернуть код ошибки.  В ответе Прожфс отменяет открытость и возвращает ошибку вызывающему объекту.
* PRJ_NOTIFICATION_NEW_FILE_CREATED — создан новый файл.
* PRJ_NOTIFICATION_FILE_OVERWRITTEN — существующий файл был перезаписан, например путем вызова [креатефилев](/windows/desktop/api/fileapi/nf-fileapi-createfilew) с флагом **CREATE_ALWAYS** _двкреатиондиспоситион_ .
* PRJ_NOTIFICATION_FILE_RENAMED — файл переименован.
* PRJ_NOTIFICATION_HARDLINK_CREATED — для файла была создана [жесткая связь](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) .
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION — файл был закрыт, а содержимое файла не было изменено, а файл не был удален.
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED — файл был закрыт, а содержимое файла было изменено.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED — файл был закрыт, а сам файл был удален в процессе закрытия маркера.

Дополнительные сведения о каждом уведомлении см. в документации по **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.

Параметр _нотификатионпараметерс_ обратного вызова **PRJ_NOTIFICATION_CB** указывает дополнительные параметры для некоторых уведомлений.  Если поставщик получает PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED или PRJ_NOTIFICATION_FILE_OVERWRITTEN или PRJ_NOTIFICATION_FILE_RENAMED уведомление, поставщик может указать новый набор уведомлений для получения файла. Дополнительные сведения см. в документации по **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.

В следующем примере показаны простые примеры того, как поставщик может обработать уведомления, зарегистрированные для, в приведенном выше фрагменте кода.

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