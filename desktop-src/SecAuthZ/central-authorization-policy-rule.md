---
description: Правило централизованной политики авторизации (КАПР) предоставляет определение изолированного аспекта политики авторизации организаций на уровне домена.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Правило централизованной политики авторизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081638"
---
# <a name="central-authorization-policy-rule"></a><span data-ttu-id="9d831-103">Правило централизованной политики авторизации</span><span class="sxs-lookup"><span data-stu-id="9d831-103">Central Authorization Policy Rule</span></span>

<span data-ttu-id="9d831-104">Правило централизованной политики авторизации (КАПР) предоставляет определение изолированного аспекта политики авторизации Организации на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="9d831-104">The purpose of the Central Authorization Policy Rule (CAPR) is to provide a domain-wide definition of an isolated aspect of the organization's authorization policy.</span></span> <span data-ttu-id="9d831-105">Администратор определяет КАПР для применения одного из конкретных требований к авторизации.</span><span class="sxs-lookup"><span data-stu-id="9d831-105">The administrator defines the CAPR to enforce one of the specific authorization requirements.</span></span> <span data-ttu-id="9d831-106">Поскольку КАПР определяет только одно необходимое требование политики авторизации, оно может быть более просто определено и понятнее, чем если бы все требования к политике авторизации в Организации были скомпилированы в одно определение политики.</span><span class="sxs-lookup"><span data-stu-id="9d831-106">Since the CAPR defines only one specific desired requirement of the authorization policy it can be more simply defined and understood than if all the authorization policy requirements of the organization are compiled into a single policy definition.</span></span>

<span data-ttu-id="9d831-107">КАПР имеет следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="9d831-107">The CAPR has the following attributes:</span></span>

-   <span data-ttu-id="9d831-108">Имя — определяет КАПР для администраторов.</span><span class="sxs-lookup"><span data-stu-id="9d831-108">Name – identifies the CAPR to the administrators.</span></span>
-   <span data-ttu-id="9d831-109">Описание — определяет назначение КАПР и любые сведения, которые могут потребоваться потребителям КАПР.</span><span class="sxs-lookup"><span data-stu-id="9d831-109">Description – defines the purpose of the CAPR and any information that may be needed by consumers of the CAPR.</span></span>
-   <span data-ttu-id="9d831-110">Выражение применимости — определяет ресурсы или ситуации, в которых будет применяться политика.</span><span class="sxs-lookup"><span data-stu-id="9d831-110">Applicability Expression – defines the resources or situations in which the policy will be applied.</span></span>
-   <span data-ttu-id="9d831-111">ID — идентификатор, используемый при аудите изменений в КАПР.</span><span class="sxs-lookup"><span data-stu-id="9d831-111">ID – identifier for use in auditing of changes to the CAPR.</span></span>
-   <span data-ttu-id="9d831-112">Эффективная политика контроля доступа — дескриптор безопасности Windows, содержащий список DACL, который определяет действующую политику авторизации.</span><span class="sxs-lookup"><span data-stu-id="9d831-112">Effective Access Control Policy – a Windows security descriptor containing a DACL that defines the effective authorization policy.</span></span>
-   <span data-ttu-id="9d831-113">Выражение исключения — одно или несколько выражений, которые предоставляют средства для переопределения политики и предоставления доступа к участнику в соответствии с вычислением выражения.</span><span class="sxs-lookup"><span data-stu-id="9d831-113">Exception Expression – one or more expressions that provide a means to override the policy and grant access to a principal according to the evaluation of the expression.</span></span>
-   <span data-ttu-id="9d831-114">Промежуточная политика — дополнительный дескриптор безопасности Windows, содержащий список DACL, который определяет предлагаемую политику авторизации (список записей контроля доступа), которые будут проверены на соответствие действующей политике, но не применяются.</span><span class="sxs-lookup"><span data-stu-id="9d831-114">Staging Policy – an optional Windows security descriptor containing a DACL that defines a proposed authorization policy (list of access control entries) that will be tested against the effective policy but not enforced.</span></span> <span data-ttu-id="9d831-115">Если существует разница между результатами действующей политики и промежуточной политикой, разница будет записана в журнал событий аудита.</span><span class="sxs-lookup"><span data-stu-id="9d831-115">If there is a difference between the results of the effective policy and the staging policy the difference will be recorded in the audit event log.</span></span>
    -   <span data-ttu-id="9d831-116">Поскольку промежуточное развертывание может привести к непредсказуемому снижению производительности системы, администратор групповая политика должен иметь возможность выбора конкретных компьютеров, на которых будет действовать промежуточное хранение.</span><span class="sxs-lookup"><span data-stu-id="9d831-116">Since staging can have an unpredictable effect on system performance, a Group Policy administrator must be able to select specific machines on which staging will be in effect.</span></span> <span data-ttu-id="9d831-117">Это позволяет использовать существующую политику на большинстве компьютеров в подразделении, в то время как промежуточное хранение происходит на подмножестве компьютеров.</span><span class="sxs-lookup"><span data-stu-id="9d831-117">This allows the existing policy to be in place on most machines in an OU while staging is happening on a subset of the machines.</span></span>
    -   <span data-ttu-id="9d831-118">P2 — локальный администратор на определенном компьютере должен иметь возможность отключить промежуточное хранение, если промежуточное хранение на этом компьютере вызывает слишком большую часть снижения производительности.</span><span class="sxs-lookup"><span data-stu-id="9d831-118">P2 – A local administrator on a particular machine should be able to disable staging if staging on that machine is causing too much of a performance degradation.</span></span>
