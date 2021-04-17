---
description: Прежде чем можно будет ставить в очередь файловые операции, необходимо открыть очередь файлов. Вызов функции Сетупопенфилекуеуе возвращает маркер в файл очереди. Этот маркер используется последующими функциями очередей для ссылки на открытую очередь и добавления в нее операций или ее сканирования.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Открытие и закрытие очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663895"
---
# <a name="opening-and-closing-a-queue"></a><span data-ttu-id="974ab-105">Открытие и закрытие очереди</span><span class="sxs-lookup"><span data-stu-id="974ab-105">Opening and Closing a Queue</span></span>

<span data-ttu-id="974ab-106">Прежде чем можно будет ставить в очередь файловые операции, необходимо открыть очередь файлов.</span><span class="sxs-lookup"><span data-stu-id="974ab-106">Before you can queue file operations, you must open a file queue.</span></span> <span data-ttu-id="974ab-107">Вызов функции [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) возвращает маркер в файл очереди.</span><span class="sxs-lookup"><span data-stu-id="974ab-107">Calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function returns a handle to a queue file.</span></span> <span data-ttu-id="974ab-108">Этот маркер используется последующими функциями очередей для ссылки на открытую очередь и добавления в нее операций или ее сканирования.</span><span class="sxs-lookup"><span data-stu-id="974ab-108">This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.</span></span>

<span data-ttu-id="974ab-109">После того как все указанные операции с файлами были поставлены в очередь и зафиксированы, необходимо вызвать функцию [**сетупклосефилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) , чтобы освободить ресурсы, выделенные во время вызова [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="974ab-109">After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span>

> [!Note]  
> <span data-ttu-id="974ab-110">Функция [**сетупклосефилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) не фиксирует очередь файлов.</span><span class="sxs-lookup"><span data-stu-id="974ab-110">The [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function does not commit the file queue.</span></span> <span data-ttu-id="974ab-111">Любые операции, которые не зафиксированы при вызове **сетупклосефилекуеуе** , выполняться не будут.</span><span class="sxs-lookup"><span data-stu-id="974ab-111">Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.</span></span>

 

 

 



