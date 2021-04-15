---
description: Сжатие файлов, содержащих преимущественно нули, эффективно использует место на диске.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Разреженные файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662531"
---
# <a name="sparse-files"></a><span data-ttu-id="77003-103">Разреженные файлы</span><span class="sxs-lookup"><span data-stu-id="77003-103">Sparse Files</span></span>

<span data-ttu-id="77003-104">Файл, в котором большая часть данных содержит нули, считается *разреженным набором данных*.</span><span class="sxs-lookup"><span data-stu-id="77003-104">A file in which much of the data is zeros is said to contain a *sparse data set*.</span></span> <span data-ttu-id="77003-105">Такие файлы обычно очень велики, например файл, содержащий данные изображения для обработки или матрицу в высокоскоростной базе данных.</span><span class="sxs-lookup"><span data-stu-id="77003-105">Files like these are typically very large for example, a file that contains image data to be processed or a matrix within a high-speed database.</span></span> <span data-ttu-id="77003-106">Проблема с файлами, содержащими разреженные наборы данных, заключается в том, что большая часть файла не содержит полезных данных и, по этой причине, это неэффективное использование дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="77003-106">The problem with files that contain sparse data sets is that the majority of the file does not contain useful data and, because of this, they are an inefficient use of disk space.</span></span>

<span data-ttu-id="77003-107">Сжатие файлов в файловой системе NTFS является частичным решением проблемы.</span><span class="sxs-lookup"><span data-stu-id="77003-107">The file compression in the NTFS file system is a partial solution to the problem.</span></span> <span data-ttu-id="77003-108">Все данные в файле, которые не были записаны явно, явно устанавливаются в ноль.</span><span class="sxs-lookup"><span data-stu-id="77003-108">All data in the file that is not explicitly written is explicitly set to zero.</span></span> <span data-ttu-id="77003-109">Сжатие файлов сжимает эти диапазоны нулей.</span><span class="sxs-lookup"><span data-stu-id="77003-109">File compression compacts these ranges of zeros.</span></span> <span data-ttu-id="77003-110">Однако недостаток сжатия файлов заключается в том, что время доступа может увеличиться из-за сжатия и распаковки данных.</span><span class="sxs-lookup"><span data-stu-id="77003-110">However, a drawback of file compression is that access time may increase due to data compression and decompression.</span></span>

<span data-ttu-id="77003-111">Поддержка разреженных файлов представлена в файловой системе NTFS другим способом повышения эффективности использования дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="77003-111">Support for sparse files is introduced in the NTFS file system as another way to make disk space usage more efficient.</span></span> <span data-ttu-id="77003-112">Если функция разреженных файлов включена, система не выделяет пространство жесткого диска для файла, за исключением регионов, в которых он содержит ненулевые данные.</span><span class="sxs-lookup"><span data-stu-id="77003-112">When sparse file functionality is enabled, the system does not allocate hard disk drive space to a file except in regions where it contains nonzero data.</span></span> <span data-ttu-id="77003-113">При попытке операции записи, когда большой объем данных в буфере равен нулю, нули не записываются в файл.</span><span class="sxs-lookup"><span data-stu-id="77003-113">When a write operation is attempted where a large amount of the data in the buffer is zeros, the zeros are not written to the file.</span></span> <span data-ttu-id="77003-114">Вместо этого файловая система создает внутренний список, содержащий расположения нулей в файле, и этот список вызывается во время всех операций чтения.</span><span class="sxs-lookup"><span data-stu-id="77003-114">Instead, the file system creates an internal list containing the locations of the zeros in the file, and this list is consulted during all read operations.</span></span> <span data-ttu-id="77003-115">При выполнении операции чтения в областях файла, где были обнаружены нули, файловая система возвращает соответствующее количество нулей в буфере, выделенном для операции чтения.</span><span class="sxs-lookup"><span data-stu-id="77003-115">When a read operation is performed in areas of the file where zeros were located, the file system returns the appropriate number of zeros in the buffer allocated for the read operation.</span></span> <span data-ttu-id="77003-116">Таким образом, Обслуживание разреженного файла прозрачно для всех процессов, обращающихся к нему, и более эффективно, чем сжатие для этого конкретного сценария.</span><span class="sxs-lookup"><span data-stu-id="77003-116">In this way, maintenance of the sparse file is transparent to all processes that access it, and is more efficient than compression for this particular scenario.</span></span>

<span data-ttu-id="77003-117">Значение данных по умолчанию разреженного файла равно нулю. Однако для него можно задать другие значения.</span><span class="sxs-lookup"><span data-stu-id="77003-117">The default data value of a sparse file is zero; however, it can be set to other values.</span></span>

<span data-ttu-id="77003-118">Дополнительные сведения о разреженных файлах см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="77003-118">For more information about sparse files, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77003-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="77003-119">In this section</span></span>



| <span data-ttu-id="77003-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="77003-120">Topic</span></span>                                                                                     | <span data-ttu-id="77003-121">Описание</span><span class="sxs-lookup"><span data-stu-id="77003-121">Description</span></span>                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77003-122">Операции с разреженными файлами</span><span class="sxs-lookup"><span data-stu-id="77003-122">Sparse File Operations</span></span>](sparse-file-operations.md)<br/>                           | <span data-ttu-id="77003-123">Определите, поддерживает ли файловая система разреженные файлы, вызвав функцию Жетволумеинформатион.</span><span class="sxs-lookup"><span data-stu-id="77003-123">Determine whether a file system supports sparse files by calling the GetVolumeInformation function.</span></span><br/>                                                                                |
| [<span data-ttu-id="77003-124">Получение размера разреженного файла</span><span class="sxs-lookup"><span data-stu-id="77003-124">Obtaining the Size of a Sparse File</span></span>](obtaining-the-size-of-a-sparse-file.md)<br/> | <span data-ttu-id="77003-125">Получите выделенный размер или общий размер файла с помощью функции [**жеткомпресседфилесизе**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) или [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) .</span><span class="sxs-lookup"><span data-stu-id="77003-125">Get the allocated size or the total size for a file by using either the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) or the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function.</span></span><br/> |
| [<span data-ttu-id="77003-126">Разреженные файлы и дисковые квоты</span><span class="sxs-lookup"><span data-stu-id="77003-126">Sparse Files and Disk Quotas</span></span>](sparse-files-and-disk-quota.md)<br/>                | <span data-ttu-id="77003-127">Разреженный файл влияет на квоты пользователей по номинальному размеру файла, а не к фактическому выделенному объему дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="77003-127">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span><br/>                                                                  |



 

 

 




