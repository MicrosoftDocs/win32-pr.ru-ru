---
description: Определение того, включена ли безопасность Role-Based
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Определение того, включена ли безопасность Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142604"
---
# <a name="determining-whether-role-based-security-is-enabled"></a><span data-ttu-id="26ffc-103">Определение того, включена ли безопасность Role-Based</span><span class="sxs-lookup"><span data-stu-id="26ffc-103">Determining Whether Role-Based Security Is Enabled</span></span>

<span data-ttu-id="26ffc-104">С помощью метода [**исекуритикаллконтекст:: иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) , доступного в объекте контекста вызова безопасности, можно определить, включена ли безопасность для текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="26ffc-104">By using the [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) method available from the security call context object, you can determine whether security is enabled for the current object.</span></span> <span data-ttu-id="26ffc-105">Необходимо вызвать **иссекуритенаблед** перед использованием исекуритикаллконтекст::[**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) для проверки членства в роли, так как **искаллеринроле** возвращает значение true, если безопасность не включена.</span><span class="sxs-lookup"><span data-stu-id="26ffc-105">You should call **IsSecurityEnabled** before you use ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to check role membership because **IsCallerInRole** returns True if security is not enabled.</span></span>

<span data-ttu-id="26ffc-106">Разработчики Microsoft Visual Basic вызывают [**жетсекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) , чтобы получить ссылку на объект [**секуритикаллконтекст**](securitycallcontext.md) , а затем вызвать [**иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="26ffc-106">Microsoft Visual Basic developers call [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) to obtain a reference to a [**SecurityCallContext**](securitycallcontext.md) object and then call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), as shown in the following example:</span></span>


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



<span data-ttu-id="26ffc-107">Microsoft Visual C++ разработчики могут вызвать метод [**исекуритикаллконтекст:: иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) , вызвав [**кожеткаллконтекст**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) , чтобы получить указатель на [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) и затем вызвать **иссекуритенаблед**.</span><span class="sxs-lookup"><span data-stu-id="26ffc-107">Microsoft Visual C++ developers can call [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) and then calling **IsSecurityEnabled**.</span></span> <span data-ttu-id="26ffc-108">Ниже приведен краткий пример.</span><span class="sxs-lookup"><span data-stu-id="26ffc-108">A brief example follows:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsEnabled;

HRESULT hr1 = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr1)) throw(hr1);
if (NULL == pSecCtx) {
    // Display error message.
    return E_FAIL;
}

HRESULT hr2 = pSecCtx->IsSecurityEnabled(&bIsEnabled);
return hr2;
```



<span data-ttu-id="26ffc-109">Хотя предпочтительным способом вызова [**иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) является использование объекта контекста безопасности вызова, можно также вызвать **иссекуритенаблед** через контекст объекта.</span><span class="sxs-lookup"><span data-stu-id="26ffc-109">Although the preferred way to call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) is by using the security call context object, you can also call **IsSecurityEnabled** through the object context.</span></span> <span data-ttu-id="26ffc-110">(Дополнительные сведения см. в разделе [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) или [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)</span><span class="sxs-lookup"><span data-stu-id="26ffc-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="26ffc-111">См. также</span><span class="sxs-lookup"><span data-stu-id="26ffc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ffc-112">Доступ к сведениям о контексте вызова безопасности</span><span class="sxs-lookup"><span data-stu-id="26ffc-112">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="26ffc-113">Проверка членства в роли</span><span class="sxs-lookup"><span data-stu-id="26ffc-113">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="26ffc-114">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="26ffc-114">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
