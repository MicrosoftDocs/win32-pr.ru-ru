---
description: При работе с API мобильной широкополосной связи следует использовать следующий набор рекомендаций для достижения наилучшей производительности.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Рекомендации по API мобильного широкополосного подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263180"
---
# <a name="mobile-broadband-api-best-practices"></a><span data-ttu-id="93b39-103">Рекомендации по API мобильного широкополосного подключения</span><span class="sxs-lookup"><span data-stu-id="93b39-103">Mobile Broadband API Best Practices</span></span>

<span data-ttu-id="93b39-104">При работе с API мобильной широкополосной связи следует использовать следующий набор рекомендаций для достижения наилучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="93b39-104">When working with the Mobile Broadband API the following set of best practices should be used in order to achieve the best possible performance.</span></span>

## <a name="do-not-cache-functional-objects"></a><span data-ttu-id="93b39-105">Не кэшировать функциональные объекты</span><span class="sxs-lookup"><span data-stu-id="93b39-105">Do Not Cache Functional Objects</span></span>

<span data-ttu-id="93b39-106">Функциональные объекты, такие как [**имбнинтерфаце**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) и другие, получаются из объектов Manager, таких как [**имбнинтерфацеманажер**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), с помощью метода перечисления для соответствующего объекта Manager.</span><span class="sxs-lookup"><span data-stu-id="93b39-106">Functional objects, such as [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) and others, are obtained from manager objects, like [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), using the enumeration method on the corresponding manager object.</span></span> <span data-ttu-id="93b39-107">Не кэшировать эти функциональные объекты, так как кэшированные функциональные объекты содержат устаревшие данные.</span><span class="sxs-lookup"><span data-stu-id="93b39-107">Do not cache these functional objects, since cached functional objects contain stale data.</span></span> <span data-ttu-id="93b39-108">Синхронные операции, выполняемые с этими функциональными объектами, будут возвращать те же данные, пока не будут снова получены функциональные объекты.</span><span class="sxs-lookup"><span data-stu-id="93b39-108">The synchronous operations performed on these functional objects will return the same data until the functional objects are obtained again.</span></span>

<span data-ttu-id="93b39-109">Вместо этого закэширование объектов диспетчера и получение функциональных объектов из объекта Manager с помощью метода перечисления для соответствующего объекта Manager снова, чтобы получить актуальные данные.</span><span class="sxs-lookup"><span data-stu-id="93b39-109">Instead, cache the manager objects and obtain the functional objects from manager object using the enumeration method on the corresponding manager object again to get the latest data.</span></span>

<span data-ttu-id="93b39-110">В следующем примере кода демонстрируется правильный способ кэширования объектов диспетчера.</span><span class="sxs-lookup"><span data-stu-id="93b39-110">The following code example demonstrates the proper way to cache manager objects.</span></span>


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a><span data-ttu-id="93b39-111">Обработайте все уведомления</span><span class="sxs-lookup"><span data-stu-id="93b39-111">Handle All Notifications</span></span>

<span data-ttu-id="93b39-112">Следуйте указаниям и обрабатывайте все уведомления, даже если они не запускаются приложением.</span><span class="sxs-lookup"><span data-stu-id="93b39-112">Follow and handle all notifications, even if they are not triggered by your application.</span></span> <span data-ttu-id="93b39-113">Это необходимо для синхронизации пользовательского интерфейса с фактическим состоянием устройства.</span><span class="sxs-lookup"><span data-stu-id="93b39-113">This is required to keep the UI in sync with the actual state of the device.</span></span>

<span data-ttu-id="93b39-114">На одном компьютере может быть установлено несколько диспетчеров соединений.</span><span class="sxs-lookup"><span data-stu-id="93b39-114">There can be more than one connection manager running on a computer.</span></span> <span data-ttu-id="93b39-115">Пользовательский интерфейс доступного для просмотра сетевого интерфейса, предоставляемый Windows 7, является диспетчером соединений.</span><span class="sxs-lookup"><span data-stu-id="93b39-115">The native View Available Network Interface UI provided by Windows 7 is a connection manager.</span></span> <span data-ttu-id="93b39-116">Любые другие диспетчеры соединений должны отвечать на все уведомления, чтобы оставаться синхронизированными с собственным ИНТЕРФЕЙСом Windows.</span><span class="sxs-lookup"><span data-stu-id="93b39-116">Any other connection managers need to respond to all notifications to remain in sync the Windows native UI.</span></span> <span data-ttu-id="93b39-117">Пользователь может выбрать выполнение некоторой операции с одним из диспетчеров соединений, что может привести к изменению состояния устройства мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="93b39-117">A user may opt to perform some operation on one of the connection managers which may result in a state change of the Mobile Broadband device.</span></span> <span data-ttu-id="93b39-118">Однако для правильного указания измененного состояния устройства другие диспетчеры соединений должны оставаться обновленными.</span><span class="sxs-lookup"><span data-stu-id="93b39-118">However, other connection managers need to remain updated in order to properly indicate the modified state of the device.</span></span>

