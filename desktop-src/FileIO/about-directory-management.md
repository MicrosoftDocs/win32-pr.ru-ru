---
description: Каталог, содержащий один или несколько каталогов, является родительским для вложенного каталога или каталогов, а каждый содержащийся каталог является дочерним по отношению к родительскому каталогу. Иерархическая структура каталогов называется деревом каталогов.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Об управлении каталогами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897426"
---
# <a name="about-directory-management"></a><span data-ttu-id="93b1f-104">Об управлении каталогами</span><span class="sxs-lookup"><span data-stu-id="93b1f-104">About Directory Management</span></span>

<span data-ttu-id="93b1f-105">Каталог, содержащий один или несколько каталогов, является *родительским* для вложенного каталога или каталогов, а каждый содержащийся каталог является *дочерним* по отношению к родительскому каталогу.</span><span class="sxs-lookup"><span data-stu-id="93b1f-105">A directory that contains one or more directories is the *parent* of the contained directory or directories, and each contained directory is a *child* of the parent directory.</span></span> <span data-ttu-id="93b1f-106">Иерархическая структура каталогов называется *деревом каталогов*.</span><span class="sxs-lookup"><span data-stu-id="93b1f-106">The hierarchical structure of directories is referred to as a *directory tree*.</span></span>

<span data-ttu-id="93b1f-107">Файловая система NTFS реализует логическую связь между каталогом и файлами, которые он содержит, как *таблицу записей каталога*.</span><span class="sxs-lookup"><span data-stu-id="93b1f-107">The NTFS file system implements the logical link between a directory and the files it contains as a *directory entry table*.</span></span> <span data-ttu-id="93b1f-108">При перемещении файла в каталог в таблице создается запись для перемещенного файла, а имя файла помещается в запись.</span><span class="sxs-lookup"><span data-stu-id="93b1f-108">When a file is moved into a directory, an entry is created in the table for the moved file and the name of the file is placed in the entry.</span></span> <span data-ttu-id="93b1f-109">При удалении файла, содержащегося в каталоге, имя и запись, соответствующие удаленному файлу, также удаляются из таблицы.</span><span class="sxs-lookup"><span data-stu-id="93b1f-109">When a file contained in a directory is deleted, the name and entry corresponding to the deleted file is also deleted from the table.</span></span> <span data-ttu-id="93b1f-110">В таблице записей каталога может находиться несколько записей для одного файла.</span><span class="sxs-lookup"><span data-stu-id="93b1f-110">More than one entry for a single file can exist in a directory entry table.</span></span> <span data-ttu-id="93b1f-111">Если в таблице для файла создается дополнительная запись, эта запись называется *жесткой ссылкой* на этот файл.</span><span class="sxs-lookup"><span data-stu-id="93b1f-111">If an additional entry is created in the table for a file, that entry is referred to as a *hard link* to that file.</span></span> <span data-ttu-id="93b1f-112">Количество жестких связей, которые можно создать для одного файла, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="93b1f-112">There is no limit to the number of hard links that can be created for a single file.</span></span>

<span data-ttu-id="93b1f-113">Каталоги также могут содержать соединения и точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="93b1f-113">Directories can also contain junctions and reparse points.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="93b1f-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="93b1f-114">In this section</span></span>



| <span data-ttu-id="93b1f-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="93b1f-115">Topic</span></span>                                                                                 | <span data-ttu-id="93b1f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="93b1f-116">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93b1f-117">Создание и удаление каталогов</span><span class="sxs-lookup"><span data-stu-id="93b1f-117">Creating and Deleting Directories</span></span>](creating-and-deleting-directories.md)<br/> | <span data-ttu-id="93b1f-118">Приложение может программно создавать и удалять каталоги.</span><span class="sxs-lookup"><span data-stu-id="93b1f-118">An application can programmatically create and delete directories.</span></span><br/>                          |
| [<span data-ttu-id="93b1f-119">Дескрипторы каталогов</span><span class="sxs-lookup"><span data-stu-id="93b1f-119">Directory Handles</span></span>](obtaining-a-handle-to-a-directory.md)<br/>                 | <span data-ttu-id="93b1f-120">Каждый раз, когда процесс создает или открывает объект каталога, он получает обработчик для объекта.</span><span class="sxs-lookup"><span data-stu-id="93b1f-120">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span><br/> |
| [<span data-ttu-id="93b1f-121">Точки повторного синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="93b1f-121">Reparse Points</span></span>](reparse-points.md)<br/>                                       | <span data-ttu-id="93b1f-122">Описывает точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="93b1f-122">Describes reparse points.</span></span><br/>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="93b1f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="93b1f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93b1f-124">Справочник по управлению каталогами</span><span class="sxs-lookup"><span data-stu-id="93b1f-124">Directory Management Reference</span></span>](directory-management-reference.md)
</dt> </dl>

 

 




