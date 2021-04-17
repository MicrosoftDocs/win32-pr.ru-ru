---
description: Для чтения из представления файла следует обращаться к указателю, возвращенному функцией MapViewOfFile, как показано в примерах ниже.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Чтение и запись в представлении файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684589"
---
# <a name="reading-and-writing-from-a-file-view"></a><span data-ttu-id="77783-103">Чтение и запись в представлении файлов</span><span class="sxs-lookup"><span data-stu-id="77783-103">Reading and Writing From a File View</span></span>

<span data-ttu-id="77783-104">Для чтения из представления файла следует обращаться к указателю, возвращенному функцией [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , как показано в примерах ниже.</span><span class="sxs-lookup"><span data-stu-id="77783-104">To read from a file view, dereference the pointer returned by the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function as shown in the examples below.</span></span>

<span data-ttu-id="77783-105">Чтение или запись в представлении файла, отличного от файла подкачки, может вызвать исключение в случае **\_ \_ \_ ошибки страницы** .</span><span class="sxs-lookup"><span data-stu-id="77783-105">Reading from or writing to a file view of a file other than the page file can cause an **EXCEPTION\_IN\_PAGE\_ERROR** exception.</span></span> <span data-ttu-id="77783-106">Например, если соединение с сервером потеряно, доступ к сопоставленному файлу, расположенному на удаленном сервере, может вызвать исключение.</span><span class="sxs-lookup"><span data-stu-id="77783-106">For example, accessing a mapped file that resides on a remote server can generate an exception if the connection to the server is lost.</span></span> <span data-ttu-id="77783-107">Исключения также могут возникать из-за переполнения диска, сбоя основного устройства или сбоя выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="77783-107">Exceptions can also occur because of a full disk, an underlying device failure, or a memory allocation failure.</span></span> <span data-ttu-id="77783-108">При записи в представление файла исключения также могут возникать из-за того, что файл является общим, а другой процесс блокирует диапазон байтов.</span><span class="sxs-lookup"><span data-stu-id="77783-108">When writing to a file view, exceptions can also occur because the file is shared and a different process has locked a byte range.</span></span> <span data-ttu-id="77783-109">Чтобы защититься от исключений из-за ошибок ввода-вывода, все попытки доступа к отображенным в памяти файлам должны быть заключены в структурированные обработчики исключений.</span><span class="sxs-lookup"><span data-stu-id="77783-109">To guard against exceptions due to input and output (I/O) errors, all attempts to access memory mapped files should be wrapped in structured exception handlers.</span></span> <span data-ttu-id="77783-110">При получении **исключения \_ на \_ странице \_ Ошибка** в фильтре, **\_ \_ Кроме** , убедитесь, что адрес находится в текущем сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="77783-110">When you receive **EXCEPTION\_IN\_PAGE\_ERROR** in your **\_\_except** filter, make sure that the address is within the mapping you are currently accessing.</span></span> <span data-ttu-id="77783-111">Если это так, восстановите или завершите работу успешно. в противном случае не обрабатывайте исключение.</span><span class="sxs-lookup"><span data-stu-id="77783-111">If so, recover or fail gracefully; otherwise, do not handle the exception.</span></span>

<span data-ttu-id="77783-112">В следующем примере используется указатель, возвращенный **MapViewOfFile** для чтения из представления файлов:</span><span class="sxs-lookup"><span data-stu-id="77783-112">The following example uses the pointer returned by **MapViewOfFile** to read from the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



<span data-ttu-id="77783-113">В следующем примере используется указатель, возвращенный функцией **MapViewOfFile** для записи в представление файла:</span><span class="sxs-lookup"><span data-stu-id="77783-113">The following example uses the pointer returned by **MapViewOfFile** to write to the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



<span data-ttu-id="77783-114">Функция [**флушвиевоффиле**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) Копирует указанное число байтов представления файла в физический файл, не дожидаясь возникновения кэшированной операции записи:</span><span class="sxs-lookup"><span data-stu-id="77783-114">The [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function copies the specified number of bytes of the file view to the physical file, without waiting for the cached write operation to occur:</span></span>


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



<span data-ttu-id="77783-115">При сопоставлении сжатого или разреженного файла в разделе NTFS может возникнуть дополнительная ошибка ввода-вывода при разбиении на страницы в части файла.</span><span class="sxs-lookup"><span data-stu-id="77783-115">If you are mapping a compressed or sparse file on an NTFS partition, there is additional potential for an I/O error when paging in a portion of the file.</span></span> <span data-ttu-id="77783-116">В этом случае адресное пространство, сопоставленное [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , может не поддерживаться выделенным дисковым пространством.</span><span class="sxs-lookup"><span data-stu-id="77783-116">In this case, the address space mapped by [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) may not be backed by allocated disk space.</span></span> <span data-ttu-id="77783-117">Это связано с тем, что разреженный файл может иметь области нулей, для которых NTFS не выделяет место на диске, а сжатый файл может занимать меньше места на диске, чем фактические данные, которые он представляет.</span><span class="sxs-lookup"><span data-stu-id="77783-117">This is because a sparse file can have regions of zeros for which NTFS does not allocate disk space, and a compressed file can take up less disk space than the actual data that it represents.</span></span> <span data-ttu-id="77783-118">При чтении или записи в часть разреженного или сжатого файла, который не поддерживается дисковым пространством, операционная система может попытаться выделить место на диске.</span><span class="sxs-lookup"><span data-stu-id="77783-118">If you read from or write to a portion of a sparse or compressed file that is not backed by disk space, the operating system may try to allocate disk space.</span></span> <span data-ttu-id="77783-119">Если диск заполнен, это может привести к возникновению исключения, указывающего на ошибку ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="77783-119">If the disk is full, this can result in an exception indicating an I/O error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77783-120">См. также</span><span class="sxs-lookup"><span data-stu-id="77783-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77783-121">Структурированная обработка исключений</span><span class="sxs-lookup"><span data-stu-id="77783-121">Structured Exception Handling</span></span>](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
