---
description: Функции, используемые для управления подключенными папками.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Функции подключенных папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346082"
---
# <a name="mounted-folder-functions"></a><span data-ttu-id="9384e-103">Функции подключенных папок</span><span class="sxs-lookup"><span data-stu-id="9384e-103">Mounted Folder Functions</span></span>

<span data-ttu-id="9384e-104">Функции подключенных папок можно разделить на три группы: функции общего назначения, функции, используемые для проверки томов, и функции, используемые для сканирования тома для подключенных папок.</span><span class="sxs-lookup"><span data-stu-id="9384e-104">The mounted folder functions can be divided into three groups: general-purpose functions, functions used to scan for volumes, and functions used to scan a volume for mounted folders.</span></span>

## <a name="general-purpose-mounted-folder-functions"></a><span data-ttu-id="9384e-105">General-Purpose функции подключенных папок</span><span class="sxs-lookup"><span data-stu-id="9384e-105">General-Purpose Mounted Folder Functions</span></span>



| <span data-ttu-id="9384e-106">Функция</span><span class="sxs-lookup"><span data-stu-id="9384e-106">Function</span></span>                                                                     | <span data-ttu-id="9384e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9384e-107">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9384e-108">**делетеволумемаунтпоинт**</span><span class="sxs-lookup"><span data-stu-id="9384e-108">**DeleteVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | <span data-ttu-id="9384e-109">Удаляет букву диска или подключенную папку.</span><span class="sxs-lookup"><span data-stu-id="9384e-109">Deletes a drive letter or mounted folder.</span></span>                                                                                                                   |
| [<span data-ttu-id="9384e-110">**жетволуменамефорволумемаунтпоинт**</span><span class="sxs-lookup"><span data-stu-id="9384e-110">**GetVolumeNameForVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | <span data-ttu-id="9384e-111">Получение пути GUID тома, связанного с указанной точкой подключения тома (буква диска, путь GUID тома или подключенная папка).</span><span class="sxs-lookup"><span data-stu-id="9384e-111">Retrieves the volume GUID path for the volume that is associated with the specified volume mount point (drive letter, volume GUID path, or mounted folder).</span></span> |
| [<span data-ttu-id="9384e-112">**жетволумепаснаме**</span><span class="sxs-lookup"><span data-stu-id="9384e-112">**GetVolumePathName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | <span data-ttu-id="9384e-113">Извлекает подключенную папку, связанную с указанным томом.</span><span class="sxs-lookup"><span data-stu-id="9384e-113">Retrieves the mounted folder that is associated with the specified volume.</span></span>                                                                                  |
| [<span data-ttu-id="9384e-114">**сетволумемаунтпоинт**</span><span class="sxs-lookup"><span data-stu-id="9384e-114">**SetVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | <span data-ttu-id="9384e-115">Связывает том с буквой диска или каталогом на другом томе.</span><span class="sxs-lookup"><span data-stu-id="9384e-115">Associates a volume with a drive letter or a directory on another volume.</span></span>                                                                                   |



 

## <a name="volume-scanning-functions"></a><span data-ttu-id="9384e-116">Функции Volume-Scanning</span><span class="sxs-lookup"><span data-stu-id="9384e-116">Volume-Scanning Functions</span></span>



| <span data-ttu-id="9384e-117">Функция</span><span class="sxs-lookup"><span data-stu-id="9384e-117">Function</span></span>                                   | <span data-ttu-id="9384e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9384e-118">Description</span></span>                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9384e-119">**финдфирстволуме**</span><span class="sxs-lookup"><span data-stu-id="9384e-119">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | <span data-ttu-id="9384e-120">Возвращает имя тома на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9384e-120">Returns the name of a volume on a computer.</span></span> <span data-ttu-id="9384e-121">[**Финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) используется для начала перечисления томов компьютера.</span><span class="sxs-lookup"><span data-stu-id="9384e-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) is used to begin enumerating the volumes of a computer.</span></span> |
| [<span data-ttu-id="9384e-122">**финднекстволуме**</span><span class="sxs-lookup"><span data-stu-id="9384e-122">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | <span data-ttu-id="9384e-123">Возобновляет поиск тома, запущенный с помощью вызова [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="9384e-123">Continues a volume search started by a call to [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span>                                                     |
| [<span data-ttu-id="9384e-124">**финдволумеклосе**</span><span class="sxs-lookup"><span data-stu-id="9384e-124">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | <span data-ttu-id="9384e-125">Закрывает Поиск томов.</span><span class="sxs-lookup"><span data-stu-id="9384e-125">Closes a search for volumes.</span></span>                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a><span data-ttu-id="9384e-126">Функции сканирования подключенных папок</span><span class="sxs-lookup"><span data-stu-id="9384e-126">Mounted Folder Scanning Functions</span></span>



| <span data-ttu-id="9384e-127">Функция</span><span class="sxs-lookup"><span data-stu-id="9384e-127">Function</span></span>                                                       | <span data-ttu-id="9384e-128">Описание</span><span class="sxs-lookup"><span data-stu-id="9384e-128">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9384e-129">**финдфирстволумемаунтпоинт**</span><span class="sxs-lookup"><span data-stu-id="9384e-129">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | <span data-ttu-id="9384e-130">Извлекает имя подключенной папки на указанном томе.</span><span class="sxs-lookup"><span data-stu-id="9384e-130">Retrieves the name of a mounted folder on the specified volume.</span></span> <span data-ttu-id="9384e-131">[**Финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) используется для начала сканирования подключенных папок на томе.</span><span class="sxs-lookup"><span data-stu-id="9384e-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) is used to begin scanning the mounted folders on a volume.</span></span> |
| [<span data-ttu-id="9384e-132">**финднекстволумемаунтпоинт**</span><span class="sxs-lookup"><span data-stu-id="9384e-132">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | <span data-ttu-id="9384e-133">Возобновляет поиск подключенных папок, начатый вызовом [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span><span class="sxs-lookup"><span data-stu-id="9384e-133">Continues a mounted folder search started by a call to [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span>                                                                    |
| [<span data-ttu-id="9384e-134">**финдволумемаунтпоинтклосе**</span><span class="sxs-lookup"><span data-stu-id="9384e-134">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | <span data-ttu-id="9384e-135">Закрывает поиск подключенных папок.</span><span class="sxs-lookup"><span data-stu-id="9384e-135">Closes a search for mounted folders.</span></span>                                                                                                                                                      |



 

 

 



