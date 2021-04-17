---
description: Передача образа или музыкального файла на устройство
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Передача образа или музыкального файла на устройство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3308212825f6c67ea79a40873fc466164d62f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712565"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a>Передача образа или музыкального файла на устройство

Одной из наиболее распространенных операций, выполняемых приложением, является перенос содержимого на подключенное устройство.

Передача содержимого выполняется с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                | Описание                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Предоставляет доступ к методам, относящимся к содержимому.               |
| [**Интерфейс Ипортабледевицедатастреам**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | Используется при записи содержимого на устройство.                   |
| [**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)         | Используется для получения свойств, описывающих содержимое.         |
| Интерфейс IStream                                                        | Используется для упрощения чтения содержимого и записи на устройство. |



 

`TransferContentToDevice`Функция в модуле контенттрансфер. cpp примера приложения демонстрирует, как приложение может передавать содержимое с компьютера на подключенное устройство. В этом конкретном примере переданное содержимое может быть файлом, содержащим изображение, музыку или контактную информацию.

Первая задача, выполняемая `TransferContentToDevice` функцией, — предложить пользователю ввести идентификатор объекта, который определяет объект для передачи.


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



Вторая задача, выполняемая `TransferContentToDevice` функцией, — создание объекта [**ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) путем вызова метода [**ипортабледевице:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Следующей задачей, выполняемой `TransferContentToDevice` функцией, является создание диалогового окна **FileOpen** , с помощью которого пользователь может указать расположение и имя переносимого файла.


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



`TransferContentToDevice`Функция передает строку фильтра ( `wszFileTypeFilter` ) в метод GetOpenFilename, который определяет тип файлов, которые может выбрать пользователь. `DoMenu`Примеры трех различных фильтров, разрешенных образцом, см. в функции в модуле впдаписампле. cpp.

После того как пользователь определит определенный файл для перемещения на устройство, `TransferContentToDevice` функция откроет этот файл как объект IStream и извлечет свойства, необходимые для завершения перемещения.


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



Обязательные свойства извлекаются путем вызова `GetRequiredPropertiesForContentType` вспомогательной функции, которая работает с объектом IStream. `GetRequiredPropertiesForContentType`Вспомогательная функция создает объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , извлекает свойства из следующего списка и добавляет их в этот объект.

-   Идентификатор родительского объекта
-   Размер потока в байтах
-   Имя файла содержимого
-   Имя содержимого (имя файла без расширения)
-   Тип содержимого (изображение, звук или контакт)
-   Формат содержимого (JFIF, WMA или vCard2)

Пример приложения использует полученные свойства для создания нового содержимого на устройстве. Это выполняется в три этапа:

1.  Приложение вызывает метод [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) для создания нового объекта IStream на устройстве.
2.  Приложение использует этот объект для получения объекта [**ипортабледевицедатастреам**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) из драйвера WPD.
3.  Приложение использует новый объект **ипортабледевицедатастреам** для записи содержимого на устройство (через вспомогательную функцию стреамкопи). Вспомогательная функция записывает данные из исходного файла в поток, возвращенный методом [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).
4.  Приложение завершает операцию, вызывая метод Commit в потоке назначения.


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицедатастреам**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



