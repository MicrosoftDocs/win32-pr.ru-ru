---
title: Использование Transport-Level безопасности на клиенте
description: Клиент указывает, как сервер олицетворяет клиент, когда клиент устанавливает привязку строк.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Удаленный вызов процедур RPC, задачи, использование безопасности на уровне транспорта на клиенте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987806"
---
# <a name="using-transport-level-security-on-the-client"></a><span data-ttu-id="2c2a8-104">Использование Transport-Level безопасности на клиенте</span><span class="sxs-lookup"><span data-stu-id="2c2a8-104">Using Transport-Level Security on the Client</span></span>

<span data-ttu-id="2c2a8-105">Клиент указывает, как сервер олицетворяет клиент, когда клиент устанавливает привязку строк.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-105">The client specifies how the server impersonates the client when the client establishes the string binding.</span></span> <span data-ttu-id="2c2a8-106">Эти сведения о QOS предоставляются в качестве параметра конечной точки в привязке строк.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-106">This QOS information is provided as an endpoint option in the string binding.</span></span> <span data-ttu-id="2c2a8-107">Клиент может указать уровень олицетворения, динамическое или статическое отслеживание и флаг "только эффективный".</span><span class="sxs-lookup"><span data-stu-id="2c2a8-107">The client can specify the level of impersonation, dynamic or static tracking, and the effective-only flag.</span></span>

<span data-ttu-id="2c2a8-108">**Предоставление сведений об качеству обслуживания для сервера**</span><span class="sxs-lookup"><span data-stu-id="2c2a8-108">**To supply quality-of-service information for the server**</span></span>

1.  <span data-ttu-id="2c2a8-109">Клиент вызывает [**рпкстрингбиндингкомпосе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) для создания строк компонентов, включая параметры конечной точки, в правильном контексте привязки строк.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-109">The client calls [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) to create the component strings, including endpoint options, in the correct string-binding context.</span></span>
2.  <span data-ttu-id="2c2a8-110">Клиент вызывает [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) , чтобы получить новый маркер привязки и применить сведения об уровне обслуживания для клиента.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-110">The client calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain a new binding handle and to apply the quality-of-service information for the client.</span></span>
3.  <span data-ttu-id="2c2a8-111">Клиент выполняет удаленные вызовы процедур с помощью маркера.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-111">The client makes remote procedure calls using the handle.</span></span>

<span data-ttu-id="2c2a8-112">Microsoft RPC поддерживает функции безопасности Windows только в [**нкакн \_ NP**](/windows/desktop/Midl/ncacn-np) и [**нкалрпк**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="2c2a8-112">Microsoft RPC supports Windows security features only on [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) and [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="2c2a8-113">Параметры безопасности для других транспортов игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-113">Security options for other transports are ignored.</span></span>

<span data-ttu-id="2c2a8-114">Клиент может связать следующие параметры безопасности с привязкой для транспорта именованного канала [**нкакн \_ NP**](/windows/desktop/Midl/ncacn-np) или [**нкалрпк**](/windows/desktop/Midl/ncalrpc):</span><span class="sxs-lookup"><span data-stu-id="2c2a8-114">The client can associate the following security parameters to the binding for the named-pipe transport [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) or [**ncalrpc**](/windows/desktop/Midl/ncalrpc):</span></span>

-   <span data-ttu-id="2c2a8-115">Идентификация, олицетворение или анонимность.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-115">Identification, Impersonation, or Anonymous.</span></span> <span data-ttu-id="2c2a8-116">Указывает используемый тип безопасности.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-116">Specifies the type of security used.</span></span> <span data-ttu-id="2c2a8-117">По умолчанию используется олицетворение.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-117">The default is Impersonation.</span></span>
-   <span data-ttu-id="2c2a8-118">Dynamic или static.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-118">Dynamic or Static.</span></span> <span data-ttu-id="2c2a8-119">Определяет, являются ли сведения о безопасности, связанные с потоком, копией сведений о безопасности, созданных во время выполнения удаленного вызова процедуры (статического) или указателя на сведения о безопасности (динамический).</span><span class="sxs-lookup"><span data-stu-id="2c2a8-119">Determines whether security information associated with a thread is a copy of the security information created at the time the remote procedure call is made (static) or a pointer to the security information (dynamic).</span></span>

    <span data-ttu-id="2c2a8-120">Статическая информация о безопасности не изменяется.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-120">Static security information does not change.</span></span> <span data-ttu-id="2c2a8-121">Динамический параметр отражает текущие параметры безопасности, включая изменения, внесенные после удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-121">The dynamic setting reflects the current security settings, including changes made after the remote procedure call is made.</span></span> <span data-ttu-id="2c2a8-122">Для удаленных подключений именованного канала по умолчанию используется статический протокол [**\_ NP**](/windows/desktop/Midl/ncacn-np), а для соединений по локальному именованному каналу по умолчанию используется Dynamic.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-122">For [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), the default for remote named pipe connections is static, for local named pipe connections the default is dynamic.</span></span>

-   <span data-ttu-id="2c2a8-123">**True** или **false**.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-123">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="2c2a8-124">Задает значение флага только для эффективного использования.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-124">Specifies the value of the effective-only flag.</span></span> <span data-ttu-id="2c2a8-125">Значение **true** указывает, что только привилегии маркера, установленные в on во время вызова, вступают в силу.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-125">A value of **TRUE** indicates that only token privileges set to on at the time of the call are effective.</span></span> <span data-ttu-id="2c2a8-126">Значение **false** указывает, что доступны все привилегии и приложение может их изменять.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-126">A value of **FALSE** indicates that all privileges are available and that the application can modify them.</span></span>

<span data-ttu-id="2c2a8-127">Для привязки можно назначить любое сочетание этих параметров, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="2c2a8-127">Any combination of these settings can be assigned to the binding, as shown in the following example:</span></span>

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

<span data-ttu-id="2c2a8-128">Параметры безопасности по умолчанию зависят от транспортного протокола.</span><span class="sxs-lookup"><span data-stu-id="2c2a8-128">Default security-parameter settings vary according to the transport protocol.</span></span>

<span data-ttu-id="2c2a8-129">Дополнительные сведения о синтаксисе параметров конечной точки см. в разделе [Endpoint](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="2c2a8-129">For additional information about the syntax of the endpoint options, see [endpoint](/windows/desktop/Midl/endpoint).</span></span>

 

 