---
description: Функции, связанные со временем, возвращают время в одном из нескольких форматов. Функции времени можно использовать для преобразования между некоторыми форматами времени для простоты сравнения и вывода. В следующей таблице перечислены форматы времени.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: О времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080906"
---
# <a name="about-time"></a><span data-ttu-id="f62e2-105">О времени</span><span class="sxs-lookup"><span data-stu-id="f62e2-105">About Time</span></span>

<span data-ttu-id="f62e2-106">Функции, связанные со временем, возвращают время в одном из нескольких форматов.</span><span class="sxs-lookup"><span data-stu-id="f62e2-106">Time-related functions return time in one of several formats.</span></span> <span data-ttu-id="f62e2-107">Функции времени можно использовать для преобразования между некоторыми форматами времени для простоты сравнения и вывода.</span><span class="sxs-lookup"><span data-stu-id="f62e2-107">You can use the time functions to convert between some time formats for ease of comparison and display.</span></span> <span data-ttu-id="f62e2-108">В следующей таблице перечислены форматы времени.</span><span class="sxs-lookup"><span data-stu-id="f62e2-108">The following table summarizes the time formats.</span></span>



| <span data-ttu-id="f62e2-109">Формат</span><span class="sxs-lookup"><span data-stu-id="f62e2-109">Format</span></span>          | <span data-ttu-id="f62e2-110">Тип</span><span class="sxs-lookup"><span data-stu-id="f62e2-110">Type</span></span>                                                                     | <span data-ttu-id="f62e2-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f62e2-111">Description</span></span>                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62e2-112">Система</span><span class="sxs-lookup"><span data-stu-id="f62e2-112">System</span></span>          | [<span data-ttu-id="f62e2-113">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="f62e2-113">**SYSTEMTIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | <span data-ttu-id="f62e2-114">Год, месяц, день, час, секунда и миллисекунда, взятые из внутренних аппаратных часов.</span><span class="sxs-lookup"><span data-stu-id="f62e2-114">Year, month, day, hour, second, and millisecond, taken from the internal hardware clock.</span></span>                                            |
| <span data-ttu-id="f62e2-115">Локальная</span><span class="sxs-lookup"><span data-stu-id="f62e2-115">Local</span></span>           | <span data-ttu-id="f62e2-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) или [ **fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span><span class="sxs-lookup"><span data-stu-id="f62e2-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) or [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span></span> | <span data-ttu-id="f62e2-117">Системное время или время файла, преобразованное в местный часовой пояс системы.</span><span class="sxs-lookup"><span data-stu-id="f62e2-117">A system time or file time converted to the system's local time zone.</span></span>                                                               |
| <span data-ttu-id="f62e2-118">Файл</span><span class="sxs-lookup"><span data-stu-id="f62e2-118">File</span></span>            | [<span data-ttu-id="f62e2-119">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="f62e2-119">**FILETIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | <span data-ttu-id="f62e2-120">Число 100-наносекундных интервалов с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="f62e2-120">The number of 100-nanosecond intervals since January 1, 1601.</span></span>                                                                       |
| <span data-ttu-id="f62e2-121">MS-DOS</span><span class="sxs-lookup"><span data-stu-id="f62e2-121">MS-DOS</span></span>          | <span data-ttu-id="f62e2-122">**WORD**</span><span class="sxs-lookup"><span data-stu-id="f62e2-122">**WORD**</span></span>                                                                 | <span data-ttu-id="f62e2-123">Упакованное слово для даты, другое для времени.</span><span class="sxs-lookup"><span data-stu-id="f62e2-123">A packed word for the date, another for the time.</span></span>                                                                                   |
| <span data-ttu-id="f62e2-124">Windows</span><span class="sxs-lookup"><span data-stu-id="f62e2-124">Windows</span></span>         | <span data-ttu-id="f62e2-125">**DWORD** или **улонглонг**</span><span class="sxs-lookup"><span data-stu-id="f62e2-125">**DWORD** or **ULONGLONG**</span></span>                                               | <span data-ttu-id="f62e2-126">Число миллисекунд с момента последнего запуска системы.</span><span class="sxs-lookup"><span data-stu-id="f62e2-126">The number of milliseconds since the system was last started.</span></span> <span data-ttu-id="f62e2-127">При извлечении в виде значения DWORD цикл по времени Windows каждые 49,7 дней.</span><span class="sxs-lookup"><span data-stu-id="f62e2-127">When retrieved as a DWORD value, Windows time cycles every 49.7 days.</span></span> |
| <span data-ttu-id="f62e2-128">Число прерываний</span><span class="sxs-lookup"><span data-stu-id="f62e2-128">Interrupt Count</span></span> | <span data-ttu-id="f62e2-129">**улонглонг**</span><span class="sxs-lookup"><span data-stu-id="f62e2-129">**ULONGLONG**</span></span>                                                            | <span data-ttu-id="f62e2-130">Число 100-наносекундных интервалов с момента последнего запуска системы.</span><span class="sxs-lookup"><span data-stu-id="f62e2-130">The number of 100-nanosecond intervals since the system was last started.</span></span>                                                           |



 

<span data-ttu-id="f62e2-131">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f62e2-131">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f62e2-132">Системное время</span><span class="sxs-lookup"><span data-stu-id="f62e2-132">System Time</span></span>](system-time.md)
-   [<span data-ttu-id="f62e2-133">Местное время</span><span class="sxs-lookup"><span data-stu-id="f62e2-133">Local Time</span></span>](local-time.md)
-   [<span data-ttu-id="f62e2-134">Время файла</span><span class="sxs-lookup"><span data-stu-id="f62e2-134">File Times</span></span>](file-times.md)
-   [<span data-ttu-id="f62e2-135">Дата и время MS-DOS</span><span class="sxs-lookup"><span data-stu-id="f62e2-135">MS-DOS Date and Time</span></span>](ms-dos-date-and-time.md)
-   [<span data-ttu-id="f62e2-136">Служба времени Windows</span><span class="sxs-lookup"><span data-stu-id="f62e2-136">Windows Time</span></span>](windows-time.md)
-   [<span data-ttu-id="f62e2-137">Время прерываний</span><span class="sxs-lookup"><span data-stu-id="f62e2-137">Interrupt Time</span></span>](interrupt-time.md)

 

 
