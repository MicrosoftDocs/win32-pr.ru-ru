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
# <a name="creating-the-device-finder"></a>Создание устройства поиска устройств

В следующих примерах показано, как создать экземпляр объекта Finder устройства на C++, Visual Basic и VBScript. В языках сценариев используется программный идентификатор (ProgID) [**UPnP. упнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) для идентификации класса Finder устройства. Код C++ использует идентификатор класса.

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



 

 




