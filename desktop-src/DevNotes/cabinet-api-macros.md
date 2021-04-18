---
description: 'Дополнительные сведения: макросы API CAB-файла'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Макросы API CAB-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538303"
---
# <a name="cabinet-api-macros"></a><span data-ttu-id="36eb2-103">Макросы API CAB-файла</span><span class="sxs-lookup"><span data-stu-id="36eb2-103">Cabinet API Macros</span></span>

<span data-ttu-id="36eb2-104">В этом разделе описываются макросы, используемые API CAB-файлов:</span><span class="sxs-lookup"><span data-stu-id="36eb2-104">This section details the macros used by the Cabinet API:</span></span>

## <a name="fci-macros"></a><span data-ttu-id="36eb2-105">FCI макросы</span><span class="sxs-lookup"><span data-stu-id="36eb2-105">FCI Macros</span></span>

<span data-ttu-id="36eb2-106">FCI использует следующие макросы:</span><span class="sxs-lookup"><span data-stu-id="36eb2-106">The following macros are used by FCI:</span></span>



| <span data-ttu-id="36eb2-107">Макрос</span><span class="sxs-lookup"><span data-stu-id="36eb2-107">Macro</span></span>                                              | <span data-ttu-id="36eb2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="36eb2-108">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36eb2-109">**фнфЦиаллок**</span><span class="sxs-lookup"><span data-stu-id="36eb2-109">**FNFCIALLOC**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | <span data-ttu-id="36eb2-110">Используется для выделения памяти в контексте FCI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-110">Used to allocate memory in an FCI context.</span></span><br/>                                          |
| [<span data-ttu-id="36eb2-111">**фнфЦиклосе**</span><span class="sxs-lookup"><span data-stu-id="36eb2-111">**FNFCICLOSE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | <span data-ttu-id="36eb2-112">Используется для закрытия файла.</span><span class="sxs-lookup"><span data-stu-id="36eb2-112">Used to close a file.</span></span><br/>                                                               |
| [<span data-ttu-id="36eb2-113">**фнфЦиделете**</span><span class="sxs-lookup"><span data-stu-id="36eb2-113">**FNFCIDELETE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | <span data-ttu-id="36eb2-114">Используется для удаления файла.</span><span class="sxs-lookup"><span data-stu-id="36eb2-114">Used to delete a file.</span></span><br/>                                                              |
| [<span data-ttu-id="36eb2-115">**фнфЦифилеплацед**</span><span class="sxs-lookup"><span data-stu-id="36eb2-115">**FNFCIFILEPLACED**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | <span data-ttu-id="36eb2-116">Используется для уведомления о помещении файла в CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="36eb2-116">Used to notify when a file is placed in the cabinet.</span></span><br/>                                |
| [<span data-ttu-id="36eb2-117">**фнфЦифри**</span><span class="sxs-lookup"><span data-stu-id="36eb2-117">**FNFCIFREE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | <span data-ttu-id="36eb2-118">Используется для высвобождения ранее выделенной памяти в контексте FCI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-118">Used to free previously allocated memory in an FCI context.</span></span><br/>                         |
| [<span data-ttu-id="36eb2-119">**фнфЦижетнексткабинет**</span><span class="sxs-lookup"><span data-stu-id="36eb2-119">**FNFCIGETNEXTCABINET**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | <span data-ttu-id="36eb2-120">Используется для запроса информации для следующего CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="36eb2-120">Used to request information for the next cabinet.</span></span><br/>                                   |
| [<span data-ttu-id="36eb2-121">**фнфЦижетопенинфо**</span><span class="sxs-lookup"><span data-stu-id="36eb2-121">**FNFCIGETOPENINFO**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | <span data-ttu-id="36eb2-122">Используется для открытия файла и получения даты, времени и атрибутов файла.</span><span class="sxs-lookup"><span data-stu-id="36eb2-122">Used to open a file and retrieve file date, time, and attributes.</span></span><br/>                   |
| [<span data-ttu-id="36eb2-123">**фнфЦижеттемпфиле**</span><span class="sxs-lookup"><span data-stu-id="36eb2-123">**FNFCIGETTEMPFILE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | <span data-ttu-id="36eb2-124">Используется для получения имени временного файла.</span><span class="sxs-lookup"><span data-stu-id="36eb2-124">Used to obtain a temporary file name.</span></span><br/>                                               |
| [<span data-ttu-id="36eb2-125">**фнфЦиопен**</span><span class="sxs-lookup"><span data-stu-id="36eb2-125">**FNFCIOPEN**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | <span data-ttu-id="36eb2-126">Используется для открытия файла в контексте FCI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-126">Used to open a file in an FCI context.</span></span><br/>                                              |
| [<span data-ttu-id="36eb2-127">**фнфЦиреад**</span><span class="sxs-lookup"><span data-stu-id="36eb2-127">**FNFCIREAD**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciread)                     | <span data-ttu-id="36eb2-128">Используется для чтения данных из файла.</span><span class="sxs-lookup"><span data-stu-id="36eb2-128">Used to read data from a file.</span></span><br/>                                                      |
| [<span data-ttu-id="36eb2-129">**фнфЦисик**</span><span class="sxs-lookup"><span data-stu-id="36eb2-129">**FNFCISEEK**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | <span data-ttu-id="36eb2-130">Используется для перемещения указателя файла в указанное место.</span><span class="sxs-lookup"><span data-stu-id="36eb2-130">Used to move a file pointer to a specified location.</span></span><br/>                                |
| [<span data-ttu-id="36eb2-131">**фнфЦистатус**</span><span class="sxs-lookup"><span data-stu-id="36eb2-131">**FNFCISTATUS**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | <span data-ttu-id="36eb2-132">Используется для обновления пользователя.</span><span class="sxs-lookup"><span data-stu-id="36eb2-132">Used to update the user.</span></span><br/>                                                            |
| [<span data-ttu-id="36eb2-133">**фнфЦиврите**</span><span class="sxs-lookup"><span data-stu-id="36eb2-133">**FNFCIWRITE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | <span data-ttu-id="36eb2-134">Используется для записи данных в файл.</span><span class="sxs-lookup"><span data-stu-id="36eb2-134">Used to write data to a file.</span></span><br/>                                                       |
| [<span data-ttu-id="36eb2-135">**ткомпфромлзксвиндов**</span><span class="sxs-lookup"><span data-stu-id="36eb2-135">**TCOMPfromLZXWindow**</span></span>](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | <span data-ttu-id="36eb2-136">Преобразует размер Windows в значение ЛКСЗ ТКОМП для [**фЦиаддфиле**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span><span class="sxs-lookup"><span data-stu-id="36eb2-136">Converts windows size into an LXZ TCOMP value for [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span></span><br/> |



 

## <a name="fdi-macros"></a><span data-ttu-id="36eb2-137">FDI макросы</span><span class="sxs-lookup"><span data-stu-id="36eb2-137">FDI Macros</span></span>

<span data-ttu-id="36eb2-138">FDI использует следующие макросы:</span><span class="sxs-lookup"><span data-stu-id="36eb2-138">The following macros are used by FDI:</span></span>



| <span data-ttu-id="36eb2-139">Макрос</span><span class="sxs-lookup"><span data-stu-id="36eb2-139">Macro</span></span>                              | <span data-ttu-id="36eb2-140">Описание</span><span class="sxs-lookup"><span data-stu-id="36eb2-140">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="36eb2-141">**фналлок**</span><span class="sxs-lookup"><span data-stu-id="36eb2-141">**FNALLOC**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | <span data-ttu-id="36eb2-142">Используется для выделения памяти в контексте FDI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-142">Used to allocate memory in an FDI context.</span></span><br/>                               |
| [<span data-ttu-id="36eb2-143">**фнклосе**</span><span class="sxs-lookup"><span data-stu-id="36eb2-143">**FNCLOSE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnclose)         | <span data-ttu-id="36eb2-144">Используется для закрытия файла в контексте FDI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-144">Used to close a file in an FDI context.</span></span><br/>                                  |
| [<span data-ttu-id="36eb2-145">**фнфдинотифи**</span><span class="sxs-lookup"><span data-stu-id="36eb2-145">**FNFDINOTIFY**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | <span data-ttu-id="36eb2-146">Используется для обновления приложения в соответствии с состоянием декодера.</span><span class="sxs-lookup"><span data-stu-id="36eb2-146">Used to update the application on the status of the decoder.</span></span><br/>             |
| [<span data-ttu-id="36eb2-147">**фнфри**</span><span class="sxs-lookup"><span data-stu-id="36eb2-147">**FNFREE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfree)           | <span data-ttu-id="36eb2-148">Используется для высвобождения ранее выделенной памяти в контексте FDI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-148">Used to free previously allocated memory in an FDI context.</span></span><br/>              |
| [<span data-ttu-id="36eb2-149">**фнопен**</span><span class="sxs-lookup"><span data-stu-id="36eb2-149">**FNOPEN**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnopen)           | <span data-ttu-id="36eb2-150">Используется для открытия файла в контексте FDI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-150">Used to open a file in an FDI context.</span></span><br/>                                   |
| [<span data-ttu-id="36eb2-151">**фнреад**</span><span class="sxs-lookup"><span data-stu-id="36eb2-151">**FNREAD**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnread)           | <span data-ttu-id="36eb2-152">Используется для чтения данных из файла в контексте FDI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-152">Used to read data from a file in an FDI context.</span></span><br/>                         |
| [<span data-ttu-id="36eb2-153">**фнсик**</span><span class="sxs-lookup"><span data-stu-id="36eb2-153">**FNSEEK**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnseek)           | <span data-ttu-id="36eb2-154">Используется для перемещения указателя файла в указанное место в контексте FDI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-154">Used to move a file pointer to the specified location in an FDI context.</span></span><br/> |
| [<span data-ttu-id="36eb2-155">**фнврите**</span><span class="sxs-lookup"><span data-stu-id="36eb2-155">**FNWRITE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | <span data-ttu-id="36eb2-156">Используется для записи данных в файл в контексте FDI.</span><span class="sxs-lookup"><span data-stu-id="36eb2-156">Used to write data to a file in an FDI context.</span></span><br/>                          |



 

## <a name="related-topics"></a><span data-ttu-id="36eb2-157">См. также</span><span class="sxs-lookup"><span data-stu-id="36eb2-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36eb2-158">Справочник по API CAB-файлов</span><span class="sxs-lookup"><span data-stu-id="36eb2-158">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="36eb2-159">Использование API CAB-файла</span><span class="sxs-lookup"><span data-stu-id="36eb2-159">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




