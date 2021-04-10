---
title: Ссылки SIS и точки повторного анализа
description: SIS — это драйвер фильтра NTFS, который заменяет дублирующиеся файлы ссылками на копии при записи (называемые связями SIS), которые указывают на один резервный файл, уменьшая диск и нагрузку на кэш этих файлов.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Резервное копирование точек повторного анализа
- Резервное копирование хранилища единственных экземпляров (SIS), ссылки SIS
- Резервное копирование хранилища единственных экземпляров (SIS), точки повторного анализа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4987e7c64a83e7d0b02ed91899a182616be7943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134335"
---
# <a name="sis-links-and-reparse-points"></a><span data-ttu-id="5915b-106">Ссылки SIS и точки повторного анализа</span><span class="sxs-lookup"><span data-stu-id="5915b-106">SIS Links and Reparse Points</span></span>

<span data-ttu-id="5915b-107">SIS — это драйвер фильтра NTFS, который заменяет дублирующиеся файлы ссылками на копии при записи (называемые связями SIS), которые указывают на один резервный файл, уменьшая диск и нагрузку на кэш этих файлов.</span><span class="sxs-lookup"><span data-stu-id="5915b-107">SIS is an NTFS filter driver that replaces duplicate files with copy-on-write links (referred to as SIS links) that point to a single backing file, reducing the disk and cache overhead of those files.</span></span> <span data-ttu-id="5915b-108">Этот резервный файл содержится в [общем хранилище](the-sis-common-store-and-common-store-files.md).</span><span class="sxs-lookup"><span data-stu-id="5915b-108">This backing file is contained in a [common store](the-sis-common-store-and-common-store-files.md).</span></span> <span data-ttu-id="5915b-109">В реализации архитектуры SIS используются [точки повторного анализа](/windows/desktop/FileIO/reparse-points) , содержащие сведения о ссылках SIS.</span><span class="sxs-lookup"><span data-stu-id="5915b-109">The implementation of the SIS architecture makes use of [reparse points](/windows/desktop/FileIO/reparse-points) that contain information about the SIS links.</span></span>

<span data-ttu-id="5915b-110">Ссылки SIS реализуются как разреженные файлы, обычно с наибольшим диапазоном файлов, которые не были распределены, и точкой повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="5915b-110">SIS links are implemented as sparse files, usually with most ranges of the file unallocated, and a reparse point.</span></span> <span data-ttu-id="5915b-111">Структура и содержимое точки повторного анализа непрозрачны для приложений резервного копирования и восстановления. Однако приложения отправляют и извлекают данные из этих точек повторного анализа в и из функций API-интерфейса SIS, которые обрабатывают информацию в них.</span><span class="sxs-lookup"><span data-stu-id="5915b-111">The structure and contents of a reparse point is opaque to your backup and restore applications; however, your applications send and retrieve the data within these reparse points to and from SIS API functions that process the information in them.</span></span> <span data-ttu-id="5915b-112">Сведения в точке повторного анализа относятся к одному резервному файлу, содержащему фактические данные файла.</span><span class="sxs-lookup"><span data-stu-id="5915b-112">The information in a reparse point refers to a single backing file that contains the actual file data.</span></span> <span data-ttu-id="5915b-113">Этот резервный файл называется [файлом общего хранилища](the-sis-common-store-and-common-store-files.md)и существует в общем хранилище.</span><span class="sxs-lookup"><span data-stu-id="5915b-113">This backing file is called a [common-store file](the-sis-common-store-and-common-store-files.md), and it exists in the common store.</span></span>

<span data-ttu-id="5915b-114">При восстановлении связи SIS приложение восстановления должно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5915b-114">When restoring a SIS link, your restore application should perform the following steps:</span></span>

1.  <span data-ttu-id="5915b-115">Определите файл или файлы общего хранилища, на которые указывает ссылка SIS.</span><span class="sxs-lookup"><span data-stu-id="5915b-115">Determine the common-store file or files to which the SIS link points.</span></span>
2.  <span data-ttu-id="5915b-116">Если файл или файлы не существуют в общем хранилище, восстановите файл или файлы вместе со ссылкой на SIS.</span><span class="sxs-lookup"><span data-stu-id="5915b-116">If the file or files do not exist in the common store, restore the file or files along with the SIS link.</span></span>
3.  <span data-ttu-id="5915b-117">Если ссылка SIS указывает на файл Common-Store или файлы, которые существуют на диске, восстановите только ссылку на SIS.</span><span class="sxs-lookup"><span data-stu-id="5915b-117">If the SIS link points to a common-store file or files that exist on the disk, then restore only the SIS link.</span></span> <span data-ttu-id="5915b-118">Помните, что данные в файлах общего хранилища никогда не изменяются, поэтому, если заданный файл общего хранилища по-прежнему находится на диске во время восстановления, он имеет то же содержимое, что и при резервном копировании, и нет необходимости перезаписывать его.</span><span class="sxs-lookup"><span data-stu-id="5915b-118">Recall that the data in common-store files never changes, so if a given common-store file is still on the disk at restore time, it has the same contents as when it was backed up and there is no need to overwrite it.</span></span>

<span data-ttu-id="5915b-119">Единственными дополнительными издержками, необходимыми для резервного копирования с помощью SIS, является то, что приложение резервного копирования должно создать резервную копию канала SIS и данные, связанные с резервными файлами.</span><span class="sxs-lookup"><span data-stu-id="5915b-119">The only additional overhead required for SIS-assisted backups is that your backup application must back up the SIS link and the data associated with the backing files.</span></span> <span data-ttu-id="5915b-120">Все операции резервного копирования и восстановления SIS являются локальными для определенного тома.</span><span class="sxs-lookup"><span data-stu-id="5915b-120">All SIS backup and restore operations are local to a specific volume.</span></span>

 

 