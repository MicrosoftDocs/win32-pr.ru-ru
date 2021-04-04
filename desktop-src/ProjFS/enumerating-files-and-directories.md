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
# <a name="enumerating-files-and-directories"></a>Перечисление файлов и каталогов

Когда поставщик сначала создает корень виртуализации, он пуст в локальной системе.  То есть ни один из элементов хранилища резервных данных еще не был кэширован на диск.  При открытии каждый элемент кэшируется, но пока элемент не будет открыт, он существует только в хранилище резервных данных.

Поскольку неоткрытые элементы не имеют локального присутствия, обычное перечисление каталогов не покажет их существование пользователю.  Поэтому поставщик должен участвовать в перечислении каталогов, возвращая сведения Прожфс о элементах в резервном хранилище данных.  Прожфс объединяет сведения от поставщика с тем, что находится в локальной файловой системе, чтобы предоставить пользователю унифицированный список содержимого каталога.

## <a name="directory-enumeration-callbacks"></a>Обратные вызовы перечисления каталогов

Для участия в перечислении каталогов поставщик должен реализовать **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** и обратные вызовы **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .  При перечислении каталога в корне виртуализации поставщика Прожфс выполняет следующие действия:

1. Прожфс вызывает обратный вызов **PRJ_START_DIRECTORY_ENUMERATION_CB** поставщика для запуска сеанса перечисления.

    В процессе обработки этого обратного вызова поставщик должен подготовиться к выполнению перечисления.  Например, он должен выделить любую память, которой может потребоваться отслеживать ход перечисления в резервном хранилище данных.

    Прожфс определяет каталог, перечисленный в члене **FilePathName** параметра _каллбаккдата_ обратного вызова.  Он указывается в качестве пути относительно корня виртуализации.  Например, если корень виртуализации расположен в `C:\virtRoot` каталоге, а каталог перечисляется `C:\virtRoot\dir1\dir2` , то элемент **FilePathName** будет содержать `dir1\dir2` .  Поставщик подготовится к перечислению этого пути в резервном хранилище данных.  В зависимости от возможностей резервного хранилища поставщика может иметь смысл выполнить перечисление резервного хранилища в ответном вызове **PRJ_START_DIRECTORY_ENUMERATION_CB** .

    Поскольку несколько перечислений могут выполняться параллельно в одном и том же каталоге, каждый обратный вызов перечисления имеет аргумент _енумератионид_ , позволяющий поставщику связать вызовы обратного вызова в одном сеансе перечисления.

    Если поставщик возвращает S_OK из обратного вызова **PRJ_START_DIRECTORY_ENUMERATION_CB** , он должен поддерживать все сведения о сеансе перечисления, пока прожфс вызывает обратный вызов **PRJ_END_DIRECTORY_ENUMERATION_CB** с тем же значением для _енумератионид_.  Если поставщик возвращает ошибку из **PRJ_START_DIRECTORY_ENUMERATION_CB**, прожфс не будет вызывать обратный вызов **PRJ_END_DIRECTORY_ENUMERATION_CB** для этого _енумератионид_.

1. Прожфс вызывает обратный вызов **PRJ_GET_DIRECTORY_ENUMERATION_CB** поставщика один или несколько раз, чтобы получить содержимое каталога от поставщика.

    В ответ на этот обратный вызов поставщик возвращает отсортированный список элементов из резервного хранилища данных.

    Обратный вызов может предоставить выражение поиска в своем параметре _сеарчекспрессион_ , который используется поставщиком для определения области результатов перечисления.  Если _сеарчекспрессион_ имеет значение null, поставщик возвращает все записи в каталоге, для которого выполняется перечисление.  Если значение не равно NULL, поставщик может использовать **[прждоеснамеконтаинвилдкардс](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** , чтобы определить, есть ли в выражении подстановочные знаки.  Если это так, поставщик использует **[пржфиленамематч](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** , чтобы определить, соответствует ли запись в каталоге поисковому выражению.

    Поставщик должен записать значение _сеарчекспрессион_ при первом вызове этого обратного вызова.  Он использует захваченное значение при каждом последующем вызове обратного вызова в том же сеансе перечисления, если только PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN не задан в поле **flags** параметра _каллбаккдата_ обратного вызова.  В этом случае необходимо перехватить значение _сеарчекспрессион_.

    Если в резервном хранилище нет совпадающих записей, поставщик просто возвращает S_OK из обратного вызова.  В противном случае поставщик форматирует каждую соответствующую запись из своего резервного хранилища в структуру **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** , а затем использует **[пржфиллдирентрибуффер](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** для заполнения буфера, предоставленного параметром _дирентрибуфферхандле_ обратного вызова.  Поставщик сохраняет Добавление записей до тех пор, пока не добавит их все или до тех пор, пока **пржфиллдирентрибуффер** не возвратит HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).  Затем поставщик возвращает S_OK обратного вызова.  Обратите внимание, что поставщик должен добавить записи в буфер _дирентрибуфферхандле_ в правильном порядке сортировки.  Поставщик должен использовать **[пржфиленамекомпаре](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** для определения правильного порядка сортировки.

    > Поставщик должен предоставить значение для элемента **datadirectory** **PRJ_FILE_BASIC_INFO**.  Если параметру **DataDirectory** присвоено значение false, поставщик также должен предоставить значение для элемента **Размер файла** .
    >
    > Если поставщик не предоставил значения для членов **CreationTime**, **lastAccessTime**, **LastWriteTime** и **чанжетиме** , прожфс будет использовать текущее системное время.
    >
    > Прожфс будет использовать любые FILE_ATTRIBUTEные Флаги наборов поставщиков в члене **FileAttributes** , за исключением FILE_ATTRIBUTE_DIRECTORY; будет задано правильное значение для FILE_ATTRIBUTE_DIRECTORY в элементе **FileAttributes** в соответствии с предоставленным значением элемента **DataDirectory** .

    Если **пржфиллдирентрибуффер** возвращает HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) до того, как Поставщик исчерпал записи для добавления, поставщик должен отследить запись, которую он пытался добавить при возникновении ошибки.  В следующий раз, когда Прожфс вызывает обратный вызов **PRJ_GET_DIRECTORY_ENUMERATION_CB** для того же сеанса перечисления, поставщик должен возобновить добавление записей в буфер _дирентрибуфферхандле_ с записью, которую он пытался добавить.

    > Если резервное хранилище поддерживает символьные ссылки, поставщик должен использовать **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** для заполнения буфера, предоставленного параметром _дирентрибуфферхандле_ обратного вызова.  **PrjFillDirEntryBuffer2** поддерживает дополнительные входные данные буфера, позволяющие поставщику указать, что запись перечисления является символьной ссылкой и что ее целью является.  В противном случае он ведет себя так, как описано выше, для **пржфиллдирентрибуффер**.  В следующем примере используется **PrjFillDirEntryBuffer2** для демонстрации поддержки символьных ссылок.
    >
    > Обратите внимание, что **PrjFillDirEntryBuffer2** поддерживается в Windows 10, версия 2004.  Поставщик должен проверять наличие **PrjFillDirEntryBuffer2**, например, с помощью **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

1. Прожфс вызывает обратный вызов **PRJ_END_DIRECTORY_ENUMERATION_CB** поставщика для завершения сеанса перечисления.

    Поставщик должен выполнить очистку, которую необходимо выполнить для завершения сеанса перечисления, например освободить память, выделенную в процессе обработки **PRJ_START_DIRECTORY_ENUMERATION_CB**.
