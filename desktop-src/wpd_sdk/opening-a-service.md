---
description: Открытие службы
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Открытие службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423924"
---
# <a name="opening-a-service"></a><span data-ttu-id="630c2-103">Открытие службы</span><span class="sxs-lookup"><span data-stu-id="630c2-103">Opening a Service</span></span>

<span data-ttu-id="630c2-104">Прежде чем приложение сможет выполнять операции со службой, например перечислить содержимое или описания поддерживаемых событий или методов, оно должно открыть службу.</span><span class="sxs-lookup"><span data-stu-id="630c2-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="630c2-105">В приложении Впдсервицесаписампле эта задача показана в модуле Сервицеенумератион. cpp с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="630c2-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



| <span data-ttu-id="630c2-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="630c2-106">Interface</span></span>                                                              | <span data-ttu-id="630c2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="630c2-107">Description</span></span>                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="630c2-108">**ипортабледевицесервицеманажер**</span><span class="sxs-lookup"><span data-stu-id="630c2-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="630c2-109">Используется для перечисления служб на устройстве.</span><span class="sxs-lookup"><span data-stu-id="630c2-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="630c2-110">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="630c2-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="630c2-111">Используется для открытия подключения к службе устройства.</span><span class="sxs-lookup"><span data-stu-id="630c2-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="630c2-112">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="630c2-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="630c2-113">Используется для хранения сведений о клиенте приложения.</span><span class="sxs-lookup"><span data-stu-id="630c2-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="630c2-114">Метод, который открывает службу, — [**ипортабледевицесервице:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="630c2-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="630c2-115">Этот метод принимает два аргумента: идентификатор Plug-and-Play (PnP) для службы и объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , содержащий сведения о клиенте приложения.</span><span class="sxs-lookup"><span data-stu-id="630c2-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="630c2-116">Чтобы получить идентификатор PnP для данной службы, приложение вызывает метод [**ипортабледевицесервицеманажер:: жетдевицесервицес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="630c2-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="630c2-117">Этот метод извлекает массив идентификаторов PnP для служб с идентификатором GUID категории службы (например, контакты службы).</span><span class="sxs-lookup"><span data-stu-id="630c2-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="630c2-118">Пример приложения службы получает идентификатор PnP для служб Contacts в методе **енумератеконтактссервицес** в модуле сервицеенумератион. cpp.</span><span class="sxs-lookup"><span data-stu-id="630c2-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="630c2-119">Следующий пример кода взят из этого метода.</span><span class="sxs-lookup"><span data-stu-id="630c2-119">The following code sample is taken from this method.</span></span>


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



<span data-ttu-id="630c2-120">После того как приложение получит идентификатор PnP для службы, оно может настроить сведения о клиенте и вызвать [**ипортабледевицесервице:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="630c2-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="630c2-121">В примере приложения этот метод вызывается в **чуседевицесервице** в модуле сервицеенумератион. cpp.</span><span class="sxs-lookup"><span data-stu-id="630c2-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="630c2-122">[**Ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) поддерживает два идентификатора CLSID для **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="630c2-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="630c2-123">**Идентификатор CLSID \_ Портабледевицесервице** возвращает указатель **ипортабледевицесервице** , который не выполняет статистическую обработку для модуля упаковки с произвольным потоком; **Идентификатор CLSID \_ Портабледевицесервицефтм** — это новый идентификатор CLSID, возвращающий указатель **ипортабледевицесервице** , который выполняет статистическую обработку маршалером свободных потоков.</span><span class="sxs-lookup"><span data-stu-id="630c2-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="630c2-124">В противном случае оба указателя поддерживают одну и ту же функциональность.</span><span class="sxs-lookup"><span data-stu-id="630c2-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="630c2-125">Приложения, которые находятся в однопотоковых апартаментах, должны использовать **CLSID \_ портабледевицесервицефтм** , так как это устраняет издержки, связанные с упаковкой указателя на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="630c2-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="630c2-126">**Идентификатор CLSID \_ Портабледевицесервице** по-прежнему поддерживается для устаревших приложений.</span><span class="sxs-lookup"><span data-stu-id="630c2-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="630c2-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="630c2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="630c2-128">**Интерфейс Ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="630c2-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="630c2-129">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="630c2-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="630c2-130">**Интерфейс Ипортабледевицесервицеманажер**</span><span class="sxs-lookup"><span data-stu-id="630c2-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="630c2-131">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="630c2-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



