---
title: Чтение файлов с устройства
description: Чтение файлов с устройства
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Диспетчер устройств мультимедиа, чтение файлов с устройств
- диспетчер устройств чтение файлов с устройств
- инструкции по программированию, чтение файлов с устройств
- Классические приложения, чтение файлов с устройств
- создание Windows мультимедиа диспетчер устройств приложений, чтение файлов с устройств
- чтение файлов с устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4352be59a335461f46bfc722146e4c51d31f72c1559e9ad8631e80cb6752c241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904004"
---
# <a name="reading-files-from-the-device"></a>Чтение файлов с устройства

Обнаружив файл, который необходимо скопировать с устройства, можно скопировать файл с устройства на компьютер в одном вызове или использовать обратный вызов для чтения байтов файла непосредственно в приложение, которое затем может обрабатывать или сохранять данные в том виде, в котором они встречаются.

Ниже показан базовый способ копирования файла с устройства за один вызов:

1.  Получение маркера файла на устройстве. Вы можете получить этот обработчик с помощью рекурсивного поиска файлов или, если вы узнали постоянный идентификатор хранилища, вызвав [**IWMDMDevice3:: финдстораже**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage). В любом случае необходим интерфейс [**ивмдмстораже**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) объекта.
2.  Определите, является ли хранилище файлом или папкой. С устройства можно копировать только файлы. Вызовите [**ивмдмстораже:: OutAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) , чтобы получить атрибуты хранилища, которые будут сообщать о том, является ли хранилище файлом или папкой.
3.  Запросите **ивмдмстораже** для [**ивмдмсторажеконтрол**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)и вызовите [**ивмдмсторажеконтрол:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) , чтобы прочитать файл с устройства и сохранить его в указанном расположении.

Если вместо этого требуется считать блок файла по блоку с устройства, необходимо реализовать интерфейс обратного вызова [**ивмдмоператион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) . передайте этот интерфейс в вызов **ивмдмсторажеконтрол:: Read** , а Windows Media диспетчер устройств будет последовательно отсылать блоки данных файлов в обратный вызов. Ниже показано, как прочитать блок файла устройства по блоку:

1.  Получите интерфейс **ивмдмстораже** для хранилища и определите, является ли он файлом, как описано выше.
2.  Подготовьте дескрипторы файлов или другие дескрипторы, необходимые для хранения полученных данных.
3.  Запрос интерфейса **ивмдмсторажеконтрол** хранилища
4.  Вызовите метод **ивмдмсторажеконтрол:: Read** , чтобы начать операцию чтения, передав реализованный интерфейс **ивмдмоператион** .
5.  Windows Носитель диспетчер устройств отправит блок данных по блоку на устройство, как описано в разделе [Обработка передачи файлов вручную](handling-file-transfers-manually.md).

Следующая функция примера C++ считывает объект хранилища с устройства. Функция принимает необязательный указатель интерфейса **ивмдмоператион** ; при передаче функция создает файл явным образом и обрабатывает запись данных в файл по его реализации **ивмдмоператион:: трансферобжектдата**; в противном случае он считывает файл и сохраняет его в назначении, заданном параметром *пвсздестнаме*.


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**создание Windows мультимедиа диспетчер устройств приложение**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




