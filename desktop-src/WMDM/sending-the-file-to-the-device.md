---
title: Отправка файла на устройство
description: Отправка файла на устройство
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Диспетчер устройств Windows Media, отправка файлов на устройства
- диспетчер устройств Отправка файлов на устройства
- Путеводитель по программированию, отправка файлов на устройства
- Классические приложения, отправка файлов на устройства
- Создание приложений диспетчер устройств Windows Media, отправка файлов на устройства
- запись файлов на устройства, отправка файлов на устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65be0c18a6022538dc5573d936f63392234e9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532189"
---
# <a name="sending-the-file-to-the-device"></a><span data-ttu-id="97303-109">Отправка файла на устройство</span><span class="sxs-lookup"><span data-stu-id="97303-109">Sending the File to the Device</span></span>

<span data-ttu-id="97303-110">После перекодирования файла при необходимости и всех метаданных, включая этот формат, приложение может отправить файл на устройство.</span><span class="sxs-lookup"><span data-stu-id="97303-110">After the file has been transcoded if necessary, and all metadata including the format has been set, your application can send the file to the device.</span></span> <span data-ttu-id="97303-111">Для этого необходимо сначала получить интерфейс **ивмдмсторажеконтрол** (или более позднюю версию) для целевого расположения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="97303-111">In order to do so, you must first get an **IWMDMStorageControl** interface (or a later version) for a target location on the device.</span></span> <span data-ttu-id="97303-112">Флаги **вставки** указывают, должно ли новое хранилище быть одноуровневым или дочерним для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="97303-112">The **Insert** flags specify whether the new storage should be a sibling or child of the target.</span></span> <span data-ttu-id="97303-113">После получения целевого объекта можно вызвать [**ивмдмсторажеконтрол:: INSERT**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)или [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) для перемещения файла.</span><span class="sxs-lookup"><span data-stu-id="97303-113">Once you have gotten the target, you can call [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to transfer the file.</span></span> <span data-ttu-id="97303-114">Приложение может выполнять чтение данных файла путем реализации [**ивмдмоператион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)или позволить методу **INSERT** автоматически считывать и передавать файл, не предоставляя указатель на реализуемый приложением **ивмдмоператион**.</span><span class="sxs-lookup"><span data-stu-id="97303-114">The application can handle reading the file data itself by implementing [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), or it can allow the **Insert** method to read and transfer the file automatically by not providing a pointer to an application-implemented **IWMDMOperation**.</span></span>

<span data-ttu-id="97303-115">В следующем коде C++ демонстрируется вызов **Insert3** для записи файла на устройство.</span><span class="sxs-lookup"><span data-stu-id="97303-115">The following C++ code demonstrates calling **Insert3** to write a file to a device.</span></span> <span data-ttu-id="97303-116">Если указатель *поператион* , переданный в **Insert3** , имеет **значение NULL**, файл будет отправлен за один шаг. Если этот указатель является допустимым указателем интерфейса, Windows Media диспетчер устройств будет вызывать метод обратного вызова для получения данных в блоках.</span><span class="sxs-lookup"><span data-stu-id="97303-116">If the *pOperation* pointer passed to **Insert3** is **NULL**, the file will be sent in one step; if this pointer is a valid interface pointer, Windows Media Device Manager will call your callback method to get data in blocks.</span></span> <span data-ttu-id="97303-117">Дополнительные сведения о реализации **ивмдмоператион** см. в разделе [Обработка передачи файлов вручную](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="97303-117">For details on how to implement **IWMDMOperation**, see [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a><span data-ttu-id="97303-118">См. также</span><span class="sxs-lookup"><span data-stu-id="97303-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97303-119">**Запись файлов на устройство**</span><span class="sxs-lookup"><span data-stu-id="97303-119">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




