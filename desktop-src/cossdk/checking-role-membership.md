---
description: Проверка членства в роли
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: Проверка членства в роли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807654"
---
# <a name="checking-role-membership"></a><span data-ttu-id="20858-103">Проверка членства в роли</span><span class="sxs-lookup"><span data-stu-id="20858-103">Checking Role Membership</span></span>

<span data-ttu-id="20858-104">Можно вызвать метод [**исекуритикаллконтекст:: искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) , чтобы определить, является ли прямой вызывающий объект объекта членом определенной роли.</span><span class="sxs-lookup"><span data-stu-id="20858-104">You can call the [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) method to determine whether an object's direct caller is a member of a particular role.</span></span> <span data-ttu-id="20858-105">Эта функция полезна, если нужно убедиться, что определенный блок кода не выполняется, если вызывающий объект не является членом определенной роли.</span><span class="sxs-lookup"><span data-stu-id="20858-105">This functionality is useful when you want to ensure that a certain block of code is not executed unless the caller is a member of a particular role.</span></span>

<span data-ttu-id="20858-106">Например, можно использовать [**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) , чтобы гарантировать, что транзакции за указанный объем, например $1000, будут выполняться только членами роли менеджеров.</span><span class="sxs-lookup"><span data-stu-id="20858-106">For example, you could use [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to ensure that transactions over a specified amount, such as $1000, are performed only by members of a Managers role.</span></span> <span data-ttu-id="20858-107">Если вызывающий объект не является диспетчером и транзакция превышает $1000, транзакция не выполняется и выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="20858-107">If the caller is not a Manager and the transaction is over $1000, the transaction is not performed and an error message is displayed.</span></span>

<span data-ttu-id="20858-108">Предпочтительный способ доступа к [**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) — через объект контекста безопасности вызова, так как для получения свойств безопасности можно использовать одну и ту же ссылку на объект контекста вызова безопасности.</span><span class="sxs-lookup"><span data-stu-id="20858-108">The preferred way to access [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) is through the security call context object because you can use the same reference to the security call context object to obtain security properties.</span></span> <span data-ttu-id="20858-109">Однако можно также получить доступ к методу **искаллеринроле** из объекта **ObjectContext** .</span><span class="sxs-lookup"><span data-stu-id="20858-109">However, you can also access the **IsCallerInRole** method from the **ObjectContext** object.</span></span> <span data-ttu-id="20858-110">(Дополнительные сведения см. в разделе [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) или [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)</span><span class="sxs-lookup"><span data-stu-id="20858-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

<span data-ttu-id="20858-111">При разработке компонентов для приложения Microsoft Visual Basic вызывается функция [**жетсекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) , а затем используется контекст вызова безопасности для вызова [**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="20858-111">If you are developing components for a Microsoft Visual Basic application, you call the [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) function and then use the security call context to call [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



<span data-ttu-id="20858-112">При разработке приложения C или C++ используйте [**кожеткаллконтекст**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) для получения указателя на интерфейс [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) .</span><span class="sxs-lookup"><span data-stu-id="20858-112">If you are developing a C or C++ application, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to retrieve a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface.</span></span> <span data-ttu-id="20858-113">Затем вызывается метод [**исекуритикаллконтекст:: искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="20858-113">Then you call [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="20858-114">См. также</span><span class="sxs-lookup"><span data-stu-id="20858-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20858-115">Доступ к сведениям о контексте вызова безопасности</span><span class="sxs-lookup"><span data-stu-id="20858-115">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="20858-116">Определение того, включена ли безопасность Role-Based</span><span class="sxs-lookup"><span data-stu-id="20858-116">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="20858-117">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="20858-117">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
