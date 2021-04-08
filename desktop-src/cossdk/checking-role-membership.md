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
# <a name="checking-role-membership"></a>Проверка членства в роли

Можно вызвать метод [**исекуритикаллконтекст:: искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) , чтобы определить, является ли прямой вызывающий объект объекта членом определенной роли. Эта функция полезна, если нужно убедиться, что определенный блок кода не выполняется, если вызывающий объект не является членом определенной роли.

Например, можно использовать [**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) , чтобы гарантировать, что транзакции за указанный объем, например $1000, будут выполняться только членами роли менеджеров. Если вызывающий объект не является диспетчером и транзакция превышает $1000, транзакция не выполняется и выводится сообщение об ошибке.

Предпочтительный способ доступа к [**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) — через объект контекста безопасности вызова, так как для получения свойств безопасности можно использовать одну и ту же ссылку на объект контекста вызова безопасности. Однако можно также получить доступ к методу **искаллеринроле** из объекта **ObjectContext** . (Дополнительные сведения см. в разделе [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) или [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .)

При разработке компонентов для приложения Microsoft Visual Basic вызывается функция [**жетсекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) , а затем используется контекст вызова безопасности для вызова [**искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), как показано в следующем примере:


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



При разработке приложения C или C++ используйте [**кожеткаллконтекст**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) для получения указателя на интерфейс [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) . Затем вызывается метод [**исекуритикаллконтекст:: искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), как показано в следующем примере:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Доступ к сведениям о контексте вызова безопасности](accessing-security-call-context-information.md)
</dt> <dt>

[Определение того, включена ли безопасность Role-Based](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Безопасность программных компонентов](programmatic-component-security.md)
</dt> </dl>

 

 
