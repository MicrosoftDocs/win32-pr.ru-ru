---
description: Каждый раз, когда процесс создает или открывает объект каталога, он получает обработчик для объекта.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Дескрипторы каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664605"
---
# <a name="directory-handles"></a><span data-ttu-id="682b2-103">Дескрипторы каталогов</span><span class="sxs-lookup"><span data-stu-id="682b2-103">Directory Handles</span></span>

<span data-ttu-id="682b2-104">Каждый раз, когда процесс создает или открывает объект каталога, он получает обработчик для объекта.</span><span class="sxs-lookup"><span data-stu-id="682b2-104">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span>

<span data-ttu-id="682b2-105">Чтобы получить маркер существующего каталога, вызовите функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с флагом **File \_ Flag \_ \_ семантики резервного копирования** .</span><span class="sxs-lookup"><span data-stu-id="682b2-105">To obtain a handle to an existing directory, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag.</span></span>

<span data-ttu-id="682b2-106">Вы можете передать маркер каталога следующим функциям.</span><span class="sxs-lookup"><span data-stu-id="682b2-106">You can pass a directory handle to the following functions.</span></span>



| <span data-ttu-id="682b2-107">Функция</span><span class="sxs-lookup"><span data-stu-id="682b2-107">Function</span></span>                                                         | <span data-ttu-id="682b2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="682b2-108">Description</span></span>                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="682b2-109">**баккупреад**</span><span class="sxs-lookup"><span data-stu-id="682b2-109">**BackupRead**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupread)                              | <span data-ttu-id="682b2-110">Создайте резервную копию файла или каталога, включая сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="682b2-110">Back up a file or directory, including the security information.</span></span><br/>                                                                                      |
| [<span data-ttu-id="682b2-111">**баккупсик**</span><span class="sxs-lookup"><span data-stu-id="682b2-111">**BackupSeek**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | <span data-ttu-id="682b2-112">Поиск вперед в потоке данных, доступ к которому осуществляется с помощью функции [**баккупреад**](/windows/desktop/api/winbase/nf-winbase-backupread) или [**баккупврите**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .</span><span class="sxs-lookup"><span data-stu-id="682b2-112">Seeks forward in a data stream initially accessed by using the [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) or [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) function.</span></span><br/> |
| [<span data-ttu-id="682b2-113">**баккупврите**</span><span class="sxs-lookup"><span data-stu-id="682b2-113">**BackupWrite**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | <span data-ttu-id="682b2-114">Восстановление файла или каталога, резервная копия которых была создана с помощью [**баккупреад**](/windows/desktop/api/winbase/nf-winbase-backupread).</span><span class="sxs-lookup"><span data-stu-id="682b2-114">Restore a file or directory that was backed up using [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span></span><br/>                                                             |
| [<span data-ttu-id="682b2-115">**жетфилеинформатионбихандле**</span><span class="sxs-lookup"><span data-stu-id="682b2-115">**GetFileInformationByHandle**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | <span data-ttu-id="682b2-116">Возвращает сведения о файле для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="682b2-116">Retrieves file information for the specified file.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="682b2-117">**GetFileSize**</span><span class="sxs-lookup"><span data-stu-id="682b2-117">**GetFileSize**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | <span data-ttu-id="682b2-118">Возвращает размер указанного файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="682b2-118">Retrieves the size of the specified file, in bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="682b2-119">**Функции getFileTime**</span><span class="sxs-lookup"><span data-stu-id="682b2-119">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="682b2-120">Извлекает дату и время создания файла или каталога, последнего доступа и последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="682b2-120">Retrieves the date and time that a file or directory was created, last accessed, and last modified.</span></span><br/>                                                   |
| [<span data-ttu-id="682b2-121">**жетфилетипе**</span><span class="sxs-lookup"><span data-stu-id="682b2-121">**GetFileType**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | <span data-ttu-id="682b2-122">Возвращает тип файла указанного файла.</span><span class="sxs-lookup"><span data-stu-id="682b2-122">Retrieves the file type of the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="682b2-123">**реаддиректоричанжесв**</span><span class="sxs-lookup"><span data-stu-id="682b2-123">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | <span data-ttu-id="682b2-124">Извлекает сведения, описывающие изменения в указанном каталоге.</span><span class="sxs-lookup"><span data-stu-id="682b2-124">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                      |
| [<span data-ttu-id="682b2-125">**сетфилетиме**</span><span class="sxs-lookup"><span data-stu-id="682b2-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="682b2-126">Задает дату и время создания указанного файла или каталога, последнего доступа или последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="682b2-126">Sets the date and time that the specified file or directory was created, last accessed, or last modified.</span></span><br/>                                             |



 

 

