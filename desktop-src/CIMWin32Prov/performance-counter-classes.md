---
description: Классы счетчиков производительности позволяют сценариям и программам получать доступ к данным производительности системы, вычисляемым существующими высокопроизводительными поставщиками.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Классы счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896514"
---
# <a name="performance-counter-classes"></a><span data-ttu-id="0030a-103">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="0030a-103">Performance Counter Classes</span></span>

<span data-ttu-id="0030a-104">Классы счетчиков производительности позволяют сценариям и программам получать доступ к данным производительности системы, вычисляемым существующими высокопроизводительными поставщиками.</span><span class="sxs-lookup"><span data-stu-id="0030a-104">Performance Counter classes allow script and program access to system performance data calculated by existing high-performance providers.</span></span> <span data-ttu-id="0030a-105">Эти классы состоят из классов счетчиков производительности необработанных данных и форматированных классов счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="0030a-105">These classes consist of raw performance counter classes and formatted performance counter classes.</span></span>

<span data-ttu-id="0030a-106">Различные поставщики предоставляют данные библиотеки производительности с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="0030a-106">Different providers supply performance library data through WMI.</span></span> <span data-ttu-id="0030a-107">Поставщики [вмиперфкласс](/windows/desktop/WmiSdk/wmiperfclass-provider) и [вмиперфинст](/windows/desktop/WmiSdk/wmiperfinst-provider) предоставляют классы для [счетчиков производительности](/windows/desktop/PerfCtrs/performance-counters-portal)версии 1 и версии 2.</span><span class="sxs-lookup"><span data-stu-id="0030a-107">The [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) and [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) providers supply classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="0030a-108">Эти поставщики поддерживают совместимость с классами, доступными в более ранних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="0030a-108">These providers maintain compatibility with the classes available in earlier operating systems.</span></span>

<span data-ttu-id="0030a-109">Классы в этом разделе являются абстрактными базовыми классами, используемыми для создания классов счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="0030a-109">The classes in this section are the abstract base classes used to create performance counter classes.</span></span> <span data-ttu-id="0030a-110">Это не полный список классов, которые могут быть найдены в вашей операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0030a-110">This is not a complete list of classes that you may find on your operating system.</span></span> <span data-ttu-id="0030a-111">Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0030a-111">For more information, see [Performance Libraries and WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0030a-112">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="0030a-112">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="0030a-113">**Производительность \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="0030a-113">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dd>

<span data-ttu-id="0030a-114">Базовый класс для классов счетчиков производительности [**Win32 \_ Перфравдата**](win32-perfrawdata.md) и [**Win32 \_ перфформаттеддата**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="0030a-114">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

</dd> <dt>

[<span data-ttu-id="0030a-115">**\_Перфформаттеддата Win32**</span><span class="sxs-lookup"><span data-stu-id="0030a-115">**Win32\_PerfFormattedData**</span></span>](win32-perfformatteddata.md)
</dt> <dd>

<span data-ttu-id="0030a-116">Абстрактный базовый класс для предварительно установленных и вычисляемых классов данных.</span><span class="sxs-lookup"><span data-stu-id="0030a-116">an abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

[<span data-ttu-id="0030a-117">**\_Перфравдата Win32**</span><span class="sxs-lookup"><span data-stu-id="0030a-117">**Win32\_PerfRawData**</span></span>](win32-perfrawdata.md)
</dt> <dd>

<span data-ttu-id="0030a-118">Абстрактный базовый класс для всех конкретных классов необработанных счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="0030a-118">The abstract base class for all concrete raw performance counter classes.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="0030a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0030a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0030a-120">Классы Win32</span><span class="sxs-lookup"><span data-stu-id="0030a-120">Win32 Classes</span></span>](win32-provider.md)
</dt> </dl>

 

 
