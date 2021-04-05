---
title: Прочие советы по повышению производительности RPC
description: В этом разделе обсуждаются различные советы по повышению производительности при разработке высокопроизводительных серверов RPC. В этом разделе содержится множество советов, которые относятся к клиенту RPC. Разработка клиента RPC правильно позволяет серверу RPC выполнять меньше работы.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067607"
---
# <a name="miscellaneous-rpc-performance-tips"></a><span data-ttu-id="c10c0-105">Прочие советы по повышению производительности RPC</span><span class="sxs-lookup"><span data-stu-id="c10c0-105">Miscellaneous RPC Performance Tips</span></span>

<span data-ttu-id="c10c0-106">В этом разделе обсуждаются различные советы по повышению производительности при разработке высокопроизводительных серверов RPC.</span><span class="sxs-lookup"><span data-stu-id="c10c0-106">This section discusses miscellaneous performance tips for developing high performance RPC servers.</span></span> <span data-ttu-id="c10c0-107">В этом разделе содержится множество советов, которые относятся к клиенту RPC.</span><span class="sxs-lookup"><span data-stu-id="c10c0-107">This section provides many tips that refer to the RPC client.</span></span> <span data-ttu-id="c10c0-108">Разработка клиента RPC правильно позволяет серверу RPC выполнять меньше работы.</span><span class="sxs-lookup"><span data-stu-id="c10c0-108">Developing an RPC client properly enables the RPC server to perform less work.</span></span>

## <a name="use-kerberos"></a><span data-ttu-id="c10c0-109">Использование Kerberos</span><span class="sxs-lookup"><span data-stu-id="c10c0-109">Use Kerberos</span></span>

<span data-ttu-id="c10c0-110">Если используется безопасность, используйте протокол Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c10c0-110">If security is used, use Kerberos.</span></span> <span data-ttu-id="c10c0-111">На стороне сервера Kerberos не требует доступа к KDC.</span><span class="sxs-lookup"><span data-stu-id="c10c0-111">On the server side, Kerberos does not require access to the KDC.</span></span> <span data-ttu-id="c10c0-112">При этом Рабочая нагрузка перемещается с сервера на клиент, что обеспечивает более эффективное выполнение серверов.</span><span class="sxs-lookup"><span data-stu-id="c10c0-112">This moves the workload from the server to the client, which provides better performing servers.</span></span>

## <a name="use-static-identity-tracking"></a><span data-ttu-id="c10c0-113">Использовать статическое отслеживание идентификаторов</span><span class="sxs-lookup"><span data-stu-id="c10c0-113">Use Static Identity Tracking</span></span>

<span data-ttu-id="c10c0-114">Если используется безопасность, попробуйте использовать статическое отслеживание идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="c10c0-114">If security is used, try to use static identity tracking.</span></span> <span data-ttu-id="c10c0-115">Отслеживание статических удостоверений является более дешевым в плане использования ресурсов, чем динамическое отслеживание идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="c10c0-115">Static identity tracking is cheaper in terms of resource usage than dynamic identity tracking.</span></span> <span data-ttu-id="c10c0-116">Если при изменении удостоверения клиента сервер не должен знать об изменении, используйте динамическое отслеживание вместо создания другого маркера привязки для каждого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="c10c0-116">If the client identity changes, and the server should not be aware of the change, use dynamic tracking instead of creating a different binding handle for each identity.</span></span> <span data-ttu-id="c10c0-117">Но если удостоверение одинаково, убедитесь в том, что RPC учитывает этот факт, чтобы избежать проверки подлинности при каждом изменении удостоверения RPC.</span><span class="sxs-lookup"><span data-stu-id="c10c0-117">But if the identity is the same, ensure RPC is aware of that fact to avoid having RPC make checks for changed identity every time.</span></span>

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a><span data-ttu-id="c10c0-118">Использование функции Рпкжетаусоризатионконтекстфорклиент</span><span class="sxs-lookup"><span data-stu-id="c10c0-118">Use the RpcGetAuthorizationContextForClient Function</span></span>

<span data-ttu-id="c10c0-119">Если необходимо проверить доступ в Windows XP, используйте функцию [**рпкжетаусоризатионконтекстфорклиент**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) .</span><span class="sxs-lookup"><span data-stu-id="c10c0-119">If you need to check access in Windows XP, use the [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) function.</span></span> <span data-ttu-id="c10c0-120">Результирующий контекст авторизации обеспечивает очень быстрые проверки доступа, которые эффективно кэшируются во время выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="c10c0-120">The resulting Authz contexts enables very fast access checks, which are efficiently cached by the RPC run time.</span></span>

## <a name="do-not-modify-the-token-unless-necessary"></a><span data-ttu-id="c10c0-121">Не изменяйте токен, если это не требуется</span><span class="sxs-lookup"><span data-stu-id="c10c0-121">Do Not Modify the Token Unless Necessary</span></span>

<span data-ttu-id="c10c0-122">Если используется динамическое отслеживание идентификаторов, не изменяйте маркер потока или процесса, если это не требуется.</span><span class="sxs-lookup"><span data-stu-id="c10c0-122">If dynamic identity tracking is used, do not modify the thread/process token unless absolutely necessary.</span></span> <span data-ttu-id="c10c0-123">Даже если он был изменен с учетом ранее настроенных параметров, маркер, как правило, достаточно отличается от системы безопасности для активации установки нового контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="c10c0-123">Even if it is modified to settings it previously had, the token often is sufficiently different to the security system to trigger the establishment of a new security context.</span></span>

## <a name="consider-mixed-mode-serialization-for-context-handles"></a><span data-ttu-id="c10c0-124">Рассмотрите возможность сериализации в смешанном режиме для дескрипторов контекста</span><span class="sxs-lookup"><span data-stu-id="c10c0-124">Consider Mixed Mode Serialization for Context Handles</span></span>

<span data-ttu-id="c10c0-125">Режим сериализации по умолчанию для маркера контекста сериализуется (исключается).</span><span class="sxs-lookup"><span data-stu-id="c10c0-125">The default serialization mode for context handle is serialized (exclusive).</span></span> <span data-ttu-id="c10c0-126">Рассмотрите возможность выполнения всех вызовов, которые не изменяют состояние обработчика контекста в режиме общей сериализации.</span><span class="sxs-lookup"><span data-stu-id="c10c0-126">Consider making all calls that do not modify the state of the context handle in shared serialization mode.</span></span> <span data-ttu-id="c10c0-127">Дополнительные сведения см. в разделе [**рпкссконтекстлоккексклусиве**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) .</span><span class="sxs-lookup"><span data-stu-id="c10c0-127">See [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) for more information.</span></span>

 

 




