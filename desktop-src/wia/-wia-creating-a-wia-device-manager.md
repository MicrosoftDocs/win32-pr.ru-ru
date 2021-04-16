---
description: Первым шагом при использовании служб получения изображений Windows (WIA) является получение указателя на интерфейс Ивиадевмгр (при программировании для Windows XP или более ранней версии) или указателя на интерфейс IWiaDevMgr2 (при программировании для Windows Vista или более поздней версии).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Создание диспетчер устройств WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693083"
---
# <a name="creating-a-wia-device-manager"></a>Создание диспетчер устройств WIA

Первым шагом при использовании служб получения изображений Windows (WIA) является получение указателя на интерфейс [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (при программировании для Windows XP или более ранней версии) или указателя на интерфейс [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (при программировании для Windows Vista или более поздней версии). Для этого вызовите [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с соответствующими параметрами. Пример приложения Виассамп создает диспетчер устройств в глобальной функции, реализованной с помощью следующего кода:


```
    HRESULT CreateWiaDeviceManager( IWiaDevMgr **ppWiaDevMgr ) //XP or earlier
    HRESULT CreateWiaDeviceManager( IWiaDevMgr2 **ppWiaDevMgr ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == ppWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevMgr = NULL;

        //
        // Create an instance of the device manager
        //
        
        //XP or earlier:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr, (void**)ppWiaDevMgr );

        //Vista or later:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr2, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr2, (void**)ppWiaDevMgr ); 

        //
        // Return the result of creating the device manager
        //
        return hr;
    }
```



В этом примере CLSID \_ виадевмгр и IID \_ ивиадевмгр являются константами WIA, которые представляют идентификатор класса и идентификатор интерфейса [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)соответственно. CLSID \_ WiaDevMgr2 и IID \_ IWiaDevMgr2 являются константами WIA, которые представляют идентификатор класса и идентификатор интерфейса [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)соответственно.

Значением аргумента *двклсконтекст* вызова [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) должен быть клскткс \_ Local \_ Server. Другие типы серверов не поддерживаются, и модель COM отклоняет любое другое значение для этого параметра.

 

 
