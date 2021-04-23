---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809815"
---
# <a name="c-volume-shadow-copy-service"></a><span data-ttu-id="f8375-103">C (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="f8375-103">C (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="f8375-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="f8375-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f8375-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="f8375-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-106">Сущность сохранность для выдачи сертификатов, подтверждающих, что получатель, компьютер или организация, запрашивающие сертификат, удовлетворяет условиям установленной политики.</span><span class="sxs-lookup"><span data-stu-id="f8375-106">An entity entrusted to issue certificates asserting that the recipient individual, machine, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="f8375-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**Теневая копия, доступная для клиента**</span><span class="sxs-lookup"><span data-stu-id="f8375-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**client-accessible shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-108">Теневая копия, созданная поставщиком системы для поддержки теневые копии общих папок и других механизмов отката, которые позволяют клиентам просматривать старые версии файлов и выполнять отмену операций без полного восстановления.</span><span class="sxs-lookup"><span data-stu-id="f8375-108">A shadow copy created by the system provider to support Shadow Copies for Shared Folders and other rollback mechanisms, which allow clients to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="f8375-109">Теневая копия, доступная для клиента, создается с использованием значения, **\_ \_ \_ доступного** для перечисления [**\_ \_ \_ контекста моментальных снимков VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) в VSS CTX.</span><span class="sxs-lookup"><span data-stu-id="f8375-109">A client-accessible shadow copy is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="f8375-110">Кроме того, \_ \_ \_ \_ для теневых копий, доступных для клиента, перечисление атрибутов VSS VOLSNAP attr, доступное для клиентского [**\_ \_ \_ моментального снимка \_ тома VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) , устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8375-110">In addition, the VSS\_VOLSNAP\_ATTR\_CLIENT\_ACCESSIBLE value of the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration is set automatically for client-accessible shadow copies.</span></span> <span data-ttu-id="f8375-111">См. также [*теневые копии общих папок*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="f8375-111">See also [*Shadow Copies for Shared Folders*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8375-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**см**</span><span class="sxs-lookup"><span data-stu-id="f8375-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-113">Группа файлов, определяемая модулем записи, которая должна обрабатываться как единица во время операций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="f8375-113">A group of files, defined by a writer, that must be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="f8375-114">См. также [*компонент базы данных*](vssgloss-d.md), [*компонент файловой группы*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="f8375-114">See also [*database component*](vssgloss-d.md), [*file group component*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8375-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**зависимость компонентов**</span><span class="sxs-lookup"><span data-stu-id="f8375-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**component dependency**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-116">В ситуации, когда компонент (и определяемый им набор компонентов), управляемый одним модулем записи, не может быть скопирован или восстановлен независимо от компонентов, управляемых модулями записи других пользователей.</span><span class="sxs-lookup"><span data-stu-id="f8375-116">A situation in which a component (and the component set it defines) managed by one writer cannot be backed up or restore independently of components managed by others writers.</span></span> <span data-ttu-id="f8375-117">Зависимость не указывает порядок предпочтения между компонентом с документированными зависимостями и компонентами, от которых он зависит: зависимость просто указывает, что компонент и компоненты, от которых он зависит, всегда должны быть резервными копиями или восстановлены вместе.</span><span class="sxs-lookup"><span data-stu-id="f8375-117">A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on: a dependency merely indicates that the component and the components it depends on must always be backed up or restored together.</span></span>

</dd> <dt>

<span data-ttu-id="f8375-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**режим компонента**</span><span class="sxs-lookup"><span data-stu-id="f8375-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**component mode**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-119">Режим, в котором операция резервного копирования или восстановления использует сведения о компоненте модуля записи.</span><span class="sxs-lookup"><span data-stu-id="f8375-119">A mode in which a backup or restore operation makes use of a writer's component information.</span></span> <span data-ttu-id="f8375-120">См. также компонент, который можно [*выбрать*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="f8375-120">See also [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8375-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**набор компонентов**</span><span class="sxs-lookup"><span data-stu-id="f8375-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**component set**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-122">Группа компонентов, имеющих по крайней мере одну выбираемую (для резервного копирования или восстановления) компонент и ряд невыбираемых компонентов, организованных по их логическим путям.</span><span class="sxs-lookup"><span data-stu-id="f8375-122">A group of components with at least one selectable (for either backup or restore) component and a number of nonselectable components organized in a hierarchy by their logical paths.</span></span> <span data-ttu-id="f8375-123">Неявное участие в операции резервного копирования или восстановления зависит от явного включения выбираемого компонента верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f8375-123">The implicit participation in a backup or restore operation depends on the explicit inclusion of the top-level selectable component.</span></span> <span data-ttu-id="f8375-124">В документ компоненты резервного копирования включаются только сведения о компонентах этого выбираемого компонента.</span><span class="sxs-lookup"><span data-stu-id="f8375-124">Only the component information of this selectable component is included in the Backup Components Document.</span></span> <span data-ttu-id="f8375-125">Набор компонентов может включать в себя выбираемые и невыбираемые подкомпоненты.</span><span class="sxs-lookup"><span data-stu-id="f8375-125">A component set may include selectable and nonselectable subcomponents.</span></span> <span data-ttu-id="f8375-126">См. также [*логический путь*](vssgloss-l.md), [*выбираемый компонент*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="f8375-126">See also [*logical path*](vssgloss-l.md), [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8375-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**Теневое копирование при записи**</span><span class="sxs-lookup"><span data-stu-id="f8375-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copy-on-write shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-128">Теневая копия, созданная путем сохранения только отличий от исходного тома.</span><span class="sxs-lookup"><span data-stu-id="f8375-128">A shadow copy created by saving only the differences from the original volume.</span></span>

</dd> <dt>

<span data-ttu-id="f8375-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**состояние отказоустойчивости**</span><span class="sxs-lookup"><span data-stu-id="f8375-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**crash consistent state**</span></span>
</dt> <dd>

<span data-ttu-id="f8375-130">Состояние дисков, эквивалентное тому, что будет найдено после разрушительного сбоя, который внезапно завершает работу системы.</span><span class="sxs-lookup"><span data-stu-id="f8375-130">The state of disks equivalent to what would be found following a catastrophic failure that abruptly shuts down the system.</span></span> <span data-ttu-id="f8375-131">Восстановление из такого набора теневых копий будет эквивалентно перезагрузке после внезапного завершения работы.</span><span class="sxs-lookup"><span data-stu-id="f8375-131">A restore from such a shadow copy set would be equivalent to a reboot following an abrupt shutdown.</span></span> <span data-ttu-id="f8375-132">Это состояние по умолчанию для данных, скопированных с помощью теневого копирования без поддержки модулей записи.</span><span class="sxs-lookup"><span data-stu-id="f8375-132">This is the default state of data that has been shadow copied without the support of writers.</span></span>

</dd> </dl>

 

 



