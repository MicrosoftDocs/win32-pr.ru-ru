---
title: Предварительное выделение дискового пространства для файла записи
description: Предварительное выделение дискового пространства для файла записи
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- Сообщение WM_CAP_FILE_ALLOCATE
- макрос Капфилеаллок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329627"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a><span data-ttu-id="d82e7-105">Предварительное выделение дискового пространства для файла записи</span><span class="sxs-lookup"><span data-stu-id="d82e7-105">Disk Space Preallocation for the Capture File</span></span>

<span data-ttu-id="d82e7-106">Предварительное выделение дискового пространства для файла записи создает файл указанного размера на диске перед началом операции записи.</span><span class="sxs-lookup"><span data-stu-id="d82e7-106">Preallocating disk space for the capture file builds a file of a specified size on the disk before the start of a capture operation.</span></span> <span data-ttu-id="d82e7-107">Предварительное выделение файла записи сокращает объем обработки, необходимый для выполнения записи, и приводит к уменьшению количества удаленных кадров.</span><span class="sxs-lookup"><span data-stu-id="d82e7-107">Preallocating a capture file reduces the processing required while capture is in progress and results in fewer dropped frames.</span></span> <span data-ttu-id="d82e7-108">Вы можете предварительно выделить файл записи с помощью сообщения [**о \_ \_ \_ выделении файла**](wm-cap-file-allocate.md) (или макроса [**Капфилеаллок**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ) с закреплениями WM.</span><span class="sxs-lookup"><span data-stu-id="d82e7-108">You can preallocate a capture file by using the [**WM\_CAP\_FILE\_ALLOCATE**](wm-cap-file-allocate.md) message (or the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro).</span></span>

<span data-ttu-id="d82e7-109">Как правило, приложение должно предварительно выделить достаточно места на диске, чтобы вместить самый большой из ожидаемых файлов записи.</span><span class="sxs-lookup"><span data-stu-id="d82e7-109">Typically, your application should preallocate enough disk space to contain the largest capture file anticipated.</span></span> <span data-ttu-id="d82e7-110">Предварительное выделение дискового пространства не ограничивает размер захваченного файла.</span><span class="sxs-lookup"><span data-stu-id="d82e7-110">Preallocating disk space does not restrict the size of the captured file.</span></span> <span data-ttu-id="d82e7-111">Размер файла автоматически увеличивается, если захваченные данные выходят за пределы выделенного пространства.</span><span class="sxs-lookup"><span data-stu-id="d82e7-111">The file size is automatically enlarged if the captured data exceeds the allocated space.</span></span> <span data-ttu-id="d82e7-112">Последующие операции записи в файл записи повторно используют части места на диске, выделенные для файла, сохраняя размер и фрагментацию файла.</span><span class="sxs-lookup"><span data-stu-id="d82e7-112">Subsequent write operations to the capture file reuse the portions of disk space allocated for the file, preserving the size and fragmentation of the file.</span></span>

<span data-ttu-id="d82e7-113">Можно также повысить производительность записи, дефрагментацию файла записи.</span><span class="sxs-lookup"><span data-stu-id="d82e7-113">You can also improve capture performance by defragmenting the capture file.</span></span> <span data-ttu-id="d82e7-114">Для дефрагментации файла используйте программу дефрагментации, например дефрагментацию диска.</span><span class="sxs-lookup"><span data-stu-id="d82e7-114">To defragment the file, use a defragmentation utility such as Disk Defragmenter.</span></span> <span data-ttu-id="d82e7-115">Если вы используете дефрагментированный файл записи и затем увеличите его, следует дефрагментировать увеличенный файл.</span><span class="sxs-lookup"><span data-stu-id="d82e7-115">If you use a defragmented capture file and later enlarge it, you should defragment the enlarged file.</span></span> <span data-ttu-id="d82e7-116">Увеличение дефрагментированного файла записи может фрагментировать развернутую часть файла и снизить производительность операции записи.</span><span class="sxs-lookup"><span data-stu-id="d82e7-116">Enlarging a defragmented capture file can fragment the expanded portion of the file and reduce performance in the capture operation.</span></span>

<span data-ttu-id="d82e7-117">Вы также можете повысить производительность, используя несжатый диск для записи видео.</span><span class="sxs-lookup"><span data-stu-id="d82e7-117">You might also improve performance by using an uncompressed disk for video capture.</span></span> <span data-ttu-id="d82e7-118">Сжатие данных во время записи может ограничить пропускную способность записи на диск.</span><span class="sxs-lookup"><span data-stu-id="d82e7-118">Compressing data during capture can limit capture throughput to the disk.</span></span>

<span data-ttu-id="d82e7-119">Приложение может зарезервировать постоянный файл записи, чтобы исключить время, необходимое для предварительного выделения и дефрагментации файла при каждом запуске.</span><span class="sxs-lookup"><span data-stu-id="d82e7-119">An application can reserve a permanent capture file to eliminate the time required to preallocate and defragment a file each time it is started.</span></span> <span data-ttu-id="d82e7-120">Поскольку файл записи может потребовать значительного места на диске, а предварительное выделение файла записи удаляет все данные из существующего файла записи, приложение должно позволить пользователю решить, является ли файл постоянным или временным.</span><span class="sxs-lookup"><span data-stu-id="d82e7-120">Because a capture file can require considerable disk space, and preallocating a capture file removes all data from an existing capture file, an application should let the user decide if the file is permanent or temporary.</span></span>

 

 




