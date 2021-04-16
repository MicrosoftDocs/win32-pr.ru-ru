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
# <a name="sending-the-file-to-the-device"></a>Отправка файла на устройство

После перекодирования файла при необходимости и всех метаданных, включая этот формат, приложение может отправить файл на устройство. Для этого необходимо сначала получить интерфейс **ивмдмсторажеконтрол** (или более позднюю версию) для целевого расположения на устройстве. Флаги **вставки** указывают, должно ли новое хранилище быть одноуровневым или дочерним для целевого объекта. После получения целевого объекта можно вызвать [**ивмдмсторажеконтрол:: INSERT**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)или [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) для перемещения файла. Приложение может выполнять чтение данных файла путем реализации [**ивмдмоператион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)или позволить методу **INSERT** автоматически считывать и передавать файл, не предоставляя указатель на реализуемый приложением **ивмдмоператион**.

В следующем коде C++ демонстрируется вызов **Insert3** для записи файла на устройство. Если указатель *поператион* , переданный в **Insert3** , имеет **значение NULL**, файл будет отправлен за один шаг. Если этот указатель является допустимым указателем интерфейса, Windows Media диспетчер устройств будет вызывать метод обратного вызова для получения данных в блоках. Дополнительные сведения о реализации **ивмдмоператион** см. в разделе [Обработка передачи файлов вручную](handling-file-transfers-manually.md).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Запись файлов на устройство**](writing-files-to-the-device.md)
</dt> </dl>

 

 




