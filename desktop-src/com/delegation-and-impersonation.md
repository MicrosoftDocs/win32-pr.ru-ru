---
title: Делегирование и олицетворение
description: В сценариях клиент/сервер часто один сервер вызывает другой сервер для выполнения некоторой задачи от имени клиента. Ситуация, когда серверу предоставляется право на действия от имени клиента, называется делегированием.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550646"
---
# <a name="delegation-and-impersonation"></a><span data-ttu-id="d581c-104">Делегирование и олицетворение</span><span class="sxs-lookup"><span data-stu-id="d581c-104">Delegation and Impersonation</span></span>

<span data-ttu-id="d581c-105">В сценариях клиент/сервер часто один сервер вызывает другой сервер для выполнения некоторой задачи от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="d581c-105">In client/server scenarios, it is common for one server to call another server to accomplish some task on a client's behalf.</span></span> <span data-ttu-id="d581c-106">Ситуация, когда серверу предоставляется право на действия от имени клиента, называется *делегированием*.</span><span class="sxs-lookup"><span data-stu-id="d581c-106">The situation where a server is given the authority to act on a client's behalf is called *delegation*.</span></span>

<span data-ttu-id="d581c-107">С точки зрения безопасности возникает две проблемы, связанные с делегированием:</span><span class="sxs-lookup"><span data-stu-id="d581c-107">From a security standpoint, two issues arise regarding delegation:</span></span>

-   <span data-ttu-id="d581c-108">Что должно быть разрешено серверу при работе от имени клиента?</span><span class="sxs-lookup"><span data-stu-id="d581c-108">What should the server be allowed to do when acting on the client's behalf?</span></span>
-   <span data-ttu-id="d581c-109">Какое удостоверение представлено сервером при вызове других серверов от имени клиента?</span><span class="sxs-lookup"><span data-stu-id="d581c-109">What identity is presented by the server when it calls other servers on behalf of a client?</span></span>

<span data-ttu-id="d581c-110">Для решения этих проблем COM предоставляет следующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="d581c-110">To deal with these issues, COM provides the following functionality.</span></span> <span data-ttu-id="d581c-111">Клиент может задать *уровень олицетворения* , определяющий, какой экстент будет использоваться сервером в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="d581c-111">The client can set an *impersonation level* that determines to what extent the server will be able to act as the client.</span></span> <span data-ttu-id="d581c-112">Если клиент предоставляет достаточно полномочий для сервера, сервер может *олицетворять* (выдавать) клиент.</span><span class="sxs-lookup"><span data-stu-id="d581c-112">If the client grants enough authority to the server, the server can *impersonate* (pretend to be) the client.</span></span> <span data-ttu-id="d581c-113">При олицетворении клиента серверу предоставляется доступ только к тем объектам или ресурсам, которые у клиента есть разрешение на использование.</span><span class="sxs-lookup"><span data-stu-id="d581c-113">When impersonating the client, the server is given access to only those objects or resources that the client has permission to use.</span></span> <span data-ttu-id="d581c-114">Сервер, выступающий в качестве клиента, может также включать *маскировку* для маскирования собственного удостоверения и проецирование удостоверения клиента в вызовах других COM-компонентов.</span><span class="sxs-lookup"><span data-stu-id="d581c-114">The server, acting as a client, can also enable *cloaking* to mask its own identity and project the client's identity in calls to other COM components.</span></span>

![Схема, показывающая, как сервер, действующий в качестве клиента, может включить маскировку.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

<span data-ttu-id="d581c-116">Рассмотрим сценарий, показанный на предыдущем рисунке, где A и B — это процессы на разных компьютерах с C. процесс A вызывает B, а B вызывает C. Client A устанавливает уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="d581c-116">Consider the scenario illustrated by the preceding figure, where A and B are processes on a different machine from C. Process A calls B, and B calls C. Client A sets the impersonation level.</span></span> <span data-ttu-id="d581c-117">B задает возможность маскировки.</span><span class="sxs-lookup"><span data-stu-id="d581c-117">B sets the cloaking capability.</span></span> <span data-ttu-id="d581c-118">Если A устанавливает уровень олицетворения, допускающий олицетворение, B может олицетворять ответ при вызове C от имени.</span><span class="sxs-lookup"><span data-stu-id="d581c-118">If A sets an impersonation level that permits impersonation, B can impersonate A when calling C on A's behalf.</span></span> <span data-ttu-id="d581c-119">Удостоверение, представленное для обработки C, будет представлять собой удостоверение или удостоверение B в зависимости от того, включено ли маскировка в B. Если Маскировка включена, удостоверение, представленное для обработки C, будет иметь значение. Если маскировка не включена, удостоверение B будет представлено на языке C.</span><span class="sxs-lookup"><span data-stu-id="d581c-119">The identity that is presented to process C will be either A's identity or B's identity, depending on whether cloaking was enabled by B. If cloaking is enabled, the identity presented to process C will be that of A. If cloaking is not enabled, B's identity will be presented to C.</span></span>

<span data-ttu-id="d581c-120">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="d581c-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d581c-121">Олицетворение</span><span class="sxs-lookup"><span data-stu-id="d581c-121">Impersonation</span></span>](impersonation.md)
-   [<span data-ttu-id="d581c-122">Уровни олицетворения</span><span class="sxs-lookup"><span data-stu-id="d581c-122">Impersonation Levels</span></span>](impersonation-levels.md)
-   [<span data-ttu-id="d581c-123">Маскировка</span><span class="sxs-lookup"><span data-stu-id="d581c-123">Cloaking</span></span>](cloaking.md)

 

 




