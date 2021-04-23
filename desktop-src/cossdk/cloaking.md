---
description: При определении поведения олицетворения клиент явным образом предоставляет сервер через уровень олицетворения, а серверы могут маскировать свои удостоверения при вызове от имени клиентов.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Маскировка (службы компонентов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807211"
---
# <a name="cloaking-component-services"></a><span data-ttu-id="c6f93-103">Маскировка (службы компонентов)</span><span class="sxs-lookup"><span data-stu-id="c6f93-103">Cloaking (Component Services)</span></span>

<span data-ttu-id="c6f93-104">Определение поведения олицетворения состоит из двух ингредиентов: центр, на котором клиент явным образом предоставляет сервер через уровень олицетворения, и возможность сервера маскировать свое удостоверение при вызове от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="c6f93-104">There are two ingredients in determining the behavior of impersonation: the authority the client explicitly grants the server through an impersonation level and the server's ability to mask its own identity when making calls on the client's behalf.</span></span> <span data-ttu-id="c6f93-105">Эта последняя возможность называется *маскировкой*.</span><span class="sxs-lookup"><span data-stu-id="c6f93-105">This latter capability is known as *cloaking*.</span></span> <span data-ttu-id="c6f93-106">Маскировка должна делать с удостоверением безопасности, под которым сервер выполняет вызовы.</span><span class="sxs-lookup"><span data-stu-id="c6f93-106">Cloaking has to do with the security identity under which the server makes calls.</span></span>

<span data-ttu-id="c6f93-107">Когда сервер олицетворяет клиента, он имеет прямой доступ к учетным данным безопасности клиента.</span><span class="sxs-lookup"><span data-stu-id="c6f93-107">When the server impersonates the client, it has direct access to the client's security credentials.</span></span> <span data-ttu-id="c6f93-108">В очень локальном смысле серверный поток принимает на себя удостоверение клиента.</span><span class="sxs-lookup"><span data-stu-id="c6f93-108">In a very local sense, the server thread takes on the identity of the client.</span></span> <span data-ttu-id="c6f93-109">Но если сервер выполняет вызовы за пределами своего процесса, удостоверение клиента не обязательно будет рассматриваться как удостоверение, под которым выполняется вызов.</span><span class="sxs-lookup"><span data-stu-id="c6f93-109">But when the server makes calls outside of its process, the client identity will not necessarily be projected as the identity under which the call is made.</span></span>

<span data-ttu-id="c6f93-110">Если включена маскировка, вызовы, выполняемые сервером, который олицетворяет клиент, могут быть выполнены под удостоверением клиента.</span><span class="sxs-lookup"><span data-stu-id="c6f93-110">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="c6f93-111">Если маскировка отключена, вызовы сервера будут выполняться по идентификатору сервера.</span><span class="sxs-lookup"><span data-stu-id="c6f93-111">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

<span data-ttu-id="c6f93-112">Более того, существует две формы маскировки, *статическое скрытие* и *Динамическое скрытие*, которые можно описать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c6f93-112">Moreover, there are two forms of cloaking, *static cloaking* and *dynamic cloaking*, which can be described as follows:</span></span>

-   <span data-ttu-id="c6f93-113">Олицетворение со статической маскировкой.</span><span class="sxs-lookup"><span data-stu-id="c6f93-113">Impersonation with static cloaking.</span></span> <span data-ttu-id="c6f93-114">Исходное удостоверение клиента (реализованное как маркер серверного потока) может быть представлено один раз на подчиненный сервер при вызове с помощью [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), Установка исходного удостоверения клиента один раз на прокси-сервере, и этот маркер потока будет использоваться при последующих вызовах метода.</span><span class="sxs-lookup"><span data-stu-id="c6f93-114">The original client identity (realized as the server thread token) can be presented once to a downstream server on a call using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), setting the original client identity once on the proxy, and that thread token will be used on subsequent method calls.</span></span>
-   <span data-ttu-id="c6f93-115">Олицетворение с динамической маскировкой.</span><span class="sxs-lookup"><span data-stu-id="c6f93-115">Impersonation with dynamic cloaking.</span></span> <span data-ttu-id="c6f93-116">Исходное удостоверение клиента обнаруживается как токен потока сервера для каждого вызова метода на подчиненном сервере.</span><span class="sxs-lookup"><span data-stu-id="c6f93-116">The original client identity is discovered as the server thread token on each method call to the downstream server.</span></span> <span data-ttu-id="c6f93-117">Фактически представленное удостоверение можно определить динамически.</span><span class="sxs-lookup"><span data-stu-id="c6f93-117">In effect, the identity that is presented can be determined dynamically.</span></span> <span data-ttu-id="c6f93-118">Накладные расходы, необходимые для этого, могут быть значительно дороже.</span><span class="sxs-lookup"><span data-stu-id="c6f93-118">The overhead required to do this can be considerably more expensive.</span></span>

<span data-ttu-id="c6f93-119">Для приложений COM+ конфигурация по умолчанию предназначена для динамической маскировки.</span><span class="sxs-lookup"><span data-stu-id="c6f93-119">For COM+ applications, the default configuration is for dynamic cloaking capability.</span></span> <span data-ttu-id="c6f93-120">Это можно изменить программно и в административном виде.</span><span class="sxs-lookup"><span data-stu-id="c6f93-120">This can be changed programmatically and administratively.</span></span> <span data-ttu-id="c6f93-121">Хотя динамическая маскировка может снизить производительность, она обеспечивает гибкость, которая обычно требуется в обстоятельствах, требующих использования олицетворения в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="c6f93-121">While dynamic cloaking can have performance overhead, it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

<span data-ttu-id="c6f93-122">Дополнительные сведения о маскировке и точных описания возможных поведений см. в разделе [маскировка](/windows/desktop/com/cloaking) в документации по com.</span><span class="sxs-lookup"><span data-stu-id="c6f93-122">For more detail regarding cloaking and precise descriptions of possible behaviors, see [Cloaking](/windows/desktop/com/cloaking) in the COM documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6f93-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c6f93-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6f93-124">Олицетворение и делегирование клиента</span><span class="sxs-lookup"><span data-stu-id="c6f93-124">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="c6f93-125">Требования к олицетворению на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="c6f93-125">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="c6f93-126">Требования для олицетворения на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="c6f93-126">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
