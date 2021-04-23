---
description: Разработка для обеспечения безопасности
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Разработка для обеспечения безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710748"
---
# <a name="designing-for-security"></a><span data-ttu-id="09cd8-103">Разработка для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="09cd8-103">Designing for Security</span></span>

<span data-ttu-id="09cd8-104">Комплексная стратегия безопасности, очевидно, зависит от типа разрабатываемого распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="09cd8-104">Your end-to-end strategy for security obviously depends on the type of distributed application you are developing.</span></span> <span data-ttu-id="09cd8-105">Ниже приведено несколько советов по обеспечению безопасности в отношении логики приложения среднего уровня.</span><span class="sxs-lookup"><span data-stu-id="09cd8-105">Following are several suggestions for addressing security with respect to middle-tier application logic:</span></span>

-   <span data-ttu-id="09cd8-106">Для повышения эффективности и производительности Проверяйте подлинность как можно ближе к пользователю.</span><span class="sxs-lookup"><span data-stu-id="09cd8-106">For efficiency and performance, authenticate as close to the user as you can.</span></span> <span data-ttu-id="09cd8-107">Если приложение включает в себя архитектуру "Обозреватель — бизнес-логику", рассмотрите возможность сопоставления клиентов браузера с удостоверениями доменов, запуска приложения COM+ в соответствии с удостоверениями для каждого приложения и настройки таблиц на уровне данных, чтобы они были доступны только определенному удостоверению приложения.</span><span class="sxs-lookup"><span data-stu-id="09cd8-107">If your application involves a browser-to-business-logic-to-database architecture, consider mapping the browser clients to domain identities, run the COM+ application under identities specific to each application, and configure tables in the data tier to be accessible only by a particular application identity.</span></span> <span data-ttu-id="09cd8-108">Этот сценарий доверенного сервера является более масштабируемым и менее проблематичным, чем использование СУБД для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="09cd8-108">This trusted server scenario is more scalable and less problematic than using the DBMS for authenticating.</span></span>
-   <span data-ttu-id="09cd8-109">При проектировании компонента, который будет использоваться в распределенном приложении с использованием безопасности на основе ролей, можно использовать функции [безопасности COM+](com--security.md) .</span><span class="sxs-lookup"><span data-stu-id="09cd8-109">If you are designing a component that will be used in a distributed application using role-based security, you can use the [COM+ security](com--security.md) functionality.</span></span> <span data-ttu-id="09cd8-110">Эта функция позволяет вызывать методы, такие как [**иобжектконтекст:: искаллеринроле**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) и [**Иобжектконтекст:: иссекуритенаблед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) , для защиты блоков кода от несанкционированного доступа.</span><span class="sxs-lookup"><span data-stu-id="09cd8-110">This functionality allows you to call methods such as [**IObjectContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) and [**IObjectContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) to help protect blocks of code from unauthorized access.</span></span> <span data-ttu-id="09cd8-111">Можно также использовать контекст вызова безопасности для получения сведений о вызывающих объектах объекта.</span><span class="sxs-lookup"><span data-stu-id="09cd8-111">You can also use the security call context to get information about an object's callers.</span></span>
-   <span data-ttu-id="09cd8-112">При проектировании компонента, который будет использоваться в распределенном приложении без использования безопасности на основе ролей, безопасность будет автоматически проверяться только на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="09cd8-112">If you are designing a component that will be used in a distributed application without using role-based security, security is automatically checked only at the process level.</span></span> <span data-ttu-id="09cd8-113">Разрешения на доступ к процессу определяют, кому предоставляется доступ к приложению.</span><span class="sxs-lookup"><span data-stu-id="09cd8-113">Process access permissions determine who is given access to the application.</span></span> <span data-ttu-id="09cd8-114">Если требуется более детальный контроль над параметрами безопасности в процессе или на уровне интерфейса, используйте программные функции безопасности, предоставляемые COM.</span><span class="sxs-lookup"><span data-stu-id="09cd8-114">If you need finer grain control over security settings at the process or at the interface level, use the programmatic security functionality provided by COM.</span></span>
-   <span data-ttu-id="09cd8-115">Если компонент, использующий программную безопасность COM+, запускается без интеграции в приложение COM+, будут созданы исключения.</span><span class="sxs-lookup"><span data-stu-id="09cd8-115">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="09cd8-116">Поэтому, если необходимо, чтобы такой компонент был успешно интегрирован в приложение, которое не является частью среды COM+, необходимо обрабатывать все исключения соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="09cd8-116">Therefore, if you want such a component to be successfully integrated into an application that is not part of the COM+ environment, you must handle all exceptions appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09cd8-117">См. также</span><span class="sxs-lookup"><span data-stu-id="09cd8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09cd8-118">Проектирование для обеспечения доступности</span><span class="sxs-lookup"><span data-stu-id="09cd8-118">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="09cd8-119">Проектирование для развертывания</span><span class="sxs-lookup"><span data-stu-id="09cd8-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="09cd8-120">Проектирование для масштабируемости</span><span class="sxs-lookup"><span data-stu-id="09cd8-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="09cd8-121">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="09cd8-121">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 



