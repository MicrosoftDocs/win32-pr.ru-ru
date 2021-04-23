---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692354"
---
# <a name="s-volume-shadow-copy-service"></a><span data-ttu-id="e2eb1-103">S (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="e2eb1-103">S (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="e2eb1-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e2eb1-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e2eb1-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**выбор для резервного копирования**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-106">Компонент считается выбираемым для резервного копирования, если его явное включение в операцию резервного копирования является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-106">A component is said to be selectable for backup if its explicit inclusion in a backup operation is optional.</span></span> <span data-ttu-id="e2eb1-107">Возможность выбора для резервного копирования включена, если значение элемента **бселектабле** структуры [**\_ компонентинфо VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) равно **true**.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-107">Selectability for backup is enabled if the value of the **bSelectable** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="e2eb1-108">Значение по умолчанию для выбора компонента для резервного копирования отсутствует. средство записи должно всегда задавать это значение явным образом.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-108">There is no default value for a component's selectability for backup; a writer must always set this value explicitly.</span></span>

<span data-ttu-id="e2eb1-109">Модули записи также используют возможность выбора для восстановления, чтобы упорядочить участие компонента в операциях восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-109">Writers also use selectability for restore to organize their component's participation in restore operations.</span></span>

<span data-ttu-id="e2eb1-110">См. также *выбираемый компонент*, возможность *выбора для восстановления*, [*явное включение компонентов*](vssgloss-e.md), [*Включение неявных компонентов*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-110">See also *selectable component*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**выбор для восстановления**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selectability for restore**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-112">Считается, что компонент является выбираемым для восстановления, если он может быть неявно резервным копированием в составе набора компонентов, а затем по отдельности восстановлен без остальной части набора компонентов.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-112">A component is said to be selectable for restore if it can be implicitly backed up as part of a component set, and then later individually restored without the rest of the component set.</span></span> <span data-ttu-id="e2eb1-113">Возможность выбора для восстановления включена, если значение элемента **бселектаблефорресторе** структуры [**\_ компонентинфо VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) равно **true**.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-113">Selectability for restore is enabled if the value of the **bSelectableForRestore** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="e2eb1-114">По умолчанию выбор компонента для восстановления имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-114">By default, a component's selectability for restore is **false**.</span></span> <span data-ttu-id="e2eb1-115">Выбор способа восстановления имеет значение только в том случае, если компонент не был добавлен в документ резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-115">Selectability for restore has meaning only when a component has not been added to the backup document.</span></span>

<span data-ttu-id="e2eb1-116">См. также *выбираемый компонент*, возможность *выбора для резервного копирования*, [*явное включение компонентов*](vssgloss-e.md), [*Включение неявных компонентов*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-116">See also *selectable component*, *selectability for backup*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**Выбираемый компонент**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**selectable component**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-118">Считается, что компонент является выбираемым, если его явное включение в операцию резервного копирования или восстановления является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-118">A component is said to be selectable if its explicit inclusion in a backup or restore operation is optional.</span></span>

<span data-ttu-id="e2eb1-119">Выбор варианта резервного копирования и возможность выбора для восстановления не зависят друг от друга — компонент может быть выбран для обеих операций, для восстановления, а не для резервного копирования, для резервного копирования и не восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-119">Selectability for backup and selectability for restore are independent of each other—a component may be selectable for both operations, for restore and not backup, or for backup and not restore.</span></span>

<span data-ttu-id="e2eb1-120">Модули записи также используют возможность выбора для организации компонентов в группы:</span><span class="sxs-lookup"><span data-stu-id="e2eb1-120">Writers also use selectability to organize their components into groups:</span></span>

-   <span data-ttu-id="e2eb1-121">Невыбираемые компоненты без выбираемых для них предков в их логических путях всегда должны включаться явным образом, если необходимо выполнить резервное копирование или восстановление модуля записи.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-121">Nonselectable components with no selectable ancestors in their logical paths must always be explicitly included if a writer is to be backed up or restored.</span></span>
-   <span data-ttu-id="e2eb1-122">Невыбираемые компоненты с выбираемыми для выбора предками будут включаться в резервную копию или восстановление только в том случае, если включен хотя бы один элемент, который можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-122">Nonselectable components with selectable ancestors will only be included in a backup or restore if at least one selectable ancestor is included.</span></span>
-   <span data-ttu-id="e2eb1-123">Выбираемые компоненты без выбора предков могут быть явно добавлены в операцию резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-123">Selectable components without selectable ancestors can only be included in a backup or restore operation explicitly.</span></span>
-   <span data-ttu-id="e2eb1-124">Выбираемые компоненты можно явно включать в операцию резервного копирования или восстановления, а также можно неявно включать, если включен один из их выбираемых предков.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-124">Selectable components with selectable ancestors can be explicitly included in a backup or restore operation, or can be implicitly included if one of their selectable ancestors is included.</span></span>

<span data-ttu-id="e2eb1-125">См. также [*компоненты*](vssgloss-c.md), возможность *выбора для резервного копирования*, *Выбор для восстановления*, [*явное включение компонентов*](vssgloss-e.md), [*Включение неявных компонентов*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-125">See also [*components*](vssgloss-c.md), *selectability for backup*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**Теневое копирование**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-127">Реплика на момент времени, доступная только для чтения для содержимого исходного тома.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-127">A read-only point-in-time replica of an original volume's contents.</span></span> <span data-ttu-id="e2eb1-128">Каждая теневая копия шифруется с помощью постоянного идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-128">Each shadow copy is keyed by a persistent GUID.</span></span> <span data-ttu-id="e2eb1-129">Также называется теневой копией тома.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-129">Also called a volume shadow copy.</span></span> <span data-ttu-id="e2eb1-130">См. также *Набор теневых копий*.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-130">See also *shadow copy set*.</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**теневые копии общих папок**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Shadow Copies for Shared Folders**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-132">Компонент Windows, который создает упрощенные оперативные резервные копии томов с помощью VSS.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-132">A feature of Windows that creates lightweight, online backup copies of volumes using VSS.</span></span> <span data-ttu-id="e2eb1-133">Клиенты могут получить доступ к этим резервным копиям через оболочку Windows для просмотра старых версий файлов и отмены ошибок без полного восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-133">Clients can access these backups through the Windows shell to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="e2eb1-134">См. также [*теневую копию, доступную для клиента*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-134">See also [*client accessible shadow copy*](vssgloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**Набор теневых копий**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**shadow copy set**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-136">Коллекция теневых копий томов, созданная одновременно и определяемая общим ИДЕНТИФИКАТОРом набора теневых копий (постоянный GUID).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-136">A collection of volume shadow copies created at the same time and identified by a common shadow copy set ID (a persistent GUID) value.</span></span> <span data-ttu-id="e2eb1-137">Это механизм, используемый для управления операциями теневого копирования на томах.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-137">This is the mechanism used to allow a shadow copy operation to be managed across volumes.</span></span> <span data-ttu-id="e2eb1-138">См. также *теневое копирование*.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-138">See also *shadow copy*.</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**поставщик программного обеспечения**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-140">Поставщик, который перехватывает запросы ввода-вывода на уровне программного обеспечения между файловой системой и диспетчером томов.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-140">A provider that intercepts I/O requests at the software level between the file system and the volume manager.</span></span> <span data-ttu-id="e2eb1-141">См. также поставщик [*оборудования*](vssgloss-h.md), [*поставщик*](vssgloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-141">See also [*hardware provider*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**вспомогательный компонент**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponent**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-143">Любой компонент, имеющий логический путь, содержащий выбираемый родительский компонент (для резервного копирования или восстановления).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-143">Any component that has a logical path containing a selectable (for either backup or restore) parent component.</span></span> <span data-ttu-id="e2eb1-144">Подкомпоненты должны иметь логический путь к форме { \_ имя компонента} \\ {имя подкомпонента \_ }.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-144">Subcomponents must have a logical path of the form {component\_name}\\{subcomponent\_name}.</span></span> <span data-ttu-id="e2eb1-145">Если можно выбрать подкомпонент (для резервного копирования или восстановления) предка явным образом в резервную копию или восстановление, то этот компонент неявно включается в операцию.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-145">If a subcomponent's selectable (for either backup or restore) ancestor is explicitly included in a backup or restore, then the subcomponent is implicitly included in the operation.</span></span> <span data-ttu-id="e2eb1-146">Неявно включенные подкомпоненты не содержат данные, включенные в документ компонентов резервного копирования, независимо от того, являются ли они выбираемыми (для восстановления или резервного копирования).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-146">Implicitly included subcomponents do not have their data included in the Backup Components Document—regardless of whether they are selectable (for either restore or backup) or not.</span></span> <span data-ttu-id="e2eb1-147">См. также: [*компонент*](vssgloss-c.md), [*логический путь*](vssgloss-l.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-147">See also [*component*](vssgloss-c.md), [*logical path*](vssgloss-l.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**Теневая копия с поверхностью**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**surfaced shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-149">Теневое копирование тома, видимое для пространства имен диспетчера подключения системы — это означает, что **финдфирстволуме** и **финднекстволуме** могут найти его, а уведомления о получении и отправлении тома будут созданы.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-149">A shadow copied volume visible to a system's Mount Manager namespace—meaning **FindFirstVolume** and **FindNextVolume** can find it and that volume arrival and departure notifications are generated.</span></span> <span data-ttu-id="e2eb1-150">Все доступные теневые копии также отображаются на теневых копиях.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-150">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="e2eb1-151">Однако не требуется предоставлять доступ к поверхностной теневой копии.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-151">However, a surfaced shadow copy need not be exposed.</span></span> <span data-ttu-id="e2eb1-152">Если теневая копия является транспортной, она не может быть выповерхности.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-152">If a shadow copy is transportable, it cannot be surfaced.</span></span> <span data-ttu-id="e2eb1-153">См. также: [*доступна теневая копия*](vssgloss-e.md), [*Переносимая теневая копия*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-153">See also [*exposed shadow copy*](vssgloss-e.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Защита системных файлов**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-155">См. раздел [*Защита файлов Windows*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb1-155">See [*Windows File Protection*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**приложения уровня системы**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**system-level applications**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-157">Указывает точку, в которой VSS уведомляет модуль записи о замораживании.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-157">Indicates the point at which VSS notifies a writer of a freeze.</span></span> <span data-ttu-id="e2eb1-158">Модули записи, инициализированные как приложения уровня системы, получают уведомления после того, как модули записи инициализированы как приложения внешнего интерфейса или как приложения серверного уровня.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-158">Writers that are initialized as system-level applications are notified after writers initialized either as front-end level applications or as back-end level applications.</span></span> <span data-ttu-id="e2eb1-159">См. также приложения уровня [*приложения*](vssgloss-a.md), [*серверного*](vssgloss-b.md)уровня, [*приложения внешнего*](vssgloss-f.md)интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-159">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*front-end level applications*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**поставщик системы**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**system provider**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-161">Предустановленный поставщик по умолчанию, предоставленный в составе Windows.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-161">The default preinstalled provider provided as part of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e2eb1-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Папка системного тома**</span><span class="sxs-lookup"><span data-stu-id="e2eb1-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**</span></span>
</dt> <dd>

<span data-ttu-id="e2eb1-163">Общий каталог, в котором хранятся общие копии общих файлов домена, то есть файлов, которые реплицируются между всеми контроллерами домена в домене.</span><span class="sxs-lookup"><span data-stu-id="e2eb1-163">A shared directory that stores the shared copies of a domain's public files—that is, those files that are replicated among all domain controllers in the domain.</span></span>

</dd> </dl>

 

 



