---
title: Перечисление устройств Windows Media диспетчер устройств
description: Узнайте, как перечислить устройства, обнаруженные диспетчер устройств Windows Media, с помощью интерфейса перечисления.
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Диспетчер устройств Windows Media, перечисление устройств
- Диспетчер устройств, перечисление устройств
- программное содержимое, перечисление устройств
- Классические приложения, перечисление устройств
- Создание приложений диспетчер устройств Windows Media, перечисление устройств
- Перечисление устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94653d59b0880e9d52f43b34e21522a220d39beb
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068201"
---
# <a name="enumerating-windows-media-device-manager-devices"></a><span data-ttu-id="b4923-109">Перечисление устройств Windows Media диспетчер устройств</span><span class="sxs-lookup"><span data-stu-id="b4923-109">Enumerating Windows Media Device Manager devices</span></span>

<span data-ttu-id="b4923-110">После проверки подлинности приложения можно приступить к перечислению устройств, обнаруженных диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b4923-110">After authenticating an application, you can begin to enumerate the devices detected by Windows Media Device Manager.</span></span> <span data-ttu-id="b4923-111">Перечисление выполняется с помощью интерфейса перечисления [**ивмдменумдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), полученного с помощью [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) или [**ивмдевицеманажер:: енумдевицес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span><span class="sxs-lookup"><span data-stu-id="b4923-111">Enumeration is done by using an enumeration interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtained by using either [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) or [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span></span> <span data-ttu-id="b4923-112">Если поддерживается, используйте метод **EnumDevices2** , поскольку более ранняя версия возвращала только устаревшие интерфейсы на устройствах, а новая версия возвращает как устаревшие, так и новые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b4923-112">If supported, use the **EnumDevices2** method, because the earlier version only returned legacy interfaces on devices, whereas the new version returns both the legacy and the new interfaces.</span></span>

<span data-ttu-id="b4923-113">Перед получением перечислителя необходимо решить, какое представление перечисления следует использовать.</span><span class="sxs-lookup"><span data-stu-id="b4923-113">Before obtaining an enumerator, you should decide what enumeration view to use.</span></span> <span data-ttu-id="b4923-114">Некоторые устройства предоставляют каждое хранилище как отдельное устройство.</span><span class="sxs-lookup"><span data-stu-id="b4923-114">Some devices expose each storage as a different device.</span></span> <span data-ttu-id="b4923-115">Например, два адаптера флэш-памяти на устройстве будут перечисляться так, как если бы они были отдельными устройствами.</span><span class="sxs-lookup"><span data-stu-id="b4923-115">For example, two flash memory cards on a device will enumerate as if they were separate devices.</span></span> <span data-ttu-id="b4923-116">Можно указать, что все хранилища на устройстве перечисляются вместе как одно устройство.</span><span class="sxs-lookup"><span data-stu-id="b4923-116">You can specify that all storages on a device are enumerated together as a single device.</span></span> <span data-ttu-id="b4923-117">Этот параметр можно задать только один раз в приложении. Если вы хотите изменить его, необходимо завершить работу приложения и перезапустить его.</span><span class="sxs-lookup"><span data-stu-id="b4923-117">You can set this preference only once in your application; if you want to change it, you must shut down the application and restart it.</span></span> <span data-ttu-id="b4923-118">Однако обратите внимание, что устаревшие устройства иногда игнорируют запрос на перечисление отдельных хранилищ устройств в качестве одного устройства и продолжают перечислять их по отдельности.</span><span class="sxs-lookup"><span data-stu-id="b4923-118">However, note that legacy devices will sometimes ignore a request to enumerate separate device storages as a single device, and continue to enumerate them separately.</span></span>

<span data-ttu-id="b4923-119">Ниже приведены инструкции по перечислению подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="b4923-119">The following steps show how to enumerate connected devices:</span></span>

1.  <span data-ttu-id="b4923-120">Задайте параметры перечисления устройств с помощью [**IWMDeviceManager3:: сетдевицеенумпреференце**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span><span class="sxs-lookup"><span data-stu-id="b4923-120">Set the device enumeration preference using [**IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span></span> <span data-ttu-id="b4923-121">Если этот метод не вызывается, метод по умолчанию отображает хранилища как отдельные устройства.</span><span class="sxs-lookup"><span data-stu-id="b4923-121">If this method is not called, the default method is to show storages as separate devices.</span></span> <span data-ttu-id="b4923-122">Чтобы определить, являются ли отдельные "устройства" на самом деле хранилищами на одном устройстве, вызовите [**IWMDMDevice2:: жетканоникалнаме**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); хранилища из одного устройства будут возвращать идентичные значения, за исключением последней цифры после последнего знака $.</span><span class="sxs-lookup"><span data-stu-id="b4923-122">To determine whether individual "devices" are actually storages on the same device, call [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); storages from the same device will return identical values, except for the final digit after the last "$" sign.</span></span>
2.  <span data-ttu-id="b4923-123">Выполните запрос для [**ивмдевицеманажер**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) или [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), а затем вызовите [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) , чтобы получить интерфейс перечислителя устройства, [**ивмдменумдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span><span class="sxs-lookup"><span data-stu-id="b4923-123">Query for [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) or [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), and then call [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) to obtain the device enumerator interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span></span> <span data-ttu-id="b4923-124">(Если поддерживается, используйте **EnumDevices2**, что более эффективно, так как предыдущая версия не может возвращать устройства MTP).</span><span class="sxs-lookup"><span data-stu-id="b4923-124">(If supported, use **EnumDevices2**, which is more efficient, as the earlier version may not return MTP devices).</span></span>
3.  <span data-ttu-id="b4923-125">Вызовите метод [**ивмдменумдевицес:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) , чтобы получить одно или несколько устройств за раз.</span><span class="sxs-lookup"><span data-stu-id="b4923-125">Call the [**IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) method to retrieve one or more devices at a time.</span></span> <span data-ttu-id="b4923-126">Продолжайте вызывать этот метод до тех пор, пока метод не возвратит \_ значение S false или сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b4923-126">Continue to call this method until the method returns S\_FALSE or an error message.</span></span> <span data-ttu-id="b4923-127">При извлечении только одного устройства за раз вам не нужно распределять массив для хранения устройств.</span><span class="sxs-lookup"><span data-stu-id="b4923-127">If retrieving only one device at a time, you do not need to allocate an array to hold the devices.</span></span>

<span data-ttu-id="b4923-128">Поскольку пользователи могут подключать или удалять устройства с компьютера во время работы приложения, рекомендуется реализовать уведомление о подключении или удалении устройства.</span><span class="sxs-lookup"><span data-stu-id="b4923-128">Because users can attach or remove devices from the computer while your application is running, it is a good idea to implement notification of device connection or removal.</span></span> <span data-ttu-id="b4923-129">Это делается путем реализации интерфейса [**ивмдмнотификатион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) и его регистрации.</span><span class="sxs-lookup"><span data-stu-id="b4923-129">This is done by implementing the [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) interface and registering it.</span></span> <span data-ttu-id="b4923-130">Дополнительные сведения об этом см. в разделе [Включение уведомлений](enabling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b4923-130">For more information on this, see [Enabling Notifications](enabling-notifications.md).</span></span>

<span data-ttu-id="b4923-131">Следующий код C++ перечисляет устройства и запрашивает сведения о каждом устройстве.</span><span class="sxs-lookup"><span data-stu-id="b4923-131">The following C++ code enumerates devices and requests information about each device.</span></span>


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b4923-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b4923-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4923-133">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b4923-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




