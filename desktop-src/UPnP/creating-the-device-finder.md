---
title: Создание устройства поиска устройств
description: В следующих примерах показано, как создать экземпляр объекта Finder устройства на C++, Visual Basic и VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888883"
---
# <a name="creating-the-device-finder"></a><span data-ttu-id="7078c-103">Создание устройства поиска устройств</span><span class="sxs-lookup"><span data-stu-id="7078c-103">Creating the Device Finder</span></span>

<span data-ttu-id="7078c-104">В следующих примерах показано, как создать экземпляр объекта Finder устройства на C++, Visual Basic и VBScript.</span><span class="sxs-lookup"><span data-stu-id="7078c-104">The following examples demonstrate how to create an instance of the Device Finder object in C++, Visual Basic, and VBScript.</span></span> <span data-ttu-id="7078c-105">В языках сценариев используется программный идентификатор (ProgID) [**UPnP. упнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) для идентификации класса Finder устройства.</span><span class="sxs-lookup"><span data-stu-id="7078c-105">The script languages use the programmatic ID (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) to identify the Device Finder class.</span></span> <span data-ttu-id="7078c-106">Код C++ использует идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="7078c-106">The C++ code uses the class identifier.</span></span>

## <a name="c-example"></a><span data-ttu-id="7078c-107">Пример C++</span><span class="sxs-lookup"><span data-stu-id="7078c-107">C++ Example</span></span>


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



<span data-ttu-id="7078c-108">Как показано в этом примере C++, объект Finder устройства предоставляет интерфейс по умолчанию [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span><span class="sxs-lookup"><span data-stu-id="7078c-108">As this C++ example indicates, the Device Finder object exposes a default interface, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span></span> <span data-ttu-id="7078c-109">Методы этого интерфейса выполняют поиск в соответствии с допустимыми критериями поиска для устройства на основе UPnP.</span><span class="sxs-lookup"><span data-stu-id="7078c-109">The methods of this interface perform searches according to the valid search criteria for a UPnP-based device.</span></span> <span data-ttu-id="7078c-110">Этот интерфейс поддерживает автоматизацию, поэтому его методы можно вызывать с помощью кода скрипта.</span><span class="sxs-lookup"><span data-stu-id="7078c-110">This interface is Automation capable, so its methods can be called by scripting code.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="7078c-111">Пример VBScript</span><span class="sxs-lookup"><span data-stu-id="7078c-111">VBScript Example</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




