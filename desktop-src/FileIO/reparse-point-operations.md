---
description: Описывает операции точки повторного анализа, которые можно выполнить с помощью DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Операции с точкой повторного анализа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081298"
---
# <a name="reparse-point-operations"></a><span data-ttu-id="dec7b-103">Операции с точкой повторного анализа</span><span class="sxs-lookup"><span data-stu-id="dec7b-103">Reparse Point Operations</span></span>

<span data-ttu-id="dec7b-104">Чтобы определить, поддерживает ли файл точки повторного анализа, вызовите функцию [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) и проверьте, что **файл \_ поддерживает битовые \_ \_ точки повторного анализа** .</span><span class="sxs-lookup"><span data-stu-id="dec7b-104">To determine whether a file system supports reparse points, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_REPARSE\_POINTS** bit flag.</span></span>

<span data-ttu-id="dec7b-105">Функция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) позволяет устанавливать, изменять, получать и удалять точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="dec7b-105">The [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables you to set, modify, obtain, and remove reparse points.</span></span> <span data-ttu-id="dec7b-106">В следующей таблице описаны операции точки повторного анализа, которые можно выполнить с помощью **DeviceIoControl**.</span><span class="sxs-lookup"><span data-stu-id="dec7b-106">The following table describes the reparse point operations that you can perform using **DeviceIoControl**.</span></span>



| <span data-ttu-id="dec7b-107">Операция</span><span class="sxs-lookup"><span data-stu-id="dec7b-107">Operation</span></span>                                                           | <span data-ttu-id="dec7b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="dec7b-108">Description</span></span>                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dec7b-109">**ФСКТЛ \_ задать \_ точку повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="dec7b-109">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | <span data-ttu-id="dec7b-110">Позволяет вызывающей программе задать новую точку повторного анализа или изменить существующую.</span><span class="sxs-lookup"><span data-stu-id="dec7b-110">Allows the calling program to set a new reparse point, or to modify an existing one.</span></span><br/> |
| [<span data-ttu-id="dec7b-111">**ФСКТЛ \_ получить \_ точку повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="dec7b-111">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | <span data-ttu-id="dec7b-112">Получает сведения, хранящиеся в существующей точке повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="dec7b-112">Obtains the information stored in an existing reparse point.</span></span><br/>                         |
| [<span data-ttu-id="dec7b-113">**ФСКТЛ \_ удалить \_ точку повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="dec7b-113">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | <span data-ttu-id="dec7b-114">Удаляет существующую точку повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="dec7b-114">Removes an existing reparse point.</span></span><br/>                                                   |



 

<span data-ttu-id="dec7b-115">При изменении, получении или удалении точки повторного анализа необходимо указать один и тот же тег повторного анализа в операции, содержащейся в файле.</span><span class="sxs-lookup"><span data-stu-id="dec7b-115">If you are modifying, getting, or deleting a reparse point, you must specify the same reparse tag in the operation that is contained in the file.</span></span> <span data-ttu-id="dec7b-116">В противном случае операция завершится ошибкой с **\_ \_ \_ несоответствием тега ошибки повторного анализа** ошибок.</span><span class="sxs-lookup"><span data-stu-id="dec7b-116">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_TAG\_MISMATCH**.</span></span> <span data-ttu-id="dec7b-117">При изменении или удалении точки повторного анализа необходимо также указать **идентификатор GUID** повторного анализа в операции, содержащейся в файле.</span><span class="sxs-lookup"><span data-stu-id="dec7b-117">If you are modifying or deleting a reparse point, you must also specify the reparse **GUID** in the operation that is contained in the file.</span></span> <span data-ttu-id="dec7b-118">В противном случае операция завершится ошибкой с **\_ \_ \_ конфликтом атрибута ошибки повторного анализа**.</span><span class="sxs-lookup"><span data-stu-id="dec7b-118">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**.</span></span>

<span data-ttu-id="dec7b-119">Чтобы определить, содержит ли файл или каталог точку повторного анализа, используйте функцию [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="dec7b-119">To determine whether a file or directory contains a reparse point, use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function.</span></span> <span data-ttu-id="dec7b-120">Если файл или каталог имеет связанную точку повторного анализа, то устанавливается **атрибут \_ File \_ \_ Point для повторного анализа** .</span><span class="sxs-lookup"><span data-stu-id="dec7b-120">If the file or directory has an associated reparse point, the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute is set.</span></span>

<span data-ttu-id="dec7b-121">Чтобы перезаписать существующую точку повторного анализа без обработки файла или каталога, вызовите [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с **\_ флагом файла \_ открыть \_ \_ точку повторного анализа**.</span><span class="sxs-lookup"><span data-stu-id="dec7b-121">To overwrite an existing reparse point without already having a handle to the file or directory, call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) with **FILE\_FLAG\_OPEN\_REPARSE\_POINT**.</span></span> <span data-ttu-id="dec7b-122">Этот флаг позволяет открыть файл независимо от того, установлен и работает соответствующий фильтр файловой системы.</span><span class="sxs-lookup"><span data-stu-id="dec7b-122">This flag allows you to open the file whether or not the corresponding file system filter is installed and working correctly.</span></span>

 

