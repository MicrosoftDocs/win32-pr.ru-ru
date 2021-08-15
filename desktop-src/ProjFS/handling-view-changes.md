---
title: Обработка изменений представления
description: Описывает, как обновить клиентское представление резервного хранилища поставщика.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 99ace7849b8967748f26210d9d6b770e424c349359aa39e828c8ad9af36a65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792651"
---
# <a name="handling-view-changes"></a>Обработка изменений представления

По мере открытия файлов и каталогов в корне виртуализации поставщик создает заполнители на диске, а файлы считываются заполнители с содержимым.  Эти заполнители представляют состояние резервного хранилища на момент создания.  Эти кэшированные элементы в сочетании с элементами, проецируемыми поставщиком в перечислениях, составляют представление резервного хранилища клиента.  Время от времени поставщику может потребоваться обновить представление клиента, будь это из-за изменений в резервном хранилище или из-за явного действия, предпринимаемого пользователем для изменения их представления.

> Если поставщик обновляет представление заранее при изменении резервного хранилища, рекомендуется, чтобы изменения в представлении были довольно редки.  Это связано с тем, что при изменении представления элемента, который был открыт, и, таким образом, на диске был создан заполнитель, необходимо обновить или удалить элемент на диске, чтобы отразить изменение представления.  Частые обновления могут привести к дополнительным действиям с диском, которые могут негативно сказаться на производительности системы.

## <a name="item-versioning"></a>Управление версиями элементов

Для поддержки обслуживания нескольких представлений Прожфс предоставляет **[PRJ_PLACEHOLDER_VERSION_INFOную](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** структуру.  Поставщик использует эту структуру автономно в вызовах **[пржмаркдиректорясплацехолдер](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** и внедряется в структуры **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** и **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .  **PRJ_PLACEHOLDER_VERSION_INFO**. В поле ContentID поставщик хранит до 128 байт сведений о версии для файла или каталога.  Поставщик может внутренне связать это значение с некоторым значением, определяющим конкретное представление.

Например, поставщик, выполняющий виртуализацию репозитория системы управления версиями, может использовать хэш содержимого файла для использования в качестве идентификатора ContentID и может использовать метки времени для обнаружения представлений репозитория в разные моменты времени.  Метки времени могут быть временем выполнения фиксации в репозитории.

Используя пример репозитория с отметкой времени, типичным потоком для использования ContentID элемента может быть:

1. Клиент устанавливает представление, указывая отметку времени, в которой будет представлено содержимое репозитория.  Это можно сделать через некоторый интерфейс, реализованный поставщиком, а не через API Прожфс.  Например, поставщик может иметь программу командной строки, которую можно использовать, чтобы сообщить поставщику о необходимости просмотра.
1. Когда клиент создает маркер для виртуализированного файла или каталога, поставщик создает для него заполнитель, используя метаданные файловой системы из резервного хранилища.  Конкретный набор метаданных, который он использует, определяется значением ContentID, связанным с меткой времени нужного представления.  Когда поставщик вызывает **[пржвритеплацехолдеринфо](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** для записи сведений заполнителя, он предоставляет идентификатор ContentID в члене versionInfo аргумента _плацехолдеринфо_ .  Затем поставщик должен записать заполнитель для этого файла или каталога, созданный в этом представлении.
1. Когда клиент считывает данные из заполнителя, вызывается обратный вызов **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** поставщика.  Элемент VersionInfo в параметре _каллбаккдата_ содержит идентификатор объекта ContentID, указанный в **пржвритеплацехолдеринфо** при создании заполнителя файла.  Поставщик использует объект ContentID для получения правильного содержимого файла из резервного хранилища.
1. Клиент запрашивает изменение представления, указывая новую метку времени.  Для каждого заполнитель поставщика, созданного в предыдущем представлении, если в новом представлении существует другая версия этого файла, поставщик может заменить заполнитель на диске обновленным, идентификатором ContentID которого связан с новой меткой времени, вызвав **[пржупдатефилеифнидед](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.  Кроме того, поставщик может удалить заполнитель, вызвав **[пржделетефиле](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** , чтобы новое представление файла было проецировано в перечислениях.  Если файл не существует в новом представлении, поставщик должен удалить его, вызвав **пржделетефиле**.

Обратите внимание, что поставщик должен гарантировать, что когда клиент перечислит каталог, поставщик предоставит содержимое, соответствующее представлению клиента.  Например, поставщик может использовать член VersionInfo параметра _каллбаккдата_ **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** и **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** обратные вызовы для получения содержимого каталога в режиме реального времени.  Кроме того, можно создать структуру каталогов для этого представления в резервном хранилище в процессе создания представления, а затем просто перечислить эту структуру.

> При вызове обратного вызова поставщика для заполнителя или частичного файла сведения о версии, указанные поставщиком при создании элемента, предоставляются в элементе VersionInfo в параметре _каллбаккдата_ обратного вызова.

## <a name="updating-the-view"></a>Обновление представления

Ниже приведен пример функции, показывающей, как поставщик может обновлять локальное представление, когда пользователь указывает новую метку времени.  Функция получает список заполнителей поставщика, созданного для представления, измененного пользователем, и обновляет локальное состояние кэша на основе состояния каждого заполнителя в новом представлении.  Для ясности эта подпрограммы не имеет определенных сложностей, связанных с файловой системой.  Например, в старом представлении указанный каталог может существовать с некоторыми файлами или каталогами, но в новом представлении этот каталог (и его содержимое) больше не может существовать.  Чтобы избежать ошибок в такой ситуации, поставщик должен обновить состояние файла и каталогов под корнем виртуализации в первую очередь.

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