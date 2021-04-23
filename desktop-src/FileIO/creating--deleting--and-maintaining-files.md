---
description: Функции, используемые для создания, удаления и обслуживания файлов.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Создание, удаление и обслуживание файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664438"
---
# <a name="creating-deleting-and-maintaining-files"></a><span data-ttu-id="5a35f-103">Создание, удаление и обслуживание файлов</span><span class="sxs-lookup"><span data-stu-id="5a35f-103">Creating, Deleting, and Maintaining Files</span></span>

<span data-ttu-id="5a35f-104">В следующих разделах описывается создание, удаление и обслуживание файлов.</span><span class="sxs-lookup"><span data-stu-id="5a35f-104">The following topics describe how to create, delete, and maintain files.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5a35f-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5a35f-105">In this section</span></span>



| <span data-ttu-id="5a35f-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="5a35f-106">Topic</span></span>                                                                   | <span data-ttu-id="5a35f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5a35f-107">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a35f-108">Именование файлов, путей и пространств имен</span><span class="sxs-lookup"><span data-stu-id="5a35f-108">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)<br/>     | <span data-ttu-id="5a35f-109">Правила, соглашения и ограничения имен для файлов и каталогов, включая соглашения об именовании, короткие имена файлов и длинные имена файлов, полные пути и относительные пути, ограничение длины пути, 8,3 имен файлов и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5a35f-109">Rules, conventions, and limitations of names for files and directories, including naming conventions, short file names vs. long file names, fully qualified paths vs. relative paths, maximum path length limitation, 8.3 file names, and namespaces.</span></span><br/>            |
| [<span data-ttu-id="5a35f-110">Создание и открытие файлов</span><span class="sxs-lookup"><span data-stu-id="5a35f-110">Creating and Opening Files</span></span>](creating-and-opening-files.md)<br/> | <span data-ttu-id="5a35f-111">Рекомендации по созданию или открытию файла с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="5a35f-111">Considerations for creating or opening a file by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="5a35f-112">Перемещение и замена файлов</span><span class="sxs-lookup"><span data-stu-id="5a35f-112">Moving and Replacing Files</span></span>](moving-and-replacing-files.md)<br/> | <span data-ttu-id="5a35f-113">Рекомендации по перемещению и замене файлов с помощью функций Копифиликс, CreateFile, Реплацефиле и Мовефиликс.</span><span class="sxs-lookup"><span data-stu-id="5a35f-113">Considerations for moving and replacing files by using the CopyFileEx, CreateFile, Replacefile, and MoveFileEx functions.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="5a35f-114">Закрытие и удаление файлов</span><span class="sxs-lookup"><span data-stu-id="5a35f-114">Closing and Deleting Files</span></span>](closing-and-deleting-files.md)<br/> | <span data-ttu-id="5a35f-115">Чтобы эффективно использовать ресурсы операционной системы, приложение должно закрыть файлы, если они больше не нужны с помощью функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="5a35f-115">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="5a35f-116">Если файл открыт после завершения работы приложения, система закрывает его автоматически.</span><span class="sxs-lookup"><span data-stu-id="5a35f-116">If a file is open when an application terminates, the system closes it automatically.</span></span><br/> |
| [<span data-ttu-id="5a35f-117">Дефрагментация файлов</span><span class="sxs-lookup"><span data-stu-id="5a35f-117">Defragmenting Files</span></span>](defragmenting-files.md)<br/>               | <span data-ttu-id="5a35f-118">*Дефрагментация* — это процесс перемещения частей файлов на диске для дефрагментации файлов, то есть процесса перемещения кластеров файлов на диске, чтобы сделать их непрерывными.</span><span class="sxs-lookup"><span data-stu-id="5a35f-118">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span><br/>                                                                               |



 

 

