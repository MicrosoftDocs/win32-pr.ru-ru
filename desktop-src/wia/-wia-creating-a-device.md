---
description: 'После того как приложение будет иметь идентификатор устройства, оно может вызвать метод Ивиадевмгр:: Креатедевице или IWiaDevMgr2:: Креатедевицемесод, который создает иерархическое дерево объектов Ивиаитем или IWiaItem2, представляющих устройство для работы с образами, а также сканирования изображений кроватях и папок, содержащихся на этом устройстве.'
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Создание устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622d22a55c4273dcc13cc1421537b94037a3bb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693082"
---
# <a name="creating-a-device"></a>Создание устройства

После того как приложение будет иметь идентификатор устройства, оно может вызвать метод [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) или [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md), который создает иерархическое дерево объектов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) , представляющих устройство обработки изображений, а также сканирование изображений кроватях и папки, содержащиеся на этом устройстве.

В следующем примере из примера приложения Виассамп реализуется функция, которая принимает идентификатор устройства в качестве параметра. Сведения о том, как получить идентификатор устройства для конкретного устройства, см. в разделе [чтение свойств устройства](-wia-reading-device-properties.md).


```
    //XP or earlier:
    HRESULT CreateWiaDevice( IWiaDevMgr *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem **ppWiaDevice ) 
    //Vista or later:
    HRESULT CreateWiaDevice( IWiaDevMgr2 *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem2 **ppWiaDevice ) 
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr || NULL == bstrDeviceID || NULL == ppWiaDevice)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevice = NULL;

        //
        // Create the WIA Device
        //
        HRESULT hr = pWiaDevMgr->CreateDevice( bstrDeviceID, ppWiaDevice );

        //
        // Return the result of creating the device
        //
        return hr;
    }
```



В этом примере **пвиадевмгр** является указателем на интерфейс [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , а **ппвиадевице** — это переменная, которая после вызова [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (или to [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md)) содержит адрес указателя на корневой элемент дерева, представляющего только что созданное устройство.

 

 



