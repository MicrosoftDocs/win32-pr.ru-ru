---
description: Открытие службы
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Открытие службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578dfee696fd17b0e360d6e344844670ca92ac6b48152242492a458a9a279f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806724"
---
# <a name="opening-a-service"></a>Открытие службы

Прежде чем приложение сможет выполнять операции со службой, например перечислить содержимое или описания поддерживаемых событий или методов, оно должно открыть службу. В приложении Впдсервицесаписампле эта задача показана в модуле Сервицеенумератион. cpp с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                              | Описание                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [**ипортабледевицесервицеманажер**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | Используется для перечисления служб на устройстве.        |
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Используется для открытия подключения к службе устройства.     |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)                 | Используется для хранения сведений о клиенте приложения. |



 

Метод, который открывает службу, — [**ипортабледевицесервице:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open). Этот метод принимает два аргумента: идентификатор Plug-and-Play (PnP) для службы и объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , содержащий сведения о клиенте приложения.

Чтобы получить идентификатор PnP для данной службы, приложение вызывает метод [**ипортабледевицесервицеманажер:: жетдевицесервицес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) . Этот метод извлекает массив идентификаторов PnP для служб с идентификатором GUID категории службы (например, контакты службы).

Пример приложения службы получает идентификатор PnP для служб Contacts в методе **енумератеконтактссервицес** в модуле сервицеенумератион. cpp. Следующий пример кода взят из этого метода.


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



После того как приложение получит идентификатор PnP для службы, оно может настроить сведения о клиенте и вызвать [**ипортабледевицесервице:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).

В примере приложения этот метод вызывается в **чуседевицесервице** в модуле сервицеенумератион. cpp.

[**Ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) поддерживает два идентификатора CLSID для **CoCreateInstance**. **Идентификатор CLSID \_ Портабледевицесервице** возвращает указатель **ипортабледевицесервице** , который не выполняет статистическую обработку для модуля упаковки с произвольным потоком; **Идентификатор CLSID \_ Портабледевицесервицефтм** — это новый идентификатор CLSID, возвращающий указатель **ипортабледевицесервице** , который выполняет статистическую обработку маршалером свободных потоков. В противном случае оба указателя поддерживают одну и ту же функциональность.

Приложения, которые находятся в однопотоковых апартаментах, должны использовать **CLSID \_ портабледевицесервицефтм** , так как это устраняет издержки, связанные с упаковкой указателя на интерфейс. **Идентификатор CLSID \_ Портабледевицесервице** по-прежнему поддерживается для устаревших приложений.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Интерфейс Ипортабледевицесервицеманажер**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



