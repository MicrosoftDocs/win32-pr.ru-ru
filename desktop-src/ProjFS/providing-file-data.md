---
title: Предоставление данных файлов
description: Описывает, как поставщик предоставляет сведения о заполнителе и данные файлов.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 4f0da65095e908ec3211bb23be654ee9e0e2853c093bb36e8a92701c24106ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792398"
---
# <a name="providing-file-data"></a>Предоставление данных файлов

Когда поставщик сначала создает корень виртуализации, он пуст в локальной системе. То есть ни один из элементов хранилища резервных данных еще не был кэширован на диск. При открытии элементов Прожфс запрашивает сведения от поставщика, чтобы разрешить создание заполнителей для этих элементов в локальной файловой системе.  При доступе к содержимому элемента Прожфс запрашивает это содержимое от поставщика.  Результат заключается в том, что с точки зрения пользователя виртуализированные файлы и каталоги похожи на обычные файлы и каталоги, которые уже находятся в локальной файловой системе.

## <a name="placeholder-creation"></a>Создание заполнителя

Когда приложение пытается открыть обработчик для виртуализированного файла, Прожфс вызывает обратный вызов **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** для каждого элемента пути, который еще не существует на диске.  Например, если приложение пытается открыть `C:\virtRoot\dir1\dir2\file.txt` , но `C:\virtRoot\dir1` на диске существует только путь, то поставщик получит обратный вызов для `C:\virtRoot\dir1\dir2` , а затем для `C:\virtRoot\dir1\dir2\file.txt` .

Когда Прожфс вызывает обратный вызов **PRJ_GET_PLACEHOLDER_INFO_CB** поставщика, поставщик выполняет следующие действия:

1. Поставщик определяет, существует ли запрошенное имя в резервном хранилище.  Поставщик должен использовать **[пржфиленамекомпаре](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** в качестве подпрограммы сравнения при поиске в резервном хранилище, чтобы определить, существует ли запрошенное имя в резервном хранилище.  В противном случае поставщик возвращает HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) обратного вызова.

