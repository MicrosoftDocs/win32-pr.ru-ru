---
title: Создание устройства поиска устройств
description: в следующих примерах показано, как создать экземпляр объекта finder устройства на C++, Visual Basic и VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6af75ea5c267e156f89f1ae1e27a08928c097bbfea731f59add575397fbc00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137362"
---
# <a name="creating-the-device-finder"></a>Создание устройства поиска устройств

в следующих примерах показано, как создать экземпляр объекта finder устройства на C++, Visual Basic и VBScript. В языках сценариев используется программный идентификатор (ProgID) [**UPnP. упнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) для идентификации класса Finder устройства. Код C++ использует идентификатор класса.

## <a name="c-example"></a>Пример C++


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



Как показано в этом примере C++, объект Finder устройства предоставляет интерфейс по умолчанию [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder). Методы этого интерфейса выполняют поиск в соответствии с допустимыми критериями поиска для устройства на основе UPnP. Этот интерфейс поддерживает автоматизацию, поэтому его методы можно вызывать с помощью кода скрипта.

## <a name="vbscript-example"></a>Пример VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




