---
description: Диспетчер очереди печати отслеживает текущие задания печати и Целевой принтер, чтобы определить соответствующее время для печати задания.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Обработчик заданий печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650792"
---
# <a name="print-processor"></a><span data-ttu-id="6268c-103">Обработчик заданий печати</span><span class="sxs-lookup"><span data-stu-id="6268c-103">Print Processor</span></span>

<span data-ttu-id="6268c-104">Диспетчер очереди печати отслеживает текущие задания печати и Целевой принтер, чтобы определить соответствующее время для печати задания.</span><span class="sxs-lookup"><span data-stu-id="6268c-104">The print spooler monitors the current print jobs and the target printer to determine an appropriate time to print a job.</span></span> <span data-ttu-id="6268c-105">После того как диспетчер очереди печати определит, что задание должно быть напечатано, оно вызывает обработчик заданий печати.</span><span class="sxs-lookup"><span data-stu-id="6268c-105">Once the spooler determines that a job should be printed, it calls the print processor.</span></span> <span data-ttu-id="6268c-106">Обработчик заданий печати — это подключаемый модуль, который обрабатывает данные заданий печати.</span><span class="sxs-lookup"><span data-stu-id="6268c-106">The print processor is a plug-in that processes print job data.</span></span>

<span data-ttu-id="6268c-107">Используйте следующие функции для работы с обработчиками печати.</span><span class="sxs-lookup"><span data-stu-id="6268c-107">Use the following functions to work with print processors.</span></span>



| <span data-ttu-id="6268c-108">Функция</span><span class="sxs-lookup"><span data-stu-id="6268c-108">Function</span></span>                                                           | <span data-ttu-id="6268c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6268c-109">Description</span></span>                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="6268c-110">**аддпринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="6268c-110">**AddPrintProcessor**</span></span>](addprintprocessor.md)                     | <span data-ttu-id="6268c-111">Устанавливает обработчик заданий печати на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="6268c-111">Installs a print processor on a specified server.</span></span>                    |
| [<span data-ttu-id="6268c-112">**делетепринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="6268c-112">**DeletePrintProcessor**</span></span>](deleteprintprocessor.md)               | <span data-ttu-id="6268c-113">Удаляет процессор принтера с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="6268c-113">Removes a printer processor from a specified server.</span></span>                 |
| [<span data-ttu-id="6268c-114">**енумпринтпроцессордататипес**</span><span class="sxs-lookup"><span data-stu-id="6268c-114">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md) | <span data-ttu-id="6268c-115">Перечисляет типы данных, поддерживаемые указанным обработчиком печати.</span><span class="sxs-lookup"><span data-stu-id="6268c-115">Enumerates the data types that a specified print processor supports.</span></span> |
| [<span data-ttu-id="6268c-116">**енумпринтпроцессорс**</span><span class="sxs-lookup"><span data-stu-id="6268c-116">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)                 | <span data-ttu-id="6268c-117">Перечисляет обработчики печати, установленные на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="6268c-117">Enumerates the print processors installed on a specified server.</span></span>     |
| [<span data-ttu-id="6268c-118">**жетпринтпроцессордиректори**</span><span class="sxs-lookup"><span data-stu-id="6268c-118">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)   | <span data-ttu-id="6268c-119">Получает путь к обработчику заданий печати на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="6268c-119">Retrieves the path for the print processor on the specified server.</span></span>  |



 

 

 



