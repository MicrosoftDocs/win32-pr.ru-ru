---
description: Windows хранит данные в операциях чтения и записи файлов в системных буферах данных для оптимизации производительности диска.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Сброс System-Buffered данных ввода-вывода на диск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546690"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a><span data-ttu-id="d59f2-103">Сброс System-Buffered данных ввода-вывода на диск</span><span class="sxs-lookup"><span data-stu-id="d59f2-103">Flushing System-Buffered I/O Data to Disk</span></span>

<span data-ttu-id="d59f2-104">Windows хранит данные в операциях чтения и записи файлов в системных буферах данных для оптимизации производительности диска.</span><span class="sxs-lookup"><span data-stu-id="d59f2-104">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span> <span data-ttu-id="d59f2-105">Когда приложение записывает в файл, система обычно помещает данные в буфер и регулярно записывает их на диск.</span><span class="sxs-lookup"><span data-stu-id="d59f2-105">When an application writes to a file, the system usually buffers the data and writes the data to the disk on a regular basis.</span></span> <span data-ttu-id="d59f2-106">Приложение может заставить операционную систему записывать содержимое этих буферов данных на диск с помощью функции [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .</span><span class="sxs-lookup"><span data-stu-id="d59f2-106">An application can force the operating system to write the contents of these data buffers to the disk by using the [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) function.</span></span> <span data-ttu-id="d59f2-107">Кроме того, приложение может указать, что операции записи обходят буфер данных и записываются непосредственно на диск, устанавливая **флаг файла без флага \_ \_ \_ буферизации** при создании или открытии файла с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="d59f2-107">Alternatively, an application can specify that write operations are to bypass the data buffer and write directly to the disk by setting the **FILE\_FLAG\_NO\_BUFFERING** flag when the file is created or opened using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="d59f2-108">Если при закрытии файла в внутреннем буфере имеются данные, операционная система не будет автоматически записывать содержимое буфера на диск перед закрытием файла.</span><span class="sxs-lookup"><span data-stu-id="d59f2-108">If there is data in the internal buffer when the file is closed, the operating system does not automatically write the contents of the buffer to the disk before closing the file.</span></span> <span data-ttu-id="d59f2-109">Если приложение не заставляет операционную систему записывать буфер на диск перед закрытием файла, алгоритм кэширования определяет время записи буфера.</span><span class="sxs-lookup"><span data-stu-id="d59f2-109">If the application does not force the operating system to write the buffer to disk before closing the file, the caching algorithm determines when the buffer is written.</span></span>

> [!Note]  
> <span data-ttu-id="d59f2-110">Доступ к буферу данных во время использования операции чтения или записи может привести к повреждению буфера.</span><span class="sxs-lookup"><span data-stu-id="d59f2-110">Accessing a data buffer while a read or write operation is using it may corrupt the buffer.</span></span> <span data-ttu-id="d59f2-111">Приложения не должны считывать, записывать, перераспределять или освобождать буфер данных, который используется операцией чтения или записи до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="d59f2-111">Applications must not read from, write to, reallocate, or free the data buffer that a read or write operation is using until the operation completes.</span></span>

 

 

 



