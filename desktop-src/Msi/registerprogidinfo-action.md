---
description: Действие Регистерпрогидинфо управляет регистрацией данных OLE ProgId в системе.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Действие Регистерпрогидинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650780"
---
# <a name="registerprogidinfo-action"></a><span data-ttu-id="a14af-103">Действие Регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-103">RegisterProgIdInfo Action</span></span>

<span data-ttu-id="a14af-104">Действие Регистерпрогидинфо управляет регистрацией данных OLE ProgId в системе.</span><span class="sxs-lookup"><span data-stu-id="a14af-104">The RegisterProgIdInfo action manages the registration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a14af-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="a14af-105">Sequence Restrictions</span></span>

<span data-ttu-id="a14af-106">Действие Регистерпрогидинфо должно быть получено после действия [инсталлфилес](installfiles-action.md) , действия [Унрегистерпрогидинфо](unregisterprogidinfo-action.md) , действия [регистерклассинфо](registerclassinfo-action.md) и действия [регистерекстенсионинфо](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a14af-106">The RegisterProgIdInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterProgIdInfo](unregisterprogidinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="a14af-107">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="a14af-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="a14af-108">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a14af-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="a14af-109">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="a14af-110">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="a14af-111">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="a14af-112">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="a14af-113">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="a14af-114">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   <span data-ttu-id="a14af-115">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-115">RegisterProgIdInfo</span></span>
-   [<span data-ttu-id="a14af-116">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="a14af-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="a14af-117">Например, Регистерпрогидинфо должен следовать после [регистерекстенсионинфо](registerextensioninfo-action.md) в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="a14af-117">For example, RegisterProgIdInfo must come after [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a14af-118">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="a14af-118">ActionData Messages</span></span>



| <span data-ttu-id="a14af-119">Поле</span><span class="sxs-lookup"><span data-stu-id="a14af-119">Field</span></span> | <span data-ttu-id="a14af-120">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="a14af-120">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="a14af-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a14af-121">\[1\]</span></span> | <span data-ttu-id="a14af-122">Идентификатор программы зарегистрированной программы.</span><span class="sxs-lookup"><span data-stu-id="a14af-122">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a14af-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a14af-123">Remarks</span></span>

<span data-ttu-id="a14af-124">Действие Регистерпрогидинфо регистрирует все сведения ProgId для серверов, указанных в [таблице ProgID](progid-table.md) , для которых был выбран соответствующий сервер классов или сервер расширений.</span><span class="sxs-lookup"><span data-stu-id="a14af-124">The RegisterProgIdInfo action registers all ProgId information for servers that are specified in the [ProgId table](progid-table.md) and for which the corresponding class server or extension server has been selected to be installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a14af-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a14af-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a14af-126">Таблица классов</span><span class="sxs-lookup"><span data-stu-id="a14af-126">Class table</span></span>](class-table.md)
</dt> <dt>

[<span data-ttu-id="a14af-127">Таблица расширения</span><span class="sxs-lookup"><span data-stu-id="a14af-127">Extension table</span></span>](extension-table.md)
</dt> </dl>

 

 



