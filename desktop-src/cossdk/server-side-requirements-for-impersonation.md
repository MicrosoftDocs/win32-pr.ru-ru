---
description: Server-Side требования для олицетворения
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side требования для олицетворения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710735"
---
# <a name="server-side-requirements-for-impersonation"></a><span data-ttu-id="16066-103">Server-Side требования для олицетворения</span><span class="sxs-lookup"><span data-stu-id="16066-103">Server-Side Requirements for Impersonation</span></span>

<span data-ttu-id="16066-104">Сервер выполняет олицетворение программным способом.</span><span class="sxs-lookup"><span data-stu-id="16066-104">The server performs impersonation programmatically.</span></span> <span data-ttu-id="16066-105">Он явно предполагает учетные данные безопасности клиента с помощью [**коимперсонатеклиент**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span><span class="sxs-lookup"><span data-stu-id="16066-105">It explicitly assumes the client's security credentials by using [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="16066-106">Когда клиент предоставил серверу достаточно полномочий, это приводит к замене учетных данных безопасности клиента токеном потока сервера вместо токена процесса.</span><span class="sxs-lookup"><span data-stu-id="16066-106">When the client has granted the server sufficient authority, this has the effect of substituting the client's security credentials with the server thread token, in place of the process token.</span></span>

<span data-ttu-id="16066-107">Когда это будет сделано, сервер может, например, использовать маркер клиента для доступа к ресурсам, защищенным с помощью дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="16066-107">When this has been done, the server can, for example, use the client token to access resources guarded with a security descriptor.</span></span> <span data-ttu-id="16066-108">Кроме того, если включена маскировка, она может выполнять вызовы под удостоверением клиента.</span><span class="sxs-lookup"><span data-stu-id="16066-108">Or it can make calls under the client identity, if cloaking is enabled.</span></span>

<span data-ttu-id="16066-109">Сервер может явно задать маскировку программно или может полагаться на административный параметр.</span><span class="sxs-lookup"><span data-stu-id="16066-109">The server can explicitly set cloaking programmatically, or it can rely on an administrative setting.</span></span> <span data-ttu-id="16066-110">По умолчанию приложения COM+ настроены для использования динамической маскировки.</span><span class="sxs-lookup"><span data-stu-id="16066-110">By default, COM+ applications are configured to use dynamic cloaking.</span></span> <span data-ttu-id="16066-111">Дополнительные сведения см. в разделе [маскировка](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="16066-111">For more detail, see [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="16066-112">Если сервер реализует делегирование от имени клиента, используя удостоверение клиента по сети, удостоверение процесса сервера должно быть помечено как "доверенное для делегирования" в службе Active Directory; в противном случае произойдет сбой делегирования.</span><span class="sxs-lookup"><span data-stu-id="16066-112">If the server is implementing delegation on behalf of the client—using the client identity over network—the server process identity must be marked as "Trusted for delegation" in the Active Directory Service; otherwise, delegation will fail.</span></span>

<span data-ttu-id="16066-113">После завершения использования удостоверения клиента сервер может вернуться к собственному маркеру процесса с помощью [**кореверттоселф**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="16066-113">When it has finished using the client's identity, the server can revert to its own process token using [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="16066-114">Дополнительные сведения о реализации олицетворения и делегирования см. в разделе [Делегирование и олицетворение](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="16066-114">For details on implementing impersonation and delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="16066-115">См. также</span><span class="sxs-lookup"><span data-stu-id="16066-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16066-116">Олицетворение и делегирование клиента</span><span class="sxs-lookup"><span data-stu-id="16066-116">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="16066-117">Требования к олицетворению на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="16066-117">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="16066-118">Маскировка</span><span class="sxs-lookup"><span data-stu-id="16066-118">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

 
