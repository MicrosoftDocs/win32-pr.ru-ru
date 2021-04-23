---
description: Приложения могут извлекать и задавать дату и время создания файла, последнего изменения или последнего доступа с помощью функций функции getFileTime и Сетфилетиме.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Установка и получение метки времени файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263247"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a><span data-ttu-id="75bd5-103">Установка и получение метки времени файла</span><span class="sxs-lookup"><span data-stu-id="75bd5-103">Setting and Getting the Timestamp of a File</span></span>

<span data-ttu-id="75bd5-104">Приложения могут извлекать и задавать дату и время создания файла, последнего изменения или последнего доступа с помощью функций [**функции getFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) и [**сетфилетиме**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .</span><span class="sxs-lookup"><span data-stu-id="75bd5-104">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span> <span data-ttu-id="75bd5-105">Дополнительные сведения см. в разделе [время файла](/windows/desktop/SysInfo/file-times).</span><span class="sxs-lookup"><span data-stu-id="75bd5-105">For more information, see [File Times](/windows/desktop/SysInfo/file-times).</span></span>

> [!Note]  
> <span data-ttu-id="75bd5-106">Не все файловые системы могут записывать время создания и последнего доступа, а не все файловые системы записывают их одинаковым образом.</span><span class="sxs-lookup"><span data-stu-id="75bd5-106">Not all file systems can record creation and last access times, and not all file systems record them in the same manner.</span></span> <span data-ttu-id="75bd5-107">Например, в файловой системе FAT время создания имеет разрешение 10 миллисекунд, время записи имеет разрешение 2 секунды, а время доступа имеет разрешение в 1 день (действительно, на дату доступа).</span><span class="sxs-lookup"><span data-stu-id="75bd5-107">For example, on FAT file system, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date).</span></span> <span data-ttu-id="75bd5-108">Файловая система NTFS задерживает обновление до последнего времени доступа к файлу до одного часа после последнего доступа.</span><span class="sxs-lookup"><span data-stu-id="75bd5-108">The NTFS file system delays update to the last access time for a file by up to one hour after the last access.</span></span>

 

 

 
