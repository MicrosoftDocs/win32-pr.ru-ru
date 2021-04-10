---
description: Функции, используемые в управлении каталогом.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Функции управления каталогом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266136"
---
# <a name="directory-management-functions"></a><span data-ttu-id="e374e-103">Функции управления каталогом</span><span class="sxs-lookup"><span data-stu-id="e374e-103">Directory Management Functions</span></span>

<span data-ttu-id="e374e-104">В управлении каталогами используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="e374e-104">The following functions are used in directory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e374e-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="e374e-105">In this section</span></span>



| <span data-ttu-id="e374e-106">Функция</span><span class="sxs-lookup"><span data-stu-id="e374e-106">Function</span></span>                                                                      | <span data-ttu-id="e374e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e374e-107">Description</span></span>                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e374e-108">**CreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="e374e-108">**CreateDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | <span data-ttu-id="e374e-109">Создает каталог.</span><span class="sxs-lookup"><span data-stu-id="e374e-109">Creates a new directory.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="e374e-110">**креатедиректорекс**</span><span class="sxs-lookup"><span data-stu-id="e374e-110">**CreateDirectoryEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | <span data-ttu-id="e374e-111">Создает новый каталог с атрибутами указанного каталога шаблонов.</span><span class="sxs-lookup"><span data-stu-id="e374e-111">Creates a new directory with the attributes of a specified template directory.</span></span><br/>                                                                                 |
| [<span data-ttu-id="e374e-112">**креатедиректоритрансактед**</span><span class="sxs-lookup"><span data-stu-id="e374e-112">**CreateDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | <span data-ttu-id="e374e-113">Создает новый каталог в качестве транзакционной операции с атрибутами указанного каталога шаблона.</span><span class="sxs-lookup"><span data-stu-id="e374e-113">Creates a new directory as a transacted operation, with the attributes of a specified template directory.</span></span><br/>                                                      |
| [<span data-ttu-id="e374e-114">**финдклосечанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="e374e-114">**FindCloseChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | <span data-ttu-id="e374e-115">Останавливает наблюдение за обработчиком уведомлений об изменениях.</span><span class="sxs-lookup"><span data-stu-id="e374e-115">Stops change notification handle monitoring.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="e374e-116">**финдфирстчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="e374e-116">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | <span data-ttu-id="e374e-117">Создает обработчик уведомлений об изменениях и настраивает начальные условия фильтра уведомлений об изменении.</span><span class="sxs-lookup"><span data-stu-id="e374e-117">Creates a change notification handle and sets up initial change notification filter conditions.</span></span><br/>                                                                |
| [<span data-ttu-id="e374e-118">**финднекстчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="e374e-118">**FindNextChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | <span data-ttu-id="e374e-119">Запрашивает обработку уведомления об изменении операционной системой в следующий раз, когда обнаруживается соответствующее изменение.</span><span class="sxs-lookup"><span data-stu-id="e374e-119">Requests that the operating system signal a change notification handle the next time it detects an appropriate change.</span></span><br/>                                         |
| [<span data-ttu-id="e374e-120">**GetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="e374e-120">**GetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | <span data-ttu-id="e374e-121">Извлекает текущий каталог для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="e374e-121">Retrieves the current directory for the current process.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="e374e-122">**реаддиректоричанжесексв**</span><span class="sxs-lookup"><span data-stu-id="e374e-122">**ReadDirectoryChangesExW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | <span data-ttu-id="e374e-123">Извлекает сведения, описывающие изменения в указанном каталоге, которые могут включать расширенные сведения, если указан этот тип сведений.</span><span class="sxs-lookup"><span data-stu-id="e374e-123">Retrieves information that describes the changes within the specified directory, which can include extended information if that information type is specified.</span></span><br/> |
| [<span data-ttu-id="e374e-124">**реаддиректоричанжесв**</span><span class="sxs-lookup"><span data-stu-id="e374e-124">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | <span data-ttu-id="e374e-125">Извлекает сведения, описывающие изменения в указанном каталоге.</span><span class="sxs-lookup"><span data-stu-id="e374e-125">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                               |
| [<span data-ttu-id="e374e-126">**ремоведиректори**</span><span class="sxs-lookup"><span data-stu-id="e374e-126">**RemoveDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | <span data-ttu-id="e374e-127">Удаляет существующий пустой каталог.</span><span class="sxs-lookup"><span data-stu-id="e374e-127">Deletes an existing empty directory.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="e374e-128">**ремоведиректоритрансактед**</span><span class="sxs-lookup"><span data-stu-id="e374e-128">**RemoveDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | <span data-ttu-id="e374e-129">Удаляет существующий пустой каталог в качестве транзакционной операции.</span><span class="sxs-lookup"><span data-stu-id="e374e-129">Deletes an existing empty directory as a transacted operation.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="e374e-130">**сеткуррентдиректори**</span><span class="sxs-lookup"><span data-stu-id="e374e-130">**SetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | <span data-ttu-id="e374e-131">Изменяет текущий каталог для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="e374e-131">Changes the current directory for the current process.</span></span><br/>                                                                                                         |



 

 

 




