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
# <a name="enumerating-windows-media-device-manager-devices"></a>Перечисление устройств Windows Media диспетчер устройств

После проверки подлинности приложения можно приступить к перечислению устройств, обнаруженных диспетчер устройств Windows Media. Перечисление выполняется с помощью интерфейса перечисления [**ивмдменумдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), полученного с помощью [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) или [**ивмдевицеманажер:: енумдевицес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices). Если поддерживается, используйте метод **EnumDevices2** , поскольку более ранняя версия возвращала только устаревшие интерфейсы на устройствах, а новая версия возвращает как устаревшие, так и новые интерфейсы.

Перед получением перечислителя необходимо решить, какое представление перечисления следует использовать. Некоторые устройства предоставляют каждое хранилище как отдельное устройство. Например, два адаптера флэш-памяти на устройстве будут перечисляться так, как если бы они были отдельными устройствами. Можно указать, что все хранилища на устройстве перечисляются вместе как одно устройство. Этот параметр можно задать только один раз в приложении. Если вы хотите изменить его, необходимо завершить работу приложения и перезапустить его. Однако обратите внимание, что устаревшие устройства иногда игнорируют запрос на перечисление отдельных хранилищ устройств в качестве одного устройства и продолжают перечислять их по отдельности.

Ниже приведены инструкции по перечислению подключенных устройств.

1.  Задайте параметры перечисления устройств с помощью [**IWMDeviceManager3:: сетдевицеенумпреференце**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference). Если этот метод не вызывается, метод по умолчанию отображает хранилища как отдельные устройства. Чтобы определить, являются ли отдельные "устройства" на самом деле хранилищами на одном устройстве, вызовите [**IWMDMDevice2:: жетканоникалнаме**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); хранилища из одного устройства будут возвращать идентичные значения, за исключением последней цифры после последнего знака $.
2.  Выполните запрос для [**ивмдевицеманажер**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) или [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), а затем вызовите [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) , чтобы получить интерфейс перечислителя устройства, [**ивмдменумдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). (Если поддерживается, используйте **EnumDevices2**, что более эффективно, так как предыдущая версия не может возвращать устройства MTP).
3.  Вызовите метод [**ивмдменумдевицес:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) , чтобы получить одно или несколько устройств за раз. Продолжайте вызывать этот метод до тех пор, пока метод не возвратит \_ значение S false или сообщение об ошибке. При извлечении только одного устройства за раз вам не нужно распределять массив для хранения устройств.

Поскольку пользователи могут подключать или удалять устройства с компьютера во время работы приложения, рекомендуется реализовать уведомление о подключении или удалении устройства. Это делается путем реализации интерфейса [**ивмдмнотификатион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) и его регистрации. Дополнительные сведения об этом см. в разделе [Включение уведомлений](enabling-notifications.md).

Следующий код C++ перечисляет устройства и запрашивает сведения о каждом устройстве.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Создание приложения диспетчер устройств Windows Media**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




