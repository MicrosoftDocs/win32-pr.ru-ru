---
description: Действие Стопсервицес останавливает системные службы. Это действие запрашивает таблицу ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Действие Стопсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673437"
---
# <a name="stopservices-action"></a><span data-ttu-id="8811e-104">Действие Стопсервицес</span><span class="sxs-lookup"><span data-stu-id="8811e-104">StopServices Action</span></span>

<span data-ttu-id="8811e-105">Действие Стопсервицес останавливает системные службы.</span><span class="sxs-lookup"><span data-stu-id="8811e-105">The StopServices action stops system services.</span></span> <span data-ttu-id="8811e-106">Это действие запрашивает [таблицу ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="8811e-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8811e-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="8811e-107">Sequence Restrictions</span></span>

<span data-ttu-id="8811e-108">Действия служб должны использоваться в следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="8811e-108">The services actions must be used in the following sequence:</span></span>

-   <span data-ttu-id="8811e-109">стопсервицес</span><span class="sxs-lookup"><span data-stu-id="8811e-109">StopServices</span></span>
-   [<span data-ttu-id="8811e-110">делетесервицес</span><span class="sxs-lookup"><span data-stu-id="8811e-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="8811e-111">Любое из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="8811e-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="8811e-112">инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="8811e-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="8811e-113">ремовефилес</span><span class="sxs-lookup"><span data-stu-id="8811e-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="8811e-114">дупликатефилес</span><span class="sxs-lookup"><span data-stu-id="8811e-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="8811e-115">мовефилес</span><span class="sxs-lookup"><span data-stu-id="8811e-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="8811e-116">патчфилес</span><span class="sxs-lookup"><span data-stu-id="8811e-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="8811e-117">ремоведупликатефилес</span><span class="sxs-lookup"><span data-stu-id="8811e-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="8811e-118">инсталлсервицес</span><span class="sxs-lookup"><span data-stu-id="8811e-118">InstallServices</span></span>](installservices-action.md)
-   [<span data-ttu-id="8811e-119">стартсервицес</span><span class="sxs-lookup"><span data-stu-id="8811e-119">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="8811e-120">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="8811e-120">ActionData Messages</span></span>



| <span data-ttu-id="8811e-121">Поле</span><span class="sxs-lookup"><span data-stu-id="8811e-121">Field</span></span> | <span data-ttu-id="8811e-122">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="8811e-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="8811e-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8811e-123">\[1\]</span></span> | <span data-ttu-id="8811e-124">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="8811e-124">Service display name.</span></span>      |
| <span data-ttu-id="8811e-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="8811e-125">\[2\]</span></span> | <span data-ttu-id="8811e-126">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="8811e-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="8811e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8811e-127">Remarks</span></span>

<span data-ttu-id="8811e-128">Для выполнения этого действия необходимо, чтобы пользователь был администратором или иметь повышенные привилегии с разрешением на управление службами или что приложение является частью управляемой установки.</span><span class="sxs-lookup"><span data-stu-id="8811e-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



