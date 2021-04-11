---
description: Установление подключения
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Установление подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081586"
---
# <a name="establishing-a-connection"></a><span data-ttu-id="fd43b-103">Установление подключения</span><span class="sxs-lookup"><span data-stu-id="fd43b-103">Establishing a Connection</span></span>

<span data-ttu-id="fd43b-104">Когда пользователь выбирает устройство, функция Чуседевице, в свою очередь, вызывает метод [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) , чтобы установить соединение между приложением и устройством.</span><span class="sxs-lookup"><span data-stu-id="fd43b-104">Once the user selects a device, the ChooseDevice function, in turn, calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method to establish a connection between the application and the device.</span></span> <span data-ttu-id="fd43b-105">Метод Ипортабледевице:: Open принимает два аргумента:</span><span class="sxs-lookup"><span data-stu-id="fd43b-105">The IPortableDevice::Open method takes two arguments:</span></span>

-   <span data-ttu-id="fd43b-106">Указатель на строку, завершающуюся нулем, которая указывает самонастраивающийся имя устройства.</span><span class="sxs-lookup"><span data-stu-id="fd43b-106">A pointer to a null-terminated string that specifies the Plug and Play name of the device.</span></span> <span data-ttu-id="fd43b-107">(Эта строка извлекается путем вызова метода [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) GetString.)</span><span class="sxs-lookup"><span data-stu-id="fd43b-107">(This string is retrieved by calling the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.)</span></span>
-   <span data-ttu-id="fd43b-108">Указатель на [**интерфейс ипортабледевицевалуес**](iportabledevicevalues.md) , указывающий сведения о клиенте для приложения.</span><span class="sxs-lookup"><span data-stu-id="fd43b-108">A pointer to an [**IPortableDeviceValues interface**](iportabledevicevalues.md) that specifies client information for the application.</span></span>


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="fd43b-109">В Windows 7 [**ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) поддерживает два идентификатора CLSID для **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="fd43b-109">For Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="fd43b-110">**Идентификатор CLSID \_ Портабледевице** возвращает указатель **ипортабледевице** , который не выполняет статистическую обработку для модуля упаковки с произвольным потоком; **Идентификатор CLSID \_ Портабледевицефтм** — это новый идентификатор CLSID, возвращающий указатель **ипортабледевице** , который выполняет статистическую обработку маршалером свободных потоков.</span><span class="sxs-lookup"><span data-stu-id="fd43b-110">**CLSID\_PortableDevice** returns an **IPortableDevice** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceFTM** is a new CLSID that returns an **IPortableDevice** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="fd43b-111">В противном случае оба указателя поддерживают одну и ту же функциональность.</span><span class="sxs-lookup"><span data-stu-id="fd43b-111">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="fd43b-112">Приложения, которые находятся в однопотоковых апартаментах, должны использовать **CLSID \_ портабледевицефтм** , так как это устраняет издержки, связанные с упаковкой указателя на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fd43b-112">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="fd43b-113">**Идентификатор CLSID \_ Портабледевице** по-прежнему поддерживается для устаревших приложений.</span><span class="sxs-lookup"><span data-stu-id="fd43b-113">**CLSID\_PortableDevice** is still supported for legacy applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd43b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fd43b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd43b-115">**Выбор устройства**</span><span class="sxs-lookup"><span data-stu-id="fd43b-115">**Selecting a Device**</span></span>](selecting-a-device.md)
</dt> </dl>

 

 



