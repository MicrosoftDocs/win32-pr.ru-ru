---
description: С помощью подключенных папок можно объединять разнородные файловые системы, такие как файловая система NTFS, 16-разрядная файловая система FAT и файловая система ISO-9660 на компакт-диске, в одну логическую файловую систему на одном томе NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Подключенные папки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683695"
---
# <a name="mounted-folders"></a><span data-ttu-id="1355d-103">Подключенные папки</span><span class="sxs-lookup"><span data-stu-id="1355d-103">Mounted Folders</span></span>

<span data-ttu-id="1355d-104">Файловая система NTFS поддерживает подключенные папки.</span><span class="sxs-lookup"><span data-stu-id="1355d-104">The NTFS file system supports mounted folders.</span></span> <span data-ttu-id="1355d-105">*Подключенная папка* — это ассоциация между Томом и каталогом на другом томе.</span><span class="sxs-lookup"><span data-stu-id="1355d-105">A *mounted folder* is an association between a volume and a directory on another volume.</span></span> <span data-ttu-id="1355d-106">При создании подключенной папки пользователи и приложения могут получить доступ к целевому тому с помощью пути к подключенной папке или с помощью буквы диска тома.</span><span class="sxs-lookup"><span data-stu-id="1355d-106">When a mounted folder is created, users and applications can access the target volume either by using the path to the mounted folder or by using the volume's drive letter.</span></span> <span data-ttu-id="1355d-107">Например, пользователь может создать подключенную папку для связывания диска D: с \\ папкой c: МНТ \\ ддриве на диске c. После создания подключенной папки пользователь может использовать путь "C: \\ МНТ \\ ддриве" для доступа к диску D: как если бы он был папкой на диске C:.</span><span class="sxs-lookup"><span data-stu-id="1355d-107">For example, a user can create a mounted folder to associate drive D: with the C:\\Mnt\\DDrive folder on drive C. After creating the mounted folder, the user can use the "C:\\Mnt\\DDrive" path to access drive D: as if it were a folder on drive C:.</span></span>

<span data-ttu-id="1355d-108">С помощью подключенных папок можно объединять разнородные файловые системы, такие как файловая система NTFS, 16-разрядная файловая система FAT и файловая система ISO-9660 на компакт-диске, в одну логическую файловую систему на одном томе NTFS.</span><span class="sxs-lookup"><span data-stu-id="1355d-108">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span> <span data-ttu-id="1355d-109">Ни пользователям, ни приложениям не требуются сведения о целевом томе, на котором находится конкретный файл.</span><span class="sxs-lookup"><span data-stu-id="1355d-109">Neither users nor applications need information about the target volume on which a specific file is located.</span></span> <span data-ttu-id="1355d-110">Все сведения, необходимые для поиска указанного файла, — это полный путь, использующий подключенную папку на томе NTFS.</span><span class="sxs-lookup"><span data-stu-id="1355d-110">All the information they need to locate a specified file is a complete path using a mounted folder on the NTFS volume.</span></span> <span data-ttu-id="1355d-111">Тома могут быть переупорядочены, заменены или разбиты на несколько томов без необходимости изменения параметров пользователями или приложениями.</span><span class="sxs-lookup"><span data-stu-id="1355d-111">Volumes can be rearranged, substituted, or subdivided into many volumes without users or applications needing to change settings.</span></span>

<span data-ttu-id="1355d-112">Сведения о подключенных папках см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="1355d-112">For information on mounted folders, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1355d-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1355d-113">In this section</span></span>



| <span data-ttu-id="1355d-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="1355d-114">Topic</span></span>                                                                                                                         | <span data-ttu-id="1355d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1355d-115">Description</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1355d-116">Создание подключенных папок</span><span class="sxs-lookup"><span data-stu-id="1355d-116">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)<br/>                                                  | <span data-ttu-id="1355d-117">Процесс создания подключенной папки состоит из двух этапов.</span><span class="sxs-lookup"><span data-stu-id="1355d-117">Creating a mounted folder is a two-step process.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="1355d-118">Перечисление подключенных папок</span><span class="sxs-lookup"><span data-stu-id="1355d-118">Enumerating Mounted Folders</span></span>](enumerating-volume-mount-points.md)<br/>                                                 | <span data-ttu-id="1355d-119">Функции, используемые для перечисления подключенных папок на томе.</span><span class="sxs-lookup"><span data-stu-id="1355d-119">Functions to use to enumerate mounted folders on a volume.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="1355d-120">Определение того, является ли каталог подключенной папкой</span><span class="sxs-lookup"><span data-stu-id="1355d-120">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | <span data-ttu-id="1355d-121">Определение того, является ли указанный каталог подключенной папкой.</span><span class="sxs-lookup"><span data-stu-id="1355d-121">How to determine whether a specified directory is a mounted folder.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="1355d-122">Назначение буквы диска тому</span><span class="sxs-lookup"><span data-stu-id="1355d-122">Assigning a Drive Letter to a Volume</span></span>](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | <span data-ttu-id="1355d-123">Вы можете назначить букву диска (например, X:) \) локальному тому с помощью функции [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , если для этой буквы диска уже не назначен том.</span><span class="sxs-lookup"><span data-stu-id="1355d-123">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span><br/> |
| [<span data-ttu-id="1355d-124">Функции подключенных папок</span><span class="sxs-lookup"><span data-stu-id="1355d-124">Mounted Folder Functions</span></span>](volume-mount-point-functions.md)<br/>                                                       | <span data-ttu-id="1355d-125">Функции, используемые для управления подключенными папками.</span><span class="sxs-lookup"><span data-stu-id="1355d-125">Functions used to manage mounted folders.</span></span><br/>                                                                                                                                                                        |



 

<span data-ttu-id="1355d-126">Примеры см. в разделе [примеры подключенной папки](volume-mount-point-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1355d-126">For examples, see [Mounted Folder Examples](volume-mount-point-examples.md).</span></span>

 

 




