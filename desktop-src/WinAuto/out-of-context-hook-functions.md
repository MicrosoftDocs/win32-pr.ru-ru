---
title: Функции-обработчики вне контекста
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Дополнительные сведения: функции-обработчики вне контекста'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911772"
---
# <a name="out-of-context-hook-functions"></a><span data-ttu-id="d9a9b-103">Функции-обработчики вне контекста</span><span class="sxs-lookup"><span data-stu-id="d9a9b-103">Out-of-Context Hook Functions</span></span>

<span data-ttu-id="d9a9b-104">В следующем списке описываются ключевые аспекты функций-обработчиков, которые выходят за пределы контекста.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-104">The following list outlines the key aspects of out-of-context hook functions:</span></span>

-   <span data-ttu-id="d9a9b-105">Функции-обработчики вне контекста находятся в адресном пространстве клиента, независимо от того, находится ли оно в теле кода или в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-105">Out-of-context hook functions are located in the client's address space, whether it is in the code body or in a DLL.</span></span>
-   <span data-ttu-id="d9a9b-106">Неконтекстные функции-обработчики не сопоставлены с адресным пространством сервера.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-106">Out-of-context hook functions are not mapped into the server's address space.</span></span>
-   <span data-ttu-id="d9a9b-107">При активации события параметры функции-обработчика маршалируются в пределах границ процесса.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-107">When an event is triggered, the parameters for the hook function are marshaled across process boundaries.</span></span>
-   <span data-ttu-id="d9a9b-108">Функции-обработчики вне контекста заметно медленнее, чем функции обработчика в контексте, вызванные упаковкой.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-108">Out-of-context hook functions are noticeably slower than in-context hook functions due to marshaling.</span></span>
-   <span data-ttu-id="d9a9b-109">Система помещает в очередь уведомления о событиях, чтобы они приступили асинхронно (из-за времени, необходимого для выполнения упаковки).</span><span class="sxs-lookup"><span data-stu-id="d9a9b-109">The system queues the event notifications so that they arrive asynchronously (because of the time required to perform marshaling).</span></span>

<span data-ttu-id="d9a9b-110">Хотя уведомления о событиях являются асинхронными, Microsoft Active Accessibility гарантирует, что функция обратного вызова получает все события в том порядке, в котором они создаются.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-110">Although the event notifications are asynchronous, Microsoft Active Accessibility assures that the callback function receives all events in the order in which they are generated.</span></span>

<span data-ttu-id="d9a9b-111">ПОЛЬЗОВАТЕЛЬСКИЙ компонент операционной системы выделяет память для событий, обрабатываемых функциями-обработчиками вне контекста.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-111">The USER component of the operating system allocates memory for events that are handled by out-of-context hook functions.</span></span> <span data-ttu-id="d9a9b-112">Память освобождается при возврате функций-обработчиков.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-112">The memory is freed when the hook functions return.</span></span> <span data-ttu-id="d9a9b-113">Если функция-обработчик не обрабатывает события достаточно быстро, пользовательские ресурсы снижаются, в результате чего происходит сбой или очень большое время отклика.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-113">If a hook function does not process events quickly enough, USER resources are lowered, eventually resulting in a fault or extremely slow response times.</span></span> <span data-ttu-id="d9a9b-114">Эти проблемы могут возникнуть в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-114">These problems may occur if:</span></span>

-   <span data-ttu-id="d9a9b-115">События запускаются очень быстро.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-115">Events are fired very rapidly.</span></span>
-   <span data-ttu-id="d9a9b-116">Система работает слишком долго.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-116">The system is slow.</span></span>
-   <span data-ttu-id="d9a9b-117">Функция-ловушка обрабатывает события медленно.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-117">The hook function processes events slowly.</span></span>
-   <span data-ttu-id="d9a9b-118">Клиент работает под управлением Windows 9x.</span><span class="sxs-lookup"><span data-stu-id="d9a9b-118">The client is running on Windows 9x.</span></span>

 

 




