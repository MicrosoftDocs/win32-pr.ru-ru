---
description: После получения обработчика файла с помощью вызова функции Сетупопенфилекуеуе можно добавить файловые операции в очередь, файлы по файлу или постановку в очередь всех файлов в разделе INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Файлы очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910039"
---
# <a name="queuing-files"></a><span data-ttu-id="cfe5d-103">Файлы очереди</span><span class="sxs-lookup"><span data-stu-id="cfe5d-103">Queuing Files</span></span>

<span data-ttu-id="cfe5d-104">После получения обработчика файла с помощью вызова функции [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) можно добавить файловые операции в очередь, файлы по файлу или постановку в очередь всех файлов в разделе INF.</span><span class="sxs-lookup"><span data-stu-id="cfe5d-104">After you have obtained a handle to a file queue by calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function, you can add file operations to the queue, either file-by-file, or by queuing all the files in an INF section.</span></span>

<span data-ttu-id="cfe5d-105">Чтобы добавить операцию копирования для отдельного файла в очередь файлов, вызовите функцию [**сетупкуеуекопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) .</span><span class="sxs-lookup"><span data-stu-id="cfe5d-105">To add a copy operation for an individual file to the file queue, call the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) function.</span></span> <span data-ttu-id="cfe5d-106">Если требуется поставить в очередь операцию копирования файлов с использованием исходного носителя по умолчанию и целевых объектов, указанных в INF-файле, можно вызвать функцию [**сетупкуеуедефаулткопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .</span><span class="sxs-lookup"><span data-stu-id="cfe5d-106">If you want to queue a file copy operation using the default source media and target destinations specified in an INF file, you can call the [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) function.</span></span>

<span data-ttu-id="cfe5d-107">Можно добавить отдельный файл операция удаления или переименования в очередь открытия файлов, вызвав функцию [**сетупкуеуеделете**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) или [**сетупкуеуеренаме**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .</span><span class="sxs-lookup"><span data-stu-id="cfe5d-107">You can add an individual file delete or rename operation to the open file queue, by calling the [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) or [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) function.</span></span>

 

 



