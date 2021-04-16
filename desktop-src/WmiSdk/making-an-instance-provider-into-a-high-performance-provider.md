---
description: Создание высокопроизводительного поставщика WMI для создания счетчиков производительности не рекомендуется.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Создание поставщика экземпляров в поставщике High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702296"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a><span data-ttu-id="41464-103">Создание поставщика экземпляров в поставщике High-Performance</span><span class="sxs-lookup"><span data-stu-id="41464-103">Making an Instance Provider into a High-Performance Provider</span></span>

<span data-ttu-id="41464-104">Создание высокопроизводительного поставщика WMI для создания счетчиков производительности не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="41464-104">Writing a WMI high-performance provider to create performance counters is not recommended.</span></span> <span data-ttu-id="41464-105">Начиная с Windows Vista, [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI больше не переносятся в библиотеки производительности Windows с помощью адаптера реконструирования и автоочистки (ADAP).</span><span class="sxs-lookup"><span data-stu-id="41464-105">Starting with Windows Vista, the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) are no longer migrated into the Windows performance libraries by the AutoDiscovery/AutoPurge (ADAP) reverse adapter.</span></span> <span data-ttu-id="41464-106">Чтобы создать поставщик счетчика производительности, используйте [счетчики производительности версии 2,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="41464-106">To create a performance counter provider, use [Performance Counters Version 2.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="41464-107">После создания объектов библиотеки производительности [поставщик вмиперфкласс](wmiperfclass-provider.md) анализирует объекты и создает или ОБНОВЛЯЕТ класс WMI, производный от [**\_ производительности Win32**](/windows/desktop/CIMWin32Prov/win32-perf) , для каждого объекта производительности.</span><span class="sxs-lookup"><span data-stu-id="41464-107">After performance library objects are created, the [WMIPerfClass Provider](wmiperfclass-provider.md) parses the objects and creates or refreshes a WMI class derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) for each performance object.</span></span> <span data-ttu-id="41464-108">Затем [поставщик вмиперфинст](wmiperfinst-provider.md) динамически предоставляет необработанные и форматированные данные счетчика производительности классам производительности WMI.</span><span class="sxs-lookup"><span data-stu-id="41464-108">The [WMIPerfInst Provider](wmiperfinst-provider.md) then dynamically provides raw and formatted performance counter data to the WMI performance classes.</span></span>

<span data-ttu-id="41464-109">Следующая высокоуровневая процедура описывает шаги, необходимые для создания высокопроизводительного поставщика.</span><span class="sxs-lookup"><span data-stu-id="41464-109">The following high-level procedure provides the steps required to create a high-performance provider.</span></span>

<span data-ttu-id="41464-110">**Создание высокопроизводительного поставщика**</span><span class="sxs-lookup"><span data-stu-id="41464-110">**To create a high-performance provider**</span></span>

1.  <span data-ttu-id="41464-111">Регистрация поставщика в WMI.</span><span class="sxs-lookup"><span data-stu-id="41464-111">Register your provider with WMI.</span></span> <span data-ttu-id="41464-112">Дополнительные сведения см. [в разделе Регистрация поставщика High-Performance](registering-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="41464-112">For more information, see [Registering a High-Performance Provider](registering-a-high-performance-provider.md).</span></span>
2.  <span data-ttu-id="41464-113">Реализуйте поставщик.</span><span class="sxs-lookup"><span data-stu-id="41464-113">Implement your provider.</span></span> <span data-ttu-id="41464-114">Дополнительные сведения см. в разделе [написание поставщика экземпляров](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="41464-114">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>
3.  <span data-ttu-id="41464-115">Реализуйте высокопроизводительный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="41464-115">Implement the high-performance interface.</span></span> <span data-ttu-id="41464-116">Дополнительные сведения см. [в разделе Реализация интерфейса High-Performance](implementing-the-high-performance-interface.md).</span><span class="sxs-lookup"><span data-stu-id="41464-116">For more information, see [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).</span></span>
4.  <span data-ttu-id="41464-117">Создайте и напишите схему MOF-файл (MOF) для получения необработанных данных о производительности.</span><span class="sxs-lookup"><span data-stu-id="41464-117">Derive and write your Managed Object Format (MOF) schema to obtain raw performance data.</span></span> <span data-ttu-id="41464-118">Дополнительные сведения см. [в разделе Поддержка \_ класса Win32 перфравдата](supporting-the-win32-perfrawdata-class.md).</span><span class="sxs-lookup"><span data-stu-id="41464-118">For more information, see [Supporting the Win32\_PerfRawData Class](supporting-the-win32-perfrawdata-class.md).</span></span>
5.  <span data-ttu-id="41464-119">Создайте производные и напишите схему MOF для получения предварительно вычисленных данных.</span><span class="sxs-lookup"><span data-stu-id="41464-119">Derive and write your MOF schema to obtain precalculated data.</span></span> <span data-ttu-id="41464-120">При поддержке этого класса поставщик не требуется для выполнения вычислений.</span><span class="sxs-lookup"><span data-stu-id="41464-120">By supporting this class, the provider is not required to perform the calculations.</span></span> <span data-ttu-id="41464-121">Эти данные будут теми же, которые отображаются в системном мониторе системного монитора.</span><span class="sxs-lookup"><span data-stu-id="41464-121">This data will be the same that appears in the System Monitor in Perfmon.</span></span> <span data-ttu-id="41464-122">Дополнительные сведения см. [в разделе Поддержка \_ класса Win32 перфформаттеддата](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="41464-122">For more information, see [Supporting the Win32\_PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41464-123">См. также</span><span class="sxs-lookup"><span data-stu-id="41464-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41464-124">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="41464-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="41464-125">Библиотеки производительности и инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="41464-125">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
