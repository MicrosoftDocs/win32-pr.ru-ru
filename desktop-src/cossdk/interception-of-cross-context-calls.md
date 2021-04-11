---
description: Когда объект активируется в заданном контексте, последующие вызовы или из него в контексте обрабатываются иначе, чем вызовы через границу контекста.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Перехват вызовов между контекстами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342262"
---
# <a name="interception-of-cross-context-calls"></a><span data-ttu-id="a1576-103">Перехват вызовов между контекстами</span><span class="sxs-lookup"><span data-stu-id="a1576-103">Interception of Cross-Context Calls</span></span>

<span data-ttu-id="a1576-104">Когда объект активируется в заданном контексте, последующие вызовы или из него в контексте обрабатываются иначе, чем вызовы через границу контекста.</span><span class="sxs-lookup"><span data-stu-id="a1576-104">When an object is activated in a given context, subsequent calls to or from it, within the context, are handled differently than calls across the context boundary.</span></span> <span data-ttu-id="a1576-105">Вызовы через границы контекста обрабатываются с помощью упрощенных прокси-серверов.</span><span class="sxs-lookup"><span data-stu-id="a1576-105">Calls across the context boundary are handled with lightweight proxies.</span></span> <span data-ttu-id="a1576-106">Эти прокси-серверы обрабатывали любое решение, необходимое для корректировки среды выполнения из одной, которая допускает вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="a1576-106">These proxies handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span> <span data-ttu-id="a1576-107">Этот процесс называется *перехватом*.</span><span class="sxs-lookup"><span data-stu-id="a1576-107">This process is known as *interception*.</span></span>

<span data-ttu-id="a1576-108">Перехват вызовов между контекстами необходим, поскольку объекты в разных контекстах имеют различные требования к времени выполнения — это именно причина для контекстов.</span><span class="sxs-lookup"><span data-stu-id="a1576-108">Cross-context call interception is necessary because objects in different contexts have different run-time requirements—this is precisely the reason for contexts.</span></span> <span data-ttu-id="a1576-109">COM+ перехватывает все ссылки на объекты, передаваемые в качестве параметров метода, и автоматически преобразует их в прокси-серверы, чтобы их можно было использовать в новом контексте.</span><span class="sxs-lookup"><span data-stu-id="a1576-109">COM+ intercepts any object references that you pass as method parameters and automatically converts them to proxies so that they are usable in the new context.</span></span>

<span data-ttu-id="a1576-110">Если ссылки на объекты совместно используются через границы контекста другими средствами, например в глобальных переменных, следует всегда использовать [**комаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) и [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="a1576-110">If you share object references across context boundaries by other means—for example, in global variables—you should always use [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> <span data-ttu-id="a1576-111">Эти функции могут преобразовать ссылку на объект в прокси-сервер, доступный в другом контексте.</span><span class="sxs-lookup"><span data-stu-id="a1576-111">These functions can translate an object reference into a proxy usable in a different context.</span></span> <span data-ttu-id="a1576-112">Никогда не предоставляйте ссылку на необработанный объект через границы контекста.</span><span class="sxs-lookup"><span data-stu-id="a1576-112">Never share a raw object reference across context boundaries.</span></span>

<span data-ttu-id="a1576-113">Поведение вызовов в контексте может иметь нежелательные последствия в случае, когда объекты предоставляют интерфейсы, которые не могут быть упакованы.</span><span class="sxs-lookup"><span data-stu-id="a1576-113">The behavior of calls across context can have unwanted consequences in the case of objects exposing interfaces that cannot be marshaled.</span></span> <span data-ttu-id="a1576-114">В этом случае вам, вероятно, придется налагать, что объект, который не может быть маршалирован, активируется только в контексте его вызывающего объекта и никогда не в своем собственном контексте.</span><span class="sxs-lookup"><span data-stu-id="a1576-114">In this circumstance, you are likely to want to insist that the object that cannot be marshaled be activated only in the context of its caller and never in its own context.</span></span> <span data-ttu-id="a1576-115">Это можно сделать, выбрав параметр **должен быть активирован в контексте вызывающего** объекта на вкладке **Активация** страницы **Свойства** компонента.</span><span class="sxs-lookup"><span data-stu-id="a1576-115">You can do this by selecting the **Must be activated in caller's context** option on the **Activation** tab of the component **Properties** page.</span></span> <span data-ttu-id="a1576-116">(Пошаговые инструкции см. [в разделе принудительная активация в контексте вызывающего объекта](enforcing-activation-in-the-caller-s-context.md) .)</span><span class="sxs-lookup"><span data-stu-id="a1576-116">(See [Enforcing Activation in the Caller's Context](enforcing-activation-in-the-caller-s-context.md) for step-by-step instructions.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1576-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a1576-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1576-118">Активация контекста</span><span class="sxs-lookup"><span data-stu-id="a1576-118">Context activation</span></span>](context-activation.md)
</dt> </dl>

 

 
