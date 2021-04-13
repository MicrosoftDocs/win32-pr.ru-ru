---
description: Так как приложение библиотеки COM+ размещено в другом процессе, у которого могут быть собственные параметры безопасности, безопасность для библиотечных приложений требует особого внимания.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Безопасность библиотечных приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538717"
---
# <a name="library-application-security"></a><span data-ttu-id="81939-103">Безопасность библиотечных приложений</span><span class="sxs-lookup"><span data-stu-id="81939-103">Library Application Security</span></span>

<span data-ttu-id="81939-104">Так как приложение библиотеки COM+ размещено в другом процессе, у которого могут быть собственные параметры безопасности, безопасность для библиотечных приложений требует особого внимания.</span><span class="sxs-lookup"><span data-stu-id="81939-104">Because a COM+ library application is hosted by another process, which may have its own security settings, security for library applications requires special consideration.</span></span>

<span data-ttu-id="81939-105">К безопасности приложения библиотеки применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="81939-105">The following constraints apply to library application security:</span></span>

-   <span data-ttu-id="81939-106">Библиотечные приложения выполняются с маркером безопасности клиентского процесса, а не с собственным удостоверением пользователя.</span><span class="sxs-lookup"><span data-stu-id="81939-106">Library applications run under the client process security token rather than under their own user identity.</span></span> <span data-ttu-id="81939-107">У них есть только такой уровень привилегий, как у клиента.</span><span class="sxs-lookup"><span data-stu-id="81939-107">They have only as much privilege as the client has.</span></span>
-   <span data-ttu-id="81939-108">Библиотечные приложения не управляют безопасностью на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="81939-108">Library applications do not control process-level security.</span></span> <span data-ttu-id="81939-109">Пользователи в ролях не будут добавлены в дескриптор безопасности для процесса.</span><span class="sxs-lookup"><span data-stu-id="81939-109">No users in roles will be added to the security descriptor for the process.</span></span> <span data-ttu-id="81939-110">Единственный способ, которым приложение библиотеки может выполнять свои собственные проверки доступа, — использовать безопасность на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="81939-110">The only way for a library application to perform its own access checks is to use component-level security.</span></span> <span data-ttu-id="81939-111">(См. раздел [границы безопасности](security-boundaries.md).)</span><span class="sxs-lookup"><span data-stu-id="81939-111">(See [Security Boundaries](security-boundaries.md).)</span></span>
-   <span data-ttu-id="81939-112">Приложения библиотеки можно настроить для участия или не участвовать в аутентификации процесса узла, включив или отключив проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="81939-112">Library applications can be configured to either participate or not participate in host process authentication, by enabling or disabling authentication.</span></span> <span data-ttu-id="81939-113">(См. раздел [Включение проверки подлинности для библиотечного приложения](enabling-authentication-for-a-library-application.md).)</span><span class="sxs-lookup"><span data-stu-id="81939-113">(See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).)</span></span>
-   <span data-ttu-id="81939-114">Библиотечные приложения не могут задавать уровень олицетворения; они используют процесс хоста.</span><span class="sxs-lookup"><span data-stu-id="81939-114">Library applications cannot set an impersonation level; they use that of the host process.</span></span>

## <a name="using-library-applications-to-limit-application-privilege"></a><span data-ttu-id="81939-115">Использование библиотечных приложений для ограничения прав приложения</span><span class="sxs-lookup"><span data-stu-id="81939-115">Using Library Applications to Limit Application Privilege</span></span>

<span data-ttu-id="81939-116">В некоторых случаях может потребоваться настроить приложение в виде библиотечного приложения, чтобы оно выполнялось под удостоверением ведущего процесса.</span><span class="sxs-lookup"><span data-stu-id="81939-116">In some cases, you may want to configure an application specifically as a library application so that it runs under the identity of the hosting process.</span></span> <span data-ttu-id="81939-117">Это позволяет существенно ограничить приложение таким образом, чтобы оно было иметь доступ только к тем ресурсам, к которым может получить доступ клиент, ведущий процесс.</span><span class="sxs-lookup"><span data-stu-id="81939-117">Doing so fundamentally limits the application so that it can access only those resources that its client, the host process, can access.</span></span> <span data-ttu-id="81939-118">Потоки, на которых выполняются компоненты приложения библиотеки, будут использовать маркер процесса по умолчанию, поэтому при вызовах вне приложения или доступе к ресурсам, таким как файлы, защищенные с помощью дескриптора безопасности, они будут выглядеть как клиент.</span><span class="sxs-lookup"><span data-stu-id="81939-118">The threads that the library application components run on will use the process token by default, and therefore when they make calls outside of the application or access resources such as files guarded with a security descriptor, they will appear to be the client.</span></span> <span data-ttu-id="81939-119">Для приложений, выполняющих важную работу, это может быть простой способ управления областью действия.</span><span class="sxs-lookup"><span data-stu-id="81939-119">For applications that perform sensitive work, this may be an easy way to control the scope of their actions.</span></span>

## <a name="effectively-securing-library-applications"></a><span data-ttu-id="81939-120">Эффективное обеспечение безопасности библиотечных приложений</span><span class="sxs-lookup"><span data-stu-id="81939-120">Effectively Securing Library Applications</span></span>

<span data-ttu-id="81939-121">Существуют особые рекомендации по настройке безопасности на основе ролей и проверке подлинности для библиотечных приложений, чтобы они выполнялись должным образом.</span><span class="sxs-lookup"><span data-stu-id="81939-121">There are special considerations in configuring role-based security and authentication for library applications so that they perform as expected.</span></span> <span data-ttu-id="81939-122">Дополнительные сведения см. в разделе [Настройка безопасности для библиотечных приложений](configuring-security-for-library-applications.md).</span><span class="sxs-lookup"><span data-stu-id="81939-122">For details, see [Configuring Security for Library Applications](configuring-security-for-library-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81939-123">См. также</span><span class="sxs-lookup"><span data-stu-id="81939-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81939-124">Аутентификация клиента</span><span class="sxs-lookup"><span data-stu-id="81939-124">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="81939-125">Олицетворение и делегирование клиента</span><span class="sxs-lookup"><span data-stu-id="81939-125">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="81939-126">Многоуровневая защита приложений</span><span class="sxs-lookup"><span data-stu-id="81939-126">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="81939-127">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="81939-127">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="81939-128">Администрирование безопасности на основе ролей</span><span class="sxs-lookup"><span data-stu-id="81939-128">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="81939-129">Использование политики ограниченного использования программ в COM+</span><span class="sxs-lookup"><span data-stu-id="81939-129">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