1. Если запрошенное имя существует в резервном хранилище, поставщик заполняет структуру [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) с помощью метаданных файловой системы элемента и вызывает **[пржвритеплацехолдеринфо](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** для отправки данных в прожфс.  Прожфс будет использовать эти сведения для создания заполнителя в локальной файловой системе для элемента.

    > Прожфс будет использовать любые FILE_ATTRIBUTE Флаги наборов поставщиков в PRJ_PLACEHOLDER_INFO члене **филебасиЦинфо. FileAttributes** , кроме FILE_ATTRIBUTE_DIRECTORY; будет задано правильное значение для FILE_ATTRIBUTE_DIRECTORY в элементе **филебасиЦинфо. FileAttributes** в соответствии с предоставленным значением элемента **филебасиЦинфо. DataDirectory** .

    > Если резервное хранилище поддерживает символьные ссылки, поставщик должен использовать **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** для отправки данных заполнителя в прожфс.  **PrjWritePlaceholderInfo2** поддерживает дополнительные входные данные буфера, позволяющие поставщику указать, что заполнитель является символьной ссылкой, и ее целью является.  В противном случае он ведет себя так, как описано выше, для **пржвритеплацехолдеринфо**.  В следующем примере показано, как использовать **PrjWritePlaceholderInfo2** для предоставления поддержки символьных ссылок.
    >
    > обратите внимание, что **PrjWritePlaceholderInfo2** поддерживается в Windows 10 версии 2004.  Поставщик должен проверять наличие **PrjWritePlaceholderInfo2**, например, с помощью **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

## <a name="providing-file-contents"></a>Предоставление содержимого файлов

Когда Прожфс необходимо обеспечить, чтобы виртуализированный файл содержал данные, например, когда приложение пытается выполнить чтение из файла, Прожфс вызывает обратный вызов **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** для этого элемента, чтобы запросить, что поставщик предоставил содержимое файла.  Поставщик получает данные файла из резервного хранилища и использует **[пржвритефиледата](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** для отправки данных в локальную файловую систему.

> Когда Прожфс вызывает этот обратный вызов, член **FilePathName** параметра _каллбаккдата_ предоставляет имя, которое файл имел при создании его заполнителя.  То есть, если файл был переименован с момента создания заполнителя, обратный вызов предоставляет исходное имя (pre-Rename), а не текущее имя (после переименования).  При необходимости поставщик может использовать член **versionInfo** параметра _каллбаккдата_ для определения того, какие данные запрашиваются.
>
> Дополнительные сведения о том, как можно использовать член **VersionInfo** PRJ_CALLBACK_DATA, см. в документации по [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) и разделу [Обработка изменений в представлении](handling-view-changes.md) .

Поставщику разрешено разбивать диапазон данных, запрошенных в **PRJ_GET_FILE_DATA_CB** обратном вызове, на несколько вызовов **пржвритефиледата**, каждый из которых предоставляет часть запрошенного диапазона.  Однако перед завершением обратного вызова поставщик должен предоставить весь запрошенный диапазон.  Например, если обратный вызов запрашивает 10 МБ данных от _byteOffset_ 0 для _длины_ 10 485 760, поставщик может указать данные в 10 вызовах **пржвритефиледата**, каждая из которых отправляет 1 МБ.

Поставщик также может предоставить больше запрошенного диапазона, вплоть до длины файла.  Диапазон, предоставляемый поставщиком, должен охватывать запрошенный диапазон.  Например, если обратный вызов запрашивает 1 МБ данных из _byteOffset_ 4096 для _длины_ 1 052 672 и файл имеет общий размер 10 МБ, поставщик может вернуть 2 МБ данных, начиная со смещения 0.

### <a name="buffer-alignment-considerations"></a>Рекомендации по выравниванию буфера

Прожфс использует [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) от вызывающего объекта, которому требуются данные для записи данных в локальную файловую систему.  Однако Прожфс не может контролировать, открыт ли FILE_OBJECT для буферизованной или небуферизованной операции ввода-вывода.  Если FILE_OBJECT был открыт для операций ввода-вывода без буферизации, операции чтения и записи в файл должны соответствовать определенным требованиям к выравниванию.  Поставщик может удовлетворять этим требованиям по выравниванию, выполняя два действия:

1. Используйте **[пржаллокатеалигнедбуффер](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** , чтобы выделить буфер для передачи в параметр _буфера_ **пржвритефиледата**.
1. Убедитесь, что параметры _byteOffset_ и _length_ параметра **пржвритефиледата** являются целыми числами, кратными требованиям к выравниванию устройства хранения (Обратите внимание, что параметр _длины_ не должен соответствовать этому требованию, если _byteOffset_  +  _Длина_ равна концу файла).  Поставщик может использовать **[пржжетвиртуализатионинстанцеинфо](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** для получения требования к выравниванию устройства хранения.

Прожфс оставляет его поставщику для вычисления правильного выравнивания.  Это обусловлено тем, что при обработке **PRJ_GET_FILE_DATA_CBного** обратного вызова поставщик может вернуть запрошенные данные между несколькими вызовами **пржвритефиледата** , каждый из которых возвращает часть общих запрошенных данных перед завершением обратного вызова.

> Если поставщик будет использовать один вызов **пржвритефиледата** для записи всего файла, т. е. от _byteOffset_ = 0 до _length_ = размера файла или для возврата точного диапазона, запрошенного в ответном вызове **PRJ_GET_FILE_DATA_CB** , поставщику не нужно выполнять вычисления выравнивания.  Однако он по-прежнему должен использовать **пржаллокатеалигнедбуффер** , чтобы обеспечить соответствие _буфера_ требованиям к выравниванию устройства хранения.

Дополнительные сведения о буферизованном и небуферизованном вводе-выводе см. в разделе [буферизация файлов](/windows/desktop/FileIO/file-buffering) разделов.

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