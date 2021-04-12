---
description: Client-Side требования для олицетворения
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side требования для олицетворения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342412"
---
# <a name="client-side-requirements-for-impersonation"></a><span data-ttu-id="89306-103">Client-Side требования для олицетворения</span><span class="sxs-lookup"><span data-stu-id="89306-103">Client-Side Requirements for Impersonation</span></span>

<span data-ttu-id="89306-104">Следующие два параметра могут быть указаны относительно олицетворения на стороне клиента:</span><span class="sxs-lookup"><span data-stu-id="89306-104">The following two settings can be specified relative to impersonation on the client side:</span></span>

-   <span data-ttu-id="89306-105">Уровень олицетворения, который указывает на готовность клиента к тому, что сервер использует его удостоверение.</span><span class="sxs-lookup"><span data-stu-id="89306-105">Impersonation level, which indicates the client's willingness to have the server use its identity.</span></span>
-   <span data-ttu-id="89306-106">Параметр в службе Active Directory, с помощью которого учетная запись клиента может быть помечена как "учетная запись является конфиденциальной и не может быть делегирована", что отключит делегирование.</span><span class="sxs-lookup"><span data-stu-id="89306-106">A setting in the Active Directory Service through which the client account can be marked "Account is sensitive and cannot be delegated," which will disable delegation.</span></span>

<span data-ttu-id="89306-107">Уровень олицетворения может быть задан различными способами.</span><span class="sxs-lookup"><span data-stu-id="89306-107">The impersonation level can be set in a variety of ways.</span></span> <span data-ttu-id="89306-108">Если клиент не указывает уровень олицетворения, COM-сервер использует значение по умолчанию на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="89306-108">If the client does not indicate an impersonation level, the machine-wide default will be used by COM.</span></span> <span data-ttu-id="89306-109">Значение по умолчанию на уровне компьютера можно задать с помощью средства администрирования "службы компонентов" или Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="89306-109">The machine-wide default can be set using either the Component Services administrative tool or Dcomcnfg.exe.</span></span> <span data-ttu-id="89306-110">Клиент также может указать предпочтительный уровень олицетворения в административном виде с Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="89306-110">The client can also indicate a preferred impersonation level administratively with Dcomcnfg.exe.</span></span>

<span data-ttu-id="89306-111">Клиент может указать уровень олицетворения программным путем с помощью метода [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)— эквивалента [**Иклиентсекурити:: сетбланкет**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), который может вызываться как можно чаще, или [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), который может вызываться один раз для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="89306-111">The client can indicate the impersonation level programmatically, using either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)—equivalent to [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), which can be called as often as necessary—or [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), which can be called once per process.</span></span>

<span data-ttu-id="89306-112">Если клиент указывает на олицетворение на уровне делегата — самый широкий из них, который он может предоставить серверу, то клиент должен работать под удостоверением, правильно настроенным в службе Active Directory, чтобы предоставить удостоверение для делегирования.</span><span class="sxs-lookup"><span data-stu-id="89306-112">If the client indicates delegate-level impersonation—the broadest authority it can grant to the server—the client should be running under an identity that is properly configured in the Active Directory Service to enable its identity to be delegated.</span></span>

<span data-ttu-id="89306-113">Дополнительные сведения о уровнях олицетворения и требованиях делегирования к работе см. в разделе [Делегирование и олицетворение](/windows/desktop/com/delegation-and-impersonation).</span><span class="sxs-lookup"><span data-stu-id="89306-113">For more detail regarding impersonation levels and the requirements for delegation to work, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

<span data-ttu-id="89306-114">Само собой, приложения COM+ всегда могут действовать как клиенты.</span><span class="sxs-lookup"><span data-stu-id="89306-114">COM+ applications can always act as clients, of course.</span></span> <span data-ttu-id="89306-115">Когда приложение COM+ выполняет вызов к другому приложению или ресурсу, оно выражает уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="89306-115">When the COM+ application makes a call to another application or resource, it expresses an impersonation level.</span></span> <span data-ttu-id="89306-116">Для серверных приложений COM+ можно задать уровень олицетворения административно.</span><span class="sxs-lookup"><span data-stu-id="89306-116">For COM+ server applications, you can set an impersonation level administratively.</span></span> <span data-ttu-id="89306-117">Приложения библиотеки COM+ не могут задавать собственный уровень олицетворения; Вместо этого они используют процесс хоста.</span><span class="sxs-lookup"><span data-stu-id="89306-117">COM+ library applications cannot set their own impersonation level; they use that of the host process instead.</span></span> <span data-ttu-id="89306-118">Сведения о настройке олицетворения для приложения COM+ см. в разделе [Установка уровня олицетворения](setting-an-impersonation-level.md).</span><span class="sxs-lookup"><span data-stu-id="89306-118">To learn how to set impersonation for a COM+ application, see [Setting an Impersonation Level](setting-an-impersonation-level.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89306-119">См. также</span><span class="sxs-lookup"><span data-stu-id="89306-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89306-120">Олицетворение и делегирование клиента</span><span class="sxs-lookup"><span data-stu-id="89306-120">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="89306-121">Маскировка</span><span class="sxs-lookup"><span data-stu-id="89306-121">Cloaking</span></span>](cloaking.md)
</dt> <dt>

[<span data-ttu-id="89306-122">Требования для олицетворения на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="89306-122">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
