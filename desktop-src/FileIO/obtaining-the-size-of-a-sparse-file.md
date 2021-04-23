---
description: Получите выделенный размер или общий размер файла с помощью функции Жеткомпресседфилесизе или GetFileSize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Получение размера разреженного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897822"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a><span data-ttu-id="685aa-103">Получение размера разреженного файла</span><span class="sxs-lookup"><span data-stu-id="685aa-103">Obtaining the Size of a Sparse File</span></span>

<span data-ttu-id="685aa-104">Используйте функцию [**жеткомпресседфилесизе**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) , чтобы получить фактический размер, выделенный на диске для разреженного файла.</span><span class="sxs-lookup"><span data-stu-id="685aa-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the actual size allocated on disk for a sparse file.</span></span> <span data-ttu-id="685aa-105">Этот итог не включает размер регионов, которые были освобождены, так как они заполнены нулями.</span><span class="sxs-lookup"><span data-stu-id="685aa-105">This total does not include the size of the regions which were deallocated because they were filled with zeros.</span></span> <span data-ttu-id="685aa-106">Используйте функцию [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) , чтобы определить общий размер файла, включая размер разреженных регионов, которые были освобождены.</span><span class="sxs-lookup"><span data-stu-id="685aa-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the total size of a file, including the size of the sparse regions that were deallocated.</span></span>

 

 



