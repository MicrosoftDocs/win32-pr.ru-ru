---
description: Системный администратор может устанавливать квоты для конкретных пользователей на томе. Администратор также может задать квоты по умолчанию для тома.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Администрирование дисковых квот на уровне системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263245"
---
# <a name="system-level-administration-of-disk-quotas"></a><span data-ttu-id="9cd99-104">Администрирование дисковых квот на уровне системы</span><span class="sxs-lookup"><span data-stu-id="9cd99-104">System-level Administration of Disk Quotas</span></span>

<span data-ttu-id="9cd99-105">Системный администратор может устанавливать квоты для конкретных пользователей на томе.</span><span class="sxs-lookup"><span data-stu-id="9cd99-105">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="9cd99-106">Администратор также может задать квоты по умолчанию для тома.</span><span class="sxs-lookup"><span data-stu-id="9cd99-106">The administrator can also set default quotas for the volume.</span></span> <span data-ttu-id="9cd99-107">Новый пользователь на томе получает квоту по умолчанию, если администратор не установил квоту специально для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9cd99-107">A new user on the volume receives the default quota unless the administrator established a quota specifically for that user.</span></span>

<span data-ttu-id="9cd99-108">Администратор может запрашивать уровень отслеживания и ограничения квоты (или состояния квоты), квоты по умолчанию и сведения о квоте для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9cd99-108">The administrator can query the level of quota tracking and enforcement (or quota states), the default quota limits, and the per-user quota information.</span></span> <span data-ttu-id="9cd99-109">Сведения о квотах для каждого пользователя содержат ограничение жесткой квоты пользователя, порог предупреждения и использование квоты.</span><span class="sxs-lookup"><span data-stu-id="9cd99-109">The per-user quota information contains the user's hard quota limit, warning threshold, and the quota usage.</span></span> <span data-ttu-id="9cd99-110">Администратор может также включить или отключить принудительную квоту.</span><span class="sxs-lookup"><span data-stu-id="9cd99-110">The administrator can also enable or disable quota enforcement.</span></span>

<span data-ttu-id="9cd99-111">Существует три состояния квоты, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9cd99-111">There are three quota states, as shown in the following table.</span></span>



| <span data-ttu-id="9cd99-112">Состояние</span><span class="sxs-lookup"><span data-stu-id="9cd99-112">State</span></span>          | <span data-ttu-id="9cd99-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9cd99-113">Description</span></span>                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd99-114">Квота отключена</span><span class="sxs-lookup"><span data-stu-id="9cd99-114">Quota disabled</span></span> | <span data-ttu-id="9cd99-115">Изменения использования квоты не записываются, но ограничения квоты не удаляются.</span><span class="sxs-lookup"><span data-stu-id="9cd99-115">Quota usage changes are not tracked, but the quota limits are not removed.</span></span> <span data-ttu-id="9cd99-116">В этом состоянии производительность не зависит от дисковых квот.</span><span class="sxs-lookup"><span data-stu-id="9cd99-116">In this state, performance is not affected by disk quotas.</span></span> <span data-ttu-id="9cd99-117">Это состояние по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9cd99-117">This is the default state.</span></span>                         |
| <span data-ttu-id="9cd99-118">Отслеживание квоты</span><span class="sxs-lookup"><span data-stu-id="9cd99-118">Quota tracked</span></span>  | <span data-ttu-id="9cd99-119">Изменения использования квоты записываются, но ограничения квоты не применяются.</span><span class="sxs-lookup"><span data-stu-id="9cd99-119">Quota usage changes are tracked, but quota limits are not enforced.</span></span> <span data-ttu-id="9cd99-120">В этом состоянии события нарушения квоты не создаются, и операции с файлами завершаются неудачей из-за нарушений дисковой квоты.</span><span class="sxs-lookup"><span data-stu-id="9cd99-120">In this state, no quota violation events are generated and no file operations fail because of disk quota violations.</span></span> |
| <span data-ttu-id="9cd99-121">Примененная квота</span><span class="sxs-lookup"><span data-stu-id="9cd99-121">Quota enforced</span></span> | <span data-ttu-id="9cd99-122">Изменения использования квоты записываются, и применяются ограничения квот.</span><span class="sxs-lookup"><span data-stu-id="9cd99-122">Quota usage changes are tracked and quota limits are enforced.</span></span>                                                                                                                           |



 

 

 



