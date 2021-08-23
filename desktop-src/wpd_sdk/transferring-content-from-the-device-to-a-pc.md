---
description: Передача содержимого с устройства на компьютер
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: Передача содержимого с устройства на компьютер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8695f8158040e75a4aae40f95386ed70af45df56a137dabc944ab6d1771e69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806524"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a>Передача содержимого с устройства на компьютер

Одной из распространенных операций, выполняемых приложением WPD, является перенос содержимого с подключенного устройства на компьютер.

Передача содержимого выполняется с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                | Описание                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Предоставляет доступ к интерфейсу **ипортабледевицепропертиес** . |
| [**Интерфейс Ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Предоставляет доступ к методам, относящимся к свойствам.                   |
| [**Интерфейс Ипортабледевицересаурцес**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | Используется для хранения ключей свойств для данного профиля.          |
| Интерфейс IStream                                                        | Используется для чтения и записи данных.                                |



 

`TransferContentFromDevice`Функция в модуле контенттрансфер. cpp примера приложения демонстрирует, как приложение может передавать контактную информацию с подключенного устройства на ПК.

Первая задача, выполняемая `TransferContentFromDevice` функцией, — предложить пользователю ввести идентификатор объекта для родительского объекта на устройстве (при этом содержимое будет передано).


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



Следующий шаг — получение объекта **ипортабледевицеконтент** , используемого образцом для доступа к методам, относящимся к содержимому.


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



Следующий шаг — получение объекта **ипортабледевицересаурцес** , используемого образцом для доступа к методам, относящимся к ресурсу.


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



Следующий шаг — получение объекта IStream, который образец использует для чтения данных, передаваемых с устройства.


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



Следующий шаг — получение имени файла объекта на устройстве. Эта строка используется для создания соответствующего имени файла на компьютере. Если у объекта нет имени файла на устройстве, идентификатор объекта преобразуется в строку и используется для создания имени целевого файла.


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



После этого в примере создается целевой объект IStream.


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



Наконец, исходный объект IStream копируется в место назначения на компьютере.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



