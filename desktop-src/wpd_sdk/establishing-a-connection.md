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
# <a name="establishing-a-connection"></a>Установление подключения

Когда пользователь выбирает устройство, функция Чуседевице, в свою очередь, вызывает метод [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) , чтобы установить соединение между приложением и устройством. Метод Ипортабледевице:: Open принимает два аргумента:

-   Указатель на строку, завершающуюся нулем, которая указывает самонастраивающийся имя устройства. (Эта строка извлекается путем вызова метода [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) GetString.)
-   Указатель на [**интерфейс ипортабледевицевалуес**](iportabledevicevalues.md) , указывающий сведения о клиенте для приложения.


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



В Windows 7 [**ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) поддерживает два идентификатора CLSID для **CoCreateInstance**. **Идентификатор CLSID \_ Портабледевице** возвращает указатель **ипортабледевице** , который не выполняет статистическую обработку для модуля упаковки с произвольным потоком; **Идентификатор CLSID \_ Портабледевицефтм** — это новый идентификатор CLSID, возвращающий указатель **ипортабледевице** , который выполняет статистическую обработку маршалером свободных потоков. В противном случае оба указателя поддерживают одну и ту же функциональность.

Приложения, которые находятся в однопотоковых апартаментах, должны использовать **CLSID \_ портабледевицефтм** , так как это устраняет издержки, связанные с упаковкой указателя на интерфейс. **Идентификатор CLSID \_ Портабледевице** по-прежнему поддерживается для устаревших приложений.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Выбор устройства**](selecting-a-device.md)
</dt> </dl>

 

 



