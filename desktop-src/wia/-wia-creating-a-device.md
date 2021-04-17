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
# <a name="creating-a-device"></a><span data-ttu-id="7a1f4-103">Создание устройства</span><span class="sxs-lookup"><span data-stu-id="7a1f4-103">Creating a Device</span></span>

<span data-ttu-id="7a1f4-104">После того как приложение будет иметь идентификатор устройства, оно может вызвать метод [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) или [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md), который создает иерархическое дерево объектов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) , представляющих устройство обработки изображений, а также сканирование изображений кроватях и папки, содержащиеся на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="7a1f4-104">Once an application has the device ID of a given device, it can call the [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)method, which creates a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects that represent an imaging device and the image scanning beds, and folders contained on that device.</span></span>

<span data-ttu-id="7a1f4-105">В следующем примере из примера приложения Виассамп реализуется функция, которая принимает идентификатор устройства в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="7a1f4-105">The following example from the sample application WiaSSamp implements a function that takes a device ID as a parameter.</span></span> <span data-ttu-id="7a1f4-106">Сведения о том, как получить идентификатор устройства для конкретного устройства, см. в разделе [чтение свойств устройства](-wia-reading-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f4-106">For information about how to obtain a device ID for a particular device, see [Reading Device Properties](-wia-reading-device-properties.md).</span></span>


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



<span data-ttu-id="7a1f4-107">В этом примере **пвиадевмгр** является указателем на интерфейс [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , а **ппвиадевице** — это переменная, которая после вызова [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (или to [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md)) содержит адрес указателя на корневой элемент дерева, представляющего только что созданное устройство.</span><span class="sxs-lookup"><span data-stu-id="7a1f4-107">In this example, **pWiaDevMgr** is a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface, and **ppWiaDevice** is a variable that, after the call to [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or to [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contains the address of a pointer to the root item of the tree that represents the newly created device.</span></span>

 

 



