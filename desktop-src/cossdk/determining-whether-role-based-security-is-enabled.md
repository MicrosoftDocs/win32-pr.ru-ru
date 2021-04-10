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
# <a name="determining-whether-role-based-security-is-enabled"></a>Определение того, включена ли безопасность Role-Based

С помощью метода [**исекуритикаллконтекст:: иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) , доступного в объекте контекста вызова безопасности, можно определить, включена ли безопасность для текущего объекта. Необходимо вызвать **иссекуритенаблед** перед использованием исекуритикаллконтекст::[**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) для проверки членства в роли, так как **искаллеринроле** возвращает значение true, если безопасность не включена.

Разработчики Microsoft Visual Basic вызывают [**жетсекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) , чтобы получить ссылку на объект [**секуритикаллконтекст**](securitycallcontext.md) , а затем вызвать [**иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), как показано в следующем примере:


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



Microsoft Visual C++ разработчики могут вызвать метод [**исекуритикаллконтекст:: иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) , вызвав [**кожеткаллконтекст**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) , чтобы получить указатель на [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) и затем вызвать **иссекуритенаблед**. Ниже приведен краткий пример.


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



Хотя предпочтительным способом вызова [**иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) является использование объекта контекста безопасности вызова, можно также вызвать **иссекуритенаблед** через контекст объекта. (Дополнительные сведения см. в разделе [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) или [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Доступ к сведениям о контексте вызова безопасности](accessing-security-call-context-information.md)
</dt> <dt>

[Проверка членства в роли](checking-role-membership.md)
</dt> <dt>

[Безопасность программных компонентов](programmatic-component-security.md)
</dt> </dl>

 

 
