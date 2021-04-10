---
description: Функции Опенперформанцедата DLL производительности в качестве входных данных принимают строковый аргумент.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Создание других записей реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998527"
---
# <a name="creating-other-registry-entries"></a><span data-ttu-id="c5af3-103">Создание других записей реестра</span><span class="sxs-lookup"><span data-stu-id="c5af3-103">Creating Other Registry Entries</span></span>

<span data-ttu-id="c5af3-104">Функция [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) библиотеки производительности DLL принимает строковый аргумент в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="c5af3-104">The performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function takes a string argument as input.</span></span> <span data-ttu-id="c5af3-105">Чтобы предоставить входную строку открытой функции, включите ключ **компоновки** в ключ **служб** .</span><span class="sxs-lookup"><span data-stu-id="c5af3-105">To provide an input string to your open function, include a **Linkage** key under your **Services** key.</span></span> <span data-ttu-id="c5af3-106">Ключ **компоновки** содержит значение **экспорта** .</span><span class="sxs-lookup"><span data-stu-id="c5af3-106">The **Linkage** key contains an **Export** value.</span></span> <span data-ttu-id="c5af3-107">Задайте данные для **экспорта** во входной строке, которую необходимо передать в функцию Open.</span><span class="sxs-lookup"><span data-stu-id="c5af3-107">Set the value data for **Export** to the input string that you want to pass to your open function.</span></span> <span data-ttu-id="c5af3-108">Тип данных **Export** — **reg \_ Multi \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="c5af3-108">The data type of **Export** is **REG\_MULTI\_SZ**.</span></span>

<span data-ttu-id="c5af3-109">Если параметр **Export** не определен (**Экспорт** является необязательным), система передает **значение NULL** в функцию [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c5af3-109">If **Export** is not defined (**Export** is optional), the system passes **NULL** to your [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span>

<span data-ttu-id="c5af3-110">Как правило, если в нескольких приложениях используется одна и та же библиотека производительности, то каждое приложение включает ключ **компоновки** и значение **экспорта** для предоставления контекста, в котором приложение вызывает библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="c5af3-110">Typically, if more than one application shares the same performance DLL, each application includes a **Linkage** key and **Export** value to provide context as to which application is calling the DLL.</span></span>

<span data-ttu-id="c5af3-111">Ниже приведены записи реестра.</span><span class="sxs-lookup"><span data-stu-id="c5af3-111">The following shows the registry entries:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

<span data-ttu-id="c5af3-112">По умолчанию функции [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) и [**коллектперформанцедата**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) DLL производительности должны возвращать значение в пределах 10 000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="c5af3-112">By default, the performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions must return within 10,000 milliseconds.</span></span> <span data-ttu-id="c5af3-113">В противном случае система не использует данные, возвращаемые библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="c5af3-113">If not, the system does not use the data that the DLL returns.</span></span> <span data-ttu-id="c5af3-114">Приложение может увеличить или уменьшить значение времени ожидания, указав в качестве ключа **производительности** время ожидания **открытия** или получения **значения реестра,** как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="c5af3-114">The application can increase or decrease the timeout value by specifying an **Open Timeout** or **Collect Timeout** registry value under their **Performance** key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

<span data-ttu-id="c5af3-115">Чтобы получить данные о производительности для некоторых приложений (которые возвращают счетчики с помощью функции [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), необходимо использовать функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , чтобы открыть устройство, связанное с приложением.</span><span class="sxs-lookup"><span data-stu-id="c5af3-115">To obtain the performance data for some applications (those that return counters using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function), it is necessary to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the device associated with the application.</span></span> <span data-ttu-id="c5af3-116">В этом случае имя, указанное в **CreateFile** , также должно быть установлено в узле DOS Devices в реестре, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="c5af3-116">In this case, the name specified in **CreateFile** must also be installed in the DOS Devices node of the registry, as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
