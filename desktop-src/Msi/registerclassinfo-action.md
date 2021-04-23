---
description: Действие Регистерклассинфо управляет регистрацией сведений о классе COM в системе. В нем используется таблица AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Действие Регистерклассинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673668"
---
# <a name="registerclassinfo-action"></a><span data-ttu-id="d3acd-104">Действие Регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-104">RegisterClassInfo Action</span></span>

<span data-ttu-id="d3acd-105">Действие Регистерклассинфо управляет регистрацией сведений о классе COM в системе.</span><span class="sxs-lookup"><span data-stu-id="d3acd-105">The RegisterClassInfo action manages the registration of COM class information with the system.</span></span> <span data-ttu-id="d3acd-106">В нем используется [Таблица AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="d3acd-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d3acd-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d3acd-107">Sequence Restrictions</span></span>

<span data-ttu-id="d3acd-108">Действие Регистерклассинфо должно следовать после действия [инсталлфилес](installfiles-action.md) и действия [унрегистерклассинфо](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d3acd-108">The RegisterClassInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterClassInfo](unregisterclassinfo-action.md) action.</span></span>

<span data-ttu-id="d3acd-109">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="d3acd-109">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="d3acd-110">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d3acd-110">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="d3acd-111">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-111">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="d3acd-112">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-112">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="d3acd-113">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-113">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="d3acd-114">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-114">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   <span data-ttu-id="d3acd-115">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-115">RegisterClassInfo</span></span>
-   [<span data-ttu-id="d3acd-116">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-116">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="d3acd-117">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-117">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="d3acd-118">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="d3acd-118">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="d3acd-119">Например, Регистерклассинфо должен следовать после [унрегистермимеинфо](unregistermimeinfo-action.md) в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="d3acd-119">For example, RegisterClassInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d3acd-120">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d3acd-120">ActionData Messages</span></span>



| <span data-ttu-id="d3acd-121">Поле</span><span class="sxs-lookup"><span data-stu-id="d3acd-121">Field</span></span> | <span data-ttu-id="d3acd-122">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="d3acd-122">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="d3acd-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d3acd-123">\[1\]</span></span> | <span data-ttu-id="d3acd-124">Идентификатор класса GUID зарегистрированного сервера COM.</span><span class="sxs-lookup"><span data-stu-id="d3acd-124">GUID class identifier of the registered COM server.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d3acd-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3acd-125">Remarks</span></span>

<span data-ttu-id="d3acd-126">Если система поддерживает установку по запросу для серверов OLE, Регистерклассинфо регистрирует все COM-классы в [таблице классов](class-table.md) , связанной с выбранным для установки или объявленным компонентом.</span><span class="sxs-lookup"><span data-stu-id="d3acd-126">If the system supports install-on-demand for OLE servers, RegisterClassInfo registers all COM classes in the [Class table](class-table.md) associated with a feature selected to be installed or advertised.</span></span> <span data-ttu-id="d3acd-127">В противном случае это действие регистрирует только классы COM, связанные с компонентом, выбранным для установки.</span><span class="sxs-lookup"><span data-stu-id="d3acd-127">Otherwise this action only registers the COM classes associated with a feature selected for installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3acd-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d3acd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3acd-129">**Олеадвтсуппорт, свойство**</span><span class="sxs-lookup"><span data-stu-id="d3acd-129">**OLEAdvtSupport property**</span></span>](oleadvtsupport.md)
</dt> </dl>

 

 



