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
# <a name="transferring-an-image-or-music-file-to-the-device"></a><span data-ttu-id="3980b-103">Передача образа или музыкального файла на устройство</span><span class="sxs-lookup"><span data-stu-id="3980b-103">Transferring an Image or Music File to the Device</span></span>

<span data-ttu-id="3980b-104">Одной из наиболее распространенных операций, выполняемых приложением, является перенос содержимого на подключенное устройство.</span><span class="sxs-lookup"><span data-stu-id="3980b-104">One of the most common operations accomplished by an application is the transfer of content to a connected device.</span></span>

<span data-ttu-id="3980b-105">Передача содержимого выполняется с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3980b-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="3980b-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="3980b-106">Interface</span></span>                                                                | <span data-ttu-id="3980b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3980b-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3980b-108">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="3980b-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="3980b-109">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="3980b-109">Provides access to the content-specific methods.</span></span>               |
| [<span data-ttu-id="3980b-110">**Интерфейс Ипортабледевицедатастреам**</span><span class="sxs-lookup"><span data-stu-id="3980b-110">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | <span data-ttu-id="3980b-111">Используется при записи содержимого на устройство.</span><span class="sxs-lookup"><span data-stu-id="3980b-111">Used when writing the content to the device.</span></span>                   |
| [<span data-ttu-id="3980b-112">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="3980b-112">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="3980b-113">Используется для получения свойств, описывающих содержимое.</span><span class="sxs-lookup"><span data-stu-id="3980b-113">Used to retrieve properties that describe the content.</span></span>         |
| <span data-ttu-id="3980b-114">Интерфейс IStream</span><span class="sxs-lookup"><span data-stu-id="3980b-114">IStream Interface</span></span>                                                        | <span data-ttu-id="3980b-115">Используется для упрощения чтения содержимого и записи на устройство.</span><span class="sxs-lookup"><span data-stu-id="3980b-115">Used to simplify reading of content and writing to the device.</span></span> |



 

<span data-ttu-id="3980b-116">`TransferContentToDevice`Функция в модуле контенттрансфер. cpp примера приложения демонстрирует, как приложение может передавать содержимое с компьютера на подключенное устройство.</span><span class="sxs-lookup"><span data-stu-id="3980b-116">The `TransferContentToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer content from a PC to a connected device.</span></span> <span data-ttu-id="3980b-117">В этом конкретном примере переданное содержимое может быть файлом, содержащим изображение, музыку или контактную информацию.</span><span class="sxs-lookup"><span data-stu-id="3980b-117">In this particular sample, the transferred content can be a file containing an image, music, or contact information.</span></span>

<span data-ttu-id="3980b-118">Первая задача, выполняемая `TransferContentToDevice` функцией, — предложить пользователю ввести идентификатор объекта, который определяет объект для передачи.</span><span class="sxs-lookup"><span data-stu-id="3980b-118">The first task accomplished by the `TransferContentToDevice` function is to prompt the user to enter an object identifier, which identifies the object to be transferred.</span></span>


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



<span data-ttu-id="3980b-119">Вторая задача, выполняемая `TransferContentToDevice` функцией, — создание объекта [**ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) путем вызова метода [**ипортабледевице:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="3980b-119">The second task accomplished by the `TransferContentToDevice` function is to create an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


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



<span data-ttu-id="3980b-120">Следующей задачей, выполняемой `TransferContentToDevice` функцией, является создание диалогового окна **FileOpen** , с помощью которого пользователь может указать расположение и имя переносимого файла.</span><span class="sxs-lookup"><span data-stu-id="3980b-120">The next task accomplished by the `TransferContentToDevice` function is the creation of a **FileOpen** dialog with which the user can specify the location and name of the file to be transferred.</span></span>


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



<span data-ttu-id="3980b-121">`TransferContentToDevice`Функция передает строку фильтра ( `wszFileTypeFilter` ) в метод GetOpenFilename, который определяет тип файлов, которые может выбрать пользователь.</span><span class="sxs-lookup"><span data-stu-id="3980b-121">The `TransferContentToDevice` function passes a filter string (`wszFileTypeFilter`) to the GetOpenFileName method, which determines the type of files that the user can choose.</span></span> <span data-ttu-id="3980b-122">`DoMenu`Примеры трех различных фильтров, разрешенных образцом, см. в функции в модуле впдаписампле. cpp.</span><span class="sxs-lookup"><span data-stu-id="3980b-122">Refer to the `DoMenu` function in the WpdApiSample.cpp module for examples of the three different filters allowed by the sample.</span></span>

<span data-ttu-id="3980b-123">После того как пользователь определит определенный файл для перемещения на устройство, `TransferContentToDevice` функция откроет этот файл как объект IStream и извлечет свойства, необходимые для завершения перемещения.</span><span class="sxs-lookup"><span data-stu-id="3980b-123">After the user identifies a particular file for transfer to the device, the `TransferContentToDevice` function opens that file as an IStream object and retrieves properties that are required to complete the transfer.</span></span>


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



<span data-ttu-id="3980b-124">Обязательные свойства извлекаются путем вызова `GetRequiredPropertiesForContentType` вспомогательной функции, которая работает с объектом IStream.</span><span class="sxs-lookup"><span data-stu-id="3980b-124">The required properties are retrieved by calling the`GetRequiredPropertiesForContentType` helper-function, which operates on the IStream object.</span></span> <span data-ttu-id="3980b-125">`GetRequiredPropertiesForContentType`Вспомогательная функция создает объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , извлекает свойства из следующего списка и добавляет их в этот объект.</span><span class="sxs-lookup"><span data-stu-id="3980b-125">The `GetRequiredPropertiesForContentType` helper-function creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, retrieves the properties in the following list, and adds them to this object.</span></span>

-   <span data-ttu-id="3980b-126">Идентификатор родительского объекта</span><span class="sxs-lookup"><span data-stu-id="3980b-126">Parent-object identifier</span></span>
-   <span data-ttu-id="3980b-127">Размер потока в байтах</span><span class="sxs-lookup"><span data-stu-id="3980b-127">Stream size in bytes</span></span>
-   <span data-ttu-id="3980b-128">Имя файла содержимого</span><span class="sxs-lookup"><span data-stu-id="3980b-128">Content file name</span></span>
-   <span data-ttu-id="3980b-129">Имя содержимого (имя файла без расширения)</span><span class="sxs-lookup"><span data-stu-id="3980b-129">Content name (the file name without the extension)</span></span>
-   <span data-ttu-id="3980b-130">Тип содержимого (изображение, звук или контакт)</span><span class="sxs-lookup"><span data-stu-id="3980b-130">Content type (image, audio, or contact)</span></span>
-   <span data-ttu-id="3980b-131">Формат содержимого (JFIF, WMA или vCard2)</span><span class="sxs-lookup"><span data-stu-id="3980b-131">Content format (JFIF, WMA, or vCard2)</span></span>

<span data-ttu-id="3980b-132">Пример приложения использует полученные свойства для создания нового содержимого на устройстве.</span><span class="sxs-lookup"><span data-stu-id="3980b-132">The sample application uses the retrieved properties to create the new content on the device.</span></span> <span data-ttu-id="3980b-133">Это выполняется в три этапа:</span><span class="sxs-lookup"><span data-stu-id="3980b-133">This is done in three phases:</span></span>

1.  <span data-ttu-id="3980b-134">Приложение вызывает метод [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) для создания нового объекта IStream на устройстве.</span><span class="sxs-lookup"><span data-stu-id="3980b-134">The application calls [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) method to create a new IStream object on the device.</span></span>
2.  <span data-ttu-id="3980b-135">Приложение использует этот объект для получения объекта [**ипортабледевицедатастреам**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) из драйвера WPD.</span><span class="sxs-lookup"><span data-stu-id="3980b-135">The application uses this object to obtain an [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) object from the WPD driver.</span></span>
3.  <span data-ttu-id="3980b-136">Приложение использует новый объект **ипортабледевицедатастреам** для записи содержимого на устройство (через вспомогательную функцию стреамкопи).</span><span class="sxs-lookup"><span data-stu-id="3980b-136">The application uses the new **IPortableDeviceDataStream** object to write the content to the device (via the StreamCopy helper function).</span></span> <span data-ttu-id="3980b-137">Вспомогательная функция записывает данные из исходного файла в поток, возвращенный методом [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="3980b-137">The helper function writes the data from the source file to the stream returned by [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span>
4.  <span data-ttu-id="3980b-138">Приложение завершает операцию, вызывая метод Commit в потоке назначения.</span><span class="sxs-lookup"><span data-stu-id="3980b-138">The application completes the operation by calling the Commit method on the destination stream.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3980b-139">См. также</span><span class="sxs-lookup"><span data-stu-id="3980b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3980b-140">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="3980b-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="3980b-141">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="3980b-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="3980b-142">**Интерфейс Ипортабледевицедатастреам**</span><span class="sxs-lookup"><span data-stu-id="3980b-142">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[<span data-ttu-id="3980b-143">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="3980b-143">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3980b-144">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="3980b-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



