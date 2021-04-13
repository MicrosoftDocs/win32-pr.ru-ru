---
description: Role-Based администрирование безопасности
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based администрирование безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539182"
---
# <a name="role-based-security-administration"></a><span data-ttu-id="ad5ca-103">Role-Based администрирование безопасности</span><span class="sxs-lookup"><span data-stu-id="ad5ca-103">Role-Based Security Administration</span></span>

<span data-ttu-id="ad5ca-104">Безопасность на основе ролей — это автоматическая служба, предоставляемая COM+, которая позволяет административно создавать и обеспечивать политику управления доступом для приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-104">Role-based security is an automatic service provided by COM+ that enables you to administratively construct and enforce an access control policy for your COM+ application.</span></span> <span data-ttu-id="ad5ca-105">Благодаря гибкой и расширяемой модели конфигурации безопасности на основе ролей обеспечивается существенное преимущество, чем обеспечение безопасности в компонентах, и обеспечивает следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="ad5ca-105">With a flexible and extensible security configuration model, role-based security offers a considerable advantage over enforcing all security within your components and provides the following benefits:</span></span>

-   <span data-ttu-id="ad5ca-106">Безопасность можно настроить в административном режиме с помощью средства администрирования служб компонентов или административных функций.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-106">You can configure security administratively, using either the Component Services administrative tool or the Administrative functions.</span></span>
-   <span data-ttu-id="ad5ca-107">Вам не нужно писать в компоненты логику безопасности, если защита ролей на уровне метода обеспечивает достаточный контроль доступа.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-107">You don't have to write security-related logic into your components when role protection at the method level provides you with fine enough access control.</span></span>
-   <span data-ttu-id="ad5ca-108">В разработке интерфейса или компонента нет необходимости приложить защиту.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-108">You don't have to factor security into interface or component design.</span></span> <span data-ttu-id="ad5ca-109">Вместо этого можно установить безопасность для каждого метода.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-109">Instead, you can set security on a method-by-method basis.</span></span>
-   <span data-ttu-id="ad5ca-110">Вы можете сосредоточиться на структуре политики безопасности, которую вы хотите применить, и с помощью ролей. Эта политика может быть явно выражена для администраторов, развертывающих приложение.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-110">You can focus on the structure of the security policy you want to enforce, and through roles, that policy can be clearly expressed to the administrators deploying your application.</span></span>
-   <span data-ttu-id="ad5ca-111">Можно легко изменить политику безопасности, чтобы адаптироваться к растущим требованиям безопасности для приложения.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-111">You can easily modify a security policy to adapt to evolving security requirements for an application.</span></span>
-   <span data-ttu-id="ad5ca-112">Более детализированные политики безопасности можно создавать программно, если необходимо, используя безопасность на основе ролей в качестве поддерживающей платформы.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-112">You can build more granular security policies programmatically if you need to, using role-based security as a supporting platform.</span></span>
-   <span data-ttu-id="ad5ca-113">Можно использовать безопасность на основе ролей для выполнения подробного аудита, так как можно получить сведения о безопасности вызывающей стороны для всей цепочки вышестоящего вызова.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-113">You can leverage role-based security to do detailed auditing, because you can obtain caller security information for an entire chain of upstream calls.</span></span>

> [!Note]  
> <span data-ttu-id="ad5ca-114">Пользователи с ролью администратора для системного приложения должны быть членами локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-114">Users in the Administrator role for the System Application must be members of the local administrators group.</span></span> <span data-ttu-id="ad5ca-115">Кроме того, начиная с Windows Server 2003, функция проверки подлинности для системного приложения COM+ включает значение ЕОАК \_ disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-115">Also, as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="ad5ca-116">Это значение, которое отключает активацию активации на основе активатора (AAA), используется в вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) при запуске системного приложения.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-116">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="ad5ca-117">Установка функции проверки подлинности в ЕОАК \_ disable \_ AAA позволяет приложению, работающему под привилегированной учетной записью (например, LocalSystem), предотвратить использование удостоверения для запуска ненадежных компонентов.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-117">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

<span data-ttu-id="ad5ca-118">Сведения о принципах работы системы безопасности на основе ролей и вопросах, которые следует учитывать при создании политики безопасности для приложения, см. в следующих разделах этого раздела.</span><span class="sxs-lookup"><span data-stu-id="ad5ca-118">See the following topics in this section for information about how role-based security works and issues to consider when using it to construct a security policy for an application:</span></span>

-   [<span data-ttu-id="ad5ca-119">Использование ролей для авторизации клиентов</span><span class="sxs-lookup"><span data-stu-id="ad5ca-119">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
-   [<span data-ttu-id="ad5ca-120">Эффективное проектирование ролей</span><span class="sxs-lookup"><span data-stu-id="ad5ca-120">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
-   [<span data-ttu-id="ad5ca-121">Границы безопасности</span><span class="sxs-lookup"><span data-stu-id="ad5ca-121">Security Boundaries</span></span>](security-boundaries.md)
-   [<span data-ttu-id="ad5ca-122">Сведения о контексте вызова безопасности</span><span class="sxs-lookup"><span data-stu-id="ad5ca-122">Security Call Context Information</span></span>](security-call-context-information.md)
-   [<span data-ttu-id="ad5ca-123">Свойство контекста безопасности</span><span class="sxs-lookup"><span data-stu-id="ad5ca-123">Security Context Property</span></span>](security-context-property.md)

<span data-ttu-id="ad5ca-124">Подробное описание действий, связанных с настройкой безопасности на основе ролей для приложения, см. в разделе [Настройка безопасности Role-Based](configuring-role-based-security.md).</span><span class="sxs-lookup"><span data-stu-id="ad5ca-124">For detailed how-to descriptions of the steps involved in configuring role-based security for an application, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad5ca-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ad5ca-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad5ca-126">Аутентификация клиента</span><span class="sxs-lookup"><span data-stu-id="ad5ca-126">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="ad5ca-127">Олицетворение и делегирование клиента</span><span class="sxs-lookup"><span data-stu-id="ad5ca-127">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="ad5ca-128">Безопасность библиотечных приложений</span><span class="sxs-lookup"><span data-stu-id="ad5ca-128">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="ad5ca-129">Многоуровневая защита приложений</span><span class="sxs-lookup"><span data-stu-id="ad5ca-129">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="ad5ca-130">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="ad5ca-130">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="ad5ca-131">Использование политики ограниченного использования программ в COM+</span><span class="sxs-lookup"><span data-stu-id="ad5ca-131">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
