---
description: Приложение, которое поддерживает счетчики производительности, должно иметь ключ производительности в разделе служб. В следующем примере показаны значения, которые необходимо включить для этого ключа.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Создание ключа производительности приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663243"
---
# <a name="creating-the-applications-performance-key"></a><span data-ttu-id="4fa17-104">Создание ключа производительности приложения</span><span class="sxs-lookup"><span data-stu-id="4fa17-104">Creating the Application's Performance Key</span></span>

<span data-ttu-id="4fa17-105">Приложение, которое поддерживает счетчики производительности, должно иметь ключ **производительности** в разделе **служб** .</span><span class="sxs-lookup"><span data-stu-id="4fa17-105">An application that supports performance counters must have a **Performance** key under the **Services** key.</span></span> <span data-ttu-id="4fa17-106">В следующем примере показаны значения, которые необходимо включить для этого ключа.</span><span class="sxs-lookup"><span data-stu-id="4fa17-106">The following example shows the values that you must include for this key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

<span data-ttu-id="4fa17-107">Значение **библиотеки** предоставляет имя библиотеки DLL производительности, а значения **Open**, **собирающего** и **Close** предоставляют имена функций, экспортированных из DLL производительности.</span><span class="sxs-lookup"><span data-stu-id="4fa17-107">The **Library** value provides the name of the performance DLL, and the **Open**, **Collect**, and **Close** values provide the names of the functions exported from the performance DLL.</span></span> <span data-ttu-id="4fa17-108">Эти значения имеют тип данных **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="4fa17-108">The data type of these values is **REG\_SZ**.</span></span> <span data-ttu-id="4fa17-109">Когда потребитель запрашивает данные о производительности, система использует эти значения, чтобы определить, какие библиотеки DLL производительности нужно загрузить и какие функции DLL следует вызывать.</span><span class="sxs-lookup"><span data-stu-id="4fa17-109">When a consumer requests performance data, the system uses these values to determine which performance DLLs to load and which DLL functions to call.</span></span>

<span data-ttu-id="4fa17-110">Значение **библиотеки** может содержать имя DLL или полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="4fa17-110">The **Library** value can contain the DLL name or a full path to the DLL.</span></span> <span data-ttu-id="4fa17-111">При использовании типа данных **\_ \_ SZ Expand** для **библиотеки** можно указать переменные среды в пути.</span><span class="sxs-lookup"><span data-stu-id="4fa17-111">If you use the **REG\_EXPAND\_SZ** data type for **Library**, you can specify environment variables in your path.</span></span>

<span data-ttu-id="4fa17-112">Ключ службы приложения должен существовать, прежде чем можно будет запустить **lodctr** для загрузки имен счетчиков и строк справки.</span><span class="sxs-lookup"><span data-stu-id="4fa17-112">The application's service key must exist before you can run **lodctr** to load your counter names and help strings.</span></span>

<span data-ttu-id="4fa17-113">Дополнительные значения реестра, которые можно создать, например указание значений времени ожидания для функций [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) и [**коллектперформанцедата**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , см. в разделе [Создание других записей реестра](creating-other-registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="4fa17-113">For additional registry values that you can create, such as specifying time out values for the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions, see [Creating Other Registry Entries](creating-other-registry-entries.md).</span></span>

 

 
