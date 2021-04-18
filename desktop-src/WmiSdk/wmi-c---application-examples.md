---
description: Примеры приложений WMI в этом разделе написаны на C++.
ms.assetid: 5c4c4c4c-adbc-4702-a6fe-5f98a6db3ba1
ms.tgt_platform: multiple
title: Примеры приложений WMI на C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883b51bd00de5e3938fef8467c68d299ac60683a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692690"
---
# <a name="wmi-c-application-examples"></a><span data-ttu-id="d5fd2-103">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="d5fd2-103">WMI C++ Application Examples</span></span>

<span data-ttu-id="d5fd2-104">Примеры приложений WMI в этом разделе написаны на C++.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-104">The WMI application examples in this section are written in C++.</span></span> <span data-ttu-id="d5fd2-105">Они демонстрируют ряд задач, которые можно выполнить с помощью компонентов WMI, и предложить альтернативный вариант использования сценариев Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-105">They demonstrate a range of tasks that can be completed using WMI components and offer an alternative over using Visual Basic scripts.</span></span> <span data-ttu-id="d5fd2-106">Каждое приложение разделяется на последовательность шагов таким же образом, чтобы разделы кода из разных примеров можно было легко комбинировать для формирования настраиваемых приложений.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-106">Each application is separated into a series of steps in a similar way so that code sections from different examples can easily be combined to form customized applications.</span></span>

<span data-ttu-id="d5fd2-107">В следующей таблице перечислены примеры C++ в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-107">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="d5fd2-108">Пример</span><span class="sxs-lookup"><span data-stu-id="d5fd2-108">Example</span></span>                                                                                                                                  | <span data-ttu-id="d5fd2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d5fd2-109">Description</span></span>                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5fd2-110">Пример. получение данных WMI с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="d5fd2-110">Example: Getting WMI Data from the Local Computer</span></span>](example--getting-wmi-data-from-the-local-computer.md)                               | <span data-ttu-id="d5fd2-111">Этот пример подключается к пространству имен WMI на локальном компьютере и получает данные из запроса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-111">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="d5fd2-112">Данные собираются полусинхронном.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-112">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="d5fd2-113">Пример. асинхронное получение данных WMI с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="d5fd2-113">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>](example--getting-wmi-data-from-the-local-computer-asynchronously.md) | <span data-ttu-id="d5fd2-114">Этот пример подключается к пространству имен WMI на локальном компьютере и получает данные из запроса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-114">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="d5fd2-115">Данные собираются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-115">The data is gathered asynchronously.</span></span>    |
| [<span data-ttu-id="d5fd2-116">Пример. получение данных WMI с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="d5fd2-116">Example: Getting WMI Data from a Remote Computer</span></span>](example--getting-wmi-data-from-a-remote-computer.md)                                 | <span data-ttu-id="d5fd2-117">Этот пример подключается к пространству имен WMI на удаленном компьютере и получает данные из запроса на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-117">This example connects to the WMI namespace on a remote computer and gets data from a query on the remote computer.</span></span> <span data-ttu-id="d5fd2-118">Данные собираются полусинхронном.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-118">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="d5fd2-119">Пример. вызов метода поставщика</span><span class="sxs-lookup"><span data-stu-id="d5fd2-119">Example: Calling a Provider Method</span></span>](example--calling-a-provider-method.md)                                                             | <span data-ttu-id="d5fd2-120">Этот пример подключается к пространству имен WMI на локальном компьютере и вызывает метод в WMI.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-120">This example connects to the WMI namespace on the local computer and calls a method in WMI.</span></span> <span data-ttu-id="d5fd2-121">Метод выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-121">The method is executed synchronously.</span></span>                          |
| [<span data-ttu-id="d5fd2-122">Пример. получение уведомлений о событиях через WMI</span><span class="sxs-lookup"><span data-stu-id="d5fd2-122">Example: Receiving Event Notifications Through WMI</span></span>](example--receiving-event-notifications-through-wmi-.md)                            | <span data-ttu-id="d5fd2-123">Этот пример подключается к пространству имен WMI на локальном компьютере и получает событие с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-123">This example connects to the WMI namespace on the local computer and receives an event from the local computer.</span></span> <span data-ttu-id="d5fd2-124">Событие получает полусинхронном.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-124">The event is received semisynchronously.</span></span>   |



 

 

 



