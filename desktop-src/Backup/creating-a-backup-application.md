---
title: Создание приложения резервного копирования
description: Для выполнения ввода-вывода на ленте приложение резервного копирования сначала должно получить маркер ленточного устройства. В следующем примере кода показано, как использовать функцию CreateFile для открытия ленточного устройства.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Резервное копирование архивных приложений
- Создание резервной копии резервных копий приложений
- Резервное копирование, создание приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070374"
---
# <a name="creating-a-backup-application"></a><span data-ttu-id="61e0a-107">Создание приложения резервного копирования</span><span class="sxs-lookup"><span data-stu-id="61e0a-107">Creating a Backup Application</span></span>

<span data-ttu-id="61e0a-108">Для выполнения ввода-вывода на ленте приложение резервного копирования сначала должно получить маркер ленточного устройства.</span><span class="sxs-lookup"><span data-stu-id="61e0a-108">To perform input or output on a tape, a backup application must first obtain a handle of the tape device.</span></span> <span data-ttu-id="61e0a-109">В следующем примере кода показано, как использовать функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для открытия ленточного устройства.</span><span class="sxs-lookup"><span data-stu-id="61e0a-109">The following code sample shows you how to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a tape device.</span></span>


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



<span data-ttu-id="61e0a-110">Чтобы создать резервную копию дерева каталогов на ленте, приложение должно использовать функции [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) и [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) для прохода по дереву каталогов.</span><span class="sxs-lookup"><span data-stu-id="61e0a-110">To back up a directory tree to a tape, an application must use the [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) functions to traverse the directory tree.</span></span> <span data-ttu-id="61e0a-111">При каждом обнаружении файла приложение должно получить атрибуты файла с помощью функции [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="61e0a-111">Each time a file is found, the application should get the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) function.</span></span>

<span data-ttu-id="61e0a-112">При наличии жестких связей приложение должно определить количество ссылок и сохранить уникальный идентификатор файла в таблице для будущих сравнений.</span><span class="sxs-lookup"><span data-stu-id="61e0a-112">If there are hard links, an application should determine the number of links, and save the unique identifier of the file in a table for future comparisons.</span></span> <span data-ttu-id="61e0a-113">При первом обнаружении файла приложение должно использовать [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , чтобы открыть файл, и функцию [**баккупреад**](/windows/desktop/api/Winbase/nf-winbase-backupread) , чтобы начать резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="61e0a-113">The first time a file is found, the application should use [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open the file, and the [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) function to begin the backup.</span></span> <span data-ttu-id="61e0a-114">Затем можно многократно использовать функцию [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) для перемещения всей информации из буфера, используемого **баккупреад** , на ленту.</span><span class="sxs-lookup"><span data-stu-id="61e0a-114">Then it can use the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function repeatedly to transfer all the information in the buffer used by **BackupRead** to the tape.</span></span> <span data-ttu-id="61e0a-115">При втором обнаружении файла (проверяется на соответствие таблице идентификаторов файлов при наличии жестких связей) приложение может записать общие сведения о файле на ленту, а затем — поток с идентификатором, который является **\_ ссылкой для резервного копирования**.</span><span class="sxs-lookup"><span data-stu-id="61e0a-115">The second time a file is found (checked against the table of file identifiers when there are hard links), the application can write the general file information to the tape, followed by a stream that has an identifier that is **BACKUP\_LINK**.</span></span>

<span data-ttu-id="61e0a-116">При восстановлении файлов с ленты на диск приложение должно использовать функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**баккупврите**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)и [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="61e0a-116">When restoring files from tape to disk, an application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite), and [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) functions.</span></span> <span data-ttu-id="61e0a-117">Для каждого файла на ленте приложение должно использовать **CreateFile** , чтобы создать новый файл на диске, и **баккупврите** начать восстановление файла.</span><span class="sxs-lookup"><span data-stu-id="61e0a-117">For each file on a tape, the application should use **CreateFile** to create a new file on disk, and **BackupWrite** to begin restoring the file.</span></span> <span data-ttu-id="61e0a-118">Затем приложение должно многократно использовать **ReadFile** , пока вся информация для файла считывается с ленты в буфер, заполненный **баккупврите**.</span><span class="sxs-lookup"><span data-stu-id="61e0a-118">Then the application should use **ReadFile** repeatedly until all the information for the file is read from the tape into the buffer filled by **BackupWrite**.</span></span>

<span data-ttu-id="61e0a-119">Если один из потоков в буфере [**баккупврите**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) имеет идентификатор потока **\_ связи резервной копии** , приложение должно установить жесткую связь.</span><span class="sxs-lookup"><span data-stu-id="61e0a-119">If one of the streams in the [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) buffer has a **BACKUP\_LINK** stream identifier, the application must establish a hard link.</span></span> <span data-ttu-id="61e0a-120">Если данные, необходимые для установления связи, не существуют, **баккупврите** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="61e0a-120">If the data needed to establish the link does not exist, **BackupWrite** fails.</span></span> <span data-ttu-id="61e0a-121">Приложение может использовать существующий каталог для поиска и восстановления исходных данных или уведомлять пользователя о том, что восстанавливаемые данные файлов находятся в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="61e0a-121">The application can use a pre-existing catalog to locate and restore the original data, or it can notify the user that the file data to be restored is in a different location.</span></span>

 

 