---
description: Инициатор запроса создает документ компонентов резервного копирования в начале выполнения резервного копирования.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Работа с документом компонентов резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692331"
---
# <a name="working-with-the-backup-components-document"></a><span data-ttu-id="8705e-103">Работа с документом компонентов резервного копирования</span><span class="sxs-lookup"><span data-stu-id="8705e-103">Working with the Backup Components Document</span></span>

<span data-ttu-id="8705e-104">Инициатор запроса создает документ компонентов резервного копирования в начале выполнения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8705e-104">A requester creates a Backup Components Document at the start of performing a backup.</span></span> <span data-ttu-id="8705e-105">Изначально документ содержит только описание состояния операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8705e-105">The document initially contains only a description of the state of the backup operation.</span></span> <span data-ttu-id="8705e-106">Во время восстановления документ должен предоставить инструкции о том, как инициатор запроса должен продолжать копирование файлов обратно на диск.</span><span class="sxs-lookup"><span data-stu-id="8705e-106">During restore, the document should provide instructions on how a requester should proceed in copying files back to disk.</span></span> <span data-ttu-id="8705e-107">В ходе операции восстановления документ компонентов резервного копирования изменяется и содержит состояние этой операции.</span><span class="sxs-lookup"><span data-stu-id="8705e-107">In the course of the restore operation, the Backup Components Document is modified and contains the state of that operation.</span></span>

<span data-ttu-id="8705e-108">В отличие от документа метаданных модуля записи, который доступен только для чтения, существует окно, в котором документ компонентов резервного копирования может быть изменен как инициаторами запроса, так и модулями записи.</span><span class="sxs-lookup"><span data-stu-id="8705e-108">Unlike the Writer Metadata Document, which is read-only, there is a window in which the Backup Components Document can be modified by both requesters and writers.</span></span> <span data-ttu-id="8705e-109">Документ можно обновить до создания события [*баккупкомплете*](vssgloss-b.md) или [*баккупшутдовн*](vssgloss-b.md) во время операций резервного копирования и до события, выполняемого при [*восстановлении*](vssgloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="8705e-109">The document can be updated until the generation of a [*BackupComplete*](vssgloss-b.md) or [*BackupShutdown*](vssgloss-b.md) event during backup operations, and until a [*PostRestore*](vssgloss-p.md) event during restores.</span></span>

<span data-ttu-id="8705e-110">Для использования документации по компонентам резервного копирования инициатора запроса необходимо понимание следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="8705e-110">To use a requester's Backup Components Document requires an understanding of the following topics:</span></span>

-   [<span data-ttu-id="8705e-111">Жизненный цикл документа компонентов резервного копирования</span><span class="sxs-lookup"><span data-stu-id="8705e-111">Backup Components Document Life Cycle</span></span>](backup-components-document-life-cycle.md)
-   [<span data-ttu-id="8705e-112">Содержимое документа компонентов резервного копирования</span><span class="sxs-lookup"><span data-stu-id="8705e-112">Backup Components Document Contents</span></span>](backup-components-document-contents.md)

 

 



