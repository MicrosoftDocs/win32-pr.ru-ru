---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692359"
---
# <a name="e-volume-shadow-copy-service"></a><span data-ttu-id="dd82a-103">E (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="dd82a-103">E (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="dd82a-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="dd82a-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="dd82a-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**явное включение компонентов**</span><span class="sxs-lookup"><span data-stu-id="dd82a-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="dd82a-106">Добавление сведений о компоненте в документ компонентов резервного копирования инициатора запроса при участии в операции резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="dd82a-106">Adding of a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span> <span data-ttu-id="dd82a-107">Запрашивающие стороны используют [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) для явного включения компонента в операцию резервного копирования, а [**Ивссбаккупкомпонентс:: сетселектедфорресторе**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) или [**ивссбаккупкомпонентс:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) для явного включения компонента в операцию восстановления.</span><span class="sxs-lookup"><span data-stu-id="dd82a-107">Requesters use [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to explicitly include a component in a backup operation, and [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) or [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) to explicitly include a component in a restore operation.</span></span>

<span data-ttu-id="dd82a-108">Если резервное копирование или восстановление какого-либо компонента модуля записи выполняется, все невыбираемые компоненты без выбора предков должны быть явно добавлены в операцию резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="dd82a-108">If any component of a writer is backed up or restored, all nonselectable components without any selectable ancestors must be explicitly included in a backup or restore operation.</span></span>

<span data-ttu-id="dd82a-109">Выбираемые компоненты без выбираемых для выбора предков, выбранных инициатором запроса для участия в резервной копии или восстановлении, необходимо явно включать в операцию.</span><span class="sxs-lookup"><span data-stu-id="dd82a-109">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore must be explicitly included in the operation.</span></span>

<span data-ttu-id="dd82a-110">Невыбираемые компоненты с выбираемым предком никогда не включаются явным образом.</span><span class="sxs-lookup"><span data-stu-id="dd82a-110">Nonselectable components with a selectable ancestor are never explicitly included.</span></span>

<span data-ttu-id="dd82a-111">Выбираемые компоненты с выбираемым предком могут быть явно добавлены или могут включаться неявно, если родительский элемент включен явным образом.</span><span class="sxs-lookup"><span data-stu-id="dd82a-111">Selectable components with a selectable ancestor may be included explicitly, or may be included implicitly if the ancestor is included explicitly.</span></span>

</dd> <dt>

<span data-ttu-id="dd82a-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**доступная теневая копия**</span><span class="sxs-lookup"><span data-stu-id="dd82a-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**exposed shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="dd82a-113">Теневая копия тома, которая подключена к системе и доступна для процессов, отличных от управляемых.</span><span class="sxs-lookup"><span data-stu-id="dd82a-113">A volume shadow copy that is mounted on a system and available to processes other than the one that manages it.</span></span> <span data-ttu-id="dd82a-114">Том теневой копии, подключенный под буквой диска или каталогом, называется "локально предоставлен".</span><span class="sxs-lookup"><span data-stu-id="dd82a-114">A shadow copy volume mounted under a drive letter or a directory location is referred to as "locally exposed."</span></span> <span data-ttu-id="dd82a-115">Том теневой копии, доступный через общую папку (за исключением теневых копий, доступных для клиента), называется "удаленно предоставлено".</span><span class="sxs-lookup"><span data-stu-id="dd82a-115">A shadow copy volume accessible through a share (except for client-accessible shadow copies) is referred to as "remotely exposed."</span></span> <span data-ttu-id="dd82a-116">Все доступные теневые копии также отображаются на теневых копиях.</span><span class="sxs-lookup"><span data-stu-id="dd82a-116">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="dd82a-117">См [*. также теневую копию,*](vssgloss-s.md) [*доступную для клиента*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="dd82a-117">See also [*client accessible shadow copy*](vssgloss-c.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



