---
description: Действие Регистермимеинфо регистрирует сведения о реестре, связанные с MIME, с системой.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Действие Регистермимеинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813648"
---
# <a name="registermimeinfo-action"></a><span data-ttu-id="c066b-103">Действие Регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-103">RegisterMIMEInfo Action</span></span>

<span data-ttu-id="c066b-104">Действие Регистермимеинфо регистрирует сведения о реестре, связанные с MIME, с системой.</span><span class="sxs-lookup"><span data-stu-id="c066b-104">The RegisterMIMEInfo action registers MIME-related registry information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c066b-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="c066b-105">Sequence Restrictions</span></span>

<span data-ttu-id="c066b-106">Действие Регистермимеинфо должно быть получено после действия [инсталлфилес](installfiles-action.md) , действия [Унрегистермимеинфо](unregistermimeinfo-action.md) , действия [регистерклассинфо](registerclassinfo-action.md) и действия [регистерекстенсионинфо](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c066b-106">The RegisterMIMEInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterMIMEInfo](unregistermimeinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="c066b-107">Последовательность действий в следующей группе ограничена.</span><span class="sxs-lookup"><span data-stu-id="c066b-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="c066b-108">Если любое подмножество этих действий выполняется вместе в таблице последовательности, они должны иметь одинаковый относительный порядок последовательности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c066b-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="c066b-109">унрегистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="c066b-110">унрегистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="c066b-111">унрегистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="c066b-112">унрегистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="c066b-113">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="c066b-114">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="c066b-115">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   <span data-ttu-id="c066b-116">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="c066b-116">RegisterMIMEInfo</span></span>

<span data-ttu-id="c066b-117">Например, Регистермимеинфо должен следовать после [унрегистермимеинфо](unregistermimeinfo-action.md) в таблице Sequence.</span><span class="sxs-lookup"><span data-stu-id="c066b-117">For example, RegisterMIMEInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c066b-118">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="c066b-118">ActionData Messages</span></span>



| <span data-ttu-id="c066b-119">Поле</span><span class="sxs-lookup"><span data-stu-id="c066b-119">Field</span></span> | <span data-ttu-id="c066b-120">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="c066b-120">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="c066b-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c066b-121">\[1\]</span></span> | <span data-ttu-id="c066b-122">Идентификатор зарегистрированного типа содержимого MIME.</span><span class="sxs-lookup"><span data-stu-id="c066b-122">Identifier of registered MIME content type.</span></span>  |
| <span data-ttu-id="c066b-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c066b-123">\[2\]</span></span> | <span data-ttu-id="c066b-124">Расширение, связанное с типом содержимого MIME.</span><span class="sxs-lookup"><span data-stu-id="c066b-124">Extension associated with MIME content type.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c066b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c066b-125">Remarks</span></span>

<span data-ttu-id="c066b-126">Действие Регистермимеинфо регистрирует все сведения MIME для серверов из [таблицы MIME](mime-table.md) , для которой установлен соответствующий сервер классов или сервер расширений.</span><span class="sxs-lookup"><span data-stu-id="c066b-126">The RegisterMIMEInfo action registers all MIME information for servers from the [MIME table](mime-table.md) for which the corresponding class server or extension server has been selected to be installed.</span></span>

 

 



