---
description: Поставщик данных о производительности в формате WMI с высокой производительностью вычисляет типы статистических счетчиков на заданном числе необработанных образцов данных счетчиков.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Типы статистических счетчиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081115"
---
# <a name="statistical-counter-types"></a><span data-ttu-id="39edf-103">Типы статистических счетчиков</span><span class="sxs-lookup"><span data-stu-id="39edf-103">Statistical Counter Types</span></span>

<span data-ttu-id="39edf-104">[Поставщик данных о производительности в формате](formatted-performance-data-provider.md) WMI с высокой производительностью вычисляет типы статистических счетчиков на заданном числе необработанных образцов данных счетчиков.</span><span class="sxs-lookup"><span data-stu-id="39edf-104">The WMI high-performance [Formatted Performance Data Provider](formatted-performance-data-provider.md) calculates the statistical counter types on a specified number of raw counter data samples.</span></span> <span data-ttu-id="39edf-105">Алгоритмы для типов счетчиков не нуждаются в наследуемых свойствах timestamp или Frequency (например, **timestamp \_ Перфтиме** или **Frequency \_ перфтиме**), которые требуются для других типов счетчиков.</span><span class="sxs-lookup"><span data-stu-id="39edf-105">The algorithms for the counter types do not require inherited timestamp or frequency properties (such as **TimeStamp\_PerfTime** or **Frequency\_PerfTime**) that other counter types require.</span></span>

<span data-ttu-id="39edf-106">Вместо этого типы статистических счетчиков поддерживают **квалификатор** , который определяет, сколько выборок следует использовать.</span><span class="sxs-lookup"><span data-stu-id="39edf-106">Instead, the statistical counter types support a **qualifier** that identifies how many samples to use.</span></span> <span data-ttu-id="39edf-107">Пример собирается при вызове метода [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) для объекта производительности.</span><span class="sxs-lookup"><span data-stu-id="39edf-107">A sample is collected when the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method is called for the performance object.</span></span> <span data-ttu-id="39edf-108">Для скриптов используется метод [**свбемрефрешер. Refresh**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="39edf-108">For scripts use the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method.</span></span> <span data-ttu-id="39edf-109">Вычисляемые данные содержат результат вычисления, выполненного на **самплевиндов** количестве выборок из свойства необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="39edf-109">The calculated data contains the result of the calculation performed on the **SampleWindow** number of samples from the raw data property.</span></span> <span data-ttu-id="39edf-110">Необработанные данные для вычисления поступают в FRM имя свойства, указанное в квалификаторе **счетчика** .</span><span class="sxs-lookup"><span data-stu-id="39edf-110">The raw data for the calculation comes frm the property name specified in the **Counter** qualifier.</span></span>

<span data-ttu-id="39edf-111">Дополнительные сведения см. в разделе [получение статистических данных о производительности](obtaining-statistical-performance-data.md) и [доступ к предустановленным классам производительности WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="39edf-111">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>



| <span data-ttu-id="39edf-112">Константа CounterType</span><span class="sxs-lookup"><span data-stu-id="39edf-112">CounterType Constant</span></span>                    | <span data-ttu-id="39edf-113">Описание</span><span class="sxs-lookup"><span data-stu-id="39edf-113">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39edf-114">Среднее время от острова \_</span><span class="sxs-lookup"><span data-stu-id="39edf-114">COOKER\_AVERAGE</span></span>](cooker-average.md)   | <span data-ttu-id="39edf-115">Суммирует повторяющиеся наблюдения за одним свойством в классе [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и делит сумму на число наблюдений.</span><span class="sxs-lookup"><span data-stu-id="39edf-115">Sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and divides the sum by the number of observations.</span></span>                              |
| [<span data-ttu-id="39edf-116">максимум острова Кука \_</span><span class="sxs-lookup"><span data-stu-id="39edf-116">COOKER\_MAX</span></span>](cooker-max.md)           | <span data-ttu-id="39edf-117">Самое большое значение из набора наблюдений свойства в классе [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="39edf-117">Largest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                    |
| [<span data-ttu-id="39edf-118">мин. \_</span><span class="sxs-lookup"><span data-stu-id="39edf-118">COOKER\_MIN</span></span>](cooker-min.md)           | <span data-ttu-id="39edf-119">Наименьшее значение из набора наблюдений свойства в классе [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="39edf-119">Smallest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                   |
| [<span data-ttu-id="39edf-120">диапазон острова Кука \_</span><span class="sxs-lookup"><span data-stu-id="39edf-120">COOKER\_RANGE</span></span>](cooker-range.md)       | <span data-ttu-id="39edf-121">Разница между значениями [min](cooker-min.md) и [Max](cooker-max.md) для набора необработанных наблюдений за свойством в классе [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="39edf-121">Difference between the [Min](cooker-min.md) and [Max](cooker-max.md) values for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span> |
| [<span data-ttu-id="39edf-122">\_отклонение от острова</span><span class="sxs-lookup"><span data-stu-id="39edf-122">COOKER\_VARIANCE</span></span>](cooker-variance.md) | <span data-ttu-id="39edf-123">Мера вариативности, которую можно использовать для определения дисперсии для набора необработанных наблюдений за свойством в классе [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="39edf-123">Measure of variability that can be used to characterize dispersion for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="39edf-124">См. также</span><span class="sxs-lookup"><span data-stu-id="39edf-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39edf-125">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="39edf-125">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="39edf-126">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="39edf-126">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="39edf-127">Обновление данных WMI в скриптах</span><span class="sxs-lookup"><span data-stu-id="39edf-127">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="39edf-128">Доступ к данным о производительности в скрипте</span><span class="sxs-lookup"><span data-stu-id="39edf-128">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="39edf-129">Доступ к данным о производительности в C++</span><span class="sxs-lookup"><span data-stu-id="39edf-129">Accessing Performance Data in C++</span></span>](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
