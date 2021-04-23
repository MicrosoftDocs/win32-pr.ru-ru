---
description: При обработке резервной копии инициаторы запроса и записи полагаются на стабильный образ системы, из которого можно выполнять резервное копирование данных (теневое копирование тома), а также объединять файлы в группы на основе их использования и сохранять информацию о сохраненных данных.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Общие сведения об обработке резервной копии в VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345022"
---
# <a name="overview-of-processing-a-backup-under-vss"></a><span data-ttu-id="2df97-103">Общие сведения об обработке резервной копии в VSS</span><span class="sxs-lookup"><span data-stu-id="2df97-103">Overview of Processing a Backup Under VSS</span></span>

<span data-ttu-id="2df97-104">При обработке резервной копии инициаторы запроса и записи полагаются на стабильный образ системы, из которого можно выполнять резервное копирование данных (теневое копирование тома), а также объединять файлы в группы на основе их использования и сохранять информацию о сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="2df97-104">In processing a backup, requester and writers coordinate to provide a stable system image from which to back up data (the shadow copied volume), to group files together on the basis of their usage, and to store information on the saved data.</span></span> <span data-ttu-id="2df97-105">Это необходимо сделать при создании лишь минимального перерыва в нормальном рабочем потоке модуля записи.</span><span class="sxs-lookup"><span data-stu-id="2df97-105">This must all be done while creating only minimal interruption to the writer's normal work flow.</span></span>

<span data-ttu-id="2df97-106">Запросивший запрос запрашивает свои метаданные, обрабатывает эти данные, уведомляет модули записи до начала теневой копии и операций резервного копирования, а затем уведомляет модули записи после завершения операции теневого копирования и резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="2df97-106">A requester queries writers for their metadata, processes this data, notifies the writers prior to the beginning of the shadow copy and of the backup operations, and then notifies the writers again after the shadow copy and backup operations end.</span></span>

<span data-ttu-id="2df97-107">В ответ на эти уведомления модуль записи предоставляет сведения о файлах для резервного копирования, включая указание групп файлов для координации ([*компонентов*](vssgloss-c.md)), приостанавливает операции ввода-вывода до создания теневой копии, а затем возвращается к нормальной работе после завершения теневой копии или в конце резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2df97-107">In response to these notifications, the writer provides information about files to be backed up—including specifying groups of files to coordinate ([*components*](vssgloss-c.md))—pauses in its I/O operations prior to a shadow copy, and then returns to normal operation following the completion of a shadow copy or at the end of the backup.</span></span>

<span data-ttu-id="2df97-108">В процессе обработки резервной копии модуль записи определяет файлы, за которыми он отвечает, с помощью его метаданных, предназначенных только для чтения — документа метаданных модуля записи (см. раздел [метаданные VSS: работа с документом метаданных модуля записи](working-with-the-writer-metadata-document.md)).</span><span class="sxs-lookup"><span data-stu-id="2df97-108">In the course of processing the backup, a writer specifies the files it is responsible for through its read-only metadata—the Writer Metadata Document (see [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)).</span></span> <span data-ttu-id="2df97-109">Затем запрашивающая сторона интерпретирует эти метаданные, выбирает, что следует архивировать, и сохраняет эти решения в собственном объекте метаданных, документе резервных компонентов (см. [метаданные VSS](working-with-the-backup-components-document.md)).</span><span class="sxs-lookup"><span data-stu-id="2df97-109">The requester then interprets this metadata, chooses what to back up, and stores these decisions in its own metadata object, the Backup Components Document (see [VSS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)).</span></span> <span data-ttu-id="2df97-110">Этот документ компонентов резервного копирования доступен для проверки и изменения модуля записи во время операций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="2df97-110">This Backup Components Document is available for writer inspection and modification during both the backup and restore operations.</span></span>

<span data-ttu-id="2df97-111">На этой диаграмме показано взаимодействие между инициатором запроса, службой VSS, поддержкой ядра VSS, всеми вовлеченными модулями записи VSS и поставщиками оборудования VSS.</span><span class="sxs-lookup"><span data-stu-id="2df97-111">This diagram shows the interactions between the requester, the VSS service, the VSS kernel support, any VSS writers involved, and any VSS hardware providers.</span></span>

![взаимодействие между инициатором запроса, компонентами резервного копирования, модулями записи и поставщиками](images/vssimpl.png)

<span data-ttu-id="2df97-113">Чтобы более полно понять основные задачи, связанные с выполнением резервного копирования, полезно разбить этот обзор на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="2df97-113">To more fully understand the basic tasks involved in performing a backup, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="2df97-114">Общие сведения об инициализации резервного копирования</span><span class="sxs-lookup"><span data-stu-id="2df97-114">Overview of Backup Initialization</span></span>](overview-of-backup-initialization.md)
-   [<span data-ttu-id="2df97-115">Обзор фазы обнаружения резервных копий</span><span class="sxs-lookup"><span data-stu-id="2df97-115">Overview of the Backup Discovery Phase</span></span>](overview-of-the-backup-discovery-phase.md)
-   [<span data-ttu-id="2df97-116">Общие сведения о задачах, выполняемых перед резервным копированием</span><span class="sxs-lookup"><span data-stu-id="2df97-116">Overview of Pre-Backup Tasks</span></span>](overview-of-pre-backup-tasks.md)
-   [<span data-ttu-id="2df97-117">Общие сведения о фактическом резервном копировании файлов</span><span class="sxs-lookup"><span data-stu-id="2df97-117">Overview of Actual Backup Of Files</span></span>](overview-of-actual-backup-of-files.md)
-   [<span data-ttu-id="2df97-118">Общие сведения о завершении резервного копирования</span><span class="sxs-lookup"><span data-stu-id="2df97-118">Overview of Backup Termination</span></span>](overview-of-backup-termination.md)

 

 



