---
description: Операция — это действие низкого уровня компьютера.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Операции и задачи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663826"
---
# <a name="operations-and-tasks"></a><span data-ttu-id="506ad-103">Операции и задачи</span><span class="sxs-lookup"><span data-stu-id="506ad-103">Operations and Tasks</span></span>

<span data-ttu-id="506ad-104">Операция — это действие низкого уровня компьютера.</span><span class="sxs-lookup"><span data-stu-id="506ad-104">An operation is a low-level computer action.</span></span> <span data-ttu-id="506ad-105">В API диспетчера авторизации операция представлена объектом [**иазоператион**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="506ad-105">In the Authorization Manager API, an operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="506ad-106">Как правило, операции слишком много в количестве и слишком низком уровне для упрощения администрирования.</span><span class="sxs-lookup"><span data-stu-id="506ad-106">In general, operations are too many in number and too low-level to facilitate administration.</span></span> <span data-ttu-id="506ad-107">Сгруппируйте операции в задачи, чтобы упростить администрирование политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="506ad-107">Group operations into tasks to simplify administration of authorization policy.</span></span>

<span data-ttu-id="506ad-108">Задача представлена объектом [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) и может содержать один или несколько объектов [**иазоператион**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="506ad-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object and can contain one or more [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) objects.</span></span> <span data-ttu-id="506ad-109">Объект **иазтаск** также может содержать другие объекты **иазтаск** , чтобы задачи могли быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="506ad-109">An **IAzTask** object can also contain other **IAzTask** objects, so that tasks can be nested.</span></span> <span data-ttu-id="506ad-110">Чтобы упростить администрирование, объект **иазтаск** должен представлять задачу, которую необходимо выполнить реальному пользователю.</span><span class="sxs-lookup"><span data-stu-id="506ad-110">To facilitate administration, an **IAzTask** object should represent a task that a real user wants to perform.</span></span>

<span data-ttu-id="506ad-111">Доступ к операциям, содержащимся в задаче, можно уточнить во время выполнения с помощью сценария бизнес-правила, связанного с объектом [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) , который представляет эту задачу.</span><span class="sxs-lookup"><span data-stu-id="506ad-111">Access to the operations contained by a task can be qualified at run time by a business rule script associated with the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents that task.</span></span> <span data-ttu-id="506ad-112">Дополнительные сведения о сценариях бизнес-правил см. в разделе [бизнес-правила](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="506ad-112">For more information about business rule scripts, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="506ad-113">Объект [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) также может представлять определение роли, присвоив свойству [**исроледефинитион**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) **значение true**.</span><span class="sxs-lookup"><span data-stu-id="506ad-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can also represent a role definition by setting its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property to **TRUE**.</span></span> <span data-ttu-id="506ad-114">Затем пользовательский интерфейс оснастки MMC **диспетчера авторизации** отображает этот объект **иазтаск** в качестве роли.</span><span class="sxs-lookup"><span data-stu-id="506ad-114">The **Authorization Manager** MMC snap-in user interface then displays that **IAzTask** object as a role.</span></span> <span data-ttu-id="506ad-115">Дополнительные сведения об определениях ролей см. в разделе [roles](roles.md).</span><span class="sxs-lookup"><span data-stu-id="506ad-115">For more information about role definitions, see [Roles](roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="506ad-116">См. также</span><span class="sxs-lookup"><span data-stu-id="506ad-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="506ad-117">Определение операций в C++</span><span class="sxs-lookup"><span data-stu-id="506ad-117">Defining Operations in C++</span></span>](defining-operations-in-c--.md)
</dt> <dt>

[<span data-ttu-id="506ad-118">Группирование операций в задачи на C++</span><span class="sxs-lookup"><span data-stu-id="506ad-118">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[<span data-ttu-id="506ad-119">Группирование задач в роли в C++</span><span class="sxs-lookup"><span data-stu-id="506ad-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="506ad-120">Пользователи и группы</span><span class="sxs-lookup"><span data-stu-id="506ad-120">Users and Groups</span></span>](users-and-groups.md)
</dt> </dl>

 

 



