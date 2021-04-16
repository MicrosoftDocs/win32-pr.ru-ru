---
description: Чтобы эффективно использовать ресурсы операционной системы, приложение должно закрыть файлы, если они больше не нужны с помощью функции CloseHandle. Если файл открыт после завершения работы приложения, система закрывает его автоматически.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Закрытие и удаление файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664437"
---
# <a name="closing-and-deleting-files"></a><span data-ttu-id="ee625-104">Закрытие и удаление файлов</span><span class="sxs-lookup"><span data-stu-id="ee625-104">Closing and Deleting Files</span></span>

<span data-ttu-id="ee625-105">Чтобы эффективно использовать ресурсы операционной системы, приложение должно закрыть файлы, если они больше не нужны с помощью функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="ee625-105">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="ee625-106">Если файл открыт после завершения работы приложения, система закрывает его автоматически.</span><span class="sxs-lookup"><span data-stu-id="ee625-106">If a file is open when an application terminates, the system closes it automatically.</span></span>

<span data-ttu-id="ee625-107">Функцию [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) можно использовать для удаления файла при закрытии.</span><span class="sxs-lookup"><span data-stu-id="ee625-107">The [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function can be used to delete a file on close.</span></span> <span data-ttu-id="ee625-108">Файл нельзя удалить, пока все его дескрипторы не будут закрыты.</span><span class="sxs-lookup"><span data-stu-id="ee625-108">A file cannot be deleted until all handles to it are closed.</span></span> <span data-ttu-id="ee625-109">Если файл не может быть удален, его имя нельзя использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="ee625-109">If a file cannot be deleted, its name cannot be reused.</span></span> <span data-ttu-id="ee625-110">Для немедленного повторного использования имени файла переименуйте существующий файл.</span><span class="sxs-lookup"><span data-stu-id="ee625-110">To reuse a file name immediately, rename the existing file.</span></span>

<span data-ttu-id="ee625-111">Если вы удаляете открытый файл или каталог на удаленном компьютере, который уже открыт на удаленном компьютере без набора разрешений на чтение, не вызывайте [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) или [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) , чтобы сначала открыть файл или каталог для удаления.</span><span class="sxs-lookup"><span data-stu-id="ee625-111">If you are deleting an open file or directory on a remote machine and it has already been opened on the remote machine without the read share permission set, do not call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) to open the file or directory for deletion first.</span></span> <span data-ttu-id="ee625-112">Это приведет к нарушению общего доступа.</span><span class="sxs-lookup"><span data-stu-id="ee625-112">Doing so will result in a sharing violation.</span></span>

 

 
