---
description: Действие Делетесервицес останавливает службу и удаляет ее регистрацию из системы. Это действие запрашивает таблицу ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Действие Делетесервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346345"
---
# <a name="deleteservices-action"></a><span data-ttu-id="281ee-104">Действие Делетесервицес</span><span class="sxs-lookup"><span data-stu-id="281ee-104">DeleteServices Action</span></span>

<span data-ttu-id="281ee-105">Действие Делетесервицес останавливает службу и удаляет ее регистрацию из системы.</span><span class="sxs-lookup"><span data-stu-id="281ee-105">The DeleteServices action stops a service and removes its registration from the system.</span></span> <span data-ttu-id="281ee-106">Это действие запрашивает [таблицу ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="281ee-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="281ee-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="281ee-107">Sequence Restrictions</span></span>

<span data-ttu-id="281ee-108">Действия служб должны использоваться в следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="281ee-108">The services actions must be used in the following sequence:</span></span>

1.  [<span data-ttu-id="281ee-109">стопсервицес</span><span class="sxs-lookup"><span data-stu-id="281ee-109">StopServices</span></span>](stopservices-action.md)
2.  <span data-ttu-id="281ee-110">делетесервицес</span><span class="sxs-lookup"><span data-stu-id="281ee-110">DeleteServices</span></span>
3.  <span data-ttu-id="281ee-111">Любое из следующих действий: [инсталлфилес](installfiles-action.md), [ремовефилес](removefiles-action.md), [дупликатефилес](duplicatefiles-action.md), [мовефилес](movefiles-action.md), [патчфилес](patchfiles-action.md)и [ремоведупликатефилес](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="281ee-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>
4.  [<span data-ttu-id="281ee-112">Действие Инсталлсервицес</span><span class="sxs-lookup"><span data-stu-id="281ee-112">InstallServices action</span></span>](installservices-action.md)
5.  [<span data-ttu-id="281ee-113">стартсервицес</span><span class="sxs-lookup"><span data-stu-id="281ee-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="281ee-114">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="281ee-114">ActionData Messages</span></span>



| <span data-ttu-id="281ee-115">Поле</span><span class="sxs-lookup"><span data-stu-id="281ee-115">Field</span></span> | <span data-ttu-id="281ee-116">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="281ee-116">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="281ee-117">\[1\]</span><span class="sxs-lookup"><span data-stu-id="281ee-117">\[1\]</span></span> | <span data-ttu-id="281ee-118">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="281ee-118">Service display name.</span></span>      |
| <span data-ttu-id="281ee-119">\[2\]</span><span class="sxs-lookup"><span data-stu-id="281ee-119">\[2\]</span></span> | <span data-ttu-id="281ee-120">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="281ee-120">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="281ee-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="281ee-121">Remarks</span></span>

<span data-ttu-id="281ee-122">Для выполнения этого действия пользователь должен быть администратором или обладать повышенными привилегиями с разрешением на удаление служб или на то, что приложение является частью управляемой установки.</span><span class="sxs-lookup"><span data-stu-id="281ee-122">This action requires the user be an administrator or have elevated privileges with permission to delete services or that the application be part of a managed installation.</span></span>

 

 



