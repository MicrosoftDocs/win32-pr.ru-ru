---
description: После того как очередь завершит фиксацию своих операций, ее следует закрыть с помощью функции Сетупклосефилекуеуе с маркером, созданным Сетупопенфилекуеуе.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Закрытие файловой очереди и INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664620"
---
# <a name="closing-the-file-queue-and-inf-file"></a><span data-ttu-id="53931-103">Закрытие файловой очереди и INF-файла</span><span class="sxs-lookup"><span data-stu-id="53931-103">Closing the File Queue and INF File</span></span>

<span data-ttu-id="53931-104">После того как очередь завершит фиксацию своих операций, ее следует закрыть с помощью функции [**сетупклосефилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) с маркером, созданным [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="53931-104">After the queue has finished committing its operations, it should be closed using the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span> <span data-ttu-id="53931-105">Обратный вызов очереди по умолчанию должен быть уничтожен и создан повторно, прежде чем можно будет зафиксировать другую очередь.</span><span class="sxs-lookup"><span data-stu-id="53931-105">The default queue callback must be destroyed and recreated before another queue can be committed.</span></span>

<span data-ttu-id="53931-106">Если контекст по умолчанию был инициирован для использования подпрограммы обратного вызова по умолчанию, он также должен быть завершен путем вызова функции [**сетуптермдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="53931-106">If a default context was initiated for use by the default callback routine, it should also be terminated by calling the [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) function.</span></span> <span data-ttu-id="53931-107">*Контекст* является указателем на структуру, возвращаемую функцией [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="53931-107">The *Context* is a pointer to the structure returned by the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) function.</span></span>

<span data-ttu-id="53931-108">Если доступ к данным INF больше не требуется, вызовите функцию [**сетупклосеинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) с маркером, созданным [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) для освобождения системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53931-108">When access to the INF information is no longer needed, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) to free system resources.</span></span>

 

 



