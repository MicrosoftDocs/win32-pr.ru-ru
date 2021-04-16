---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692362"
---
# <a name="a-volume-shadow-copy-service"></a><span data-ttu-id="ec777-103">A (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="ec777-103">A (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="ec777-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ec777-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ec777-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Событие прерывания**</span><span class="sxs-lookup"><span data-stu-id="ec777-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**</span></span>
</dt> <dd>

<span data-ttu-id="ec777-106">Событие VSS, выданное служба теневого копирования томов, указывающее, что соответствующая операция резервного копирования или восстановления была прервана.</span><span class="sxs-lookup"><span data-stu-id="ec777-106">A VSS event issued by the Volume Shadow Copy Service indicating that a compliant backup or restore operation has been aborted.</span></span> <span data-ttu-id="ec777-107">Обработчик событий — **квссвритер:: OnAbort**.</span><span class="sxs-lookup"><span data-stu-id="ec777-107">The event handler is **CVssWriter::OnAbort**.</span></span>

</dd> <dt>

<span data-ttu-id="ec777-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="ec777-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span></span>
</dt> <dd>

<span data-ttu-id="ec777-109">Служба Active Directory (ADSI) — это служба на основе COM, предоставляющая механизм для поиска, идентификации и доступа к пользователям и ресурсам, доступным в системе распределенной вычислительной среды.</span><span class="sxs-lookup"><span data-stu-id="ec777-109">Active Directory Service (ADSI) is a COM-based service providing a mechanism for locating, identifying, and accessing the users and resources available in a distributed computing environment system.</span></span> <span data-ttu-id="ec777-110">В частности, служба Active Directory используется для управления данными каталога предприятия для распространения сервером домена Windows.</span><span class="sxs-lookup"><span data-stu-id="ec777-110">In particular, the Active Directory service is used to manage enterprise directory information for distribution by a Windows domain server.</span></span>

</dd> <dt>

<span data-ttu-id="ec777-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**сопоставление альтернативного расположения**</span><span class="sxs-lookup"><span data-stu-id="ec777-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**alternate location mapping**</span></span>
</dt> <dd>

<span data-ttu-id="ec777-112">Путь, отличный от исходного пути к файлу, в который может быть восстановлен файл при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="ec777-112">A path, other than a file's original path, to which the file may be restored under certain conditions.</span></span> <span data-ttu-id="ec777-113">Как правило, сопоставления альтернативного расположения не определяются для одного хорошо определенного файла, но для пары "путь-файл" и "спецификация файла" и могут быть рекурсивными.</span><span class="sxs-lookup"><span data-stu-id="ec777-113">Typically, alternate location mappings are not defined for a single well-defined file, but for a path/file specification pair, and may be recursive.</span></span>

<span data-ttu-id="ec777-114">Сопоставление альтернативного расположения используется только во время операции восстановления и не следует путать с альтернативным путем, который используется только во время операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ec777-114">An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.</span></span> <span data-ttu-id="ec777-115">См. также *альтернативный путь*.</span><span class="sxs-lookup"><span data-stu-id="ec777-115">See also *alternate path*.</span></span>

</dd> <dt>

<span data-ttu-id="ec777-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**альтернативный путь**</span><span class="sxs-lookup"><span data-stu-id="ec777-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**alternate path**</span></span>
</dt> <dd>

<span data-ttu-id="ec777-117">Во время операций резервного копирования пара спецификаций пути или файла (обрабатываемая экземпляром интерфейса **ивссвмфиледеск** ) называется альтернативным путем, если его дескриптор файла (возвращенный **Ивссвмфиледеск:: жеталтернателокатион**) не равен null.</span><span class="sxs-lookup"><span data-stu-id="ec777-117">During backup operations, a path/file specification pair (handled by an instance of the **IVssWMFiledesc** interface) is said to have an alternate path if its file descriptor (as returned by **IVssWMFiledesc::GetAlternateLocation**) is non-NULL.</span></span> <span data-ttu-id="ec777-118">Это происходит по указанному пути, а не по умолчанию, файлы копируются при резервном копировании тома.</span><span class="sxs-lookup"><span data-stu-id="ec777-118">It is from this path, rather than the default specified path, that files are to be copied when a volume is backed up.</span></span>

