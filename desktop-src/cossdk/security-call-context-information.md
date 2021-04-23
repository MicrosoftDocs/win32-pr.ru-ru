---
description: Сведения о контексте вызова безопасности
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Сведения о контексте вызова безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262760"
---
# <a name="security-call-context-information"></a><span data-ttu-id="d7805-103">Сведения о контексте вызова безопасности</span><span class="sxs-lookup"><span data-stu-id="d7805-103">Security Call Context Information</span></span>

<span data-ttu-id="d7805-104">Безопасность на основе ролей основана на общем механизме, который позволяет получать сведения о безопасности для всех вышестоящего вызывающего объекта в цепочке вызовов компонента.</span><span class="sxs-lookup"><span data-stu-id="d7805-104">Role-based security is built on a general mechanism that enables you to retrieve security information regarding all upstream callers in the chain of calls to your component.</span></span> <span data-ttu-id="d7805-105">Эта информация доступна только в том случае, если включена проверка роли на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="d7805-105">This information is available only when you have component-level role checking enabled.</span></span> <span data-ttu-id="d7805-106">Дополнительные сведения о настройке безопасности на уровне компонентов см. в разделе [Настройка уровня безопасности для проверок доступа](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="d7805-106">For details about how to set component-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="d7805-107">Интерфейс [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) можно использовать для доступа к сведениям о контексте вызова безопасности программным способом.</span><span class="sxs-lookup"><span data-stu-id="d7805-107">You can use the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface to access security call context information programmatically.</span></span> <span data-ttu-id="d7805-108">Описание см. в разделе [Программная безопасность компонентов](programmatic-component-security.md).</span><span class="sxs-lookup"><span data-stu-id="d7805-108">For a description, see [Programmatic Component Security](programmatic-component-security.md).</span></span>

<span data-ttu-id="d7805-109">Контекст вызова безопасности передается при каждом пересечении границы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d7805-109">Security call context is passed along every time a security boundary is crossed.</span></span> <span data-ttu-id="d7805-110">Для вызовов между компонентами в приложении, которые находятся в пределах одной и той же границы безопасности, сведения о контексте вызова не передаются.</span><span class="sxs-lookup"><span data-stu-id="d7805-110">For calls between components within an application, which reside within the same security boundary, no call context information is passed.</span></span> <span data-ttu-id="d7805-111">Для вызовов между процессами или между приложениями внутри процесса вызывайте контекстные информационные потоки.</span><span class="sxs-lookup"><span data-stu-id="d7805-111">For calls between processes or between applications within a process, call context information flows along.</span></span>

<span data-ttu-id="d7805-112">Это особенно полезно, если вы хотите выполнить подробный аудит и ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="d7805-112">This facility is particularly useful if you wish to do detailed auditing and logging.</span></span> <span data-ttu-id="d7805-113">Вы можете получать и записывать сведения о безопасности для каждого вышестоящего абонента.</span><span class="sxs-lookup"><span data-stu-id="d7805-113">You can retrieve and record security information for every upstream caller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7805-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d7805-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7805-115">Эффективное проектирование ролей</span><span class="sxs-lookup"><span data-stu-id="d7805-115">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="d7805-116">Границы безопасности</span><span class="sxs-lookup"><span data-stu-id="d7805-116">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="d7805-117">Свойство контекста безопасности</span><span class="sxs-lookup"><span data-stu-id="d7805-117">Security Context Property</span></span>](security-context-property.md)
</dt> <dt>

[<span data-ttu-id="d7805-118">Использование ролей для авторизации клиентов</span><span class="sxs-lookup"><span data-stu-id="d7805-118">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



