---
description: Прежде чем добавлять или удалять файловые операции из списка дискового пространства, необходимо создать его с помощью функции Сетупкреатедискспацелист.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Использование списка Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662847"
---
# <a name="using-the-disk-space-list"></a><span data-ttu-id="39a91-103">Использование списка Disk-Space</span><span class="sxs-lookup"><span data-stu-id="39a91-103">Using the Disk-Space List</span></span>

<span data-ttu-id="39a91-104">Прежде чем добавлять или удалять файловые операции из списка дискового пространства, необходимо создать его с помощью функции [**сетупкреатедискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="39a91-104">Before you can add or remove file operations from the disk-space list, you must create it by using the [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) function.</span></span>

<span data-ttu-id="39a91-105">После создания списка дискового пространства можно добавить отдельные операции копирования или удаления файлов в список с помощью [**сетупаддтодискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span><span class="sxs-lookup"><span data-stu-id="39a91-105">After you create a disk-space list you can add individual file copy or delete operations to the list by using [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span></span> <span data-ttu-id="39a91-106">Чтобы добавить все операции копирования или удаления файлов во весь раздел INF, используйте функцию [**сетупаддсектионтодискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) или [**сетупаддинсталлсектионтодискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="39a91-106">To add all the file copy or delete operations in an entire INF section, use either the [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) or [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) function.</span></span>

<span data-ttu-id="39a91-107">После добавления всех операций установки в список дискового пространства можно запросить его, чтобы узнать, сколько места на диске требуется для указанной установки с помощью функции [**сетупкуериспацерекуиредондриве**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .</span><span class="sxs-lookup"><span data-stu-id="39a91-107">After you add all the installation operations to the disk-space list, you can query it to find out how much disk space is required for the specified installation by using the [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) function.</span></span>

<span data-ttu-id="39a91-108">Функция [**сетупкуеридривесиндискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) возвращает спецификации диска для каждого целевого диска, на который ссылается файловые операции в списке дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="39a91-108">The [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) function returns the drive specifications for each target drive referenced in the file operations on the disk-space list.</span></span> <span data-ttu-id="39a91-109">Эти сведения можно использовать для программного сравнения доступного пространства на этих дисках с пространством, необходимым для установки.</span><span class="sxs-lookup"><span data-stu-id="39a91-109">You can use this information to programmatically compare the available space on these drives with the space required by the installation.</span></span>

<span data-ttu-id="39a91-110">Чтобы удалить файловую операцию из списка дискового пространства, используйте функцию [**сетупремовефромдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="39a91-110">To remove a file operation from the disk-space list, use the [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) function.</span></span> <span data-ttu-id="39a91-111">Чтобы удалить все операции копирования или удаления файлов из всего раздела INF, используйте функцию [**сетупремовесектионфромдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) или [**сетупремовеинсталлсектионфромдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="39a91-111">To remove all file copy or delete operations from an entire INF section, use the [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) or [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) function.</span></span>

<span data-ttu-id="39a91-112">После того как список дискового пространства больше не требуется, можно освободить ресурсы, выделенные для него, вызвав функцию [**сетупдестройдискспацелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .</span><span class="sxs-lookup"><span data-stu-id="39a91-112">After the disk-space list is no longer required, you can release the resources allocated to it by calling the [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) function.</span></span>

 

 



