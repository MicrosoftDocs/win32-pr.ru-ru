---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541730"
---
# <a name="p-volume-shadow-copy-service"></a><span data-ttu-id="797d8-103">P (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="797d8-103">P (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="797d8-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="797d8-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="797d8-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**Частичная поддержка файлов**</span><span class="sxs-lookup"><span data-stu-id="797d8-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**partial file support**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-106">Емкость для реализации операций резервного копирования путем изменения подразделов используемых файлов вместо работы со всеми файлами.</span><span class="sxs-lookup"><span data-stu-id="797d8-106">The capacity to implement backup operations by modifying subsections of the files involved, rather than working with the entire files.</span></span> <span data-ttu-id="797d8-107">См. также [*направленное нацеливание*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="797d8-107">See also [*directed targeting*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="797d8-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**Постоянная теневая копия**</span><span class="sxs-lookup"><span data-stu-id="797d8-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistent shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-109">Теневая копия, которая не удаляется автоматически, когда инициатор запроса освобождает объект [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) или перезапускает компьютер.</span><span class="sxs-lookup"><span data-stu-id="797d8-109">A shadow copy that is not deleted automatically when the requester releases an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object or when the computer is restarted.</span></span> <span data-ttu-id="797d8-110">См. также [*Автоматическое освобождение теневой*](vssgloss-a.md)копии [*.*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="797d8-110">See also [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="797d8-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Плексов**</span><span class="sxs-lookup"><span data-stu-id="797d8-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-112">Специальный тип тома теневых копий, который полностью и полностью представляет том теневой копии без необходимости использования какого-либо исходного тома.</span><span class="sxs-lookup"><span data-stu-id="797d8-112">A special type of shadow copy volume that fully and completely represents a shadow copy volume without the need for either original volume.</span></span> <span data-ttu-id="797d8-113">Это также называется разделением зеркального отображения, но в этой документации используется термин плекс.</span><span class="sxs-lookup"><span data-stu-id="797d8-113">This is also commonly known as a split-mirror, but this documentation uses the term Plex.</span></span>

</dd> <dt>

<span data-ttu-id="797d8-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Событие восстановления**</span><span class="sxs-lookup"><span data-stu-id="797d8-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-115">Событие VSS, указывающее, что восстановление VSS завершено.</span><span class="sxs-lookup"><span data-stu-id="797d8-115">A VSS event indicating that a VSS restore has completed.</span></span>

</dd> <dt>

<span data-ttu-id="797d8-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Событие моментального снимка**</span><span class="sxs-lookup"><span data-stu-id="797d8-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-117">Событие VSS, указывающее, что теневая копия завершена.</span><span class="sxs-lookup"><span data-stu-id="797d8-117">A VSS event indicating that a shadow copy has been completed.</span></span> <span data-ttu-id="797d8-118">См. также [*теневое копирование*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="797d8-118">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="797d8-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Событие PrepareForBackup**</span><span class="sxs-lookup"><span data-stu-id="797d8-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup event**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-120">Событие VSS, указывающее, что должна быть выполнена операция резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="797d8-120">A VSS event indicating that a backup operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="797d8-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Событие Препарефорснапшот**</span><span class="sxs-lookup"><span data-stu-id="797d8-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-122">Событие VSS, указывающее, что модули записи должны предпринять шаги для подготовки к предстоящей операции теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="797d8-122">A VSS event indicating that writers should take steps to prepare for an upcoming shadow copy operation.</span></span> <span data-ttu-id="797d8-123">См. также [*теневое копирование*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="797d8-123">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="797d8-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Событие перед восстановлением**</span><span class="sxs-lookup"><span data-stu-id="797d8-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-125">Событие VSS, указывающее, что должна быть выполнена операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="797d8-125">A VSS event indicating that a restore operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="797d8-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**поставщики**</span><span class="sxs-lookup"><span data-stu-id="797d8-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="797d8-127">Объект операционной системы, который перехватывает и управляет запросами ввода-вывода для создания и представления теневых копий томов в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="797d8-127">An operating system object that intercepts and manages I/O requests to create and represent volume shadow copies to the file system.</span></span> <span data-ttu-id="797d8-128">См. также [*поставщик оборудования*](vssgloss-h.md), [*поставщик программного обеспечения*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="797d8-128">See also [*hardware provider*](vssgloss-h.md), [*software provider*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



