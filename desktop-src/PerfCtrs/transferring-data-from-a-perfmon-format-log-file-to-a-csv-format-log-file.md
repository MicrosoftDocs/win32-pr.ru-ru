---
description: В следующем примере данные передаются из файла журнала счетчиков, созданного средством Performance, в формат CSV (с разделителями-запятыми).
ms.assetid: 5adeda14-0312-45ce-af91-6888f3aa1c95
title: Преобразование данных из файла журнала в двоичном формате в файл журнала формата CSV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fea03ab810ff0ed357f72e3283323ee776bdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663146"
---
# <a name="converting-data-from-a-binary-format-log-file-to-a-csv-format-log-file"></a><span data-ttu-id="3e3fd-103">Преобразование данных из файла журнала в двоичном формате в файл журнала формата CSV</span><span class="sxs-lookup"><span data-stu-id="3e3fd-103">Converting Data from a Binary-format Log File to a CSV-format Log File</span></span>

<span data-ttu-id="3e3fd-104">В следующем примере данные передаются из файла журнала счетчиков, созданного средством Performance, в формат CSV (с разделителями-запятыми).</span><span class="sxs-lookup"><span data-stu-id="3e3fd-104">The following example transfers data from a counter log file created by the Performance tool to a comma separated format (.csv).</span></span> <span data-ttu-id="3e3fd-105">Этот пример передает данные счетчика времени процессора, собранные с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="3e3fd-105">The example transfers Processor Time counter data collected from the local computer.</span></span> <span data-ttu-id="3e3fd-106">Чтобы указать другой тип данных счетчика, измените переменную Сзкаунтерпас.</span><span class="sxs-lookup"><span data-stu-id="3e3fd-106">To specify another type of counter data, change the szCounterPath variable.</span></span> <span data-ttu-id="3e3fd-107">Если собранные данные счетчика относятся к определенному компьютеру, добавьте имя компьютера в путь (например, " \\ \\ \\ \\ <computername> \\ \\ процессор (0) \\ \\ % загруженности процессора").</span><span class="sxs-lookup"><span data-stu-id="3e3fd-107">If the collected counter data is from a specific computer, add the computer name to the path (for example, "\\\\\\\\<computername>\\\\Processor(0)\\\\% Processor Time").</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH = L"\\Processor(0)\\% Processor Time";

void DisplayCommandLineHelp(void)
{
    wprintf(L"Syntax: convertlog <input file name> <output file name>\n"
        L"\nThe input log file must be in the Perfmon format. The output\n"
        L"log file will written in the CSV file format, so specify a .csv extension.");
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HLOG hOutputLog = NULL;
    HCOUNTER hCounter = NULL;
    PDH_STATUS pdhStatus = ERROR_SUCCESS;
    DWORD dwOutputLogType = PDH_LOG_TYPE_CSV;

    if (3 != argc)
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Create the query object using the input log file.
    pdhStatus = PdhOpenQuery(argv[1], 0, &hQuery);

    if (ERROR_SUCCESS != pdhStatus)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }
   
    // Add the counter to the query object; identifies the counter
    // records from the log file that you are going to relog to 
    // the new log file.
    pdhStatus = PdhAddCounter(hQuery,
        COUNTER_PATH,
        0,
        &hCounter);

    if (ERROR_SUCCESS != pdhStatus)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Create and open the output log file.
    pdhStatus = PdhOpenLog(argv[2], 
        PDH_LOG_WRITE_ACCESS | 
        PDH_LOG_CREATE_ALWAYS,
        &dwOutputLogType,
        hQuery,
        0, 
        NULL,
        &hOutputLog);

    if (ERROR_SUCCESS != pdhStatus)
    {
        wprintf(L"PdhOpenLog failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Transfer the log records from the input file to the output file.
    while (ERROR_SUCCESS == pdhStatus) 
    { 
        pdhStatus = PdhUpdateLog(hOutputLog, NULL);
    }

    if (PDH_NO_MORE_DATA != pdhStatus)
    {
        wprintf(L"PdhUpdateLog failed with 0x%x\n", pdhStatus);
    }

cleanup:

   // Close the output log file.
   if (hOutputLog)
      PdhCloseLog(hOutputLog, 0);

   // Close the query object and input log file.
   if (hQuery)
      PdhCloseQuery(hQuery);
}
```



 

 



