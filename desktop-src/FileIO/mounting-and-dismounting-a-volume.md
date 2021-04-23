---
description: Процесс создания подключенной папки состоит из двух этапов.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Создание подключенных папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684564"
---
# <a name="creating-mounted-folders"></a><span data-ttu-id="bcea1-103">Создание подключенных папок</span><span class="sxs-lookup"><span data-stu-id="bcea1-103">Creating Mounted Folders</span></span>

<span data-ttu-id="bcea1-104">Процесс создания подключенной папки состоит из двух этапов.</span><span class="sxs-lookup"><span data-stu-id="bcea1-104">Creating a mounted folder is a two-step process.</span></span> <span data-ttu-id="bcea1-105">Сначала вызовите [**жетволуменамефорволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) с точкой подключения (буква диска, путь GUID тома или подключенная папка) тома, который будет назначен подключенной папке.</span><span class="sxs-lookup"><span data-stu-id="bcea1-105">First, call [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) with the mount point (drive letter, volume GUID path, or mounted folder) of the volume to be assigned to the mounted folder.</span></span> <span data-ttu-id="bcea1-106">Затем используйте функцию [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , чтобы связать возвращенный путь GUID тома с нужным каталогом на другом томе.</span><span class="sxs-lookup"><span data-stu-id="bcea1-106">Then use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to associate the returned volume GUID path with the desired directory on another volume.</span></span> <span data-ttu-id="bcea1-107">Пример кода см. [в разделе Создание подключенной папки](mounting-a-volume-at-a-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="bcea1-107">For example code, see [Creating a Mounted Folder](mounting-a-volume-at-a-mount-point.md).</span></span>

<span data-ttu-id="bcea1-108">Приложение может назначить любой пустой каталог на томе, отличном от корневого, в качестве подключенной папки.</span><span class="sxs-lookup"><span data-stu-id="bcea1-108">Your application can designate any empty directory on a volume other than the root as a mounted folder.</span></span> <span data-ttu-id="bcea1-109">При вызове функции [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) этот каталог преобразуется в подключенную папку.</span><span class="sxs-lookup"><span data-stu-id="bcea1-109">When you call the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, that directory becomes the mounted folder.</span></span> <span data-ttu-id="bcea1-110">Один и тот же том можно назначить нескольким подключенным папкам.</span><span class="sxs-lookup"><span data-stu-id="bcea1-110">You can assign the same volume to multiple mounted folders.</span></span>

<span data-ttu-id="bcea1-111">После установки подключенной папки она будет поддерживаться автоматически при перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="bcea1-111">After the mounted folder has been established, it is maintained through computer restarts automatically.</span></span>

<span data-ttu-id="bcea1-112">В случае сбоя тома все тома, назначенные подключенным папкам на этом томе, больше не будут доступны через эти подключенные папки.</span><span class="sxs-lookup"><span data-stu-id="bcea1-112">If a volume fails, any volumes that have been assigned to mounted folders on that volume can no longer be accessed through those mounted folders.</span></span> <span data-ttu-id="bcea1-113">Например, предположим, что у вас есть два тома C: и D:, и что D: связано с подключенной папкой C: \\ Mount \\ .</span><span class="sxs-lookup"><span data-stu-id="bcea1-113">For example, suppose you have two volumes, C: and D:, and that D: is associated with the mounted folder C:\\MountD\\.</span></span> <span data-ttu-id="bcea1-114">Если том C: завершается сбоем, том D: не может быть доступен по пути C: \\ Mount \\ .</span><span class="sxs-lookup"><span data-stu-id="bcea1-114">If volume C: fails, volume D: can no longer be accessed through the path C:\\MountD\\.</span></span>

<span data-ttu-id="bcea1-115">Подключенные папки могут иметь только тома файловой системы NTFS, но целевые тома для подключенных папок могут быть томами не NTFS.</span><span class="sxs-lookup"><span data-stu-id="bcea1-115">Only NTFS file system volumes can have mounted folders, but the target volumes for the mounted folders can be non-NTFS volumes.</span></span>

<span data-ttu-id="bcea1-116">Подключенные папки реализуются с помощью точек повторного анализа и подвержены их ограничениям.</span><span class="sxs-lookup"><span data-stu-id="bcea1-116">Mounted folders are implemented by using reparse points and are subject to their restrictions.</span></span> <span data-ttu-id="bcea1-117">Дополнительные сведения см. в разделе [точки повторного анализа](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="bcea1-117">For more information, see [Reparse Points](reparse-points.md).</span></span> <span data-ttu-id="bcea1-118">Нет необходимости манипулировать точками повторного анализа для использования подключенных папок. такие функции, как [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , обрабатывали все данные точки повторной обработки.</span><span class="sxs-lookup"><span data-stu-id="bcea1-118">It is not necessary to manipulate reparse points to use mounted folders; functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) handle all the reparse point details for you.</span></span>

<span data-ttu-id="bcea1-119">Поскольку подключенные папки являются каталогами, их можно переименовывать, удалять, перемещать и иным образом манипулировать ими, как и другие каталоги.</span><span class="sxs-lookup"><span data-stu-id="bcea1-119">Because mounted folders are directories, you can rename, remove, move, and otherwise manipulate them, as you would other directories.</span></span>

<span data-ttu-id="bcea1-120">(Примечание. в документации TechNet используется термин *подключенные диски* для ссылки на *подключенные папки*.)</span><span class="sxs-lookup"><span data-stu-id="bcea1-120">(Note: The TechNet documentation uses the term *mounted drives* to refer to *mounted folders*.)</span></span>

 

 



