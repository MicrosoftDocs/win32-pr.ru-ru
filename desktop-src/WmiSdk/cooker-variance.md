---
description: '\_Формула с типом счетчика «вариативность» обеспечивает вариативность, которая используется для характеризующее дисперсии для набора необработанных наблюдений за одним свойством в \_ экземпляре Win32 перфравдата.'
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080588"
---
# <a name="cooker_variance"></a><span data-ttu-id="9f597-103">\_отклонение от острова</span><span class="sxs-lookup"><span data-stu-id="9f597-103">COOKER\_VARIANCE</span></span>

<span data-ttu-id="9f597-104">\_Формула с типом счетчика «вариативность» обеспечивает вариативность, которая используется для характеризующее дисперсии для набора необработанных наблюдений за одним свойством в экземпляре [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="9f597-104">The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) instance.</span></span> <span data-ttu-id="9f597-105">Дисперсия вычисляется путем деления суммы квадрата отклонения от среднего значения каждого счетчика на число счетчиков.</span><span class="sxs-lookup"><span data-stu-id="9f597-105">The variance is calculated by dividing the sum of the square of the deviation from the mean of each counter by the number of counters.</span></span> <span data-ttu-id="9f597-106">Иными словами, дисперсия является средним значением квадратов отклонения от среднего значения для каждого счетчика.</span><span class="sxs-lookup"><span data-stu-id="9f597-106">In other words, the variance is the average of the squared deviations from the mean for each counter.</span></span> <span data-ttu-id="9f597-107">Этот тип счетчика определен только в инструментарии WMI и недоступен для технологий наблюдения за производительностью, таких как [счетчики производительности версии 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="9f597-107">This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="9f597-108">Дополнительные сведения о формуле типа счетчика см. в разделе [типы счетчиков](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9f597-108">For more information about the counter type formula, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>

<span data-ttu-id="9f597-109">Дополнительные сведения о высокопроизводительных поставщиках и сценариях см. в разделе [типы счетчиков производительности WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="9f597-109">For more information about high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="9f597-110">Пример кода</span><span class="sxs-lookup"><span data-stu-id="9f597-110">Example Code</span></span>

<span data-ttu-id="9f597-111">Примеры кода см. в разделе [получение статистических данных о производительности](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="9f597-111">For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f597-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9f597-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f597-113">Типы статистических счетчиков</span><span class="sxs-lookup"><span data-stu-id="9f597-113">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> <dt>

[<span data-ttu-id="9f597-114">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="9f597-114">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
