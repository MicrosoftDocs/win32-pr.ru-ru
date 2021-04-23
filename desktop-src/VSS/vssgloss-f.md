---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809808"
---
# <a name="f-volume-shadow-copy-service"></a><span data-ttu-id="e1f2d-103">F (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="e1f2d-103">F (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="e1f2d-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e1f2d-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e1f2d-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**компонент файловой группы**</span><span class="sxs-lookup"><span data-stu-id="e1f2d-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**file group component**</span></span>
</dt> <dd>

<span data-ttu-id="e1f2d-106">Группа файлов, отличных от используемых в качестве базы данных и определяемая модулем записи, которая должна обрабатываться как единица во время операций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-106">A group of files other than those used as a database and defined by a writer as needing to be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="e1f2d-107">См. [](vssgloss-c.md)также компонент [*базы данных*](vssgloss-d.md)Component.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-107">See also [*component*](vssgloss-c.md), [*database component*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1f2d-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**набор файлов**</span><span class="sxs-lookup"><span data-stu-id="e1f2d-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**file set**</span></span>
</dt> <dd>

<span data-ttu-id="e1f2d-109">Сочетание пути, спецификации файла и рекурсивного флага, описывающего один из файлов или групп файлов.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-109">The combination of a path, file specification, and recursive flag describing one of a file or group of files.</span></span> <span data-ttu-id="e1f2d-110">Например, файлы добавляются к компонентам в наборах файлов.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-110">For example, files are added to components in file sets.</span></span>

<span data-ttu-id="e1f2d-111">Если не указано иное, пути к набору файлов являются стандартными путями Windows и могут содержать переменные среды (например,% SystemRoot%). но не может содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-111">Unless otherwise indicated, a file set's paths are standard Windows paths and can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.</span></span> <span data-ttu-id="e1f2d-112">Нет необходимости в конце пути символом обратной косой черты (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="e1f2d-112">There is no requirement that the path end with a backslash ("\\").</span></span> <span data-ttu-id="e1f2d-113">Это приложения, которые извлекают эти сведения для проверки.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-113">It is up to applications that retrieve this information to check it.</span></span>

<span data-ttu-id="e1f2d-114">Спецификация файла, содержащаяся в наборе файлов, указывает имя файла или включаемых в него файлов.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-114">The file specification contained in a file set indicates the name of the file or files it includes.</span></span> <span data-ttu-id="e1f2d-115">Спецификация файла не может содержать спецификации каталогов (например, без обратных косых черт), но может содержать символ?</span><span class="sxs-lookup"><span data-stu-id="e1f2d-115">This file specification cannot contain directory specifications (for example, no backslashes) but can contain the ?</span></span> <span data-ttu-id="e1f2d-116">и \* подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-116">and \* wildcard characters.</span></span>

<span data-ttu-id="e1f2d-117">Рекурсивный тег — это логическое значение, указывающее, должен ли путь к набору файлов рассматриваться как единственный каталог или он указывает иерархию каталогов для рекурсивного обхода.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-117">The recursive tag is a Boolean specifying whether the file set's path should be treated as a only a single directory or if it indicates a hierarchy of directories to be traversed recursively.</span></span> <span data-ttu-id="e1f2d-118">Логическое значение равно **true** , если путь рассматривается как иерархия каталогов для рекурсивного прохода, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-118">The Boolean is **true** if the path is treated as a hierarchy of directories to be traversed recursively, or **false** if not.</span></span>

<span data-ttu-id="e1f2d-119">Сведения о наборе файлов возвращаются через экземпляры интерфейса **ивссвмфиледеск** и могут содержать дополнительные сведения, включая альтернативные пути, сопоставления альтернативного расположения и параметры поддержки схемы на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-119">Information about a file set is returned through instances of the **IVssWMFiledesc** interface, and can contain additional information includes alternate paths, alternate location mappings, and file-level schema support settings.</span></span>

<span data-ttu-id="e1f2d-120">См. также [*альтернативный путь*](vssgloss-a.md), [*сопоставление альтернативного расположения*](vssgloss-a.md), [*компонент*](vssgloss-c.md), *Спецификация файла*.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-120">See also [*alternate path*](vssgloss-a.md), [*alternate location mapping*](vssgloss-a.md), [*component*](vssgloss-c.md), *file specification*.</span></span>

</dd> <dt>

<span data-ttu-id="e1f2d-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Спецификация файла**</span><span class="sxs-lookup"><span data-stu-id="e1f2d-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**file specification**</span></span>
</dt> <dd>

<span data-ttu-id="e1f2d-122">Используется для сопоставления файлов в каталоге и определения набора файлов.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-122">Used to match files within a directory and to define a file set.</span></span> <span data-ttu-id="e1f2d-123">Он не может содержать спецификации каталогов (например, без обратных косых черт), но может содержать символ?</span><span class="sxs-lookup"><span data-stu-id="e1f2d-123">It cannot contain directory specifications (for example, no backslashes) but it can contain the ?</span></span> <span data-ttu-id="e1f2d-124">и \* подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-124">and \* wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="e1f2d-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Служба репликации файлов**</span><span class="sxs-lookup"><span data-stu-id="e1f2d-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**File Replication Service**</span></span>
</dt> <dd>

<span data-ttu-id="e1f2d-126">Используется для репликации системных файлов в каталоге избыточного системного тома (SysVol) для поддержки бесперебойной работы файловой системы, особенно для распределенных файловых систем.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-126">Used to replicate system files in a redundant system volume (SysVol) directory to support file system survivability, particularly for distributed file systems.</span></span>

</dd> <dt>

<span data-ttu-id="e1f2d-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**фиксировать**</span><span class="sxs-lookup"><span data-stu-id="e1f2d-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**freeze**</span></span>
</dt> <dd>

<span data-ttu-id="e1f2d-128">Период времени в процессе создания теневой копии, когда все модули записи записывают свои записи в тома и не инициируют дополнительные операции записи.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-128">A period of time during the shadow copy creation process when all writers have flushed their writes to the volumes and are not initiating additional writes.</span></span>

</dd> <dt>

<span data-ttu-id="e1f2d-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Заморозить событие**</span><span class="sxs-lookup"><span data-stu-id="e1f2d-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze event**</span></span>
</dt> <dd>

<span data-ttu-id="e1f2d-130">Событие VSS, указывающее, что выполняется заморозка теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-130">A VSS event indicating that a shadow copy freeze is in progress.</span></span> <span data-ttu-id="e1f2d-131">См. также раздел *заморозить*, [*теневое копирование*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="e1f2d-131">See also *freeze*, [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1f2d-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**приложения уровня внешнего интерфейса**</span><span class="sxs-lookup"><span data-stu-id="e1f2d-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**front-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="e1f2d-133">Указывает точку, в которой модуль записи получает уведомления о замораживании службой VSS.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-133">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="e1f2d-134">Модули записи, инициализированные как приложения внешнего уровня, получают уведомления перед потоками записи, инициализированными как приложения уровня сервера или как приложения уровня системы.</span><span class="sxs-lookup"><span data-stu-id="e1f2d-134">Writers that were initialized as front-end level applications are notified prior to writers initialized either as back-end level applications or as system-level applications.</span></span> <span data-ttu-id="e1f2d-135">См. также [*уровень приложений*](vssgloss-a.md), [*приложения серверной*](vssgloss-b.md)части, [*приложения уровня системы*](vssgloss-s.md), [*модуль записи*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="e1f2d-135">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> </dl>

 

 



