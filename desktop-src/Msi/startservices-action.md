---
description: Действие Стартсервицес запускает системные службы. Это действие запрашивает таблицу ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Действие Стартсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673559"
---
# <a name="startservices-action"></a><span data-ttu-id="a775f-104">Действие Стартсервицес</span><span class="sxs-lookup"><span data-stu-id="a775f-104">StartServices Action</span></span>

<span data-ttu-id="a775f-105">Действие Стартсервицес запускает системные службы.</span><span class="sxs-lookup"><span data-stu-id="a775f-105">The StartServices action starts system services.</span></span> <span data-ttu-id="a775f-106">Это действие запрашивает [таблицу ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="a775f-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a775f-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="a775f-107">Sequence Restrictions</span></span>

<span data-ttu-id="a775f-108">Действия служб должны использоваться в следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="a775f-108">The services actions must be used in the following sequence:</span></span>

-   [<span data-ttu-id="a775f-109">стопсервицес</span><span class="sxs-lookup"><span data-stu-id="a775f-109">StopServices</span></span>](stopservices-action.md)
-   [<span data-ttu-id="a775f-110">делетесервицес</span><span class="sxs-lookup"><span data-stu-id="a775f-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="a775f-111">Любое из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="a775f-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="a775f-112">инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="a775f-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="a775f-113">ремовефилес</span><span class="sxs-lookup"><span data-stu-id="a775f-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="a775f-114">дупликатефилес</span><span class="sxs-lookup"><span data-stu-id="a775f-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="a775f-115">мовефилес</span><span class="sxs-lookup"><span data-stu-id="a775f-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="a775f-116">патчфилес</span><span class="sxs-lookup"><span data-stu-id="a775f-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="a775f-117">ремоведупликатефилес</span><span class="sxs-lookup"><span data-stu-id="a775f-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="a775f-118">инсталлсервицес</span><span class="sxs-lookup"><span data-stu-id="a775f-118">InstallServices</span></span>](installservices-action.md)
-   <span data-ttu-id="a775f-119">стартсервицес</span><span class="sxs-lookup"><span data-stu-id="a775f-119">StartServices</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a775f-120">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="a775f-120">ActionData Messages</span></span>



| <span data-ttu-id="a775f-121">Поле</span><span class="sxs-lookup"><span data-stu-id="a775f-121">Field</span></span> | <span data-ttu-id="a775f-122">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="a775f-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="a775f-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a775f-123">\[1\]</span></span> | <span data-ttu-id="a775f-124">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="a775f-124">Service display name.</span></span>      |
| <span data-ttu-id="a775f-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a775f-125">\[2\]</span></span> | <span data-ttu-id="a775f-126">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="a775f-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="a775f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a775f-127">Remarks</span></span>

<span data-ttu-id="a775f-128">Для выполнения этого действия необходимо, чтобы пользователь был администратором или иметь повышенные привилегии с разрешением на управление службами или что приложение является частью управляемой установки.</span><span class="sxs-lookup"><span data-stu-id="a775f-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



