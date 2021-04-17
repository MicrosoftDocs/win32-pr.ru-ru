---
description: Если источником данных является файл журнала, можно указать диапазон времени для запроса.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Задание диапазона времени для запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663155"
---
# <a name="setting-a-time-range-for-a-query"></a><span data-ttu-id="ed2b1-103">Задание диапазона времени для запроса</span><span class="sxs-lookup"><span data-stu-id="ed2b1-103">Setting a Time Range for a Query</span></span>

<span data-ttu-id="ed2b1-104">Если источником данных является файл журнала, можно указать диапазон времени для запроса.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-104">If the data source is a log file, you can specify a time range for the query.</span></span> <span data-ttu-id="ed2b1-105">Запрос получает данные счетчика из файла журнала, собранного в течение заданного диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-105">The query retrieves counter data from the log file that was collected during the specified time range.</span></span> <span data-ttu-id="ed2b1-106">Чтобы задать диапазон времени, вызовите функцию [**пдхсеткуеритимеранже**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) .</span><span class="sxs-lookup"><span data-stu-id="ed2b1-106">To set the time range, call the [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) function.</span></span> <span data-ttu-id="ed2b1-107">**Пдхсеткуеритимеранже** не используется для запроса данных о производительности из источников данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-107">**PdhSetQueryTimeRange** is not used to query performance data from real time data sources.</span></span>

<span data-ttu-id="ed2b1-108">Чтобы создать значение времени, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-108">To create time value, use the following steps.</span></span>

1.  <span data-ttu-id="ed2b1-109">Выделите структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) и инициализируйте поля с нужным значением времени.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-109">Allocate a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure and initialize the fields with the desired time value.</span></span>
2.  <span data-ttu-id="ed2b1-110">Вызовите [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) , чтобы преобразовать значение времени структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) в время структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="ed2b1-110">Call [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) to convert the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure time value to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure time.</span></span>
3.  <span data-ttu-id="ed2b1-111">Приведите структуру [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) как переменную лонглонг, учитывая соглашения о заполнении членов структуры платформы и компилятора.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-111">Cast the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure as a LONGLONG variable, keeping in mind the structure member padding conventions of your platform and compiler.</span></span>
4.  <span data-ttu-id="ed2b1-112">Скопируйте значение ЛОНГЛОНГ в соответствующее поле в структуре [**\_ \_ сведений о времени PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .</span><span class="sxs-lookup"><span data-stu-id="ed2b1-112">Copy the LONGLONG value to the appropriate field in the [**PDH\_TIME\_INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) structure.</span></span>

<span data-ttu-id="ed2b1-113">Чтобы получить диапазон времени всех данных о производительности, содержащихся в файле журнала, вызовите функцию [**пдхжетдатасаурцетимеранже**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .</span><span class="sxs-lookup"><span data-stu-id="ed2b1-113">To retrieve the time range of all of the performance data contained in a log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span>

 

 
