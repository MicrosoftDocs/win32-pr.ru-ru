---
description: Согласование уровня проверки подлинности
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Согласование уровня проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701295"
---
# <a name="negotiation-of-authentication-level"></a><span data-ttu-id="05f85-103">Согласование уровня проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="05f85-103">Negotiation of Authentication Level</span></span>

<span data-ttu-id="05f85-104">Как клиент, так и сервер должны участвовать в проверке подлинности, и каждая Сторона указывает, что требуется выполнить определенный уровень проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="05f85-104">Both client and server must participate in authentication, and each party indicates that it wants to perform a certain level of authentication.</span></span> <span data-ttu-id="05f85-105">В начале вызова уровень проверки подлинности согласовывается между двумя сторонами, выбирается соответствующая служба, после чего вызывается проверка подлинности и продолжается (с возможным шифрованием в зависимости от выбранного уровня проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="05f85-105">At the beginning of a call, the authentication level is negotiated between the two parties, an appropriate service is chosen, and the call is authenticated and proceeds (with possible encryption, depending on the authentication level chosen).</span></span> <span data-ttu-id="05f85-106">Уровень проверки подлинности, согласованный между клиентом и сервером, определяется как максимальный (*предпочтения клиента*, *предпочтения сервера*).</span><span class="sxs-lookup"><span data-stu-id="05f85-106">The authentication level negotiated between client and server is determined as Maximum(*Client preference*, *Server preference*).</span></span> <span data-ttu-id="05f85-107">Это означает, что сервер всегда может надиктовать минимальный уровень проверки подлинности, с которым он работает. то есть проверка подлинности может быть административно зависеть от сервера.</span><span class="sxs-lookup"><span data-stu-id="05f85-107">The effect of this means that the server can always dictate a minimum level of authentication that it is comfortable with; that is, authentication can be administratively dictated from the server.</span></span>

<span data-ttu-id="05f85-108">Клиент указывает, что требуется выполнять проверку подлинности на определенном уровне, как и в любом приложении COM.</span><span class="sxs-lookup"><span data-stu-id="05f85-108">The client specifies that it wants to perform authentication at a certain level as with any COM application.</span></span> <span data-ttu-id="05f85-109">Уровень проверки подлинности клиента может быть указан следующим образом:</span><span class="sxs-lookup"><span data-stu-id="05f85-109">The client authentication level can be indicated as follows:</span></span>

-   <span data-ttu-id="05f85-110">На клиентский компьютер с уровнем проверки подлинности COM на уровне компьютера, установленным с помощью команды [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) или средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="05f85-110">Per client machine, with the machine-wide COM authentication level set by using either [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) or the Component Services administrative tool.</span></span>
-   <span data-ttu-id="05f85-111">Для каждого клиентского приложения в административном состоянии с помощью [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) или средства администрирования служб компонентов, если клиент должен быть приложением COM+.</span><span class="sxs-lookup"><span data-stu-id="05f85-111">Per client application administratively, using [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) or using the Component Services administrative tool if the client should be a COM+ application.</span></span>
-   <span data-ttu-id="05f85-112">На клиентский процесс программным путем с помощью [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="05f85-112">Per client process programmatically, with [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="05f85-113">В любой точке программным способом используется метод [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="05f85-113">At any point programmatically, using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="05f85-114">Серверное приложение COM+ задает уровень проверки подлинности в административном виде с помощью средства администрирования "службы компонентов" (или с помощью административного сценария).</span><span class="sxs-lookup"><span data-stu-id="05f85-114">The COM+ server application specifies an authentication level administratively by using the Component Services administrative tool (or through an administrative script).</span></span>

<span data-ttu-id="05f85-115">Согласование проверки подлинности для вызова продолжается в следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="05f85-115">Negotiating authentication for a call proceeds in the following sequence:</span></span>

1.  <span data-ttu-id="05f85-116">Уровень проверки подлинности выбирается как MAX (*клиент*, *сервер*).</span><span class="sxs-lookup"><span data-stu-id="05f85-116">Authentication level is chosen as MAX(*client*, *server*).</span></span>
2.  <span data-ttu-id="05f85-117">Согласование протокола проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="05f85-117">Negotiation of authentication protocol.</span></span>
3.  <span data-ttu-id="05f85-118">Сервер проверяет подлинность удостоверения клиента.</span><span class="sxs-lookup"><span data-stu-id="05f85-118">Server authenticates client identity.</span></span>
4.  <span data-ttu-id="05f85-119">При необходимости клиент проверяет подлинность удостоверения сервера в зависимости от протокола проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="05f85-119">Optionally, client authenticates server identity, depending on the authentication protocol.</span></span>
5.  <span data-ttu-id="05f85-120">Вызовы методов взаимодействуют с выбранным уровнем проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="05f85-120">Method calls are communicated with the chosen level of authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05f85-121">См. также</span><span class="sxs-lookup"><span data-stu-id="05f85-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05f85-122">Аутентификация клиента</span><span class="sxs-lookup"><span data-stu-id="05f85-122">Client Authentication</span></span>](client-authentication.md)
</dt> </dl>

 

 
