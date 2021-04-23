---
description: Приложение считывает данные из файла и выполняет запись в него с помощью функций ReadFile, Реадфиликс, WriteFile и Вритефиликс.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Чтение и запись в файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664049"
---
# <a name="reading-from-and-writing-to-files"></a><span data-ttu-id="abbaa-103">Чтение и запись в файлы</span><span class="sxs-lookup"><span data-stu-id="abbaa-103">Reading From and Writing to Files</span></span>

<span data-ttu-id="abbaa-104">Приложение считывает данные из файла и выполняет запись в него с помощью функций [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)и [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .</span><span class="sxs-lookup"><span data-stu-id="abbaa-104">An application reads from and writes to a file by using the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) functions.</span></span> <span data-ttu-id="abbaa-105">Для этих функций требуется, чтобы файл был открыт для чтения и записи соответственно.</span><span class="sxs-lookup"><span data-stu-id="abbaa-105">These functions require a handle to a file to be opened for reading and writing, respectively.</span></span> <span data-ttu-id="abbaa-106">Они считывают и записывают заданное число байтов в расположении, указанном указателем файла.</span><span class="sxs-lookup"><span data-stu-id="abbaa-106">They read and write a specified number of bytes at the location indicated by the file pointer.</span></span> <span data-ttu-id="abbaa-107">Данные считываются и записываются в точности так, как указано. функции не отформатируют данные.</span><span class="sxs-lookup"><span data-stu-id="abbaa-107">The data is read and written exactly as specified; the functions do not format the data.</span></span>

<span data-ttu-id="abbaa-108">Когда указатель файла достигает конца файла и приложение пытается выполнить чтение из файла, ошибка не возникает, но байты не считываются.</span><span class="sxs-lookup"><span data-stu-id="abbaa-108">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="abbaa-109">Поэтому чтение нулевых байтов без ошибки означает, что приложение достиг конца файла.</span><span class="sxs-lookup"><span data-stu-id="abbaa-109">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="abbaa-110">При записи нулевых байтов ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="abbaa-110">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="abbaa-111">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="abbaa-111">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="abbaa-112">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="abbaa-112">In this section</span></span>



| <span data-ttu-id="abbaa-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="abbaa-113">Topic</span></span>                                                                                                                                           | <span data-ttu-id="abbaa-114">Описание</span><span class="sxs-lookup"><span data-stu-id="abbaa-114">Description</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abbaa-115">Размещение указателя на файл</span><span class="sxs-lookup"><span data-stu-id="abbaa-115">Positioning a File Pointer</span></span>](positioning-a-file-pointer.md)<br/>                                                                         | <span data-ttu-id="abbaa-116">Windows использует указатель на файл для хранения прочитанных или записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="abbaa-116">Windows uses a file pointer to keep track of bytes read or written.</span></span><br/>                                                       |
| [<span data-ttu-id="abbaa-117">Чтение или запись в файлы с помощью схемы Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="abbaa-117">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | <span data-ttu-id="abbaa-118">Описывает схему разбивки на части для чтения или записи несмежных фрагментов данных за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="abbaa-118">Describes a scatter-gather scheme for reading or writing noncontiguous chunks of data in one operation.</span></span><br/>                   |
| [<span data-ttu-id="abbaa-119">Сброс System-Buffered данных ввода-вывода на диск</span><span class="sxs-lookup"><span data-stu-id="abbaa-119">Flushing System-Buffered I/O Data to Disk</span></span>](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | <span data-ttu-id="abbaa-120">Windows хранит данные в операциях чтения и записи файлов в системных буферах данных для оптимизации производительности диска.</span><span class="sxs-lookup"><span data-stu-id="abbaa-120">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span><br/> |
| [<span data-ttu-id="abbaa-121">Усечение или расширение файлов</span><span class="sxs-lookup"><span data-stu-id="abbaa-121">Truncating or Extending Files</span></span>](truncating-or-extending-files.md)<br/>                                                                   | <span data-ttu-id="abbaa-122">Приложение может усечь или расширить файл путем вызова [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="abbaa-122">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span><br/>                             |



 

 

 




