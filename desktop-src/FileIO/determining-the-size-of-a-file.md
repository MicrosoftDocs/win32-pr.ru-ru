---
description: Функция GetFileSize получает размер файла.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Определение размера файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998639"
---
# <a name="determining-the-size-of-a-file"></a><span data-ttu-id="6c63a-103">Определение размера файла</span><span class="sxs-lookup"><span data-stu-id="6c63a-103">Determining the Size of a File</span></span>

<span data-ttu-id="6c63a-104">Функция [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) получает размер файла.</span><span class="sxs-lookup"><span data-stu-id="6c63a-104">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span>

<span data-ttu-id="6c63a-105">Поскольку реализация файлов в файловой системе NTFS позволяет использовать несколько потоков в файле, любое приложение, которое записывает доступ к файлам, должно учитывать возможность того, что создатель файла может включать в него несколько потоков.</span><span class="sxs-lookup"><span data-stu-id="6c63a-105">Because the NTFS file system implementation of files allows for multiple streams within a file, any application you write that accesses files must account for the possibility that the creator of the file can include multiple streams in the file.</span></span> <span data-ttu-id="6c63a-106">Если в файле не проверяются несколько потоков, приложение может недооценивать общий размер файла, помимо других ошибок.</span><span class="sxs-lookup"><span data-stu-id="6c63a-106">If multiple streams are not checked for in a file, the application can underestimate the total size of the file, among other errors.</span></span>

 

 



