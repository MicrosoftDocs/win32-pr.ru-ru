---
description: Операции резервного копирования и восстановления обычно копируют файлы из заданного расположения по умолчанию на диск для резервного носителя, а затем восстанавливаются с этого носителя в то же расположение по умолчанию на диске.
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: Расположения резервного копирования и восстановления не по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692902"
---
# <a name="non-default-backup-and-restore-locations"></a><span data-ttu-id="828d6-103">Расположения резервного копирования и восстановления не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="828d6-103">Non-Default Backup and Restore Locations</span></span>

<span data-ttu-id="828d6-104">Операции резервного копирования и восстановления обычно копируют файлы из заданного расположения по умолчанию на диск для резервного носителя, а затем восстанавливаются с этого носителя в то же расположение по умолчанию на диске.</span><span class="sxs-lookup"><span data-stu-id="828d6-104">Backup and restore operations typically copy files from a given, default location on disk to backup media and then restore from that media to the same default location on disk.</span></span>

<span data-ttu-id="828d6-105">Существует множество причин, особенно при работе с запущенными процессами, а не для выполнения этой простой модели.</span><span class="sxs-lookup"><span data-stu-id="828d6-105">There are many reasons, particularly when dealing with running processes, not to follow this simple model.</span></span> <span data-ttu-id="828d6-106">VSS поддерживает использование нестандартных источников для резервного копирования и альтернативных целевых объектов для восстановления и включает механизмы для работы с подмножествами файлов и сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="828d6-106">VSS supports using nonstandard sources for backup and alternate destinations for restore, and includes mechanisms to work with subsets of files and to remap files.</span></span>

-   [<span data-ttu-id="828d6-107">Работа с альтернативными путями во время резервного копирования</span><span class="sxs-lookup"><span data-stu-id="828d6-107">Working with Alternate Paths during Backup</span></span>](working-with-alternate-paths-during-backup.md)
-   [<span data-ttu-id="828d6-108">Работа с альтернативными расположениями во время восстановления</span><span class="sxs-lookup"><span data-stu-id="828d6-108">Working with Alternate Locations during Restore</span></span>](working-with-alternate-locations-during-restore.md)
-   [<span data-ttu-id="828d6-109">Работа с новыми целевыми объектами во время восстановления</span><span class="sxs-lookup"><span data-stu-id="828d6-109">Working with New Targets during Restore</span></span>](working-with-new-targets-during-restore.md)
-   [<span data-ttu-id="828d6-110">Работа с частичными файлами</span><span class="sxs-lookup"><span data-stu-id="828d6-110">Working with Partial Files</span></span>](working-with-partial-files.md)
-   [<span data-ttu-id="828d6-111">Работа с направленными целями</span><span class="sxs-lookup"><span data-stu-id="828d6-111">Working with Directed Targets</span></span>](working-with-directed-targets.md)

 

 



