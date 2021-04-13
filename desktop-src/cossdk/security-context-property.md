---
description: Свойство контекста безопасности
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Свойство контекста безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262758"
---
# <a name="security-context-property"></a><span data-ttu-id="b2882-103">Свойство контекста безопасности</span><span class="sxs-lookup"><span data-stu-id="b2882-103">Security Context Property</span></span>

<span data-ttu-id="b2882-104">Как и при каждой автоматической службе, предоставляемой COM+, автоматическая проверка ролей основана на свойствах, включенных в контекст объекта.</span><span class="sxs-lookup"><span data-stu-id="b2882-104">As with every automatic service provided by COM+, automatic role checking is based on properties included on the object context.</span></span> <span data-ttu-id="b2882-105">Определение того, должна ли проверка безопасности выполняться при вызове компонента, зависит от свойства безопасности контекста объекта, созданного при создании экземпляра настроенного компонента.</span><span class="sxs-lookup"><span data-stu-id="b2882-105">The determination of whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span>

<span data-ttu-id="b2882-106">Обычно нет необходимости беспокоиться о данном свойстве. Он используется непосредственно COM+, а не для вас.</span><span class="sxs-lookup"><span data-stu-id="b2882-106">You generally don't need to be concerned with this property; it is used directly by COM+, not you.</span></span> <span data-ttu-id="b2882-107">Однако в некоторых случаях может потребоваться обеспечить более полный контроль над активацией объекта.</span><span class="sxs-lookup"><span data-stu-id="b2882-107">However, in some circumstances, you might want strict control over the activation of an object.</span></span> <span data-ttu-id="b2882-108">В этом случае свойство безопасности может повлиять на контекст, в котором активируется объект.</span><span class="sxs-lookup"><span data-stu-id="b2882-108">In this case, the security property can affect which context your object is activated in.</span></span> <span data-ttu-id="b2882-109">То есть, если объект имеет конфигурацию, несовместимую с контекстом его создателя, он будет активирован в собственном контексте.</span><span class="sxs-lookup"><span data-stu-id="b2882-109">That is, if an object has a configuration incompatible with the context of its creator, it will be activated in its own context.</span></span> <span data-ttu-id="b2882-110">Свойство безопасности может влиять на это, как и любое свойство в контексте объекта.</span><span class="sxs-lookup"><span data-stu-id="b2882-110">The security property can influence this, as can any property on the object context.</span></span>

<span data-ttu-id="b2882-111">Если вы не хотите, чтобы параметры безопасности влияли на активацию, можно выбрать только проверку доступа на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="b2882-111">If you don't want security settings to influence activation, you can choose process-level access checking only.</span></span> <span data-ttu-id="b2882-112">Это подавляет свойство безопасности в контексте объекта, хотя он фактически отключает проверку на основе ролей и делает [сведения о контексте вызова безопасности](security-call-context-information.md) недоступными.</span><span class="sxs-lookup"><span data-stu-id="b2882-112">This suppresses the security property on the object context, although it effectively disables role-based checking and makes [security call context information](security-call-context-information.md) unavailable.</span></span>

<span data-ttu-id="b2882-113">Дополнительные сведения о проверках доступа на уровне процесса см. в разделе [границы безопасности](security-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="b2882-113">For more information about process-level access checks, see [Security Boundaries](security-boundaries.md).</span></span> <span data-ttu-id="b2882-114">Сведения о настройке безопасности на уровне процесса см. в разделе [Настройка уровня безопасности для проверок доступа](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="b2882-114">To see how to set process-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="b2882-115">Дополнительные сведения о контексте объектов [см. в разделе контексты](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="b2882-115">For more information about object context, see [Contexts](com--contexts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2882-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b2882-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2882-117">Эффективное проектирование ролей</span><span class="sxs-lookup"><span data-stu-id="b2882-117">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="b2882-118">Границы безопасности</span><span class="sxs-lookup"><span data-stu-id="b2882-118">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="b2882-119">Сведения о контексте вызова безопасности</span><span class="sxs-lookup"><span data-stu-id="b2882-119">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="b2882-120">Использование ролей для авторизации клиентов</span><span class="sxs-lookup"><span data-stu-id="b2882-120">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



