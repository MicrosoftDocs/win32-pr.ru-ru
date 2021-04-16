---
description: Помимо операций с файлами в очереди, можно также поставить в очередь все файлы, перечисленные в разделе INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Постановка в очередь раздела INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546394"
---
# <a name="queuing-an-inf-section"></a><span data-ttu-id="7131a-103">Постановка в очередь раздела INF</span><span class="sxs-lookup"><span data-stu-id="7131a-103">Queuing an INF Section</span></span>

<span data-ttu-id="7131a-104">Помимо операций с файлами в очереди, можно также поставить в очередь все файлы, перечисленные в разделе INF.</span><span class="sxs-lookup"><span data-stu-id="7131a-104">In addition to queuing file operations individually, you can also queue all the files listed in an INF section.</span></span>

<span data-ttu-id="7131a-105">Вы можете поместить в очередь все файлы, перечисленные в разделе " **копирование файлов** " INF-файла, вызвав [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span><span class="sxs-lookup"><span data-stu-id="7131a-105">You can queue all the files listed in a **Copy Files** section of an INF file by calling [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span></span> <span data-ttu-id="7131a-106">Чтобы эта функция была успешной, раздел **Copy Files** должен иметь правильный формат, а INF-файл или один из его добавленных файлов должен содержать разделы **саурцедисксфилес** и **саурцедискснамес** .</span><span class="sxs-lookup"><span data-stu-id="7131a-106">For this function to be successful, the **Copy Files** section must be in the proper format and the INF file, or one of its appended files, must contain the **SourceDisksFiles** and **SourceDisksNames** sections.</span></span>

<span data-ttu-id="7131a-107">Аналогично, если вы хотите удалить все файлы, указанные в разделе **Удаление файлов** INF-файла, можно вызвать [**сетупкуеуеделетесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span><span class="sxs-lookup"><span data-stu-id="7131a-107">Similarly, if you want to delete all the files specified in a **Delete Files** section of an INF file, you can call [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span></span> <span data-ttu-id="7131a-108">Чтобы переименовать все файлы в разделе " **Переименование файлов** " INF-файла, используйте [**сетупкуеуеренамесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span><span class="sxs-lookup"><span data-stu-id="7131a-108">To rename all the files in a **Rename Files** section of an INF file use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span></span>

 

 



