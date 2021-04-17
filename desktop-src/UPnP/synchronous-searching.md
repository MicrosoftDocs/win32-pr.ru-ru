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
# <a name="synchronous-searching"></a>Синхронный поиск

Объект Finder устройства обеспечивает как синхронный, так и асинхронный поиск. Синхронный поиск завершается и возвращает управление вызывающему приложению только после обнаружения всех доступных устройств. Для выполнения синхронного поиска используйте один из методов синхронного поиска интерфейса [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .

> [!Note]  
> Для возврата синхронный поиск должен быть не менее девяти секунд. Задержка вызвана тем, что исходное сообщение поиска UDP должно отправляться несколько раз. Это дублирование учетных записей для унрелиабилити базового сетевого протокола. Для интерфейсов командной строки лучше использовать синхронный поиск. Они не рекомендуются для графических пользовательских интерфейсов.

 

Метод [**иупнпдевицефиндер:: финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) выполняет поиск по типу устройства или службы. Этот метод принимает универсальный код ресурса (URI) типа в качестве входного параметра и возвращает коллекцию объектов устройства. Объект устройства представляет отдельное устройство.

В следующих примерах показано, как выполнить синхронный поиск устройств в VBScript. Каждый скрипт использует [**иупнпдевицефиндер:: финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), который вызывается с URI типа (идентификатор службы) для устройства проигрывателя мультимедиа типа, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*. Метод возвращает коллекцию объектов устройств, соответствующих обнаруженным устройствам проигрывателя мультимедиа. Сведения о извлечении отдельных объектов устройств из коллекции см. в разделе [коллекции устройств, возвращаемые при синхронном поиске](device-collections-returned-by-synchronous-searches.md).

## <a name="search-for-devices-by-type-in-vbscript"></a>Поиск устройств по типу в VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Поиск устройства по типу в C++

В следующем примере демонстрируется синхронный поиск устройств проигрывателя мультимедиа с помощью C++. Функция принимает указатель на интерфейс [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) в качестве входных данных и возвращает указатель интерфейса [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

В примере сначала выделяется тип **BSTR** для представления универсального кода ресурса (URI) типа устройства, а затем он передается методу [**Иупнпдевицефиндер:: финдбитипе**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) . Он также передает адрес локального указателя [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) в буфере, в котором метод сохраняет коллекцию найденных устройств. Если вызов функции выполнен успешно, он возвращает указатель на эту коллекцию.


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



 

 




