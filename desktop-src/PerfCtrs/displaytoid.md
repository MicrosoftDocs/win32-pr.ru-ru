---
description: Таблица Дисплайтоид связывает удобную для пользователя строку, отображаемую системным монитором, с идентификатором GUID, хранящимся в других таблицах.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: дисплайтоид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663238"
---
# <a name="displaytoid"></a><span data-ttu-id="7db76-103">дисплайтоид</span><span class="sxs-lookup"><span data-stu-id="7db76-103">DisplayToID</span></span>

<span data-ttu-id="7db76-104">Таблица **дисплайтоид** связывает удобную для пользователя строку, отображаемую системным монитором, с идентификатором GUID, хранящимся в других таблицах.</span><span class="sxs-lookup"><span data-stu-id="7db76-104">The **DisplayToID** table relates the user-friendly string displayed by the System Monitor to the GUID stored in the other tables.</span></span>

<span data-ttu-id="7db76-105">В таблице **дисплайтоид** определены следующие поля:</span><span class="sxs-lookup"><span data-stu-id="7db76-105">The **DisplayToID** table defines the following fields:</span></span>

-   <span data-ttu-id="7db76-106">**Идентификатор GUID:** Уникальный идентификатор, созданный для журнала.</span><span class="sxs-lookup"><span data-stu-id="7db76-106">**GUID:** Unique identifier generated for a log.</span></span> <span data-ttu-id="7db76-107">Это поле является первичным ключом этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="7db76-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="7db76-108">**RunID:** Зарезервировано для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="7db76-108">**RunID:** Reserved for internal use.</span></span>
-   <span data-ttu-id="7db76-109">**DisplayString:** Имя файла журнала, отображаемое в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="7db76-109">**DisplayString:** Name of the log file as displayed in the System Monitor.</span></span>
-   <span data-ttu-id="7db76-110">**Логстарттиме:** Время начала процесса ведения журнала в формате гггг-мм-дд чч: мм: СС: nnn.</span><span class="sxs-lookup"><span data-stu-id="7db76-110">**LogStartTime:** Time the logging process started in yyyy-mm-dd hh:mm:ss:nnn format.</span></span>
-   <span data-ttu-id="7db76-111">**Логстоптиме:** Время остановки процесса ведения журнала в формате гггг-мм-дд чч: мм: СС: nnn.</span><span class="sxs-lookup"><span data-stu-id="7db76-111">**LogStopTime:** Time the logging process stopped in yyyy-mm-dd hh:mm:ss:nnn format.</span></span> <span data-ttu-id="7db76-112">Несколько файлов журнала с одинаковым значением **DisplayString** можно различать с помощью значений в полях и **логстарттиме** .</span><span class="sxs-lookup"><span data-stu-id="7db76-112">Multiple log files with the same **DisplayString** value can be differentiated by using the value in this and the **LogStartTime** fields.</span></span> <span data-ttu-id="7db76-113">Значения в полях **логстарттиме** и **логстоптиме** также позволяют быстро получить доступ к общему времени сбора.</span><span class="sxs-lookup"><span data-stu-id="7db76-113">The values in the **LogStartTime** and **LogStopTime** fields also allows the total collection time to be accessed quickly.</span></span>
-   <span data-ttu-id="7db76-114">**Нумберофрекордс:** Количество выборок, сохраненных в таблице для каждой коллекции журналов.</span><span class="sxs-lookup"><span data-stu-id="7db76-114">**NumberOfRecords:** Number of samples stored in the table for each log collection.</span></span>
-   <span data-ttu-id="7db76-115">**Минутестаутк:** Значение, используемое для преобразования данных строки, хранящихся в формате UTC, в местное время.</span><span class="sxs-lookup"><span data-stu-id="7db76-115">**MinutesToUTC:** Value used to convert the row data stored in UTC time to local time.</span></span>
-   <span data-ttu-id="7db76-116">**Тимезоненаме:** Имя часового пояса, в который были собраны данные.</span><span class="sxs-lookup"><span data-stu-id="7db76-116">**TimeZoneName:** Name of the time zone where the data was collected.</span></span> <span data-ttu-id="7db76-117">Если вы собираете или записали данные из файла, собранного на системах в собственном часовом поясе, это поле будет содержать расположение.</span><span class="sxs-lookup"><span data-stu-id="7db76-117">If you are collecting or have relogged data from a file collected on systems in your own time zone, this field will state the location.</span></span>

<span data-ttu-id="7db76-118">**Примечание**  .  До Windows Vista Наборы сборщиков данных хранились в реестре по адресу</span><span class="sxs-lookup"><span data-stu-id="7db76-118">**Note**  Prior to Windows Vista, the data collector sets were stored in the registry at</span></span>

<span data-ttu-id="7db76-119">**\_ \_ \\ \\ \\ \\ Запросы журнала SysmonLog CURRENTCONTROLSET Services System \\ для локального компьютера hKey**</span><span class="sxs-lookup"><span data-stu-id="7db76-119">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\SysmonLog\\Log Queries**</span></span>

<span data-ttu-id="7db76-120">.</span><span class="sxs-lookup"><span data-stu-id="7db76-120">.</span></span> <span data-ttu-id="7db76-121">Указанные выше поля не соответствуют значениям в реестре.</span><span class="sxs-lookup"><span data-stu-id="7db76-121">The fields listed above do not correspond to the values in registry.</span></span> <span data-ttu-id="7db76-122">В Windows Vista Наборы сборщиков данных не хранятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="7db76-122">For Windows Vista, the data collector sets are not stored in the registry.</span></span>

 

 



