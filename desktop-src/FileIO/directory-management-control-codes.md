---
description: Управляющие коды, используемые с сжатием и распаковкой файлов и с точками повторного анализа.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Управляющие коды управления каталогами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912312"
---
# <a name="directory-management-control-codes"></a><span data-ttu-id="b83db-103">Управляющие коды управления каталогами</span><span class="sxs-lookup"><span data-stu-id="b83db-103">Directory Management Control Codes</span></span>

<span data-ttu-id="b83db-104">При [сжатии и](file-compression-and-decompression.md)распаковке файлов используются следующие управляющие коды.</span><span class="sxs-lookup"><span data-stu-id="b83db-104">The following control codes are used with [file compression and decompression](file-compression-and-decompression.md).</span></span>



| <span data-ttu-id="b83db-105">Контрольный код</span><span class="sxs-lookup"><span data-stu-id="b83db-105">Control Code</span></span>                                             | <span data-ttu-id="b83db-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b83db-106">Meaning</span></span>                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b83db-107">**ФСКТЛ \_ получить \_ Сжатие**</span><span class="sxs-lookup"><span data-stu-id="b83db-107">**FSCTL\_GET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | <span data-ttu-id="b83db-108">Извлекает текущее состояние сжатия файла или каталога на томе, файловая система которого поддерживает сжатие на поток.</span><span class="sxs-lookup"><span data-stu-id="b83db-108">Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.</span></span><br/>    |
| [<span data-ttu-id="b83db-109">**ФСКТЛ \_ Установка \_ сжатия**</span><span class="sxs-lookup"><span data-stu-id="b83db-109">**FSCTL\_SET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | <span data-ttu-id="b83db-110">Задает состояние сжатия файла или каталога на томе, файловая система которого поддерживает сжатие на уровне файлов и на уровне каталога.</span><span class="sxs-lookup"><span data-stu-id="b83db-110">Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.</span></span><br/> |



 

<span data-ttu-id="b83db-111">В [точках повторного анализа](reparse-points.md)используются следующие управляющие коды.</span><span class="sxs-lookup"><span data-stu-id="b83db-111">The following control codes are used with [reparse points](reparse-points.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b83db-112">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="b83db-112">In this section</span></span>



| <span data-ttu-id="b83db-113">Контрольный код</span><span class="sxs-lookup"><span data-stu-id="b83db-113">Control Code</span></span>                                                                   | <span data-ttu-id="b83db-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b83db-114">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b83db-115">**ФСКТЛ \_ удалить \_ точку повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="b83db-115">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | <span data-ttu-id="b83db-116">Удаляет точку повторного анализа из указанного файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="b83db-116">Deletes a reparse point from the specified file or directory.</span></span><br/>                                              |
| [<span data-ttu-id="b83db-117">**ФСКТЛ \_ получить \_ точку повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="b83db-117">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | <span data-ttu-id="b83db-118">Извлекает данные точки повторного анализа, связанные с файлом или каталогом, идентифицируемым указанным маркером.</span><span class="sxs-lookup"><span data-stu-id="b83db-118">Retrieves the reparse point data associated with the file or directory identified by the specified handle.</span></span><br/> |
| [<span data-ttu-id="b83db-119">**ФСКТЛ \_ задать \_ точку повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="b83db-119">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | <span data-ttu-id="b83db-120">Задает точку повторного анализа для файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="b83db-120">Sets a reparse point on a file or directory.</span></span><br/>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b83db-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b83db-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b83db-122">Управляющие коды для управления файлами</span><span class="sxs-lookup"><span data-stu-id="b83db-122">File Management Control Codes</span></span>](file-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="b83db-123">Управляющие коды для управления томами</span><span class="sxs-lookup"><span data-stu-id="b83db-123">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

