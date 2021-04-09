---
description: Поставщик счетчика производительности — это высокопроизводительный поставщик, который предоставляет необработанные данные счетчиков производительности в классы счетчиков производительности WMI, производные от Win32 \_ перфравдата. \_ \_ Имя экземпляра Win32Provider — &\# 0034; ПРЕОБРАЗОВАТЬ права NT5 \_ женерикперфпровидер \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Поставщик счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081477"
---
# <a name="performance-counter-provider"></a><span data-ttu-id="9cafa-104">Поставщик счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="9cafa-104">Performance Counter Provider</span></span>

<span data-ttu-id="9cafa-105">\[Поставщик счетчиков производительности больше не доступен для использования.</span><span class="sxs-lookup"><span data-stu-id="9cafa-105">\[The Performance Counter Provider is no longer available for use.</span></span> <span data-ttu-id="9cafa-106">Вместо этого используйте поставщик [вмиперфинст](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="9cafa-106">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="9cafa-107">Поставщик счетчика производительности — это высокопроизводительный поставщик, который предоставляет необработанные данные счетчиков производительности в [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="9cafa-107">The Performance Counter provider is a high-performance provider that provides raw performance counter data to the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="9cafa-108">Имя экземпляра [**\_ \_ Win32Provider**](--win32provider.md) — "преобразовать права NT5 \_ женерикперфпровидер \_ v1".</span><span class="sxs-lookup"><span data-stu-id="9cafa-108">The [**\_\_Win32Provider**](--win32provider.md) instance name is "NT5\_GenericPerfProvider\_V1".</span></span>

<span data-ttu-id="9cafa-109">Классы [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) находятся в пространстве имен WMI "root \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="9cafa-109">The [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes are located in the WMI "Root\\CIMv2" namespace.</span></span> <span data-ttu-id="9cafa-110">Каждый класс производительности WMI соответствует объекту производительности в библиотеке производительности.</span><span class="sxs-lookup"><span data-stu-id="9cafa-110">Each WMI performance class corresponds to a performance object in a performance library.</span></span> <span data-ttu-id="9cafa-111">Свойства этих классов представляют счетчики для объекта.</span><span class="sxs-lookup"><span data-stu-id="9cafa-111">The properties of these classes represent the counters for the object.</span></span> <span data-ttu-id="9cafa-112">Имя класса WMI для необработанного объекта счетчика имеет вид \**Win32 \_ \_ \_ перфравдата* службы имя \_ *\_* объекта \_ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="9cafa-112">The WMI class name for a raw counter object is of the form \**Win32\_PerfRawData\_\_* service\_name *\_* object\_name\*\*\*.</span></span> <span data-ttu-id="9cafa-113">Например, имя класса WMI, содержащего счетчики логических дисков, — [**Win32 \_ перфравдата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="9cafa-113">For example, the WMI class name that contains the logical disk counters is [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="9cafa-114">Для получения предварительно вычисленных данных производительности, отображаемых в [*системном мониторе*](gloss-s.md), можно использовать соответствующий класс [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="9cafa-114">You can use the corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class to get the pre-calculated performance data shown in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="9cafa-115">Например, чтобы получить предварительно вычисленные данные диска, используйте класс [**\_ \_ \_ LogicalDisk перфформаттеддата перфдиск Win32**](./retrieving-raw-and-formatted-performance-data.md) .</span><span class="sxs-lookup"><span data-stu-id="9cafa-115">For example, use the [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class to get pre-calculated disk data.</span></span>

<span data-ttu-id="9cafa-116">Дополнительные сведения о написании клиента, который может получать доступ к необработанным данным производительности, см. [в разделе доступ к данным производительности в C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="9cafa-116">For more information about how to write a client that can access raw performance data, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="9cafa-117">Как высокопроизводительный поставщик, поставщик счетчиков производительности реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , а также метод [**Ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) и следующие методы [**ивбемхиперфпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :</span><span class="sxs-lookup"><span data-stu-id="9cafa-117">As a high-performance provider, the Performance Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="9cafa-118">**креатерефрешаблинум**</span><span class="sxs-lookup"><span data-stu-id="9cafa-118">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="9cafa-119">**креатерефрешаблеобжект**</span><span class="sxs-lookup"><span data-stu-id="9cafa-119">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="9cafa-120">**креатерефрешер**</span><span class="sxs-lookup"><span data-stu-id="9cafa-120">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="9cafa-121">**Объекты GetObject**</span><span class="sxs-lookup"><span data-stu-id="9cafa-121">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="9cafa-122">**куеринстанцес**</span><span class="sxs-lookup"><span data-stu-id="9cafa-122">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="9cafa-123">**стопрефрешинг**</span><span class="sxs-lookup"><span data-stu-id="9cafa-123">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="9cafa-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9cafa-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cafa-125">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="9cafa-125">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
