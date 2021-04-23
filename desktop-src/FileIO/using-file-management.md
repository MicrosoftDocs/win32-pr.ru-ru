---
description: В следующих примерах используются функции управления файлами.
ms.assetid: 0879898b-b661-48b3-af94-9ba24811503f
title: Использование управления файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88838ee99dde16c5c2288c00e2e2f3b35747dae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081372"
---
# <a name="using-file-management"></a><span data-ttu-id="59f27-103">Использование управления файлами</span><span class="sxs-lookup"><span data-stu-id="59f27-103">Using File Management</span></span>

<span data-ttu-id="59f27-104">В следующих примерах используются функции управления файлами.</span><span class="sxs-lookup"><span data-stu-id="59f27-104">The following samples use the file management functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="59f27-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="59f27-105">In this section</span></span>



| <span data-ttu-id="59f27-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="59f27-106">Topic</span></span>                                                                                                   | <span data-ttu-id="59f27-107">Описание</span><span class="sxs-lookup"><span data-stu-id="59f27-107">Description</span></span>                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59f27-108">Добавление пользователей в зашифрованный файл</span><span class="sxs-lookup"><span data-stu-id="59f27-108">Adding Users to an Encrypted File</span></span>](adding-users-to-an-encrypted-file.md)<br/>                   | <span data-ttu-id="59f27-109">Пример кода, демонстрирующий Добавление нового пользователя в существующий зашифрованный файл с помощью функции [**аддусерстоенкриптедфиле**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) .</span><span class="sxs-lookup"><span data-stu-id="59f27-109">Example code that shows how to add a new user to an existing encrypted file by using the [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) function.</span></span><br/>                         |
| [<span data-ttu-id="59f27-110">Добавление одного файла в другой файл</span><span class="sxs-lookup"><span data-stu-id="59f27-110">Appending One File to Another File</span></span>](appending-one-file-to-another-file.md)<br/>                 | <span data-ttu-id="59f27-111">Пример кода, демонстрирующий, как приложение может добавлять один файл в конец другого файла, включая открытие и закрытие файлов, чтение и запись в файлы, а также блокировку и разблокировку файлов.</span><span class="sxs-lookup"><span data-stu-id="59f27-111">Example code that shows how an application can append one file to the end of another file, including how to open and close files, read and write to files, and lock and unlock files.</span></span><br/> |
| [<span data-ttu-id="59f27-112">Создание и использование временного файла</span><span class="sxs-lookup"><span data-stu-id="59f27-112">Creating and Using a Temporary File</span></span>](creating-and-using-a-temporary-file.md)<br/>               | <span data-ttu-id="59f27-113">Пример кода, показывающий, как создать временный файл для обработки данных с помощью функций метода GetTempFileName и Жеттемппас.</span><span class="sxs-lookup"><span data-stu-id="59f27-113">Example code that shows how to create a temporary file for data manipulation purposes by using the GetTempFileName and GetTempPath functions.</span></span><br/>                                         |
| [<span data-ttu-id="59f27-114">Блокировка и разблокировка диапазонов байтов в файлах</span><span class="sxs-lookup"><span data-stu-id="59f27-114">Locking and Unlocking Byte Ranges in Files</span></span>](locking-and-unlocking-byte-ranges-in-files.md)<br/> | <span data-ttu-id="59f27-115">Пример кода, который показывает блокировку диапазона байтов и разблокировку с помощью функций Локкфиликс и Унлоккфиликс.</span><span class="sxs-lookup"><span data-stu-id="59f27-115">Example code that shows byte range locking and unlocking by using the LockFileEx and UnlockFileEx functions.</span></span><br/>                                                                          |
| [<span data-ttu-id="59f27-116">Открытие файла для чтения или записи</span><span class="sxs-lookup"><span data-stu-id="59f27-116">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)<br/>           | <span data-ttu-id="59f27-117">Пример кода, демонстрирующий использование функции CreateFile для создания нового файла или открытия существующего файла.</span><span class="sxs-lookup"><span data-stu-id="59f27-117">Example code that shows how to use the CreateFile function to create a new file or open an existing file.</span></span><br/>                                                                             |
| [<span data-ttu-id="59f27-118">Получение и изменение атрибутов файлов</span><span class="sxs-lookup"><span data-stu-id="59f27-118">Retrieving and Changing File Attributes</span></span>](retrieving-and-changing-file-attributes.md)<br/>       | <span data-ttu-id="59f27-119">Пример кода, демонстрирующий использование функции сбой getfileattributesex для получения атрибутов файла.</span><span class="sxs-lookup"><span data-stu-id="59f27-119">Example code that shows how to use the GetFileAttributesEx function to retrieve file attributes.</span></span><br/>                                                                                      |
| [<span data-ttu-id="59f27-120">Проверка на конец файла</span><span class="sxs-lookup"><span data-stu-id="59f27-120">Testing for the End of a File</span></span>](testing-for-the-end-of-a-file.md)<br/>                           | <span data-ttu-id="59f27-121">Пример кода, который показывает, как проверить конец файла во время синхронной операции чтения и во время асинхронной операции чтения.</span><span class="sxs-lookup"><span data-stu-id="59f27-121">Example code that shows how to test for the end of file during a synchronous read operation and during an asynchronous read operation.</span></span><br/>                                                |
| [<span data-ttu-id="59f27-122">Использование потоков</span><span class="sxs-lookup"><span data-stu-id="59f27-122">Using Streams</span></span>](using-streams.md)<br/>                                                           | <span data-ttu-id="59f27-123">Пример кода, демонстрирующий использование базовых потоков файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="59f27-123">Example code that shows how to use basic NTFS file system streams.</span></span><br/>                                                                                                                    |



 

 

 




