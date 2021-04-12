---
title: Чтение файлов с устройства
description: Чтение файлов с устройства
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Диспетчер устройств Windows Media, чтение файлов с устройств
- диспетчер устройств чтение файлов с устройств
- инструкции по программированию, чтение файлов с устройств
- Классические приложения, чтение файлов с устройств
- Создание приложений диспетчер устройств Windows Media, чтение файлов с устройств
- чтение файлов с устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b80cf820e889b29e612206f90b07e1cb02c4c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252915"
---
# <a name="reading-files-from-the-device"></a><span data-ttu-id="5ccaa-109">Чтение файлов с устройства</span><span class="sxs-lookup"><span data-stu-id="5ccaa-109">Reading Files from the Device</span></span>

<span data-ttu-id="5ccaa-110">Обнаружив файл, который необходимо скопировать с устройства, можно скопировать файл с устройства на компьютер в одном вызове или использовать обратный вызов для чтения байтов файла непосредственно в приложение, которое затем может обрабатывать или сохранять данные в том виде, в котором они встречаются.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-110">When you have found a file you would like to copy from the device, you can then copy the file from the device to the computer in a single call, or use a callback to have the file bytes read directly to your application, which can then process or store the data as it sees fits.</span></span>

<span data-ttu-id="5ccaa-111">Ниже показан базовый способ копирования файла с устройства за один вызов:</span><span class="sxs-lookup"><span data-stu-id="5ccaa-111">The following steps show the basic way to copy a file from a device in a single call:</span></span>

1.  <span data-ttu-id="5ccaa-112">Получение маркера файла на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-112">Get a handle to the file on the device.</span></span> <span data-ttu-id="5ccaa-113">Вы можете получить этот обработчик с помощью рекурсивного поиска файлов или, если вы узнали постоянный идентификатор хранилища, вызвав [**IWMDMDevice3:: финдстораже**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span><span class="sxs-lookup"><span data-stu-id="5ccaa-113">You might obtain the handle by using a recursive file search or, if you know the persistent ID of the storage, by calling [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span></span> <span data-ttu-id="5ccaa-114">В любом случае необходим интерфейс [**ивмдмстораже**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) объекта.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-114">In either case, you need the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface of the object.</span></span>
2.  <span data-ttu-id="5ccaa-115">Определите, является ли хранилище файлом или папкой.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-115">Determine whether the storage is a file or a folder.</span></span> <span data-ttu-id="5ccaa-116">С устройства можно копировать только файлы.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-116">Only files can be copied from the device.</span></span> <span data-ttu-id="5ccaa-117">Вызовите [**ивмдмстораже:: OutAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) , чтобы получить атрибуты хранилища, которые будут сообщать о том, является ли хранилище файлом или папкой.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-117">Call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to get storage attributes, which will tell you whether the storage is a file or a folder.</span></span>
3.  <span data-ttu-id="5ccaa-118">Запросите **ивмдмстораже** для [**ивмдмсторажеконтрол**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)и вызовите [**ивмдмсторажеконтрол:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) , чтобы прочитать файл с устройства и сохранить его в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-118">Query **IWMDMStorage** for [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol), and call [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) to read the file from the device and save it to a specified location.</span></span>

<span data-ttu-id="5ccaa-119">Если вместо этого требуется считать блок файла по блоку с устройства, необходимо реализовать интерфейс обратного вызова [**ивмдмоператион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) .</span><span class="sxs-lookup"><span data-stu-id="5ccaa-119">If, instead, you want to read the file block by block from the device, you must implement the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) callback interface.</span></span> <span data-ttu-id="5ccaa-120">Передайте этот интерфейс в вызов **ивмдмсторажеконтрол:: Read** , и Windows Media Диспетчер устройств будет последовательно передавать блоки данных файлов в обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-120">Pass this interface into the **IWMDMStorageControl::Read** call, and Windows Media Device Manager will send chunks of file data sequentially to your callback.</span></span> <span data-ttu-id="5ccaa-121">Ниже показано, как прочитать блок файла устройства по блоку:</span><span class="sxs-lookup"><span data-stu-id="5ccaa-121">The following steps show how to read a device file block by block:</span></span>

1.  <span data-ttu-id="5ccaa-122">Получите интерфейс **ивмдмстораже** для хранилища и определите, является ли он файлом, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-122">Get the **IWMDMStorage** interface for the storage and determine whether it is a file, as described previously.</span></span>
2.  <span data-ttu-id="5ccaa-123">Подготовьте дескрипторы файлов или другие дескрипторы, необходимые для хранения полученных данных.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-123">Prepare any file handles or other handles you need to hold the received data.</span></span>
3.  <span data-ttu-id="5ccaa-124">Запрос интерфейса **ивмдмсторажеконтрол** хранилища</span><span class="sxs-lookup"><span data-stu-id="5ccaa-124">Query for the storage's **IWMDMStorageControl** interface</span></span>
4.  <span data-ttu-id="5ccaa-125">Вызовите метод **ивмдмсторажеконтрол:: Read** , чтобы начать операцию чтения, передав реализованный интерфейс **ивмдмоператион** .</span><span class="sxs-lookup"><span data-stu-id="5ccaa-125">Call **IWMDMStorageControl::Read** to begin the read operation, passing in the **IWMDMOperation** interface you have implemented.</span></span>
5.  <span data-ttu-id="5ccaa-126">Диспетчер устройств Windows Media отправит блок данных по блоку на устройство, как описано в разделе [Обработка передачи файлов вручную](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="5ccaa-126">Windows Media Device Manager will send the data block by block to your device as described in [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>

<span data-ttu-id="5ccaa-127">Следующая функция примера C++ считывает объект хранилища с устройства.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-127">The following C++ example function reads a storage object from a device.</span></span> <span data-ttu-id="5ccaa-128">Функция принимает необязательный указатель интерфейса **ивмдмоператион** ; при передаче функция создает файл явным образом и обрабатывает запись данных в файл по его реализации **ивмдмоператион:: трансферобжектдата**; в противном случае он считывает файл и сохраняет его в назначении, заданном параметром *пвсздестнаме*.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-128">The function accepts an optional **IWMDMOperation** interface pointer; if submitted, the function will create a file explicitly and handle writing the data to file on its implementation of **IWMDMOperation::TransferObjectData**; if not, it will read the file and save to the destination specified by *pwszDestName*.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5ccaa-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5ccaa-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ccaa-130">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5ccaa-130">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




