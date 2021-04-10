---
description: Тип счетчика производительности обозначает формулу, необходимую для получения вычисляемых счетчиков производительности. Это те же типы счетчиков, которые используются в мониторинге производительности Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Типы счетчиков производительности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155994"
---
# <a name="wmi-performance-counter-types"></a><span data-ttu-id="68c0f-104">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="68c0f-104">WMI Performance Counter Types</span></span>

<span data-ttu-id="68c0f-105">[Тип счетчика](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) производительности обозначает формулу, необходимую для получения вычисляемых счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="68c0f-105">The performance [counter type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) designates a formula required to obtain calculated performance counters.</span></span> <span data-ttu-id="68c0f-106">Это те же типы счетчиков, которые используются в [мониторинге производительности](/windows/desktop/PerfCtrs/performance-counters-portal)Windows.</span><span class="sxs-lookup"><span data-stu-id="68c0f-106">These are the same counter types used by Windows [Performance Monitoring](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="68c0f-107">В классах производительности WMI необработанные данные для формулы типа счетчика берутся из класса [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , а вычисленный результат находится в свойстве с тем же именем соответствующего класса [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="68c0f-107">In WMI performance classes, the raw data for the counter type formula comes from a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and the calculated result is found in the same-named property of a corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class.</span></span>

<span data-ttu-id="68c0f-108">Типы счетчиков отображаются в качестве квалификатора **CounterType** для свойств в классах [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , а также в качестве квалификатора **Кукингтипе** для свойств в классах [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="68c0f-108">Counter types appear as the **CounterType** qualifier for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes, and as the **CookingType** qualifier for properties in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="68c0f-109">Например, свойство **авгдискбитесперреад** класса [**\_ \_ \_ LogicalDisk Win32 перфравдата перфдиск**](./retrieving-raw-and-formatted-performance-data.md) является необработанным источником данных для свойства **авгдискбитесперреад** в классе [**Win32 \_ перфформаттеддата \_ Перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), который содержит те же данные, что показаны в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="68c0f-109">For example, the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class is the raw data source for the **AvgDiskBytesPerRead** property in the class [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), which contains the same data as shown in System Monitor.</span></span>

<span data-ttu-id="68c0f-110">Следующий список упорядочивает описания типов счетчиков по функциональному типу:</span><span class="sxs-lookup"><span data-stu-id="68c0f-110">The following list organizes counter type descriptions by functional type:</span></span>

-   [<span data-ttu-id="68c0f-111">Базовые типы счетчиков</span><span class="sxs-lookup"><span data-stu-id="68c0f-111">Base Counter Types</span></span>](base-counter-types.md)
-   [<span data-ttu-id="68c0f-112">Типы счетчиков базового алгоритма</span><span class="sxs-lookup"><span data-stu-id="68c0f-112">Basic Algorithm Counter Types</span></span>](basic-algorithm-counter-types.md)
-   [<span data-ttu-id="68c0f-113">Типы счетчиков алгоритмов счетчиков</span><span class="sxs-lookup"><span data-stu-id="68c0f-113">Counter Algorithm Counter Types</span></span>](counter-algorithm-counter-types.md)
-   [<span data-ttu-id="68c0f-114">Невычислительные типы счетчиков</span><span class="sxs-lookup"><span data-stu-id="68c0f-114">Noncomputational Counter Types</span></span>](noncomputational-counter-types.md)
-   [<span data-ttu-id="68c0f-115">Типы счетчиков для алгоритма таймера точности</span><span class="sxs-lookup"><span data-stu-id="68c0f-115">Precision Timer Algorithm Counter Types</span></span>](precision-timer-algorithm-counter-types.md)
-   [<span data-ttu-id="68c0f-116">Типы счетчиков алгоритма длины очереди</span><span class="sxs-lookup"><span data-stu-id="68c0f-116">Queue-length Algorithm Counter Types</span></span>](queue-length-algorithm-counter-types.md)
-   [<span data-ttu-id="68c0f-117">Типы статистических счетчиков</span><span class="sxs-lookup"><span data-stu-id="68c0f-117">Statistical Counter Types</span></span>](statistical-counter-types.md)
-   [<span data-ttu-id="68c0f-118">Типы счетчиков алгоритмов таймера</span><span class="sxs-lookup"><span data-stu-id="68c0f-118">Timer Algorithm Counter Types</span></span>](timer-algorithm-counter-types.md)

 

 
