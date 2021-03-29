---
description: Когда файл открывается процессом с помощью функции CreateFile, с ним связывается маркер файла до завершения процесса или закрытия обработчика с помощью функции CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Дескрипторы файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912863"
---
# <a name="file-handles"></a><span data-ttu-id="0bbb9-103">Дескрипторы файлов</span><span class="sxs-lookup"><span data-stu-id="0bbb9-103">File Handles</span></span>

<span data-ttu-id="0bbb9-104">Когда файл открывается процессом с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , с ним связывается *маркер файла* до завершения процесса или закрытия обработчика с помощью функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="0bbb9-104">When a file is opened by a process using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, a *file handle* is associated with it until either the process terminates or the handle is closed using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="0bbb9-105">Этот файл используется для обнаружения файла во многих вызовах функций.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-105">The file handle is used to identify the file in many function calls.</span></span>

<span data-ttu-id="0bbb9-106">Каждый дескриптор файла и объект File обычно уникальны для каждого процесса, открывающего файл — единственным исключением является то, что дескриптор файла, удерживаемого процессом, дублируется или если дочерний процесс наследует дескрипторы файлов родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-106">Each file handle and file object is generally unique to each process that opens a file—the only exceptions to this are when a file handle held by a process is duplicated, or when a child process inherits the file handles of the parent process.</span></span> <span data-ttu-id="0bbb9-107">В таких ситуациях эти дескрипторы файлов являются уникальными, но видят один общий объект файла.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-107">In these situations, these file handles are unique, but see a single, shared file object.</span></span> <span data-ttu-id="0bbb9-108">Дополнительные сведения о копировании дескрипторов файлов, хранящихся в процессах, см. в разделе [**дупликатехандле**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="0bbb9-108">See [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) for more information on duplicating file handles held by processes.</span></span>

<span data-ttu-id="0bbb9-109">Обратите внимание, что несмотря на то, что дескрипторы файлов обычно являются частными для процесса, данные файла, на которые указывает файл, не имеют.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-109">Note that while the file handles are typically private to a process, the file data that the file handles point to is not.</span></span> <span data-ttu-id="0bbb9-110">Поэтому процессы и потоки, которые совместно используют один и тот же файл, должны синхронизировать свои права доступа.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-110">Therefore, processes and threads that share the same file must synchronize their access.</span></span> <span data-ttu-id="0bbb9-111">Для большинства операций с файлом процесс идентифицирует файл через его частный пул дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-111">For most operations on a file, a process identifies the file through its private pool of handles.</span></span>

 

 
