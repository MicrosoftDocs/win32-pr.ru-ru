---
description: Вычисляемые блоки (&\# 0034; обработанные&\# 0034;) данные счетчика производительности. Предоставляет динамические данные классам WMI, производным от Win32 \_ перфформаттеддата. Также известен как поставщик счетчика обработанные.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Поставщик форматированных данных о производительности
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702061"
---
# <a name="formatted-performance-data-provider"></a><span data-ttu-id="62ca9-105">Поставщик форматированных данных о производительности</span><span class="sxs-lookup"><span data-stu-id="62ca9-105">Formatted Performance Data Provider</span></span>

<span data-ttu-id="62ca9-106">\[Отформатированный поставщик данных о производительности, также известный как "поставщик счетчиков обработанные", больше недоступен для использования.</span><span class="sxs-lookup"><span data-stu-id="62ca9-106">\[The Formatted Performance Data Provider, also known as the "Cooked Counter Provider," is no longer available for use.</span></span> <span data-ttu-id="62ca9-107">Вместо этого используйте поставщик [вмиперфинст](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="62ca9-107">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="62ca9-108">Высокопроизводительный поставщик данных о производительности предоставляет вычисленные ("обработанные") данные счетчика производительности, например процент времени, затрачиваемого диском на запись данных.</span><span class="sxs-lookup"><span data-stu-id="62ca9-108">The high-performance Formatted Performance Data provider supplies calculated ("cooked") performance counter data, such as the percentage of time a disk spends writing data.</span></span> <span data-ttu-id="62ca9-109">Этот поставщик предоставляет динамические данные классам WMI, производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="62ca9-109">This provider supplies dynamic data to the WMI classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="62ca9-110">Различие между этим поставщиком и [поставщиком счетчика производительности](performance-counter-provider.md) заключается в том, что поставщик счетчика производительности предоставляет необработанные данные, а поставщик счетчиков обработанные предоставляет данные производительности, которые отображаются в точности так же, как в [*системном мониторе*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="62ca9-110">The difference between this provider and the [Performance Counter provider](performance-counter-provider.md) is that the Performance Counter provider supplies raw data and the Cooked Counter provider supplies performance data that appears exactly as in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="62ca9-111">Имя экземпляра [**\_ \_ Win32Provider**](--win32provider.md) — "хиперфкукер \_ v1".</span><span class="sxs-lookup"><span data-stu-id="62ca9-111">The [**\_\_Win32Provider**](--win32provider.md) instance name is "HiPerfCooker\_v1".</span></span>

<span data-ttu-id="62ca9-112">Имя класса в формате WMI для объекта счетчика имеет вид "Win32 \_ перфформаттеддата \_ *Service \_* Name \_ *Object \_* Name".</span><span class="sxs-lookup"><span data-stu-id="62ca9-112">The WMI formatted class name for a counter object is of the form "Win32\_PerfFormattedData\_*service\_name*\_*object\_name*".</span></span> <span data-ttu-id="62ca9-113">Например, имя класса WMI, содержащего счетчики логических дисков, — **Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="62ca9-113">For example, the WMI class name that contains the logical disk counters is **Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**.</span></span> <span data-ttu-id="62ca9-114">Эти классы находятся в \\ пространстве имен root CIMv2.</span><span class="sxs-lookup"><span data-stu-id="62ca9-114">These classes are located in the "Root\\CIMv2" namespace.</span></span>

<span data-ttu-id="62ca9-115">Поскольку классы данных о производительности добавляются и изменяются динамически в определенной системе, невозможно формально документировать свойства всех известных объектов производительности.</span><span class="sxs-lookup"><span data-stu-id="62ca9-115">Because performance data classes are added and modified dynamically on a given system, it is not possible to formally document the properties of all known performance objects.</span></span> <span data-ttu-id="62ca9-116">Чтобы определить, какие классы доступны для вас, а также определить, какие члены имеют эти классы, см. статью [получение документации по необработанным и форматированным объектам данных о производительности](retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="62ca9-116">To determine what classes are available to you, and to identify what members those classes have, see [Retrieving Documentation for Raw and Formatted Performance Data Objects](retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="62ca9-117">Классы [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) используют квалификатор **кукингтипе** в [типах счетчиков производительности WMI](wmi-performance-counter-types.md) для указания формулы для вычисления данных о производительности.</span><span class="sxs-lookup"><span data-stu-id="62ca9-117">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes use the **CookingType** qualifier in [WMI Performance Counter Types](wmi-performance-counter-types.md) to specify the formula for calculating performance data.</span></span> <span data-ttu-id="62ca9-118">Этот квалификатор совпадает с квалификатором **CounterType** в классах [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="62ca9-118">This qualifier is the same as the **CounterType** qualifier in the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span>

<span data-ttu-id="62ca9-119">Как высокопроизводительный поставщик, поставщик счетчиков обработанные реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , а также метод [**Ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) и следующие методы [**ивбемхиперфпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :</span><span class="sxs-lookup"><span data-stu-id="62ca9-119">As a high-performance provider, the Cooked Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="62ca9-120">**креатерефрешаблинум**</span><span class="sxs-lookup"><span data-stu-id="62ca9-120">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="62ca9-121">**креатерефрешаблеобжект**</span><span class="sxs-lookup"><span data-stu-id="62ca9-121">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="62ca9-122">**креатерефрешер**</span><span class="sxs-lookup"><span data-stu-id="62ca9-122">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="62ca9-123">**Объекты GetObject**</span><span class="sxs-lookup"><span data-stu-id="62ca9-123">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="62ca9-124">**куеринстанцес**</span><span class="sxs-lookup"><span data-stu-id="62ca9-124">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="62ca9-125">**стопрефрешинг**</span><span class="sxs-lookup"><span data-stu-id="62ca9-125">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="62ca9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="62ca9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62ca9-127">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="62ca9-127">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
