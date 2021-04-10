---
title: Интерфейсы шлюза удаленный рабочий стол
description: Интерфейс API шлюза удаленный рабочий стол поддерживает следующие интерфейсы. Эти интерфейсы можно использовать для реализации подключаемых модулей, обеспечивающих настраиваемую проверку подлинности и авторизацию.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986205"
---
# <a name="remote-desktop-gateway-interfaces"></a><span data-ttu-id="08363-104">Интерфейсы шлюза удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="08363-104">Remote Desktop Gateway Interfaces</span></span>

<span data-ttu-id="08363-105">Интерфейс API шлюза удаленный рабочий стол поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="08363-105">The Remote Desktop Gateway (RD Gateway) API supports the following interfaces.</span></span> <span data-ttu-id="08363-106">Эти интерфейсы можно использовать для реализации подключаемых модулей, обеспечивающих настраиваемую проверку подлинности и авторизацию.</span><span class="sxs-lookup"><span data-stu-id="08363-106">You can use these interfaces to implement plug-ins that provide customized authentication and authorization.</span></span> <span data-ttu-id="08363-107">Между подключаемым модулем проверки подлинности и подключаемым модулем авторизации нет зависимостей, и при необходимости можно реализовать только один подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="08363-107">There is no dependency between the authentication plug-in and the authorization plug-in, and you can implement only a single plug-in if you choose.</span></span>

<span data-ttu-id="08363-108">Подключаемые модули проверки подлинности — [**итсгаусентикатеусерсинк**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) и [**итсгаусентикатионенгине**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span><span class="sxs-lookup"><span data-stu-id="08363-108">The authentication plug-ins are [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) and [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span></span>

<span data-ttu-id="08363-109">Подключаемые модули авторизации — это [**итсгаккаунтинженгине**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**итсгаусоризеконнектионсинк**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**итсгаусоризересаурцесинк**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)и [**итсгполициенгине**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span><span class="sxs-lookup"><span data-stu-id="08363-109">The authorization plug-ins are [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink), and [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="08363-110">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="08363-110">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="08363-111">**итсгаккаунтинженгине**</span><span class="sxs-lookup"><span data-stu-id="08363-111">**ITSGAccountingEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

<span data-ttu-id="08363-112">Предоставляет методы, предоставляющие сведения о создании или закрытии сеансов для соединения.</span><span class="sxs-lookup"><span data-stu-id="08363-112">Exposes methods that provide information about the creation or closing of sessions for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="08363-113">**итсгаусентикатеусерсинк**</span><span class="sxs-lookup"><span data-stu-id="08363-113">**ITSGAuthenticateUserSink**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

<span data-ttu-id="08363-114">Предоставляет методы, уведомляющие шлюз удаленных рабочих столов о событиях проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="08363-114">Exposes methods that notify RD Gateway about authentication events.</span></span>

</dd> <dt>

[<span data-ttu-id="08363-115">**итсгаусентикатионенгине**</span><span class="sxs-lookup"><span data-stu-id="08363-115">**ITSGAuthenticationEngine**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

<span data-ttu-id="08363-116">Предоставляет методы, которые проверяют подлинность пользователей для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="08363-116">Exposes methods that authenticate users for RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="08363-117">**итсгаусоризеконнектионсинк**</span><span class="sxs-lookup"><span data-stu-id="08363-117">**ITSGAuthorizeConnectionSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

<span data-ttu-id="08363-118">Предоставляет методы, уведомляющие шлюз удаленных рабочих столов о результатах попытки авторизации подключения.</span><span class="sxs-lookup"><span data-stu-id="08363-118">Exposes methods that notify RD Gateway about the result of an attempt to authorize a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="08363-119">**итсгаусоризересаурцесинк**</span><span class="sxs-lookup"><span data-stu-id="08363-119">**ITSGAuthorizeResourceSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

<span data-ttu-id="08363-120">Предоставляет методы, уведомляющие шлюз удаленных рабочих столов о результатах попытки авторизации ресурса.</span><span class="sxs-lookup"><span data-stu-id="08363-120">Exposes methods that notify RD Gateway about the result of an attempt to authorize a resource.</span></span>

</dd> <dt>

[<span data-ttu-id="08363-121">**итсгполициенгине**</span><span class="sxs-lookup"><span data-stu-id="08363-121">**ITSGPolicyEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

<span data-ttu-id="08363-122">Предоставляет методы, которые позволяют авторизовать подключения и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="08363-122">Exposes methods that authorize connections and resources.</span></span>

</dd> </dl>

 

 




