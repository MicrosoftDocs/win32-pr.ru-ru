---
description: Многоуровневая защита приложений
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Многоуровневая защита приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673125"
---
# <a name="multi-tier-application-security"></a><span data-ttu-id="6871c-103">Многоуровневая защита приложений</span><span class="sxs-lookup"><span data-stu-id="6871c-103">Multi-Tier Application Security</span></span>

<span data-ttu-id="6871c-104">При принятии решения о необходимости принудительного применения безопасности в многоуровневом приложении на базе базы данных можно выбрать нужный вариант.</span><span class="sxs-lookup"><span data-stu-id="6871c-104">You can face difficult choices in deciding precisely where to enforce security in a multi-tier, component-based application: At the database?</span></span> <span data-ttu-id="6871c-105">На среднем уровне?</span><span class="sxs-lookup"><span data-stu-id="6871c-105">At the middle tier?</span></span> <span data-ttu-id="6871c-106">В каких компонентах?</span><span class="sxs-lookup"><span data-stu-id="6871c-106">In the components?</span></span> <span data-ttu-id="6871c-107">Где-то еще?</span><span class="sxs-lookup"><span data-stu-id="6871c-107">Somewhere else?</span></span> <span data-ttu-id="6871c-108">Везде?</span><span class="sxs-lookup"><span data-stu-id="6871c-108">Everywhere?</span></span> <span data-ttu-id="6871c-109">Поскольку механизмы безопасности увеличивают число и сложность, снижение производительности и поведение приложения становятся менее предсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="6871c-109">As security mechanisms increase in number and complexity, performance declines and application behavior becomes less predictable.</span></span> <span data-ttu-id="6871c-110">Тем не менее, необходимо убедиться, что данные защищены, Бизнес-правила выполняются, а значительная активность зарегистрирована, и все еще работает приложение для клиентов, как задумано.</span><span class="sxs-lookup"><span data-stu-id="6871c-110">Nevertheless, you must ensure that data is protected, business rules are followed, and significant activity is logged, and still have your application work for clients as intended.</span></span> <span data-ttu-id="6871c-111">Необходимо убедиться в том, что каждый клиентский путь в приложении является правильным и все контрольные точки безопасности на месте будут достаточно.</span><span class="sxs-lookup"><span data-stu-id="6871c-111">You must be certain that every client path through your application is correct and that the security checkpoints you have in place will suffice.</span></span>

<span data-ttu-id="6871c-112">Самым сложным решением часто является необходимость принудительного применения безопасности в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6871c-112">The hardest decision is often whether to enforce security at the database.</span></span> <span data-ttu-id="6871c-113">Исторически, именно в этом заключается в том, что безопасность очень тесна, так как она считается одним Королевством, который должен быть действительно безопасным, и администраторы баз данных очень неохотно, чтобы обеспечить безопасность для них.</span><span class="sxs-lookup"><span data-stu-id="6871c-113">Historically, this is where security is tightest because it is perceived as the one kingdom that needs to be truly secure, and database administrators are very reluctant to trust someone else to enforce security for them.</span></span> <span data-ttu-id="6871c-114">Но обеспечение безопасности в базе данных может быть довольно дорогостоящим и сложным для масштабирования, что в первую очередь пишет многоуровневые приложения.</span><span class="sxs-lookup"><span data-stu-id="6871c-114">But enforcing security at the database can be quite expensive and difficult to scale, which is precisely the point of writing multi-tier applications in the first place.</span></span>

<span data-ttu-id="6871c-115">Общее правило для выполнения масштабируемых многоуровневых приложений с помощью COM+ заключается в том, что при любой возможности необходимо обеспечить детальную безопасность в приложении COM+ на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="6871c-115">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="6871c-116">Это позволит вам полностью использовать масштабируемые службы, предоставляемые COM+.</span><span class="sxs-lookup"><span data-stu-id="6871c-116">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="6871c-117">Проверка подлинности в базе данных выполняется только в том случае, когда вам абсолютно нужно, и полностью взвесьте влияние этого на производительность.</span><span class="sxs-lookup"><span data-stu-id="6871c-117">Authenticate at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="6871c-118">Обсуждение вопросов, которые следует учитывать при принятии решения о том, где следует выполнять проверки безопасности, см. в разделе [Выбор места для обеспечения безопасности](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="6871c-118">For a discussion of issues to consider in deciding where to perform security checks, see [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

<span data-ttu-id="6871c-119">Обсуждение некоторых базовых сценариев защиты многоуровневых приложений см. в разделе [основные сценарии защиты данных в многоуровневых приложениях](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6871c-119">For a discussion of some basic scenarios in securing multi-tier applications, see [Basic Scenarios for Securing Data in Multi-Tier Applications](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6871c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6871c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6871c-121">Аутентификация клиента</span><span class="sxs-lookup"><span data-stu-id="6871c-121">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="6871c-122">Олицетворение и делегирование клиента</span><span class="sxs-lookup"><span data-stu-id="6871c-122">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="6871c-123">Безопасность библиотечных приложений</span><span class="sxs-lookup"><span data-stu-id="6871c-123">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="6871c-124">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="6871c-124">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="6871c-125">Администрирование безопасности на основе ролей</span><span class="sxs-lookup"><span data-stu-id="6871c-125">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="6871c-126">Использование политики ограниченного использования программ в COM+</span><span class="sxs-lookup"><span data-stu-id="6871c-126">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



