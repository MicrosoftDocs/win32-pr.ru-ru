---
title: Перечисление устройств (пакет SDK для WMP)
description: Перечисление устройств
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
ms.openlocfilehash: d5025d0e0a7e99028b22cc24ebc56337ea84d2fb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987197"
---
# <a name="enumerating-devices"></a>Перечисление устройств

Проигрыватель Windows Media представляет переносные устройства с помощью интерфейса **ивмпсинкдевице** . В следующем примере кода показана функция, которая создает массив указателей на **ивмпсинкдевице**. Каждый указатель в массиве представляет устройство, для которого проигрыватель Windows Media хранит информацию. Устройство не обязательно должно быть подключено к компьютеру и не должно иметь связи с текущим экземпляром проигрывателя Windows Media.

При получении события **DeviceConnect** или **девицедисконнект** необходимо перечислить устройства.

Следующая функция перечисляет устройства. Параметр *бконнектедонли* указывает, следует ли перечислять только те устройства, которые в настоящее время подключены к компьютеру пользователя.


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



Аналогичный код можно использовать для получения других списков устройств. Например, можно использовать [ивмпсинкдевице:: Get \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) , чтобы создать массив устройств, для которых существует партнерство.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IWMPEvents2::D Евицеконнект**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2::D Евицедисконнект**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**Интерфейс Ивмпсинкдевице**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Ивмпсинкдевице:: получить \_ подключение**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**Интерфейс Ивмпсинксервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Работа с портативными устройствами**](working-with-portable-devices.md)
</dt> </dl>

 

 




