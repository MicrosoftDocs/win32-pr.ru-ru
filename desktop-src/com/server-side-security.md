---
title: Безопасность Server-Side
description: Безопасность Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987920"
---
# <a name="server-side-security"></a><span data-ttu-id="18f5e-103">Безопасность Server-Side</span><span class="sxs-lookup"><span data-stu-id="18f5e-103">Server-Side Security</span></span>

<span data-ttu-id="18f5e-104">Сервер может получать сведения о безопасности вызывающего объекта или олицетворять вызывающий объект с помощью методов [**исерверсекурити**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span><span class="sxs-lookup"><span data-stu-id="18f5e-104">The server can retrieve security information about a caller or impersonate the caller by using the methods of [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span></span> <span data-ttu-id="18f5e-105">Реализация **исерверсекурити** предоставляется COM в объекте контекста для текущего вызова при использовании стандартного маршалирования.</span><span class="sxs-lookup"><span data-stu-id="18f5e-105">An implementation of **IServerSecurity** is supplied by COM on the context object for the current call when standard marshaling is used.</span></span> <span data-ttu-id="18f5e-106">Однако этот интерфейс может отсутствовать для некоторых пользовательских интерфейсов, которые маршалируются.</span><span class="sxs-lookup"><span data-stu-id="18f5e-106">However, this interface may be absent for some custom-marshaled interfaces.</span></span>

<span data-ttu-id="18f5e-107">При поступлении вызова на сервер сервер может вызвать [**кожеткаллконтекст**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) , чтобы получить указатель на интерфейс [**исерверсекурити**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) .</span><span class="sxs-lookup"><span data-stu-id="18f5e-107">When a call arrives at the server, the server can call [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to the [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface.</span></span> <span data-ttu-id="18f5e-108">С помощью этого указателя методы **исерверсекурити** могут вызываться сервером для определения параметров проверки подлинности клиента и олицетворения клиента при необходимости.</span><span class="sxs-lookup"><span data-stu-id="18f5e-108">With this pointer, **IServerSecurity** methods can be called by the server to find out what the client's authentication settings are and to impersonate the client, if needed.</span></span> <span data-ttu-id="18f5e-109">Объект **исерверсекурити** действителен в любом потоке в подразделении до тех пор, пока не завершится вызов, представленный параметром **исерверсекурити** .</span><span class="sxs-lookup"><span data-stu-id="18f5e-109">The **IServerSecurity** object is valid on any thread in the apartment until the call represented by **IServerSecurity** completes.</span></span> <span data-ttu-id="18f5e-110">Дополнительные сведения об олицетворении см. в разделе [олицетворение](impersonation.md) и [маскировка](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="18f5e-110">For more information about impersonation, see [Impersonation](impersonation.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="18f5e-111">Также доступны следующие вспомогательные функции, зависящие от реализации интерфейса [**исерверсекурити**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) в объекте контекста вызова.</span><span class="sxs-lookup"><span data-stu-id="18f5e-111">The following helper functions that rely on the call context object's [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface implementation are also available:</span></span>

-   [<span data-ttu-id="18f5e-112">**кокуериклиентбланкет**</span><span class="sxs-lookup"><span data-stu-id="18f5e-112">**CoQueryClientBlanket**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [<span data-ttu-id="18f5e-113">**коимперсонатеклиент**</span><span class="sxs-lookup"><span data-stu-id="18f5e-113">**CoImpersonateClient**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [<span data-ttu-id="18f5e-114">**кореверттоселф**</span><span class="sxs-lookup"><span data-stu-id="18f5e-114">**CoRevertToSelf**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a><span data-ttu-id="18f5e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="18f5e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18f5e-116">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="18f5e-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 