---
title: Получение возможностей драйвера записи
description: Получение возможностей драйвера записи
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- Сообщение WM_CAP_DRIVER_GET_CAPS
- макрос Капдривержеткапс
- Структура КАПДРИВЕРКАПС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672185"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a><span data-ttu-id="2b9e5-106">Получение возможностей драйвера записи</span><span class="sxs-lookup"><span data-stu-id="2b9e5-106">Obtaining the Capabilities of a Capture Driver</span></span>

<span data-ttu-id="2b9e5-107">Сообщение [**о \_ \_ \_ \_ получении политики авторизации устройств WM Cap**](wm-cap-driver-get-caps.md) Возвращает возможности драйвера записи и базового оборудования в структуре [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="2b9e5-107">The [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span> <span data-ttu-id="2b9e5-108">Каждый раз, когда приложение подключается к новому драйверу записи в окне Capture, необходимо обновить структуру **капдриверкапс** .</span><span class="sxs-lookup"><span data-stu-id="2b9e5-108">Each time an application connects a new capture driver to the capture window, it should update the **CAPDRIVERCAPS** structure.</span></span> <span data-ttu-id="2b9e5-109">В следующем примере используется макрос [**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) для получения возможностей драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="2b9e5-109">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to obtain the capture driver capabilities.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a><span data-ttu-id="2b9e5-110">См. также</span><span class="sxs-lookup"><span data-stu-id="2b9e5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b9e5-111">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="2b9e5-111">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




