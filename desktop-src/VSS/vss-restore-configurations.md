---
description: Восстановление файлов в работающей системе может быть проблематичным. Важно, чтобы работающие приложения (модули записи) указывали, что делать при возникновении трудностей во время восстановления, например, если восстанавливаемый файл используется в данный момент.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Конфигурации восстановления VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145217"
---
# <a name="vss-restore-configurations"></a><span data-ttu-id="3f494-104">Конфигурации восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="3f494-104">VSS Restore Configurations</span></span>

<span data-ttu-id="3f494-105">Восстановление файлов в работающей системе может быть проблематичным.</span><span class="sxs-lookup"><span data-stu-id="3f494-105">File restoration on a running system can be problematic.</span></span> <span data-ttu-id="3f494-106">Важно, чтобы работающие приложения (модули записи) указывали, что делать при возникновении трудностей во время восстановления, например, если восстанавливаемый файл используется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3f494-106">It is important that running applications (writers) indicate what to do when difficulties arise during restores, for instance, if the file being restored is currently in use.</span></span>

<span data-ttu-id="3f494-107">В VSS модули записи имеют два дополнительных способа управления восстановлением —[*методы восстановления*](vssgloss-r.md) и [*целевые объекты восстановления*](vssgloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="3f494-107">Under VSS, writers have two complementary ways of managing restores—[*restore methods*](vssgloss-r.md) and [*restore targets*](vssgloss-r.md).</span></span>

<span data-ttu-id="3f494-108">Кроме того, инициаторы запроса могут восстанавливать файлы в ранее неуказанных расположениях и уведомлять модули записи (см. [**ивссбаккупкомпонентс:: аддневтаржет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span><span class="sxs-lookup"><span data-stu-id="3f494-108">In addition, requesters can choose to restore files to previously unspecified locations and notify writers (see [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span></span>

<span data-ttu-id="3f494-109">Метод Restore (также называемый исходным целевым объектом восстановления) задается модулем записи во время резервного копирования и задает определение метода в масштабе записи, которое будет использоваться для восстановления всех его компонентов в будущем.</span><span class="sxs-lookup"><span data-stu-id="3f494-109">The restore method (also call the original restore target) is specified by a writer at a backup time, and sets a writer-wide definition of the method to be used to restore all its components in the future.</span></span> <span data-ttu-id="3f494-110">Все файлы и компоненты, управляемые модулем записи, используют один и тот же метод Restore.</span><span class="sxs-lookup"><span data-stu-id="3f494-110">All files and components managed by a writer share the same restore method.</span></span>

<span data-ttu-id="3f494-111">Целевые объекты восстановления позволяют модулям записи изменять способ восстановления конкретных компонентов во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="3f494-111">Restore targets allow writers to change how specific components are to be restored at restore time.</span></span> <span data-ttu-id="3f494-112">В отличие от методов восстановления, целевые объекты восстановления определены для набора компонентов.</span><span class="sxs-lookup"><span data-stu-id="3f494-112">Unlike restore methods, restore targets are defined for a component set.</span></span>

<span data-ttu-id="3f494-113">Подробное обсуждение использования методов восстановления и целевых объектов восстановления см. в разделах, перечисленных ниже.</span><span class="sxs-lookup"><span data-stu-id="3f494-113">A detailed discussion of the usage of restore methods and restore targets is found in the topics listed below:</span></span>

-   [<span data-ttu-id="3f494-114">Состояние восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="3f494-114">VSS Restore State</span></span>](vss-restore-state.md)
-   [<span data-ttu-id="3f494-115">Настройка методов восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="3f494-115">Setting VSS Restore Methods</span></span>](setting-vss-restore-methods.md)
-   [<span data-ttu-id="3f494-116">Настройка целевых объектов восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="3f494-116">Setting VSS Restore Targets</span></span>](setting-vss-restore-targets.md)
-   [<span data-ttu-id="3f494-117">Настройка параметров восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="3f494-117">Setting VSS Restore Options</span></span>](setting-vss-restore-options.md)

<span data-ttu-id="3f494-118">(Сведения о восстановлении, которые не используют эти механизмы, см. в разделе [восстановление без участия в записи](restores-without-writer-participation.md).)</span><span class="sxs-lookup"><span data-stu-id="3f494-118">(For information on restores that do not use these mechanisms, see [Restores without Writer Participation](restores-without-writer-participation.md).)</span></span>

 

 