-   <span data-ttu-id="9d831-119">Посмотрите to CAP — список ссылок на любые прописные, которые могут ссылаться на этот КАПР.</span><span class="sxs-lookup"><span data-stu-id="9d831-119">Backlink to CAP – A list of backlinks to any CAPs that may be referring to this CAPR.</span></span>

<span data-ttu-id="9d831-120">Во время проверки доступа КАПР оценивается на предмет применимости на основе выражения применимости.</span><span class="sxs-lookup"><span data-stu-id="9d831-120">During access check, the CAPR is be evaluated for applicability based on the applicability expression.</span></span> <span data-ttu-id="9d831-121">Если КАПР применимо, он вычисляется, чтобы предоставить запрашивающему пользователю запрошенный доступ к идентифицированному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9d831-121">If a CAPR is applicable, it is evaluated for whether it provides the requesting user the requested access to the identified resource.</span></span> <span data-ttu-id="9d831-122">Результаты оценки зеленого значения затем объединяются в **и** с результатами списка DACL для ресурса и любыми остальными капрс, действующими на ресурс.</span><span class="sxs-lookup"><span data-stu-id="9d831-122">The results of the CAPE evaluation is then logically joined by **AND** with the results of the DACL on the resource and any other applicable CAPRs in effect on the resource.</span></span>

<span data-ttu-id="9d831-123">Пример Капрс:</span><span class="sxs-lookup"><span data-stu-id="9d831-123">Example CAPRs:</span></span>

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a><span data-ttu-id="9d831-124">Запретить ACE в Капес</span><span class="sxs-lookup"><span data-stu-id="9d831-124">Deny ACEs in CAPEs</span></span>

<span data-ttu-id="9d831-125">В Windows 8 ACE Deny не будет поддерживаться в КАПР.</span><span class="sxs-lookup"><span data-stu-id="9d831-125">In Windows 8 deny ACEs will not be supported in a CAPR.</span></span> <span data-ttu-id="9d831-126">РАЗРАБОТЧИК КАПР не разрешит Создание запрещающего ACE.</span><span class="sxs-lookup"><span data-stu-id="9d831-126">The CAPR authoring UX will not allow creation of a deny ACE.</span></span> <span data-ttu-id="9d831-127">Кроме того, когда LSA получает ограничение от Active Directory, LSA проверяет, что ни одна из Капрс не имеет запрещенных ACE.</span><span class="sxs-lookup"><span data-stu-id="9d831-127">Additionally, when the LSA retrieves the CAP from Active Directory, LSA will verify that no CAPRs have deny ACEs.</span></span> <span data-ttu-id="9d831-128">Если в КАПР найден запрещенный ACE, то ограничение будет рассматриваться как недопустимое и не должно быть скопировано в реестр или СРМ.</span><span class="sxs-lookup"><span data-stu-id="9d831-128">If a deny ACE is found in a CAPR then the CAP will be treated as invalid and not be copied to the registry or SRM.</span></span>

> [!Note]  
> <span data-ttu-id="9d831-129">Проверка доступа не будет требовать наличия запрещенных ACE.</span><span class="sxs-lookup"><span data-stu-id="9d831-129">The access check will not enforce that no deny ACEs are present.</span></span> <span data-ttu-id="9d831-130">Будут применены Deny ACE в КАПР.</span><span class="sxs-lookup"><span data-stu-id="9d831-130">Deny ACEs in a CAPR will be applied.</span></span> <span data-ttu-id="9d831-131">Предполагается, что средства разработки не препятствуют этому.</span><span class="sxs-lookup"><span data-stu-id="9d831-131">It is expected that authoring tools will prevent this from happening.</span></span>

 

## <a name="cape-definition"></a><span data-ttu-id="9d831-132">Определение зеленого</span><span class="sxs-lookup"><span data-stu-id="9d831-132">CAPE Definition</span></span>

<span data-ttu-id="9d831-133">Капрс создаются в том случае, если в центр администрирования Active Directory (ADAC) создается новый интерфейс. В ADAC для создания КАПР предоставляется новый параметр задачи.</span><span class="sxs-lookup"><span data-stu-id="9d831-133">CAPRs are created though a new UX provided in Active Directory Administrative Center (ADAC.) In ADAC a new task option is provided to create a CAPR.</span></span> <span data-ttu-id="9d831-134">При выборе этой задачи ADAC запрашивает у пользователя диалоговое окно с запросом имени КАПР и его описания.</span><span class="sxs-lookup"><span data-stu-id="9d831-134">When this task is selected, ADAC will prompt the user with a dialog asking the user for a CAPR name and a description.</span></span> <span data-ttu-id="9d831-135">Когда они предоставляются, элементы управления для определения любого из оставшихся элементов КАПР становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="9d831-135">When these are provided, the controls to define any of the remaining CAPR elements become enabled.</span></span> <span data-ttu-id="9d831-136">Для каждого из оставшихся элементов КАПР интерфейс пользователя будет обращаться к ACL-UI, чтобы разрешить определение выражений и/или списков ACL.</span><span class="sxs-lookup"><span data-stu-id="9d831-136">For each of the remaining CAPR elements, the UX will call out to the ACL-UI to allow definition of expression and/or ACLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d831-137">См. также</span><span class="sxs-lookup"><span data-stu-id="9d831-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d831-138">**AccessCheck**</span><span class="sxs-lookup"><span data-stu-id="9d831-138">**AccessCheck**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[<span data-ttu-id="9d831-139">Сценарий динамического управления доступом (DAC)</span><span class="sxs-lookup"><span data-stu-id="9d831-139">Dynamic Access Control (DAC) scenario</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
