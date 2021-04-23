---
description: При использовании нескольких мониторов в качестве независимых дисплеев Рабочий стол содержит один экран или набор дисплеев.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Использование нескольких мониторов в качестве независимых дисплеев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985913"
---
# <a name="using-multiple-monitors-as-independent-displays"></a><span data-ttu-id="90a42-103">Использование нескольких мониторов в качестве независимых дисплеев</span><span class="sxs-lookup"><span data-stu-id="90a42-103">Using Multiple Monitors as Independent Displays</span></span>

<span data-ttu-id="90a42-104">При использовании нескольких мониторов в качестве независимых дисплеев Рабочий стол содержит один экран или набор дисплеев.</span><span class="sxs-lookup"><span data-stu-id="90a42-104">When using multiple monitors as independent displays, the desktop contains one display or set of displays.</span></span> <span data-ttu-id="90a42-105">Этот набор отображения всегда включает основной монитор и ведет себя, как упоминалось в других разделах этого раздела.</span><span class="sxs-lookup"><span data-stu-id="90a42-105">This set of displays always includes the primary monitor and behaves as mentioned in the other sections of this topic.</span></span> <span data-ttu-id="90a42-106">Приложение может использовать любой другой монитор в качестве независимого экрана.</span><span class="sxs-lookup"><span data-stu-id="90a42-106">An application can use any other monitor as an independent display.</span></span>

> [!Note]  
> <span data-ttu-id="90a42-107">Использование других мониторов в качестве независимых дисплеев не поддерживается в драйверах, реализованных в модели WDDM.</span><span class="sxs-lookup"><span data-stu-id="90a42-107">Using other monitors as independent displays isn't supported on drivers that are implemented to the Windows Display Driver Model (WDDM).</span></span>

 

<span data-ttu-id="90a42-108">Диспетчер окон ничего не знает о независимых экранах.</span><span class="sxs-lookup"><span data-stu-id="90a42-108">The window manager knows nothing about the independent displays.</span></span> <span data-ttu-id="90a42-109">Они полностью контролируются приложением, и для приложения не доступны функции диспетчера окон (все вызовы диспетчера окон автоматически переходят на основной дисплей).</span><span class="sxs-lookup"><span data-stu-id="90a42-109">They are completely controlled by the application, and no window manager functions are available to the application (all window manager calls automatically go to the primary display).</span></span> <span data-ttu-id="90a42-110">Каждый независимый дисплей имеет собственный исходный и горизонтальный и вертикальный координаты, доступ к которому осуществляется через функции GDI, такие как [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) , или функции DirectX, такие как **директдравкреате**.</span><span class="sxs-lookup"><span data-stu-id="90a42-110">Each independent display has its own origin and horizontal and vertical coordinates, and is accessed through the GDI functions such as [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) or the DirectX functions such as **DirectDrawCreate**.</span></span>

<span data-ttu-id="90a42-111">Чтобы найти независимые экраны, вызовите [**енумдисплайдевицес**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) и найдите дисплеи, для которых в \_ \_ \_ \_ структуре [**\_ устройства отображения**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) не подключено устройство отображения.</span><span class="sxs-lookup"><span data-stu-id="90a42-111">To locate the independent displays, call [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and look for the displays that do not have DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span>

<span data-ttu-id="90a42-112">Приложение может открыть отображение, вызвав</span><span class="sxs-lookup"><span data-stu-id="90a42-112">An application can open a display by calling</span></span>


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



<span data-ttu-id="90a42-113">В этом вызове параметр *лпсздисплайнаме* является одним из имен устройств, возвращенных [**Енумдисплайдевицес**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) , а *лпдевмоде* — описание графического режима для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="90a42-113">In this call, the *lpszDisplayName* parameter is one of the device names returned by [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and *lpDevMode* is a description of the graphics mode for this device.</span></span> <span data-ttu-id="90a42-114">Результирующий параметр hdc можно использовать для выполнения любых графических операций на устройстве.</span><span class="sxs-lookup"><span data-stu-id="90a42-114">The resulting hdc can be used to perform any graphics operation to the device.</span></span>

 

 



