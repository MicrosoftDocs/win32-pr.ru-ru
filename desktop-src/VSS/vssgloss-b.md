---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: Б (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343572"
---
# <a name="b-volume-shadow-copy-service"></a><span data-ttu-id="dbc58-103">Б (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="dbc58-103">B (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="dbc58-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="dbc58-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="dbc58-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**приложения уровня серверной части**</span><span class="sxs-lookup"><span data-stu-id="dbc58-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**back-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="dbc58-106">Указывает точку, в которой модуль записи получает уведомления о замораживании службой VSS.</span><span class="sxs-lookup"><span data-stu-id="dbc58-106">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="dbc58-107">Модули записи, инициализированные как приложения серверного уровня, получают уведомления после того, как модули записи инициализируются как приложения внешнего уровня и до тех, которые были инициализированы как приложения уровня системы.</span><span class="sxs-lookup"><span data-stu-id="dbc58-107">Writers that are initialized as back-end level applications are notified after writers initialized as front-end level applications and prior to those initialized as system-level applications.</span></span> <span data-ttu-id="dbc58-108">См. также [*уровень приложения*](vssgloss-a.md), [*приложения внешнего*](vssgloss-f.md)интерфейса, [*приложения уровня системы*](vssgloss-s.md), [*модуль записи*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="dbc58-108">See also [*application level*](vssgloss-a.md), [*front-end level applications*](vssgloss-f.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc58-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Событие Баккупкомплете**</span><span class="sxs-lookup"><span data-stu-id="dbc58-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete event**</span></span>
</dt> <dd>

<span data-ttu-id="dbc58-110">Событие VSS, указывающее, что резервное копирование VSS завершено.</span><span class="sxs-lookup"><span data-stu-id="dbc58-110">A VSS event indicating that a VSS backup has completed.</span></span> <span data-ttu-id="dbc58-111">За этим событием следует событие Баккупшутдовн при нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="dbc58-111">This event should be followed by a BackupShutdown event under normal operation.</span></span> <span data-ttu-id="dbc58-112">См. также *событие баккупшутдовн*.</span><span class="sxs-lookup"><span data-stu-id="dbc58-112">See also *BackupShutdown event*.</span></span>

</dd> <dt>

<span data-ttu-id="dbc58-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Документ компонентов резервного копирования**</span><span class="sxs-lookup"><span data-stu-id="dbc58-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Backup Components Document**</span></span>
</dt> <dd>

<span data-ttu-id="dbc58-114">XML-документ, созданный инициатором запроса (с помощью интерфейса **ивссбаккупкомпонентс** ) в процессе настройки операции восстановления или резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="dbc58-114">An XML document created by a requester (using the **IVssBackupComponents** interface) in the course of setting up a restore or backup operation.</span></span> <span data-ttu-id="dbc58-115">Документ компонентов резервного копирования содержит список явно добавленных компонентов из одного или нескольких модулей записи, участвующих в операции резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="dbc58-115">The Backup Components Document contains a list of those explicitly included components, from one or more writers, participating in a backup or restore operation.</span></span> <span data-ttu-id="dbc58-116">Он не содержит сведения о неявно включаемых компонентах.</span><span class="sxs-lookup"><span data-stu-id="dbc58-116">It does not contain implicitly included component information.</span></span> <span data-ttu-id="dbc58-117">В отличие от этого, документ метаданных модуля записи содержит только компоненты модуля записи, которые могут участвовать в резервном копировании.</span><span class="sxs-lookup"><span data-stu-id="dbc58-117">In contrast, a Writer Metadata Document contains only writer components that may participate in a backup.</span></span>

<span data-ttu-id="dbc58-118">Документ компонентов резервного копирования можно сохранить на диск.</span><span class="sxs-lookup"><span data-stu-id="dbc58-118">A Backup Components Document can be saved to disk.</span></span> <span data-ttu-id="dbc58-119">См. также [*явное включение компонентов*](vssgloss-e.md), [*Включение неявных компонентов*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="dbc58-119">See also [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc58-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**резервный набор данных**</span><span class="sxs-lookup"><span data-stu-id="dbc58-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**backup set**</span></span>
</dt> <dd>

<span data-ttu-id="dbc58-121">Файлы для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="dbc58-121">Those files to be backed up.</span></span> <span data-ttu-id="dbc58-122">Сюда входят файлы, выбранные путем включения в компонент, указанные инструкциями include уровня записи, которые меньше, чем файлы, которые были включены явным образом.</span><span class="sxs-lookup"><span data-stu-id="dbc58-122">It includes files selected by inclusion in a component, those indicated by writer-level include statements, less those files that have been explicitly included.</span></span>

</dd> <dt>

<span data-ttu-id="dbc58-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Событие Баккупшутдовн**</span><span class="sxs-lookup"><span data-stu-id="dbc58-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown event**</span></span>
</dt> <dd>

<span data-ttu-id="dbc58-124">Событие VSS, указывающее на завершение работы соответствующего приложения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="dbc58-124">A VSS event indicating that a compliant backup application has shut down.</span></span> <span data-ttu-id="dbc58-125">Обычно перед ним стоит событие Баккупкомплете.</span><span class="sxs-lookup"><span data-stu-id="dbc58-125">Normally, this is preceded by a BackupComplete event.</span></span> <span data-ttu-id="dbc58-126">Однако при неожиданном завершении резервного копирования это событие может быть создано без предшествующего события Баккупкомплете.</span><span class="sxs-lookup"><span data-stu-id="dbc58-126">However, if a backup terminates unexpectedly, this event can be generated without a preceding BackupComplete event.</span></span> <span data-ttu-id="dbc58-127">См. также *событие баккупкомплете*.</span><span class="sxs-lookup"><span data-stu-id="dbc58-127">See also *BackupComplete event*.</span></span>

</dd> <dt>

<span data-ttu-id="dbc58-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**метка резервной копии**</span><span class="sxs-lookup"><span data-stu-id="dbc58-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**backup stamp**</span></span>
</dt> <dd>

<span data-ttu-id="dbc58-129">Строка, содержащая сведения о том, когда была выполнена резервная копия.</span><span class="sxs-lookup"><span data-stu-id="dbc58-129">A string containing information as to when a backup took place.</span></span> <span data-ttu-id="dbc58-130">Служба VSS не накладывает ограничений на формат этой строки, за исключением того, что ее можно прочесть для всех экземпляров модуля записи данного класса.</span><span class="sxs-lookup"><span data-stu-id="dbc58-130">VSS places no restriction on the format of this string, except that it be intelligible to all the writer instances of a given class.</span></span> <span data-ttu-id="dbc58-131">Он может содержать сведения о времени и датах, логические порядковые номера или любые другие сведения, позволяющие модулю записи одного и того же класса определять время последнего резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="dbc58-131">It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has take place.</span></span>

</dd> </dl>

 

 