<span data-ttu-id="93b39-119">Например, при выполнении подключения с помощью одного из диспетчеров соединений состояние устройства будет изменено с "доступно для подключения".</span><span class="sxs-lookup"><span data-stu-id="93b39-119">For example, performing a connect using one of the connection managers will change the state of the device from available to connected.</span></span> <span data-ttu-id="93b39-120">Это изменение должно быть видимым для диспетчеров соединений, которые не инициировали это действие.</span><span class="sxs-lookup"><span data-stu-id="93b39-120">This change should be visible to the connection managers that didn’t initiate this action.</span></span> <span data-ttu-id="93b39-121">Все диспетчеры соединений, имеющие пользовательский интерфейс, указывающий состояние подключения устройства, должны прослушивать и обменять уведомления о состоянии соединения, чтобы правильно обновить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="93b39-121">All connection managers that have UI that indicates the connection state of the device, need to listen to and handle the connection state notifications in order to properly update their user interface.</span></span>

## <a name="sending-and-receiving-bytes"></a><span data-ttu-id="93b39-122">Отправка и получение байтов</span><span class="sxs-lookup"><span data-stu-id="93b39-122">Sending And Receiving Bytes</span></span>

<span data-ttu-id="93b39-123">Используйте вспомогательные функции IP [жетлфентри](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) и [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) для отправки и получения байтов.</span><span class="sxs-lookup"><span data-stu-id="93b39-123">Use the IP Helper functions [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) and [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) to send and receive bytes.</span></span>

## <a name="using-the-pin-unblock-api"></a><span data-ttu-id="93b39-124">Использование API разблокировки ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="93b39-124">Using The Pin Unblock API</span></span>

<span data-ttu-id="93b39-125">Чтобы успешно вызвать [**имбнпин:: Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock), необходимо повысить уровень вызывающего клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="93b39-125">A calling client application must be elevated in order to successfully to invoke [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span></span> <span data-ttu-id="93b39-126">Этот метод является единственной частью API мобильной широкополосной связи, для которой требуются права администратора или NCO.</span><span class="sxs-lookup"><span data-stu-id="93b39-126">This method is the only portion of the Mobile Broadband API that requires administrator or NCO privileges.</span></span> <span data-ttu-id="93b39-127">Дополнительные сведения см. [в описании группы операторов конфигурации сети]( https://support.microsoft.com/kb/297938/en-us) .</span><span class="sxs-lookup"><span data-stu-id="93b39-127">See [A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) for more information.</span></span>

## <a name="working-with-safearrays"></a><span data-ttu-id="93b39-128">Работа с SafeArray</span><span class="sxs-lookup"><span data-stu-id="93b39-128">Working With SafeArrays</span></span>

-   <span data-ttu-id="93b39-129">Используйте Зеромемори () перед доступом к любым элементам массива SafeArray.</span><span class="sxs-lookup"><span data-stu-id="93b39-129">Use ZeroMemory() before accessing any elements in a SafeArray.</span></span>

-   <span data-ttu-id="93b39-130">Не следует проверять индексы SafeArray.</span><span class="sxs-lookup"><span data-stu-id="93b39-130">Don’t check on the indexes of a SafeArray.</span></span> <span data-ttu-id="93b39-131">Они могут быть отрицательными.</span><span class="sxs-lookup"><span data-stu-id="93b39-131">They may be negative.</span></span>

<span data-ttu-id="93b39-132">В следующем примере кода показано, как правильно обработайте SafeArray.</span><span class="sxs-lookup"><span data-stu-id="93b39-132">The following code example shows how to properly handle a SafeArray.</span></span>


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
