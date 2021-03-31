---
description: Microsoft&\# 160; Поставщик Win32 извлекает и обновляет данные, относящиеся к системам Windows&\# 8212; такие данные, как текущие параметры переменных среды и атрибуты логического диска.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Поставщик Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807078"
---
# <a name="win32-provider"></a><span data-ttu-id="da066-103">Поставщик Win32</span><span class="sxs-lookup"><span data-stu-id="da066-103">Win32 Provider</span></span>

<span data-ttu-id="da066-104">Поставщик Microsoft Win32 извлекает и обновляет данные, относящиеся к системам Windows — такие данные, как текущие параметры переменных среды и атрибуты логического диска.</span><span class="sxs-lookup"><span data-stu-id="da066-104">The Microsoft Win32 provider retrieves and updates data relevant to Windows systems—data such as the current settings of environment variables and the attributes of a logical disk.</span></span> <span data-ttu-id="da066-105">С помощью поставщика Win32 приложения управления могут использовать инструментарий WMI для простого доступа к этим данным.</span><span class="sxs-lookup"><span data-stu-id="da066-105">With the Win32 provider, management applications can use WMI to easily access this data.</span></span> <span data-ttu-id="da066-106">Поставщик Win32 извлекает свои данные, делая вызов функций Windows и запрашивая системный реестр.</span><span class="sxs-lookup"><span data-stu-id="da066-106">The Win32 provider retrieves its information by making Windows function calls and querying the system registry.</span></span>

<span data-ttu-id="da066-107">Поставщик Win32 определяет классы, используемые для описания оборудования или программного обеспечения, доступного в системах Windows, и связи между ними.</span><span class="sxs-lookup"><span data-stu-id="da066-107">The Win32 provider defines the classes used to describe hardware or software available on Windows systems and the relationships between them.</span></span>

<span data-ttu-id="da066-108">Как экземпляр и поставщик методов, поставщик Win32 реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) , а также следующие методы [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="da066-108">As an instance and method provider, the Win32 provider implements the standard [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface as well as the following [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="da066-109">**креатеинстанцеенумасинк**</span><span class="sxs-lookup"><span data-stu-id="da066-109">**CreateInstanceEnumAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="da066-110">**делетеинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="da066-110">**DeleteInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="da066-111">**ексекмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="da066-111">**ExecMethodAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="da066-112">**ексеккуерясинк**</span><span class="sxs-lookup"><span data-stu-id="da066-112">**ExecQueryAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="da066-113">**жетобжектасинк**</span><span class="sxs-lookup"><span data-stu-id="da066-113">**GetObjectAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="da066-114">**путинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="da066-114">**PutInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="da066-115">В следующей таблице перечислены категории классов поставщиков Win32.</span><span class="sxs-lookup"><span data-stu-id="da066-115">The following table lists the Win32 provider class categories.</span></span>



| <span data-ttu-id="da066-116">Классы</span><span class="sxs-lookup"><span data-stu-id="da066-116">Classes</span></span>                                                                             | <span data-ttu-id="da066-117">Описание</span><span class="sxs-lookup"><span data-stu-id="da066-117">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="da066-118">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="da066-118">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)<br/> | <span data-ttu-id="da066-119">Объекты, связанные с оборудованием.</span><span class="sxs-lookup"><span data-stu-id="da066-119">Hardware-related objects.</span></span><br/>                                      |
| [<span data-ttu-id="da066-120">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="da066-120">Operating System Classes</span></span>](operating-system-classes.md)<br/>                 | <span data-ttu-id="da066-121">Объекты, связанные с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="da066-121">Operating system related objects.</span></span><br/>                              |
| [<span data-ttu-id="da066-122">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="da066-122">Performance Counter Classes</span></span>](performance-counter-classes.md)<br/>           | <span data-ttu-id="da066-123">Необработанные и вычисленные данные производительности из счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="da066-123">Raw and calculated performance data from performance counters.</span></span><br/> |
| [<span data-ttu-id="da066-124">Классы управления службами WMI</span><span class="sxs-lookup"><span data-stu-id="da066-124">WMI Service Management Classes</span></span>](wmi-service-management-classes.md)<br/>     | <span data-ttu-id="da066-125">Управление для WMI.</span><span class="sxs-lookup"><span data-stu-id="da066-125">Management for WMI.</span></span><br/>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="da066-126">См. также</span><span class="sxs-lookup"><span data-stu-id="da066-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da066-127">Поставщик WMI CIMWin32</span><span class="sxs-lookup"><span data-stu-id="da066-127">CIMWin32 WMI Provider</span></span>](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
