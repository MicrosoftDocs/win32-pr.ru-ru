---
description: При использовании безопасности на основе ролей объект контекста вызова безопасности может использоваться для доступа к сведениям о безопасности текущего вызова.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Доступ к сведениям о контексте вызова безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262701"
---
# <a name="accessing-security-call-context-information"></a><span data-ttu-id="df047-103">Доступ к сведениям о контексте вызова безопасности</span><span class="sxs-lookup"><span data-stu-id="df047-103">Accessing Security Call Context Information</span></span>

<span data-ttu-id="df047-104">При использовании безопасности на основе ролей объект контекста вызова безопасности может использоваться для доступа к сведениям о безопасности текущего вызова.</span><span class="sxs-lookup"><span data-stu-id="df047-104">When role-based security is being used, the security call context object can be used to access security information about the current call.</span></span>

<span data-ttu-id="df047-105">Следующие коллекции свойств доступны в объекте контекста вызова безопасности:</span><span class="sxs-lookup"><span data-stu-id="df047-105">The following collections of properties are available from the security call context object:</span></span>

-   [<span data-ttu-id="df047-106">Коллекция Секуритикаллконтекст</span><span class="sxs-lookup"><span data-stu-id="df047-106">SecurityCallContext Collection</span></span>](#securitycallcontext-collection)
-   [<span data-ttu-id="df047-107">Коллекция Секуритикаллерс</span><span class="sxs-lookup"><span data-stu-id="df047-107">SecurityCallers Collection</span></span>](#securitycallers-collection)
-   [<span data-ttu-id="df047-108">Коллекция Секуритидентити</span><span class="sxs-lookup"><span data-stu-id="df047-108">SecurityIdentity Collection</span></span>](#securityidentity-collection)
-   [<span data-ttu-id="df047-109">См. также</span><span class="sxs-lookup"><span data-stu-id="df047-109">Related topics</span></span>](#related-topics)

## <a name="securitycallcontext-collection"></a><span data-ttu-id="df047-110">Коллекция Секуритикаллконтекст</span><span class="sxs-lookup"><span data-stu-id="df047-110">SecurityCallContext Collection</span></span>



| <span data-ttu-id="df047-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="df047-111">Property</span></span>                          | <span data-ttu-id="df047-112">Описание</span><span class="sxs-lookup"><span data-stu-id="df047-112">Description</span></span>                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df047-113">NumCallers</span><span class="sxs-lookup"><span data-stu-id="df047-113">NumCallers</span></span><br/>             | <span data-ttu-id="df047-114">Количество вызывающих объектов в цепочке вызовов.</span><span class="sxs-lookup"><span data-stu-id="df047-114">The number of callers in the chain of calls.</span></span><br/>                                                                                |
| <span data-ttu-id="df047-115">MinAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="df047-115">MinAuthenticationLevel</span></span><br/> | <span data-ttu-id="df047-116">Наименее безопасный уровень проверки подлинности всех вызывающих объектов в цепочке.</span><span class="sxs-lookup"><span data-stu-id="df047-116">The least secure authentication level of all callers in the chain.</span></span><br/>                                                          |
| <span data-ttu-id="df047-117">Callers</span><span class="sxs-lookup"><span data-stu-id="df047-117">Callers</span></span><br/>                | <span data-ttu-id="df047-118">Сведения об удостоверении вышестоящего вызывающего объекта в форме коллекции [**секуритикаллерс**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="df047-118">Information about the identity of upstream callers, in the form of a [**SecurityCallers**](securitycallers.md) collection.</span></span><br/> |
| <span data-ttu-id="df047-119">DirectCaller</span><span class="sxs-lookup"><span data-stu-id="df047-119">DirectCaller</span></span><br/>           | <span data-ttu-id="df047-120">Вызывающий объект, который вызвал непосредственное обращение к объекту (без промежуточных вызовов).</span><span class="sxs-lookup"><span data-stu-id="df047-120">The caller that called the object directly (with no intervening callers).</span></span> <br/>                                                  |
| <span data-ttu-id="df047-121">OriginalCaller</span><span class="sxs-lookup"><span data-stu-id="df047-121">OriginalCaller</span></span><br/>         | <span data-ttu-id="df047-122">Вызывающий объект, порожденный цепочкой вызовов объекта.</span><span class="sxs-lookup"><span data-stu-id="df047-122">The caller that originated the chain of calls to the object.</span></span> <br/>                                                               |



 

<span data-ttu-id="df047-123">Дополнительные сведения о том, как использовать эту коллекцию, разработчики Microsoft Visual Basic должны видеть класс [**секуритикаллконтекст**](securitycallcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="df047-123">For more information about how to use this collection, Microsoft Visual Basic developers should see the [**SecurityCallContext**](securitycallcontext.md) class.</span></span> <span data-ttu-id="df047-124">Разработчики C и C++ должны ссылаться на [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="df047-124">C and C++ developers should refer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="securitycallers-collection"></a><span data-ttu-id="df047-125">Коллекция Секуритикаллерс</span><span class="sxs-lookup"><span data-stu-id="df047-125">SecurityCallers Collection</span></span>

<span data-ttu-id="df047-126">Коллекция [**секуритикаллерс**](securitycallers.md) представляет вызывающие объекты, которые могут быть извлечены с помощью индекса от 0 до 1 меньше нумкаллерс включительно.</span><span class="sxs-lookup"><span data-stu-id="df047-126">The [**SecurityCallers**](securitycallers.md) collection represents callers that can be retrieved by using an index between 0 and 1 less than NumCallers, inclusive.</span></span> <span data-ttu-id="df047-127">Каждый вызывающий объект представлен объектом [**секуритидентити**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="df047-127">Each caller is represented by a [**SecurityIdentity**](securityidentity.md) object.</span></span>

<span data-ttu-id="df047-128">Для получения дополнительных сведений об этой коллекции Visual Basic разработчики должны увидеть класс [**секуритикаллерс**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="df047-128">For more information about this collection, Visual Basic developers should see the [**SecurityCallers**](securitycallers.md) class.</span></span> <span data-ttu-id="df047-129">Разработчики C и C++ должны ссылаться на [**исекуритикаллерсколл**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="df047-129">C and C++ developers should refer to [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="securityidentity-collection"></a><span data-ttu-id="df047-130">Коллекция Секуритидентити</span><span class="sxs-lookup"><span data-stu-id="df047-130">SecurityIdentity Collection</span></span>



| <span data-ttu-id="df047-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="df047-131">Property</span></span>                         | <span data-ttu-id="df047-132">Описание</span><span class="sxs-lookup"><span data-stu-id="df047-132">Description</span></span>                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df047-133">SID</span><span class="sxs-lookup"><span data-stu-id="df047-133">SID</span></span><br/>                   | <span data-ttu-id="df047-134">Идентификатор безопасности для вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="df047-134">The security identifier for the caller.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="df047-135">AccountName</span><span class="sxs-lookup"><span data-stu-id="df047-135">AccountName</span></span><br/>           | <span data-ttu-id="df047-136">Имя учетной записи вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="df047-136">The account name of the caller.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="df047-137">AuthenticationService</span><span class="sxs-lookup"><span data-stu-id="df047-137">AuthenticationService</span></span><br/> | <span data-ttu-id="df047-138">Используемая служба проверки подлинности, например NTLMSSP, Kerberos или SSL.</span><span class="sxs-lookup"><span data-stu-id="df047-138">The authentication service used, such as NTLMSSP, Kerberos, or SSL.</span></span><br/>                                                                                       |
| <span data-ttu-id="df047-139">аусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="df047-139">AuthenticationLevel</span></span><br/>   | <span data-ttu-id="df047-140">Используемый уровень проверки подлинности, который представляет объем защиты, используемый при взаимодействии с объектом.</span><span class="sxs-lookup"><span data-stu-id="df047-140">The authentication level used, which represents the amount of protection used when communicating with the object.</span></span><br/>                                         |
| <span data-ttu-id="df047-141">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="df047-141">ImpersonationLevel</span></span><br/>    | <span data-ttu-id="df047-142">Уровень олицетворения, заданный клиентом, если использовалось олицетворение.</span><span class="sxs-lookup"><span data-stu-id="df047-142">The level of impersonation set by the client, if impersonation was used.</span></span> <span data-ttu-id="df047-143">Этот уровень указывает количество полномочий, предоставленных клиентом для сервера.</span><span class="sxs-lookup"><span data-stu-id="df047-143">This level indicates the amount of authority given to the server by the client.</span></span> <br/> |



 

<span data-ttu-id="df047-144">Для получения дополнительных сведений об этой коллекции Visual Basic разработчики должны увидеть класс [**секуритидентити**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="df047-144">For more information on this collection, Visual Basic developers should see the [**SecurityIdentity**](securityidentity.md) class.</span></span> <span data-ttu-id="df047-145">Разработчики C и C++ должны ссылаться на [**исекуритидентитиколл**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="df047-145">C and C++ developers should refer to [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df047-146">См. также</span><span class="sxs-lookup"><span data-stu-id="df047-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df047-147">Проверка членства в роли</span><span class="sxs-lookup"><span data-stu-id="df047-147">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="df047-148">Определение того, включена ли безопасность Role-Based</span><span class="sxs-lookup"><span data-stu-id="df047-148">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="df047-149">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="df047-149">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 