<span data-ttu-id="ec777-119">Альтернативный путь используется только во время операции резервного копирования, и его не следует путать с сопоставлением альтернативного расположения.</span><span class="sxs-lookup"><span data-stu-id="ec777-119">An alternate path is used only during a backup operation and should not be confused with an alternate location mapping.</span></span> <span data-ttu-id="ec777-120">Сопоставление альтернативного расположения используется только во время операций восстановления.</span><span class="sxs-lookup"><span data-stu-id="ec777-120">An alternate location mapping is used only during restore operations.</span></span> <span data-ttu-id="ec777-121">См. также *сопоставление альтернативного расположения*.</span><span class="sxs-lookup"><span data-stu-id="ec777-121">See also *alternate location mapping*.</span></span>

</dd> <dt>

<span data-ttu-id="ec777-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**уровень приложения**</span><span class="sxs-lookup"><span data-stu-id="ec777-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**application level**</span></span>
</dt> <dd>

<span data-ttu-id="ec777-123">Используется службой VSS для указания точки в процессе создания теневой копии, уведомленной модулю записи о замораживании.</span><span class="sxs-lookup"><span data-stu-id="ec777-123">Used by VSS to indicate the point in the course of the creation of a shadow copy that a writer is notified of a freeze.</span></span> <span data-ttu-id="ec777-124">См. также: [*приложения серверной*](vssgloss-b.md)части, [*замораживание*](vssgloss-f.md), [*интерфейсные приложения*](vssgloss-f.md), [*теневое копирование*](vssgloss-s.md), [*приложения на уровне системы*](vssgloss-s.md), [*модуль записи*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="ec777-124">See also [*back-end level applications*](vssgloss-b.md), [*freeze*](vssgloss-f.md), [*front-end level applications*](vssgloss-f.md), [*shadow copy*](vssgloss-s.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec777-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**Автоматическая восстановленная теневая копия**</span><span class="sxs-lookup"><span data-stu-id="ec777-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**auto-recovered shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ec777-126">Теневая копия, которая была дополнительной обработкой модуля записи, должна находиться в полностью стабильном состоянии для операций резервного копирования или интеллектуального анализа данных (например, откатить все транзакции, которые еще не были выполнены в момент создания теневой копии). Это может быть инициировано модулем записи путем указания соответствующего флага из **перечисления \_ \_ флагов компонента VSS** в члене **двкомпонентфлагс** структуры **VSS \_ компонентинфо** или инициатором запроса путем добавления флага **восстановления VSS для \_ \_ \_ отката \_** к контексту для теневой копии.</span><span class="sxs-lookup"><span data-stu-id="ec777-126">A shadow copy that has had additional processing by a writer to be in a completely consistent state for backup or data mining actions (for example, rolling back all transactions that did not yet complete at the point that the shadow copy was created.) This can be initiated by a writer by specifying an appropriate flag from the **VSS\_COMPONENT\_FLAGS** enumeration in the **dwComponentFlags** member of the **VSS\_COMPONENTINFO** structure or by a requester by adding the **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** flag to the context for the shadow copy.</span></span> <span data-ttu-id="ec777-127">Автоматическое восстановление позволяет использовать теневые скопированные данные на томе, доступном только для чтения, для интеллектуального анализа данных, частичного восстановления (например, выбранных элементов в базе данных) или в других целях.</span><span class="sxs-lookup"><span data-stu-id="ec777-127">Auto-recovery allows the shadow copied data to be used on a read-only volume, for data mining, partial restores (for example selected items in a database), or other purposes.</span></span>

<span data-ttu-id="ec777-128">См. также [*транспортную теневую копию*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="ec777-128">See also [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec777-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**Автоматическое освобождение теневого копирования**</span><span class="sxs-lookup"><span data-stu-id="ec777-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**auto-release shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ec777-130">Теневая копия, которая будет удалена после завершения операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ec777-130">A shadow copy that will be deleted upon the termination of a backup operation.</span></span> <span data-ttu-id="ec777-131">Программно, это означает, что теневая копия будет удалена при освобождении интерфейса **ивссбаккупкомпонентс** .</span><span class="sxs-lookup"><span data-stu-id="ec777-131">Programmatically, this means the shadow copy will be deleted when the **IVssBackupComponents** interface is released.</span></span> <span data-ttu-id="ec777-132">Теневая копия автоматического выпуска не может быть постоянной.</span><span class="sxs-lookup"><span data-stu-id="ec777-132">An auto-release shadow copy cannot be persistent.</span></span>

<span data-ttu-id="ec777-133">По умолчанию все теневые копии имеют автоматический выпуск.</span><span class="sxs-lookup"><span data-stu-id="ec777-133">By default, all shadow copies are auto-release.</span></span> <span data-ttu-id="ec777-134">См. также [*Постоянная теневая копия*](vssgloss-p.md), [*Переносимая теневая копия*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="ec777-134">See also [*persistent shadow copy*](vssgloss-p.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> </dl>

 

 



