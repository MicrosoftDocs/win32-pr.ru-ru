---
description: Чтобы получить сжатый размер файла, используйте функцию Жеткомпресседфилесизе.
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: Получение размера сжатого файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4954a53184e55341838fef7cd70f01639f13bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542754"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a><span data-ttu-id="1d0a6-103">Получение размера сжатого файла</span><span class="sxs-lookup"><span data-stu-id="1d0a6-103">Obtaining the Size of a Compressed File</span></span>

<span data-ttu-id="1d0a6-104">Чтобы получить сжатый размер файла, используйте функцию [**жеткомпресседфилесизе**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) .</span><span class="sxs-lookup"><span data-stu-id="1d0a6-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the compressed size of a file.</span></span> <span data-ttu-id="1d0a6-105">Если файл сжат, его сжатый размер будет меньше его несжатого размера.</span><span class="sxs-lookup"><span data-stu-id="1d0a6-105">If the file is compressed, its compressed size will be less than its uncompressed size.</span></span> <span data-ttu-id="1d0a6-106">Для определения несжатого размера файла используйте функцию [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) .</span><span class="sxs-lookup"><span data-stu-id="1d0a6-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the uncompressed size of a file.</span></span>

 

 



