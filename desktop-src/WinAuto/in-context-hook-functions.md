---
title: Функции-обработчики In-Context
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Дополнительные сведения: функции-обработчики In-Context'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272757"
---
# <a name="in-context-hook-functions"></a><span data-ttu-id="c5c51-103">Функции-обработчики In-Context</span><span class="sxs-lookup"><span data-stu-id="c5c51-103">In-Context Hook Functions</span></span>

<span data-ttu-id="c5c51-104">В следующем списке описываются ключевые аспекты функций-обработчиков в контексте.</span><span class="sxs-lookup"><span data-stu-id="c5c51-104">The following list outlines the key aspects of in-context hook functions:</span></span>

-   <span data-ttu-id="c5c51-105">Функции обработчиков в контексте должны находиться в библиотеке динамической компоновки (DLL), сопоставленной системой с адресным пространством сервера.</span><span class="sxs-lookup"><span data-stu-id="c5c51-105">In-context hooks functions must be located in a dynamic-link library (DLL) that the system maps into the server's address space.</span></span>
-   <span data-ttu-id="c5c51-106">Функции-обработчики в контексте совместно используют адресное пространство с сервером.</span><span class="sxs-lookup"><span data-stu-id="c5c51-106">In-context hook functions share the address space with the server.</span></span>
-   <span data-ttu-id="c5c51-107">Когда сервер запускает событие, система вызывает функцию-обработчик без маршалирования (упаковка и отправка параметров интерфейса через границы процесса).</span><span class="sxs-lookup"><span data-stu-id="c5c51-107">When the server triggers an event, the system calls a hook function without marshaling (packaging and sending interface parameters across process boundaries).</span></span>
-   <span data-ttu-id="c5c51-108">Функции-обработчики в контексте обычно направляются очень быстро и получают уведомления о событиях синхронно, так как отсутствует упаковка.</span><span class="sxs-lookup"><span data-stu-id="c5c51-108">In-context hook functions tend to be very fast and receive event notifications synchronously because there is no marshaling.</span></span>
-   <span data-ttu-id="c5c51-109">Некоторые события могут доставляться вне процесса, даже если вы запрашиваете их доставку в процессе (с помощью флага WINEVENT в \_ контексте).</span><span class="sxs-lookup"><span data-stu-id="c5c51-109">Some events may be delivered out-of-process, even though you request that they be delivered in-process (using the WINEVENT\_INCONTEXT flag).</span></span> <span data-ttu-id="c5c51-110">Такая ситуация может возникнуть с 64-разрядными и 32-разрядными проблемами взаимодействия приложений и с событиями консоли Windows.</span><span class="sxs-lookup"><span data-stu-id="c5c51-110">You might see this situation with 64-bit and 32-bit application interoperability issues and with Windows console events.</span></span>

 

 




