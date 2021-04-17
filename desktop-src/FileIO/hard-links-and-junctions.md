---
description: Описывает жесткие связи и соединения.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Жесткие связи и соединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684370"
---
# <a name="hard-links-and-junctions"></a><span data-ttu-id="434b7-103">Жесткие связи и соединения</span><span class="sxs-lookup"><span data-stu-id="434b7-103">Hard Links and Junctions</span></span>

<span data-ttu-id="434b7-104">В файловой системе NTFS поддерживаются три типа ссылок на файлы: жесткие связи, точки соединения и символьные ссылки.</span><span class="sxs-lookup"><span data-stu-id="434b7-104">There are three types of file links supported in the NTFS file system: hard links, junctions, and symbolic links.</span></span> <span data-ttu-id="434b7-105">В этом разделе приводятся общие сведения о жестких связях и соединениях.</span><span class="sxs-lookup"><span data-stu-id="434b7-105">This topic is an overview of hard links and junctions.</span></span> <span data-ttu-id="434b7-106">Дополнительные сведения о символических ссылках см. в разделе [создание символьных ссылок](creating-symbolic-links.md).</span><span class="sxs-lookup"><span data-stu-id="434b7-106">For information about symbolic links, see [Creating Symbolic Links](creating-symbolic-links.md).</span></span>

## <a name="hard-links"></a><span data-ttu-id="434b7-107">Жесткие связи</span><span class="sxs-lookup"><span data-stu-id="434b7-107">Hard Links</span></span>

<span data-ttu-id="434b7-108">*Жесткая связь* — это представление файловой системы, в котором несколько путей ссылаются на один файл в том же томе.</span><span class="sxs-lookup"><span data-stu-id="434b7-108">A *hard link* is the file system representation of a file by which more than one path references a single file in the same volume.</span></span> <span data-ttu-id="434b7-109">Чтобы создать жесткую связь, используйте функцию [**креатехардлинк**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) .</span><span class="sxs-lookup"><span data-stu-id="434b7-109">To create a hard link, use the [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) function.</span></span> <span data-ttu-id="434b7-110">Любые изменения в этом файле сразу же видны приложениям, которые обращаются к нему по жестким ссылкам, ссылающимся на него.</span><span class="sxs-lookup"><span data-stu-id="434b7-110">Any changes to that file are instantly visible to applications that access it through the hard links that reference it.</span></span> <span data-ttu-id="434b7-111">Однако сведения о размере и атрибуте записи каталога обновляются только для ссылки, через которую было внесено изменение.</span><span class="sxs-lookup"><span data-stu-id="434b7-111">However, the directory entry size and attribute information is updated only for the link through which the change was made.</span></span> <span data-ttu-id="434b7-112">Обратите внимание, что атрибуты файла отражаются в каждой жесткой ссылке на этот файл, а изменения атрибутов этого файла распространяются на все жесткие связи.</span><span class="sxs-lookup"><span data-stu-id="434b7-112">Note that the attributes on the file are reflected in every hard link to that file, and changes to that file's attributes propagate to all the hard links.</span></span> <span data-ttu-id="434b7-113">Например, если сбросить атрибут READONLY на жесткой связи, чтобы удалить эту конкретную жесткую связь, и существует несколько жестких связей с фактическим файлом, то необходимо сбросить бит только для чтения файла с одной из оставшихся жестких связей, чтобы вернуть файл и все оставшиеся жесткие связи в состояние READONLY.</span><span class="sxs-lookup"><span data-stu-id="434b7-113">For example if you reset the READONLY attribute on a hard link to delete that particular hard link, and there are multiple hard links to the actual file, then you will need to reset the READONLY bit on the file from one of the remaining hard links to bring the file and all remaining hard links back to the READONLY state.</span></span>

<span data-ttu-id="434b7-114">Например, в системе, где C: и D: являются локальными дисками и Z: — сетевой диск, сопоставленный с \\ \\ Fred- \\ ресурсом, следующие ссылки разрешены в качестве жесткой связи:</span><span class="sxs-lookup"><span data-stu-id="434b7-114">For example, in a system where C: and D: are local drives and Z: is a network drive mapped to \\\\fred\\share, the following references are permitted as a hard link:</span></span>

