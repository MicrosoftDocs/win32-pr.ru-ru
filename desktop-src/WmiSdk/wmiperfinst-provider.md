---
description: Начиная с Windows Vista, поставщик Вмиперфинст динамически предоставляет данные счетчиков производительности необработанных и неформатированных данных для классов счетчиков производительности WMI, производных от Win32 \_ perf.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Поставщик Вмиперфинст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692820"
---
# <a name="wmiperfinst-provider"></a><span data-ttu-id="61be2-103">Поставщик Вмиперфинст</span><span class="sxs-lookup"><span data-stu-id="61be2-103">WmiPerfInst Provider</span></span>

<span data-ttu-id="61be2-104">Начиная с Windows Vista, поставщик Вмиперфинст динамически предоставляет данные счетчиков производительности необработанных и неформатированных данных для [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI, производных от [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="61be2-104">Starting with Windows Vista, the WmiPerfInst provider supplies raw and formatted performance counter data dynamically to WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span> <span data-ttu-id="61be2-105">Этот поставщик заменяет [отформатированный поставщик данных о производительности](formatted-performance-data-provider.md), также известный как "поставщик счетчиков обработанные", и [Поставщик счетчика производительности](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="61be2-105">This provider replaces the [Formatted Performance Data Provider](formatted-performance-data-provider.md), also known as the "Cooked Counter Provider", and the [Performance Counter Provider](performance-counter-provider.md).</span></span>

<span data-ttu-id="61be2-106">Поставщик Вмиперфинст предоставляет данные классам WMI, предоставляемым поставщиком [вмиперфкласс](wmiperfclass-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="61be2-106">The WmiPerfInst provider supplies data to the WMI classes that are provided by the [WMIPerfClass](wmiperfclass-provider.md) provider.</span></span> <span data-ttu-id="61be2-107">Этот поставщик представляет собой мост между экземплярами модуля поддержки данных производительности (PDH) и классами производительности WMI, предоставляемыми поставщиком Вмиперфкласс.</span><span class="sxs-lookup"><span data-stu-id="61be2-107">This provider is a bridge between Performance Data Helper (PDH) instances and the WMI performance classes supplied by the WmiPerfClass Provider.</span></span> <span data-ttu-id="61be2-108">Когда Вмиперфинст получает запрос данных, он загружает класс и использует [Квалификаторы](qualifiers-specific-to-wmi-performance-classes.md) класса и свойства для поиска экземпляров PDH.</span><span class="sxs-lookup"><span data-stu-id="61be2-108">When WmiPerfInst receives a query for data, it loads the class and uses the class and property [qualifiers](qualifiers-specific-to-wmi-performance-classes.md) to locate the PDH instances.</span></span> <span data-ttu-id="61be2-109">Дополнительные сведения см. в разделе [Использование функций PDH для использования данных счетчика](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="61be2-109">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

<span data-ttu-id="61be2-110">Не рекомендуется разрабатывать новые объекты производительности путем создания высокопроизводительного поставщика WMI и зависеть от процесса рескоростного [*адаптера ADAP*](gloss-r.md) для перемещения данных в библиотеки производительности.</span><span class="sxs-lookup"><span data-stu-id="61be2-110">It is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries.</span></span> <span data-ttu-id="61be2-111">Исключением является разработка драйвера WDM и требуется предоставить данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="61be2-111">The exception is when you are developing a Windows Driver Model driver and want to supply performance data.</span></span> <span data-ttu-id="61be2-112">Несмотря на то, что процесс обратного адаптера продолжит работать в целях обратной совместимости, рекомендуется использовать [счетчики производительности версии 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="61be2-112">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="61be2-113">Имя экземпляра [**\_ \_ Win32Provider**](--win32provider.md) этого поставщика — "вмиперфинст".</span><span class="sxs-lookup"><span data-stu-id="61be2-113">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfInst".</span></span>

## <a name="related-topics"></a><span data-ttu-id="61be2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="61be2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61be2-115">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="61be2-115">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="61be2-116">Библиотеки производительности и инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="61be2-116">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="61be2-117">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="61be2-117">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
