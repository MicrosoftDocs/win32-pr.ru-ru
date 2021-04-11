---
description: Разреженный файл влияет на квоты пользователей по номинальному размеру файла, а не к фактическому выделенному объему дискового пространства.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Разреженные файлы и дисковые квоты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154603"
---
# <a name="sparse-files-and-disk-quotas"></a><span data-ttu-id="8cfa4-103">Разреженные файлы и дисковые квоты</span><span class="sxs-lookup"><span data-stu-id="8cfa4-103">Sparse Files and Disk Quotas</span></span>

<span data-ttu-id="8cfa4-104">Разреженный файл влияет на квоты пользователей по номинальному размеру файла, а не к фактическому выделенному объему дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="8cfa4-104">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span> <span data-ttu-id="8cfa4-105">Это значит, что создание файла размером 50 МБ со всеми нулевыми байтами потребляет 50 Мб квоты этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8cfa4-105">That is, creating a 50-MB file with all zero bytes consumes 50 MB of that user's quota.</span></span> <span data-ttu-id="8cfa4-106">Это означает, что, когда пользователь записывает данные в разреженный файл, ему не нужно беспокоиться о превышении предельной квоты, так как он уже заряжен на место.</span><span class="sxs-lookup"><span data-stu-id="8cfa4-106">This means that as the user writes data to the sparse file, he need not worry about exceeding his hard quota limit, because he has already been charged for the space.</span></span> <span data-ttu-id="8cfa4-107">Системные администраторы не должны подсчитывать размер разреженного файла, который остался небольшим.</span><span class="sxs-lookup"><span data-stu-id="8cfa4-107">System administrators should not count on the size of a sparse file remaining small.</span></span> <span data-ttu-id="8cfa4-108">Поэтому они не должны предоставлять пользователям ограничения на жесткие квоты, превышающие доступное физическое пространство, несмотря на использование разреженных файлов.</span><span class="sxs-lookup"><span data-stu-id="8cfa4-108">Therefore they should not grant their users hard quota limits that exceed the physical space available, despite the use of sparse files.</span></span>

 

 