-   <span data-ttu-id="434b7-115">C: \\ дира \\ethel.txt связан с C: \\ Дирб \\ Дирк \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="434b7-115">C:\\dira\\ethel.txt linked to C:\\dirb\\dirc\\lucy.txt</span></span>
-   <span data-ttu-id="434b7-116">Г: \\ dir1 \\tinker.txt до d: \\ Dir2 \\ Диркс \\bell.txt</span><span class="sxs-lookup"><span data-stu-id="434b7-116">D:\\dir1\\tinker.txt to D:\\dir2\\dirx\\bell.txt</span></span>
-   <span data-ttu-id="434b7-117">C: \\ Дири \\ Bob. bak, связанный с C: \\ Dir2 \\mina.txt</span><span class="sxs-lookup"><span data-stu-id="434b7-117">C:\\diry\\bob.bak linked to C:\\dir2\\mina.txt</span></span>

<span data-ttu-id="434b7-118">Следующие:</span><span class="sxs-lookup"><span data-stu-id="434b7-118">The following are not:</span></span>

-   <span data-ttu-id="434b7-119">C: \\ Дира, связанный с C: \\ Дирб</span><span class="sxs-lookup"><span data-stu-id="434b7-119">C:\\dira linked to C:\\dirb</span></span>
-   <span data-ttu-id="434b7-120">C: \\ дира \\ethel.txt связан с D: \\ Дирб \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="434b7-120">C:\\dira\\ethel.txt linked to D:\\dirb\\lucy.txt</span></span>
-   <span data-ttu-id="434b7-121">C: \\ дира \\ethel.txt связан с Z: \\ Дирб \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="434b7-121">C:\\dira\\ethel.txt linked to Z:\\dirb\\lucy.txt</span></span>

<span data-ttu-id="434b7-122">Чтобы удалить жесткую связь, используйте функцию [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) .</span><span class="sxs-lookup"><span data-stu-id="434b7-122">To delete a hard link, use the [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function.</span></span> <span data-ttu-id="434b7-123">Можно удалить жесткие связи в любом порядке независимо от порядка их создания.</span><span class="sxs-lookup"><span data-stu-id="434b7-123">You can delete hard links in any order regardless of the order in which they are created.</span></span>

## <a name="junctions"></a><span data-ttu-id="434b7-124">Соединения</span><span class="sxs-lookup"><span data-stu-id="434b7-124">Junctions</span></span>

<span data-ttu-id="434b7-125">*Соединение* (называемое также *мягкой ссылкой*) отличается от жесткой связи тем, что объекты хранилища, на которые он ссылается, являются отдельными каталогами, а соединение может ссылаться на каталоги, расположенные на разных локальных томах на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="434b7-125">A *junction* (also called a *soft link*) differs from a hard link in that the storage objects it references are separate directories, and a junction can link directories located on different local volumes on the same computer.</span></span> <span data-ttu-id="434b7-126">В противном случае соединения работают идентично с жесткими связями.</span><span class="sxs-lookup"><span data-stu-id="434b7-126">Otherwise, junctions operate identically to hard links.</span></span> <span data-ttu-id="434b7-127">Соединения реализуются через [точки повторного анализа](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="434b7-127">Junctions are implemented through [reparse points](reparse-points.md).</span></span>

<span data-ttu-id="434b7-128">При условии, что в разделе «жесткие связи» имеются такие же условия, в качестве соединений разрешены следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="434b7-128">Assuming the same conditions in the Hard Links section, the following references are permitted as junctions:</span></span>

-   <span data-ttu-id="434b7-129">C: \\ Дира, связанный с C: \\ Дирб \\ Дирк</span><span class="sxs-lookup"><span data-stu-id="434b7-129">C:\\dira linked to C:\\dirb\\dirc</span></span>
-   <span data-ttu-id="434b7-130">C: \\ Диркс связан с D: \\ Дири</span><span class="sxs-lookup"><span data-stu-id="434b7-130">C:\\dirx linked to D:\\diry</span></span>

<span data-ttu-id="434b7-131">Следующие:</span><span class="sxs-lookup"><span data-stu-id="434b7-131">The following are not:</span></span>

-   <span data-ttu-id="434b7-132">C: \\ дира \\one.txt связанный с C: \\ Дирб \\two.txt</span><span class="sxs-lookup"><span data-stu-id="434b7-132">C:\\dira\\one.txt linked to C:\\dirb\\two.txt</span></span>
-   <span data-ttu-id="434b7-133">C: \\ Dir1, связанная с Z: \\ Dir2</span><span class="sxs-lookup"><span data-stu-id="434b7-133">C:\\dir1 linked to Z:\\dir2</span></span>

## <a name="related-topics"></a><span data-ttu-id="434b7-134">См. также</span><span class="sxs-lookup"><span data-stu-id="434b7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="434b7-135">Создание символьных ссылок</span><span class="sxs-lookup"><span data-stu-id="434b7-135">Creating Symbolic Links</span></span>](creating-symbolic-links.md)
</dt> </dl>

 

 



