---
description: 'Данные производительности можно использовать с помощью одного из следующих интерфейсов: интерфейс данных производительности (PDH), который обеспечивает высокоуровневый доступ к данным из поставщиков счетчиков производительности версии 1 и версии 2. Интерфейс реестра, предоставляющий доступ к данным из поставщиков счетчиков производительности низкого уровня. Интерфейс библиотеки производительности, предоставляющий прямой доступ к данным поставщиков счетчиков производительности версии 2. Интерфейс PDH проще в использовании, чем интерфейс реестра, и рекомендуется для большинства задач сбора данных о производительности. Интерфейс PDH — это, по сути, более высокий уровень абстракции функций, предоставляемых интерфейсом реестра. Интерфейс библиотеки производительности следует использовать только в том случае, если нельзя использовать функции уровня абстракции PDH.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Использование данных счетчиков
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: c8c50b29d8f898f544b021f7fe3f3fd0d4a2094e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663248"
---
# <a name="consuming-counter-data"></a><span data-ttu-id="fc6d5-105">Использование данных счетчиков</span><span class="sxs-lookup"><span data-stu-id="fc6d5-105">Consuming Counter Data</span></span>

<span data-ttu-id="fc6d5-106">Программы, которые хотят читать и использовать данные счетчиков производительности Windows, могут использовать один из нескольких интерфейсов в соответствии с ситуацией.</span><span class="sxs-lookup"><span data-stu-id="fc6d5-106">Programs that want to read and make use of Windows Performance Counter data can use one of several interfaces as appropriate for the scenario.</span></span>

- <span data-ttu-id="fc6d5-107">Скрипты могут использовать [Классы счетчиков производительности WMI](/windows/desktop/WmiSdk/monitoring-performance-data) или средство [типеперф](/windows-server/administration/windows-commands/typeperf) .</span><span class="sxs-lookup"><span data-stu-id="fc6d5-107">Scripts can use the [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) or the [TypePerf](/windows-server/administration/windows-commands/typeperf) tool.</span></span>
- <span data-ttu-id="fc6d5-108">Программы .NET могут использовать [класс PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).</span><span class="sxs-lookup"><span data-stu-id="fc6d5-108">.NET programs can use the [PerformanceCounter Class](/dotnet/api/system.diagnostics.performancecounter).</span></span>
- <span data-ttu-id="fc6d5-109">[Библиотека поддержки данных производительности (PDH)](using-the-pdh-functions-to-consume-counter-data.md) предоставляет высокоуровневый доступ к данным из поставщиков счетчиков производительности v1 и v2 через API Win32 (C/C++).</span><span class="sxs-lookup"><span data-stu-id="fc6d5-109">The [Performance Data Helper (PDH) library](using-the-pdh-functions-to-consume-counter-data.md) provides high-level access to data from both V1 and V2 performance counter providers via a Win32 (C/C++) API.</span></span>
- <span data-ttu-id="fc6d5-110">[Интерфейс реестра](using-the-registry-functions-to-consume-counter-data.md) предоставляет доступ к данным из поставщиков счетчиков производительности v1 и v2 через Специальный `HKEY_PERFORMANCE_DATA` раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="fc6d5-110">The [registry interface](using-the-registry-functions-to-consume-counter-data.md) provides access to data from both V1 and V2 performance counter providers via the special `HKEY_PERFORMANCE_DATA` registry key.</span></span>
- <span data-ttu-id="fc6d5-111">[Функции-потребители версии PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) предоставляют низкоуровневый доступ к данным из поставщиков счетчиков производительности v2 через API Win32 (C/C++).</span><span class="sxs-lookup"><span data-stu-id="fc6d5-111">The [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) provide low-level access to data from V2 performance counter providers via a Win32 (C/C++) API.</span></span>

<span data-ttu-id="fc6d5-112">Для большинства задач сбора данных о производительности C/C++ рекомендуется использовать интерфейс PDH, поскольку он проще в использовании по сравнению с реестром и интерфейсом PerfLib.</span><span class="sxs-lookup"><span data-stu-id="fc6d5-112">The PDH interface is recommended for most C/C++ performance data collection tasks because it is easier to use than the registry and PerfLib interfaces.</span></span>
