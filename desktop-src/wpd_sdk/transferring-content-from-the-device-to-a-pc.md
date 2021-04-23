---
description: Передача содержимого с устройства на компьютер
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: Передача содержимого с устройства на компьютер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de06861ba74b4b7883c8d96e25cebe3fbb64e21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265983"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a><span data-ttu-id="1ed1f-103">Передача содержимого с устройства на компьютер</span><span class="sxs-lookup"><span data-stu-id="1ed1f-103">Transferring Content from the Device to a PC</span></span>

<span data-ttu-id="1ed1f-104">Одной из распространенных операций, выполняемых приложением WPD, является перенос содержимого с подключенного устройства на компьютер.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-104">One common operation accomplished by a WPD application is the transfer of content from a connected device to the PC.</span></span>

<span data-ttu-id="1ed1f-105">Передача содержимого выполняется с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="1ed1f-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="1ed1f-106">Interface</span></span>                                                                | <span data-ttu-id="1ed1f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1ed1f-107">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="1ed1f-108">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="1ed1f-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="1ed1f-109">Предоставляет доступ к интерфейсу **ипортабледевицепропертиес** .</span><span class="sxs-lookup"><span data-stu-id="1ed1f-109">Provides access to the **IPortableDeviceProperties** interface.</span></span> |
| [<span data-ttu-id="1ed1f-110">**Интерфейс Ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="1ed1f-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="1ed1f-111">Предоставляет доступ к методам, относящимся к свойствам.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-111">Provides access to property-specific methods.</span></span>                   |
| [<span data-ttu-id="1ed1f-112">**Интерфейс Ипортабледевицересаурцес**</span><span class="sxs-lookup"><span data-stu-id="1ed1f-112">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | <span data-ttu-id="1ed1f-113">Используется для хранения ключей свойств для данного профиля.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-113">Used to store the property keys for the given profile.</span></span>          |
| <span data-ttu-id="1ed1f-114">Интерфейс IStream</span><span class="sxs-lookup"><span data-stu-id="1ed1f-114">IStream Interface</span></span>                                                        | <span data-ttu-id="1ed1f-115">Используется для чтения и записи данных.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-115">Used to read and write the data.</span></span>                                |



 

<span data-ttu-id="1ed1f-116">`TransferContentFromDevice`Функция в модуле контенттрансфер. cpp примера приложения демонстрирует, как приложение может передавать контактную информацию с подключенного устройства на ПК.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-116">The `TransferContentFromDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a connected device to a PC.</span></span>

<span data-ttu-id="1ed1f-117">Первая задача, выполняемая `TransferContentFromDevice` функцией, — предложить пользователю ввести идентификатор объекта для родительского объекта на устройстве (при этом содержимое будет передано).</span><span class="sxs-lookup"><span data-stu-id="1ed1f-117">The first task accomplished by the `TransferContentFromDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                            hr                   = S_OK;
WCHAR                              szSelection[81]      = {0};
CComPtr<IPortableDeviceContent>    pContent;
CComPtr<IPortableDeviceResources>  pResources;
CComPtr<IPortableDeviceProperties> pProperties;
CComPtr<IStream>                   pObjectDataStream;
CComPtr<IStream>                   pFinalFileStream;
DWORD                              cbOptimalTransferSize = 0;
CAtlStringW                        strOriginalFileName;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Prompt user to enter an object identifier on the device to transfer.
printf("Enter the identifer of the object you wish to transfer.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="1ed1f-118">Следующий шаг — получение объекта **ипортабледевицеконтент** , используемого образцом для доступа к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-118">The next step is the retrieval of an **IPortableDeviceContent** object that the sample uses to access the content-specific methods.</span></span>


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



<span data-ttu-id="1ed1f-119">Следующий шаг — получение объекта **ипортабледевицересаурцес** , используемого образцом для доступа к методам, относящимся к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-119">The next step is the retrieval of an **IPortableDeviceResources** object that the sample uses to access the resource-specific methods.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="1ed1f-120">Следующий шаг — получение объекта IStream, который образец использует для чтения данных, передаваемых с устройства.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-120">The next step is the retrieval of an IStream object that the sample uses to read the data it is transferring from the device.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pResources->GetStream(szSelection,             // Identifier of the object we want to transfer
                               WPD_RESOURCE_DEFAULT,    // We are transferring the default resource (which is the entire object's data)
                               STGM_READ,               // Opening a stream in READ mode, because we are reading data from the device.
                               &cbOptimalTransferSize,  // Driver supplied optimal transfer size
                               &pObjectDataStream);
    if (FAILED(hr))
    {
        printf("! Failed to get IStream (representing object data on the device) from IPortableDeviceResources, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="1ed1f-121">Следующий шаг — получение имени файла объекта на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-121">The next step is the retrieval of the object's file name on the device.</span></span> <span data-ttu-id="1ed1f-122">Эта строка используется для создания соответствующего имени файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-122">This string is used to create the corresponding file name on the PC.</span></span> <span data-ttu-id="1ed1f-123">Если у объекта нет имени файла на устройстве, идентификатор объекта преобразуется в строку и используется для создания имени целевого файла.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-123">If the object does not have a file name on the device, the object's identifier is converted to a string and used to create the destination file name.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (SUCCEEDED(hr))
    {
        hr = GetStringValue(pProperties,
                            szSelection,
                            WPD_OBJECT_ORIGINAL_FILE_NAME,
                            strOriginalFileName);
        if (FAILED(hr))
        {
            printf("! Failed to read WPD_OBJECT_ORIGINAL_FILE_NAME on object '%ws', hr = 0x%lx\n", szSelection, hr);
            strOriginalFileName.Format(L"%ws.data", szSelection);
            printf("* Creating a filename '%ws' as a default.\n", (PWSTR)strOriginalFileName.GetString());
            // Set the HRESULT to S_OK, so we can continue with our newly generated
            // temporary file name.
            hr = S_OK;
        }
    }
    else
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="1ed1f-124">После этого в примере создается целевой объект IStream.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-124">After this, the sample creates a destination IStream object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = SHCreateStreamOnFile(strOriginalFileName, STGM_CREATE|STGM_WRITE, &pFinalFileStream);
    if (FAILED(hr))
    {
        printf("! Failed to create a temporary file named (%ws) to transfer object (%ws), hr = 0x%lx\n",(PWSTR)strOriginalFileName.GetString(), szSelection, hr);
    }
}
```



<span data-ttu-id="1ed1f-125">Наконец, исходный объект IStream копируется в место назначения на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1ed1f-125">Finally, the source IStream object is copied to the destination on the PC.</span></span>


```C++
if (SUCCEEDED(hr))
{
    DWORD cbTotalBytesWritten = 0;

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    hr = StreamCopy(pFinalFileStream,       // Destination (The Final File to transfer to)
                    pObjectDataStream,      // Source (The Object's data to transfer from)
                    cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                    &cbTotalBytesWritten);  // The total number of bytes transferred from device to the finished file
    if (FAILED(hr))
    {
        printf("! Failed to transfer object from device, hr = 0x%lx\n",hr);
    }
    else
    {
        printf("* Transferred object '%ws' to '%ws'.\n", szSelection, (PWSTR)strOriginalFileName.GetString());
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="1ed1f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1ed1f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ed1f-127">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="1ed1f-127">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="1ed1f-128">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="1ed1f-128">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="1ed1f-129">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="1ed1f-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="1ed1f-130">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="1ed1f-130">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



