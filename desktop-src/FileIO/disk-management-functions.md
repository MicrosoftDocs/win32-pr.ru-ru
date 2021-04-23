---
description: Функции, используемые в управлении дисками.
ms.assetid: 301d3062-29a1-4b44-bbcd-e9d5b7d7823b
title: Функции управления дисками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677443c58aa8b9a60758d817e31e3804ef25ae66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684195"
---
# <a name="disk-management-functions"></a><span data-ttu-id="8e5cf-103">Функции управления дисками</span><span class="sxs-lookup"><span data-stu-id="8e5cf-103">Disk Management Functions</span></span>

<span data-ttu-id="8e5cf-104">В оснастке «Управление дисками» используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-104">The following functions are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8e5cf-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="8e5cf-105">In this section</span></span>



| <span data-ttu-id="8e5cf-106">Функция</span><span class="sxs-lookup"><span data-stu-id="8e5cf-106">Function</span></span>                                                    | <span data-ttu-id="8e5cf-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8e5cf-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e5cf-108">**жетдискфриспаце**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-108">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)<br/>     | <span data-ttu-id="8e5cf-109">Извлекает сведения о указанном диске, включая объем свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-109">Retrieves information about the specified disk, including the amount of free space on the disk.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="8e5cf-110">**жетдискфриспацеекс**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-110">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)<br/> | <span data-ttu-id="8e5cf-111">Извлекает сведения о объеме пространства, доступного на томе диска, общем объеме пространства, общем объеме свободного пространства и общем объеме свободного пространства, доступного пользователю, связанному с вызывающим потоком.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-111">Retrieves information about the amount of space that is available on a disk volume, which is the total amount of space, the total amount of free space, and the total amount of free space available to the user that is associated with the calling thread.</span></span><br/> |



 

<span data-ttu-id="8e5cf-112">Другие функции, используемые в управлении дисками.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-112">Other functions used in disk management.</span></span>



| <span data-ttu-id="8e5cf-113">Функция</span><span class="sxs-lookup"><span data-stu-id="8e5cf-113">Function</span></span>                         | <span data-ttu-id="8e5cf-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8e5cf-114">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e5cf-115">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-115">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) | <span data-ttu-id="8e5cf-116">Создает или открывает файл или устройство ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-116">Creates or opens a file or I/O device.</span></span> <span data-ttu-id="8e5cf-117">Чаще всего используются следующие устройства ввода-вывода: файл, файловый поток, каталог, физический диск, том, буфер консоли, ленточный накопитель, ресурс связи, почтовый слот и канал.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-117">The most commonly used I/O devices are as follows: file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe.</span></span><br/> |
| [<span data-ttu-id="8e5cf-118">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-118">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) | <span data-ttu-id="8e5cf-119">Удаляет существующий файл.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-119">Deletes an existing file.</span></span><br/>                                                                                                                                                                                               |



 

 

 




