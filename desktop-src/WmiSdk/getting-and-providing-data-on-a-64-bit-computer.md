---
description: Клиентские приложения и скрипты, обращающиеся к стандартным поставщикам WMI 32-bit, продолжают работать в обычном режиме при работе в 64-разрядной операционной системе.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Получение и предоставление данных на 64-разрядном компьютере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563298"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a><span data-ttu-id="70768-103">Получение и предоставление данных на 64-разрядном компьютере</span><span class="sxs-lookup"><span data-stu-id="70768-103">Getting and Providing Data on a 64-bit Computer</span></span>

<span data-ttu-id="70768-104">Клиентские приложения и скрипты, обращающиеся к стандартным поставщикам WMI 32-bit, продолжают работать в обычном режиме при работе в 64-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="70768-104">Client applications and scripts that access standard WMI 32-bit providers continue to operate normally when running on a 64-bit operating system.</span></span> <span data-ttu-id="70768-105">Только два предварительно установленных поставщика, [системный реестр](/previous-versions/windows/desktop/regprov/system-registry-provider) и [поставщик представлений](view-provider.md), имеют 64-разрядные версии, которые работают параллельно с 32-разрядными версиями.</span><span class="sxs-lookup"><span data-stu-id="70768-105">Only two preinstalled providers, the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [View provider](view-provider.md), have 64-bit versions which run side-by-side with the 32-bit versions.</span></span> <span data-ttu-id="70768-106">Однако 32-разрядное приложение, запрашивающее экземпляры 32-bit WDM (WDM), получает экземпляры класса WDM по умолчанию (64-bit) в 64-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="70768-106">However, a 32-bit application that requests 32-bit Windows Driver Model (WDM) instances receives the default 64-bit WDM class instances on a 64-bit operating system.</span></span>

## <a name="accessing-default-and-nondefault-provider-data"></a><span data-ttu-id="70768-107">Доступ к данным поставщика по умолчанию и не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="70768-107">Accessing Default and Nondefault Provider Data</span></span>

<span data-ttu-id="70768-108">Как правило, модули записи поставщика не включают как 32-разрядные, так и 64-разрядные версии поставщика в одной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="70768-108">Generally, provider writers do not include both 32-bit and 64-bit versions of a provider in the same operating system.</span></span> <span data-ttu-id="70768-109">Если у вас нет 64-разрядного поставщика, 32-разрядный поставщик может продолжать работу с помощью средств WOW64.</span><span class="sxs-lookup"><span data-stu-id="70768-109">If no 64-bit provider exists, a 32-bit provider can continue to run through the facilities of WOW64.</span></span> <span data-ttu-id="70768-110">64-разрядный поставщик может также передавать данные в 32-разрядное приложение.</span><span class="sxs-lookup"><span data-stu-id="70768-110">A 64-bit provider can likewise supply data to a 32-bit application.</span></span> <span data-ttu-id="70768-111">Дополнительные сведения см. в разделе [предоставление данных WMI на 64-разрядной платформе](providing-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="70768-111">For more information, see [Providing WMI Data on a 64-bit Platform](providing-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="70768-112">Если существуют две версии, клиентские приложения и скрипты могут использовать контекстные параметры, доступные в [API COM](com-api-for-wmi.md) , и [API сценариев](scripting-api-for-wmi.md) для явного подключения к конкретному поставщику WMI, не используемому по умолчанию, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="70768-112">If two versions exist, client applications and scripts can use the context parameters available in the [COM API](com-api-for-wmi.md) and the [Scripting API](scripting-api-for-wmi.md) to connect explicitly to a specific nondefault WMI provider, if it is available.</span></span> <span data-ttu-id="70768-113">Дополнительные сведения см. в разделе [запрос данных WMI на 64-разрядной платформе](requesting-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="70768-113">For more information, see [Requesting WMI Data on a 64-bit Platform](requesting-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="70768-114">На следующей диаграмме показаны подключения по умолчанию и не используемые по умолчанию, используя реестр как пример, в котором два поставщика могут параллельно существовать на 64-разрядной платформе.</span><span class="sxs-lookup"><span data-stu-id="70768-114">The following diagram shows the default and nondefault connections, using the registry as an example for which two providers can exist side-by-side on a 64-bit platform.</span></span>

![по умолчанию и нестандартные подключения на 64-разрядной платформе](images/32-64bit-registry.png)

## <a name="related-topics"></a><span data-ttu-id="70768-116">См. также</span><span class="sxs-lookup"><span data-stu-id="70768-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70768-117">Запрос данных WMI на 64-разрядной платформе</span><span class="sxs-lookup"><span data-stu-id="70768-117">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="70768-118">Предоставление данных WMI на 64-разрядной платформе</span><span class="sxs-lookup"><span data-stu-id="70768-118">Providing WMI Data on a 64-bit Platform</span></span>](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
