---
description: Вызов методов службы
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Вызов методов службы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0553e1490a6f8d0903756767397c30c2e1137a16a80609ed3a22da69188f799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843111"
---
# <a name="invoking-service-methods"></a>Вызов методов службы

Приложение Впдсервицесаписампле содержит код, демонстрирующий синхронное выполнение приложением методов, поддерживаемых данной службой контактов. В этом образце используются следующие интерфейсы



| Интерфейс    | Описание    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Используется для получения интерфейса **ипортабледевицесервицемесодс** для вызова методов в заданной службе.                                                                  |
| [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Используется для вызова метода службы.                                                                                                                                        |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)                 | Используется для хранения параметров исходящего метода и результатов входящего метода. Может иметь **значение NULL** , если метод не требует никаких параметров или не возвращает никаких результатов. |



 

Когда пользователь выбирает параметр "9" в командной строке, приложение вызывает метод **инвокемесодс** , который находится в модуле сервицемесодс. cpp. Обратите внимание, что до вызова методов пример приложения открывает службу контактов на подключенном устройстве.

Методы службы инкапсулируют функциональные возможности, определяемые и реализуемые каждой службой. Они уникальны для каждого типа службы и представлены идентификатором GUID. Например, служба Contacts определяет метод **бегинсинк** , который вызывается приложениями для подготовки устройства к синхронизации объектов Contact, и метод **ендсинк** для уведомления устройства о завершении синхронизации. Приложения выполняют метод путем вызова [**ипортабледевицесервицемесодс:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Методы службы не следует путать с командами WPD. Команды WPD являются частью стандартного интерфейса драйвера устройства WPD (DDI) и являются механизмом обмена данными между приложением WPD и драйвером. Команды являются предопределенными, сгруппированные по категориям, **например \_ категории WPD \_ Common**, и представляются структурой **PROPERTYKEY** . Приложение отправляет команды драйверу устройства, вызывая [**ипортабледевицесервице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Дополнительные сведения см. в разделе команды.

Метод **инвокемесодс** вызывает метод [**Ипортабледевицесервице:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . С помощью этого интерфейса он вызывает методы **бегинсинк** и **ендсинк** , вызывая метод [**ипортабледевицесервицемесодс:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . При каждом вызове **Invoke** приложение предоставляет рефгуид для вызываемого метода.

В следующем коде используется метод **инвокемесодс** .


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



