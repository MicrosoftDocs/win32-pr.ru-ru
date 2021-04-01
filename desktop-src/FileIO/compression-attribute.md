---
description: На томе файловой системы NTFS каждый файл и каталог имеет атрибут сжатия.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Атрибут Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913711"
---
# <a name="compression-attribute"></a><span data-ttu-id="4df7d-103">Атрибут Compression</span><span class="sxs-lookup"><span data-stu-id="4df7d-103">Compression Attribute</span></span>

<span data-ttu-id="4df7d-104">На томе файловой системы NTFS каждый файл и каталог имеет *атрибут сжатия*.</span><span class="sxs-lookup"><span data-stu-id="4df7d-104">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span> <span data-ttu-id="4df7d-105">Другие файловые системы также могут реализовывать атрибут сжатия для отдельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="4df7d-105">Other file systems may also implement a compression attribute for individual files and directories.</span></span>

<span data-ttu-id="4df7d-106">Определить, поддерживает ли файловая система атрибут сжатия для файлов и каталогов, можно путем вызова функции [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) и проверки флага бита **\_ \_ сжатия** файлового файла.</span><span class="sxs-lookup"><span data-stu-id="4df7d-106">You can determine whether a file system supports a compression attribute for files and directories by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_FILE\_COMPRESSION** bit flag.</span></span>

<span data-ttu-id="4df7d-107">Используйте функцию [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) или [**сбой getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) , чтобы определить атрибут сжатия файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="4df7d-107">Use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function to determine the compression attribute of a file or directory.</span></span>

<span data-ttu-id="4df7d-108">Если задан атрибут сжатия файла (**\_ \_ сжатый атрибут файла**), все данные в файле сжимаются.</span><span class="sxs-lookup"><span data-stu-id="4df7d-108">If a file's compression attribute is set (**FILE\_ATTRIBUTE\_COMPRESSED**), all data in the file is compressed.</span></span> <span data-ttu-id="4df7d-109">Если атрибут является четким, ни один из данных в файле не сжимается.</span><span class="sxs-lookup"><span data-stu-id="4df7d-109">If the attribute is clear, none of the data in the file is compressed.</span></span> <span data-ttu-id="4df7d-110">Нет частично сжатого состояния с точки зрения программирования в пользовательском режиме; атрибут Compression является простым логическим индикатором состояния сжатия.</span><span class="sxs-lookup"><span data-stu-id="4df7d-110">There is no partially compressed state from a user-mode programming perspective; the compression attribute is a simple Boolean indicator of compression state.</span></span>

<span data-ttu-id="4df7d-111">Атрибут сжатия каталога предоставляет атрибут сжатия по умолчанию для вновь создаваемых файлов и подкаталогов.</span><span class="sxs-lookup"><span data-stu-id="4df7d-111">A directory's compression attribute provides a default compression attribute for newly created files and subdirectories.</span></span> <span data-ttu-id="4df7d-112">При вызове [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) или [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) для создания нового файла или каталога новый файл или каталог наследует атрибут сжатия своего родительского каталога.</span><span class="sxs-lookup"><span data-stu-id="4df7d-112">When you call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) to create a new file or directory, the new file or directory inherits the compression attribute of its parent directory.</span></span>

<span data-ttu-id="4df7d-113">Чтобы изменить **\_ \_ сжатый атрибут файла** для файла или каталога, необходимо использовать функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с управляющим кодом [**фсктл \_ Set \_ Compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .</span><span class="sxs-lookup"><span data-stu-id="4df7d-113">To modify the **FILE\_ATTRIBUTE\_COMPRESSED** attribute for a file or directory, you must use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4df7d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4df7d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4df7d-115">**Константы атрибутов файлов**</span><span class="sxs-lookup"><span data-stu-id="4df7d-115">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 
