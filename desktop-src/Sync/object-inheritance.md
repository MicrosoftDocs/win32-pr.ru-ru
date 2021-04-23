---
description: При создании процесса с помощью функции CreateProcess можно указать, что процесс наследует обработчики для мьютексов, событий, семафоров или объектов таймера с помощью \_ структуры АТРИБУТОВ безопасности.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Наследование объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663777"
---
# <a name="object-inheritance"></a><span data-ttu-id="aae3e-103">Наследование объектов</span><span class="sxs-lookup"><span data-stu-id="aae3e-103">Object Inheritance</span></span>

<span data-ttu-id="aae3e-104">При создании процесса с помощью функции [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) можно указать, что процесс наследует обработчики для мьютексов, событий, семафоров или объектов таймера с помощью [**структуры \_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aae3e-104">When you create a process with the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, you can specify that the process inherit handles to mutex, event, semaphore, or timer objects using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="aae3e-105">Маркер, наследуемый процессом, имеет тот же доступ к объекту, что и исходный маркер.</span><span class="sxs-lookup"><span data-stu-id="aae3e-105">The handle inherited by the process has the same access to the object as the original handle.</span></span> <span data-ttu-id="aae3e-106">Унаследованный обработчик отображается в таблице Handle созданного процесса, но необходимо передать значение этого обработчика в созданный процесс.</span><span class="sxs-lookup"><span data-stu-id="aae3e-106">The inherited handle appears in the handle table of the created process, but you must communicate the handle value to the created process.</span></span> <span data-ttu-id="aae3e-107">Это можно сделать, указав значение в качестве аргумента командной строки при вызове **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="aae3e-107">You can do this by specifying the value as a command-line argument when you call **CreateProcess**.</span></span> <span data-ttu-id="aae3e-108">Затем созданный процесс использует функцию [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) для получения строки командной строки и преобразует аргумент Handle в пригодный для использования описатель.</span><span class="sxs-lookup"><span data-stu-id="aae3e-108">The created process then uses the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function to retrieve the command-line string and convert the handle argument into a usable handle.</span></span> <span data-ttu-id="aae3e-109">Дополнительные сведения см. в разделе [Наследование](../procthread/inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="aae3e-109">For more information, see [Inheritance](../procthread/inheritance.md).</span></span>

 

 
