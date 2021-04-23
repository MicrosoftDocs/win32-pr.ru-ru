---
title: Синхронный поиск
description: Объект Finder устройства обеспечивает как синхронный, так и асинхронный поиск. Синхронный поиск завершается и возвращает управление вызывающему приложению только после обнаружения всех доступных устройств.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691334"
---
# <a name="synchronous-searching"></a><span data-ttu-id="f1569-104">Синхронный поиск</span><span class="sxs-lookup"><span data-stu-id="f1569-104">Synchronous Searching</span></span>

<span data-ttu-id="f1569-105">Объект Finder устройства обеспечивает как синхронный, так и асинхронный поиск.</span><span class="sxs-lookup"><span data-stu-id="f1569-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="f1569-106">Синхронный поиск завершается и возвращает управление вызывающему приложению только после обнаружения всех доступных устройств.</span><span class="sxs-lookup"><span data-stu-id="f1569-106">Synchronous searches are completed and return control to the calling application only after all available devices are found.</span></span> <span data-ttu-id="f1569-107">Для выполнения синхронного поиска используйте один из методов синхронного поиска интерфейса [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .</span><span class="sxs-lookup"><span data-stu-id="f1569-107">To perform a synchronous search, use one of the synchronous search methods of the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface.</span></span>

> [!Note]  
> <span data-ttu-id="f1569-108">Для возврата синхронный поиск должен быть не менее девяти секунд.</span><span class="sxs-lookup"><span data-stu-id="f1569-108">Synchronous searches take at least nine seconds to return.</span></span> <span data-ttu-id="f1569-109">Задержка вызвана тем, что исходное сообщение поиска UDP должно отправляться несколько раз.</span><span class="sxs-lookup"><span data-stu-id="f1569-109">The delay is caused because the initial UDP search message must be sent multiple times.</span></span> <span data-ttu-id="f1569-110">Это дублирование учетных записей для унрелиабилити базового сетевого протокола.</span><span class="sxs-lookup"><span data-stu-id="f1569-110">This duplication accounts for the unreliability of the underlying network protocol.</span></span> <span data-ttu-id="f1569-111">Для интерфейсов командной строки лучше использовать синхронный поиск.</span><span class="sxs-lookup"><span data-stu-id="f1569-111">Synchronous searches are best for command-line interfaces.</span></span> <span data-ttu-id="f1569-112">Они не рекомендуются для графических пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f1569-112">They are not recommended for graphical user interfaces.</span></span>

 

<span data-ttu-id="f1569-113">Метод [**иупнпдевицефиндер:: финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) выполняет поиск по типу устройства или службы.</span><span class="sxs-lookup"><span data-stu-id="f1569-113">The [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method searches by device or service type.</span></span> <span data-ttu-id="f1569-114">Этот метод принимает универсальный код ресурса (URI) типа в качестве входного параметра и возвращает коллекцию объектов устройства.</span><span class="sxs-lookup"><span data-stu-id="f1569-114">This method takes a type URI as an input parameter and returns a collection of Device objects.</span></span> <span data-ttu-id="f1569-115">Объект устройства представляет отдельное устройство.</span><span class="sxs-lookup"><span data-stu-id="f1569-115">A Device object represents an individual device.</span></span>

<span data-ttu-id="f1569-116">В следующих примерах показано, как выполнить синхронный поиск устройств в VBScript.</span><span class="sxs-lookup"><span data-stu-id="f1569-116">The following examples demonstrate how to perform a synchronous search for devices in VBScript.</span></span> <span data-ttu-id="f1569-117">Каждый скрипт использует [**иупнпдевицефиндер:: финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), который вызывается с URI типа (идентификатор службы) для устройства проигрывателя мультимедиа типа, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*.</span><span class="sxs-lookup"><span data-stu-id="f1569-117">Each script uses [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), called with the type URI (service ID) for the media player device type, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*.</span></span> <span data-ttu-id="f1569-118">Метод возвращает коллекцию объектов устройств, соответствующих обнаруженным устройствам проигрывателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f1569-118">The method returns a collection of Device objects that corresponds to media player devices that were found.</span></span> <span data-ttu-id="f1569-119">Сведения о извлечении отдельных объектов устройств из коллекции см. в разделе [коллекции устройств, возвращаемые при синхронном поиске](device-collections-returned-by-synchronous-searches.md).</span><span class="sxs-lookup"><span data-stu-id="f1569-119">For information on extracting individual device objects from a collection, see [Device Collections Returned By Synchronous Searches](device-collections-returned-by-synchronous-searches.md).</span></span>

## <a name="search-for-devices-by-type-in-vbscript"></a><span data-ttu-id="f1569-120">Поиск устройств по типу в VBScript</span><span class="sxs-lookup"><span data-stu-id="f1569-120">Search for Devices by Type in VBScript</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a><span data-ttu-id="f1569-121">Поиск устройства по типу в C++</span><span class="sxs-lookup"><span data-stu-id="f1569-121">Search for Device by Type in C++</span></span>

<span data-ttu-id="f1569-122">В следующем примере демонстрируется синхронный поиск устройств проигрывателя мультимедиа с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="f1569-122">The following example demonstrates a synchronous search for media player devices using C++.</span></span> <span data-ttu-id="f1569-123">Функция принимает указатель на интерфейс [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) в качестве входных данных и возвращает указатель интерфейса [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="f1569-123">The function takes a pointer to the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface as input, and returns the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface pointer.</span></span>

<span data-ttu-id="f1569-124">В примере сначала выделяется тип **BSTR** для представления универсального кода ресурса (URI) типа устройства, а затем он передается методу [**Иупнпдевицефиндер:: финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) .</span><span class="sxs-lookup"><span data-stu-id="f1569-124">The example first allocates a **BSTR** to represent the device type URI and then passes this to the [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method.</span></span> <span data-ttu-id="f1569-125">Он также передает адрес локального указателя [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) в буфере, в котором метод сохраняет коллекцию найденных устройств.</span><span class="sxs-lookup"><span data-stu-id="f1569-125">It also passes the address of a local [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) pointer in the buffer in which the method then stores the collection of devices found.</span></span> <span data-ttu-id="f1569-126">Если вызов функции выполнен успешно, он возвращает указатель на эту коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f1569-126">If the function call is successful, it returns the pointer to this collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




