---
title: Перечисление устройств (пакет SDK для WMP)
description: В этом примере кода показана функция, которая перечисляет устройства, создавая массив указателей, каждый из которых представляет устройство.
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Проигрыватель Windows Media, переносные устройства
- Объектная модель проигрывателя Windows Media, переносные устройства
- Объектная модель, портативные устройства
- Элемент управления ActiveX проигрывателя Windows Media, переносные устройства
- Элемент управления ActiveX, переносные устройства
- Мобильный элемент управления ActiveX проигрывателя Windows Media, портативные устройства
- Проигрыватель Windows Media Mobile, переносные устройства
- переносные устройства, перечисление
- перечисления, портативные устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44f71fa26f40983424ced70280d9c03e0892a00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068441"
---
# <a name="enumerating-devices"></a><span data-ttu-id="b21d3-112">Перечисление устройств</span><span class="sxs-lookup"><span data-stu-id="b21d3-112">Enumerating Devices</span></span>

<span data-ttu-id="b21d3-113">Проигрыватель Windows Media представляет переносные устройства с помощью интерфейса **ивмпсинкдевице** .</span><span class="sxs-lookup"><span data-stu-id="b21d3-113">Windows Media Player represents portable devices by using the **IWMPSyncDevice** interface.</span></span> <span data-ttu-id="b21d3-114">В следующем примере кода показана функция, которая создает массив указателей на **ивмпсинкдевице**.</span><span class="sxs-lookup"><span data-stu-id="b21d3-114">The following example code shows a function that creates an array of pointers to **IWMPSyncDevice**.</span></span> <span data-ttu-id="b21d3-115">Каждый указатель в массиве представляет устройство, для которого проигрыватель Windows Media хранит информацию.</span><span class="sxs-lookup"><span data-stu-id="b21d3-115">Each pointer in the array represents a device for which Windows Media Player has stored information.</span></span> <span data-ttu-id="b21d3-116">Устройство не обязательно должно быть подключено к компьютеру и не должно иметь связи с текущим экземпляром проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b21d3-116">A device is not required to be connected to the computer, nor is it required to have a partnership with the current Windows Media Player instance.</span></span>

<span data-ttu-id="b21d3-117">При получении события **DeviceConnect** или **девицедисконнект** необходимо перечислить устройства.</span><span class="sxs-lookup"><span data-stu-id="b21d3-117">You should enumerate devices whenever you receive the **DeviceConnect** event or the **DeviceDisconnect** event.</span></span>

<span data-ttu-id="b21d3-118">Следующая функция перечисляет устройства.</span><span class="sxs-lookup"><span data-stu-id="b21d3-118">The following function enumerates devices.</span></span> <span data-ttu-id="b21d3-119">Параметр *бконнектедонли* указывает, следует ли перечислять только те устройства, которые в настоящее время подключены к компьютеру пользователя.</span><span class="sxs-lookup"><span data-stu-id="b21d3-119">The *bConnectedOnly* parameter specifies whether to enumerate only devices currently connected to the user's computer.</span></span>


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="b21d3-120">Аналогичный код можно использовать для получения других списков устройств.</span><span class="sxs-lookup"><span data-stu-id="b21d3-120">You might use similar code to retrieve other such device lists.</span></span> <span data-ttu-id="b21d3-121">Например, можно использовать [ивмпсинкдевице:: Get \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) , чтобы создать массив устройств, для которых существует партнерство.</span><span class="sxs-lookup"><span data-stu-id="b21d3-121">For example, you could use [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) to create an array of devices for which a partnership exists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b21d3-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b21d3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b21d3-123">**IWMPEvents2::D Евицеконнект**</span><span class="sxs-lookup"><span data-stu-id="b21d3-123">**IWMPEvents2::DeviceConnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[<span data-ttu-id="b21d3-124">**IWMPEvents2::D Евицедисконнект**</span><span class="sxs-lookup"><span data-stu-id="b21d3-124">**IWMPEvents2::DeviceDisconnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[<span data-ttu-id="b21d3-125">**Интерфейс Ивмпсинкдевице**</span><span class="sxs-lookup"><span data-stu-id="b21d3-125">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="b21d3-126">**Ивмпсинкдевице:: получить \_ подключение**</span><span class="sxs-lookup"><span data-stu-id="b21d3-126">**IWMPSyncDevice::get\_connected**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[<span data-ttu-id="b21d3-127">**Интерфейс Ивмпсинксервицес**</span><span class="sxs-lookup"><span data-stu-id="b21d3-127">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[<span data-ttu-id="b21d3-128">**Работа с портативными устройствами**</span><span class="sxs-lookup"><span data-stu-id="b21d3-128">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




