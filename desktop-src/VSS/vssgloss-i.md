---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809803"
---
# <a name="i-volume-shadow-copy-service"></a><span data-ttu-id="812b0-103">I (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="812b0-103">I (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="812b0-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) . J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="812b0-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="812b0-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Выявление события**</span><span class="sxs-lookup"><span data-stu-id="812b0-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identify event**</span></span>
</dt> <dd>

<span data-ttu-id="812b0-106">Событие VSS, указывающее, что модулю записи или инициатору запроса необходимо запросить текущий модуль записи.</span><span class="sxs-lookup"><span data-stu-id="812b0-106">A VSS event indicating that a writer or a requester needs to query the current writer.</span></span> <span data-ttu-id="812b0-107">Он используется для создания сведений о метаданных текущего модуля записи.</span><span class="sxs-lookup"><span data-stu-id="812b0-107">It is used to construct the current writer's metadata information.</span></span> <span data-ttu-id="812b0-108">См. также [*инициатор запроса*](vssgloss-r.md), [*модуль записи*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="812b0-108">See also [*requester*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="812b0-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**Включение неявного компонента**</span><span class="sxs-lookup"><span data-stu-id="812b0-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="812b0-110">Не добавляйте сведения о компоненте в документ компонентов резервного копирования инициатора запроса, когда он участвует в операции резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="812b0-110">Not adding a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span>

<span data-ttu-id="812b0-111">Невыбираемые компоненты с выбираемым предком неявным образом включаются только при включении их предков.</span><span class="sxs-lookup"><span data-stu-id="812b0-111">Nonselectable components with a selectable ancestor are only implicitly included if their ancestor is included.</span></span>

<span data-ttu-id="812b0-112">Выбираемые компоненты с выбираемым предком могут включаться неявно, если родительский элемент включен или может быть включен явным образом.</span><span class="sxs-lookup"><span data-stu-id="812b0-112">Selectable components with a selectable ancestor may be included implicitly, if the ancestor is included, or may be included explicitly.</span></span>

<span data-ttu-id="812b0-113">Невыбираемые компоненты без выбранных предков никогда не включаются в операцию резервного копирования или восстановления. все такие компоненты должны быть явно добавлены в документ компонентов резервного копирования, если участвуют компоненты модуля записи.</span><span class="sxs-lookup"><span data-stu-id="812b0-113">Nonselectable components without any selectable ancestors are never implicitly included in a backup or restore operation—all such components must be explicitly added to the Backup Components Document if any of the writer's components participate.</span></span>

<span data-ttu-id="812b0-114">Выбираемые компоненты без выбираемых для выбора предков, выбранных инициатором запроса для участия в резервной копии или восстановлении, не могут быть неявно включены в операцию, но должны быть явно добавлены в документ компонентов резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="812b0-114">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore cannot be implicitly included in the operation, but must be explicitly added to the Backup Components Document.</span></span>

</dd> <dt>

<span data-ttu-id="812b0-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**операции добавочного резервного копирования**</span><span class="sxs-lookup"><span data-stu-id="812b0-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**incremental backup operations**</span></span>
</dt> <dd>

<span data-ttu-id="812b0-116">Операция резервного копирования или восстановления выполняется только для файлов, созданных или измененных с момента сохранения последней полной, добавочной или разностной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="812b0-116">A backup or restore operation is performed only on files created or changed since the last full, incremental, or differential backup was saved.</span></span> <span data-ttu-id="812b0-117">См. также [*разностные операции резервного копирования*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="812b0-117">See also [*differential backup operations*](vssgloss-d.md).</span></span>

</dd> </dl>

 

 



