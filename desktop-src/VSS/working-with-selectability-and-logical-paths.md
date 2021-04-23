---
description: Участие модуля записи в операции резервного копирования или восстановления, а также сведения о том, какие из его данных сохраняются, зависит от того, какие из его компонентов явно включены в документ компонентов резервного копирования инициатора запроса, и на связь между этими компонентами и логическим путем к другим компонентам в документе метаданных модуля записи.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Работа с выборкой и логическими путями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692333"
---
# <a name="working-with-selectability-and-logical-paths"></a><span data-ttu-id="4ec03-103">Работа с выборкой и логическими путями</span><span class="sxs-lookup"><span data-stu-id="4ec03-103">Working with Selectability and Logical Paths</span></span>

<span data-ttu-id="4ec03-104">Участие модуля записи в операции резервного копирования или восстановления, а также сведения о том, какие из его данных сохраняются, зависит от того, какие из его компонентов [*явно включены*](vssgloss-e.md) в документ компонентов резервного копирования инициатора запроса, и на связь между этими компонентами и логическим путем к другим компонентам в документе метаданных модуля записи.</span><span class="sxs-lookup"><span data-stu-id="4ec03-104">A writer's participation in a backup or restore operation, and which of its data are saved, depends on which of its components are [*explicitly included*](vssgloss-e.md) as part of a requester's Backup Components Document and the relationship between those components and the logical path of other components within the Writer Metadata Document.</span></span>

<span data-ttu-id="4ec03-105">Модули записи без компонентов, добавленные в документ компонента резервного копирования инициатора запроса до создания события [*PrepareForBackup*](vssgloss-p.md) (в случае операций резервного копирования) или события предварительного [**восстановления**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (в случае операций восстановления), не получают события после этой точки и не будут участвовать в операции резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="4ec03-105">Writers with no components added to a requester's Backup Component Document prior to the generation of a [*PrepareForBackup*](vssgloss-p.md) event (in the case of backup operations) or of a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event (in the case of restore operations) receive no events after this point and will not participate in the backup or restore operation.</span></span>

<span data-ttu-id="4ec03-106">Тем не менее, чтобы включить или исключить любой заданный компонент в резервной копии или восстановлении, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4ec03-106">However, a requester's freedom to include or exclude any given component in a backup or restore is governed by the following:</span></span>

-   <span data-ttu-id="4ec03-107">Любая иерархия, существующая между компонентами, управляемыми модулем записи и выраженными [ *логическими путями*](vssgloss-l.md)</span><span class="sxs-lookup"><span data-stu-id="4ec03-107">Any hierarchy that exists between the components managed by a writer and expressed by [*logical paths*](vssgloss-l.md)</span></span>
-   <span data-ttu-id="4ec03-108">Назначается ли компонент как [ *выбираемый для резервного копирования*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="4ec03-108">Whether the component is designated as being [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="4ec03-109">Указывает, является ли он [ *выбираемым для восстановления*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="4ec03-109">Whether it is designated as being [*selectable for restore*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="4ec03-110">Существует ли явная зависимость между данным компонентом в заданном средстве записи и другими компонентами в других модулях записи</span><span class="sxs-lookup"><span data-stu-id="4ec03-110">Whether an explicit dependency exists between a given component in a given writer and other components in other writers</span></span>

<span data-ttu-id="4ec03-111">Дополнительные сведения об этих проблемах см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="4ec03-111">More information on these issues is in the following topics:</span></span>

-   [<span data-ttu-id="4ec03-112">Логическое расположение компонентов</span><span class="sxs-lookup"><span data-stu-id="4ec03-112">Logical Pathing of Components</span></span>](logical-pathing-of-components.md)
-   [<span data-ttu-id="4ec03-113">Работа с выборкой для резервного копирования</span><span class="sxs-lookup"><span data-stu-id="4ec03-113">Working with Selectability for Backup</span></span>](working-with-selectability-for-backup.md)
-   [<span data-ttu-id="4ec03-114">Работа с выборкой для восстановления и подкомпонентов</span><span class="sxs-lookup"><span data-stu-id="4ec03-114">Working with Selectability For Restore and Subcomponents</span></span>](working-with-selectability-for-restore-and-subcomponents.md)
-   [<span data-ttu-id="4ec03-115">Выбор и работа со свойствами компонентов</span><span class="sxs-lookup"><span data-stu-id="4ec03-115">Selectability and Working with Component Properties</span></span>](selectability-and-working-with-component-properties.md)
-   [<span data-ttu-id="4ec03-116">Зависимости между компонентами, управляемыми разными модулями записи</span><span class="sxs-lookup"><span data-stu-id="4ec03-116">Dependencies between Components Managed by Different Writers</span></span>](dependencies-between-components-managed-by-different-writers.md)

 

 



