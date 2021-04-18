---
description: Наследование ручных транзакций
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Наследование ручных транзакций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701169"
---
# <a name="inheriting-manual-transactions"></a><span data-ttu-id="23435-103">Наследование ручных транзакций</span><span class="sxs-lookup"><span data-stu-id="23435-103">Inheriting Manual Transactions</span></span>

<span data-ttu-id="23435-104">Если объект с транзакцией BYOT в своем контексте создает второй объект, нисходящий объект может наследовать транзакцию BYOT (если она настроена для наследования транзакций).</span><span class="sxs-lookup"><span data-stu-id="23435-104">If an object with a BYOT transaction in its context creates a second object, the downstream object can inherit the BYOT transaction (if configured to inherit transactions).</span></span> <span data-ttu-id="23435-105">Первый объект, созданный с помощью шлюза BYOT, должен быть настроен на использование транзакций "требуется" или "поддержка".</span><span class="sxs-lookup"><span data-stu-id="23435-105">The first object created using the BYOT gateway needs to be configured to "require" or "support" transactions.</span></span> <span data-ttu-id="23435-106">Последующие объекты в действии можно настроить на основе требований приложения.</span><span class="sxs-lookup"><span data-stu-id="23435-106">Subsequent objects in the activity could be configured based on application requirements.</span></span>

<span data-ttu-id="23435-107">Для автоматических транзакций среда выполнения COM+ не пытается зафиксировать транзакцию до тех пор, пока корневой объект не покажет, что он готов (вызвав [**сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) перед возвратом из вызова).</span><span class="sxs-lookup"><span data-stu-id="23435-107">For automatic transactions, the COM+ runtime does not attempt to commit the transaction until the root object indicates that it is ready (by calling [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) before returning from a call).</span></span> <span data-ttu-id="23435-108">Пользователи должны иметь в виду, что транзакция BYOT может преждевременно зафиксироваться (в том, что работа дочерних объектов не была завершена), так как "root" не выполняется в среде выполнения COM+, а семантика фиксации не привязана к времени существования объекта.</span><span class="sxs-lookup"><span data-stu-id="23435-108">Users should be aware that a BYOT transaction could commit prematurely (in that the work of child objects has not been completed), because the "root" is not running under the COM+ runtime environment, and the commit semantics are not tied to the lifetime of the object.</span></span> <span data-ttu-id="23435-109">Как правило, пользователь должен не нарушать границы синхронизации транзакции.</span><span class="sxs-lookup"><span data-stu-id="23435-109">In general, the user should take care to not violate the synchronization boundary of the transaction.</span></span>

<span data-ttu-id="23435-110">В противном случае применяется семантика фиксации COM+.</span><span class="sxs-lookup"><span data-stu-id="23435-110">Otherwise, COM+ commit semantics apply.</span></span> <span data-ttu-id="23435-111">COM+ не будет пытаться зафиксировать транзакцию, пока объект в пределах границы синхронизации находится в вызове.</span><span class="sxs-lookup"><span data-stu-id="23435-111">COM+ will not attempt to commit a transaction while an object within a synchronization boundary is in call.</span></span> <span data-ttu-id="23435-112">Кроме того, объекты могут указывать на их согласованность с помощью [**дисаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span><span class="sxs-lookup"><span data-stu-id="23435-112">Also, objects can indicate their consistency using [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span></span> <span data-ttu-id="23435-113">Если предпринимается попытка фиксации транзакции, которая включает в себя работу объекта с именем **дисаблекоммит**, транзакция будет прервана.</span><span class="sxs-lookup"><span data-stu-id="23435-113">If an attempt is made to commit a transaction which includes the work of an object that has called **DisableCommit**, the transaction will abort.</span></span>

 

 



