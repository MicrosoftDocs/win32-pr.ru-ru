---
description: При использовании безопасности на основе ролей в приложении COM+, которое содержит компонент, у вас есть доступ к программным функциям безопасности из компонента.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Безопасность программных компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701227"
---
# <a name="programmatic-component-security"></a><span data-ttu-id="49265-103">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="49265-103">Programmatic Component Security</span></span>

<span data-ttu-id="49265-104">При использовании безопасности на основе ролей в приложении COM+, которое содержит компонент, у вас есть доступ к программным функциям безопасности из компонента.</span><span class="sxs-lookup"><span data-stu-id="49265-104">When you use role-based security in the COM+ application that contains your component, you have access to programmatic security functionality from within your component.</span></span> <span data-ttu-id="49265-105">Можно проверить членство в роли, чтобы определить, выполняются ли определенные разделы кода, получить доступ к сведениям о безопасности с помощью объекта контекста вызова безопасности, а также определить, включена ли безопасность для текущего вызова.</span><span class="sxs-lookup"><span data-stu-id="49265-105">You can check role membership to determine whether particular sections of code are executed, you can access security information using the security call context object, and you can determine whether security is enabled for the current call.</span></span> <span data-ttu-id="49265-106">Все эти задачи можно выполнить с помощью ссылки на объект [**секуритикаллконтекст**](securitycallcontext.md) (для приложений Microsoft Visual Basic) или указателя на интерфейс [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (для приложений C и Microsoft Visual C++).</span><span class="sxs-lookup"><span data-stu-id="49265-106">You can perform all of these tasks by using a reference to a [**SecurityCallContext**](securitycallcontext.md) object (for Microsoft Visual Basic applications) or a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface (for C and Microsoft Visual C++ applications).</span></span>

<span data-ttu-id="49265-107">Дополнительные сведения о программной безопасности на основе ролей см. в следующих подразделах этого раздела:</span><span class="sxs-lookup"><span data-stu-id="49265-107">For more information regarding programmatic role-based security, see the following topics in this section:</span></span>

-   [<span data-ttu-id="49265-108">Проверка членства в роли</span><span class="sxs-lookup"><span data-stu-id="49265-108">Checking Role Membership</span></span>](checking-role-membership.md)
-   [<span data-ttu-id="49265-109">Определение того, включена ли безопасность Role-Based</span><span class="sxs-lookup"><span data-stu-id="49265-109">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
-   [<span data-ttu-id="49265-110">Доступ к сведениям о контексте вызова безопасности</span><span class="sxs-lookup"><span data-stu-id="49265-110">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a><span data-ttu-id="49265-111">Функции олицетворения и безопасности COM</span><span class="sxs-lookup"><span data-stu-id="49265-111">Impersonation and COM Security Features</span></span>

<span data-ttu-id="49265-112">Если компонент используется в приложении COM+, которое не использует безопасность на основе ролей, сведения о программной проверке ролей и контексте вызова безопасности недоступны.</span><span class="sxs-lookup"><span data-stu-id="49265-112">If your component is used in a COM+ application that does not use role-based security, programmatic role checking and security call context information are not available.</span></span> <span data-ttu-id="49265-113">Однако можно использовать программные функции безопасности, предоставляемые COM.</span><span class="sxs-lookup"><span data-stu-id="49265-113">However, you can use the programmatic security functionality provided by COM.</span></span> <span data-ttu-id="49265-114">Дополнительные сведения см. [в разделе Безопасность в com](/windows/desktop/com/security-in-com).</span><span class="sxs-lookup"><span data-stu-id="49265-114">For more information, see [Security in COM](/windows/desktop/com/security-in-com).</span></span>

<span data-ttu-id="49265-115">Хотя большинство функций безопасности, предоставляемых COM, можно использовать, вы не можете вызывать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) из компонента, который является частью приложения COM+, так как **CoInitializeSecurity** вызывается суррогатом, в котором выполняется приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="49265-115">Although you can use most of the security functionality provided by COM, you cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) from a component that is part of a COM+ application because **CoInitializeSecurity** is called by the surrogate that the COM+ application runs in.</span></span> <span data-ttu-id="49265-116">Однако можно вызывать другие функции безопасности, такие как [**кокуериклиентбланкет**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), которые извлекают сведения о клиенте.</span><span class="sxs-lookup"><span data-stu-id="49265-116">However, you can call other security functions, such as [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), which retrieves information about the client.</span></span>

<span data-ttu-id="49265-117">В частности, если необходимо использовать удостоверение клиента для доступа к некоторым ресурсам (например, доступ к файлу, защищенному дескриптором безопасности, или распространение удостоверения клиента через базу данных), можно выполнить олицетворение программным способом.</span><span class="sxs-lookup"><span data-stu-id="49265-117">In particular, when you need to use the client's identity to access some resource—for example, accessing a file protected by a security descriptor, or propagating the client's identity through to a database—you can perform impersonation programmatically.</span></span> <span data-ttu-id="49265-118">Дополнительные сведения о том, когда и как это сделать, см. в разделе [олицетворение и делегирование клиента](client-impersonation-and-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="49265-118">For more detail about when and how to do this, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="testing-security-functionality"></a><span data-ttu-id="49265-119">Тестирование функций безопасности</span><span class="sxs-lookup"><span data-stu-id="49265-119">Testing Security Functionality</span></span>

<span data-ttu-id="49265-120">Если в компоненте используется программная безопасность COM+, необходимо интегрировать компонент в приложение COM+, когда будете готовы к тестированию функций безопасности компонента.</span><span class="sxs-lookup"><span data-stu-id="49265-120">If you use COM+ programmatic security in your component, you must integrate the component into a COM+ application when you are ready to test the component's security functionality.</span></span> <span data-ttu-id="49265-121">Если компонент, использующий программную безопасность COM+, запускается без интеграции в приложение COM+, будут созданы исключения.</span><span class="sxs-lookup"><span data-stu-id="49265-121">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="49265-122">Таким образом, если вы хотите убедиться, что такой компонент также может быть успешно интегрирован в приложение, которое не является частью среды COM+, необходимо убедиться, что эти исключения обрабатываются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="49265-122">Therefore, if you want to ensure that such a component is also capable of being successfully integrated into an application that is not part of the COM+ environment, you must ensure that these exceptions are handled appropriately.</span></span>

## <a name="documenting-security-requirements"></a><span data-ttu-id="49265-123">Документирование требований к безопасности</span><span class="sxs-lookup"><span data-stu-id="49265-123">Documenting Security Requirements</span></span>

<span data-ttu-id="49265-124">При написании отдельного компонента для приложений COM+, использующих безопасность на основе ролей, необходимо документировать компонент, чтобы обеспечить безопасность при интеграции компонента в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="49265-124">If you are writing a stand-alone component for COM+ applications that use role-based security, you need to document the component so that security can be configured appropriately when the component is integrated into a COM+ application.</span></span> <span data-ttu-id="49265-125">Например, необходимо указать роли, которые необходимо добавить, и объяснить, какие методы и интерфейсы должны быть назначены каждой роли.</span><span class="sxs-lookup"><span data-stu-id="49265-125">For example, you should identify the roles that must be added and explain which methods and interfaces each role should be assigned to.</span></span> <span data-ttu-id="49265-126">Кроме того, если вызывается метод, например Искаллеринроле ("говорят"), следует описать функциональные возможности, к которым имеют доступ только средства доступа.</span><span class="sxs-lookup"><span data-stu-id="49265-126">In addition, if a method such as IsCallerInRole("Teller") is called, you should describe the functionality that only Tellers have access to.</span></span> <span data-ttu-id="49265-127">Кроме того, необходимо указать, нужна ли роль для защиты доступа ко всему компоненту.</span><span class="sxs-lookup"><span data-stu-id="49265-127">You should also specify whether a role is required to help protect access to the entire component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49265-128">См. также</span><span class="sxs-lookup"><span data-stu-id="49265-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49265-129">Аутентификация клиента</span><span class="sxs-lookup"><span data-stu-id="49265-129">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="49265-130">Олицетворение и делегирование клиента</span><span class="sxs-lookup"><span data-stu-id="49265-130">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="49265-131">Безопасность библиотечных приложений</span><span class="sxs-lookup"><span data-stu-id="49265-131">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="49265-132">Многоуровневая защита приложений</span><span class="sxs-lookup"><span data-stu-id="49265-132">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="49265-133">Администрирование безопасности на основе ролей</span><span class="sxs-lookup"><span data-stu-id="49265-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="49265-134">Использование политики ограниченного использования программ в COM+</span><span class="sxs-lookup"><span data-stu-id="49265-134">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
