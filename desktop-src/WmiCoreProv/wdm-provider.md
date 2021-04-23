---
description: Поставщик WDM (WDM) предоставляет доступ к классам, экземплярам, методам и событиям драйверов оборудования, которые соответствуют модели WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Поставщик WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811434"
---
# <a name="wdm-provider"></a><span data-ttu-id="06ac1-103">Поставщик WDM</span><span class="sxs-lookup"><span data-stu-id="06ac1-103">WDM Provider</span></span>

<span data-ttu-id="06ac1-104">Поставщик WDM (WDM) предоставляет доступ к классам, экземплярам, методам и событиям драйверов оборудования, которые соответствуют модели WDM.</span><span class="sxs-lookup"><span data-stu-id="06ac1-104">The WDM (Windows Driver Model) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="06ac1-105">Классы для драйверов оборудования находятся в корневом \\ пространстве имен WMI.</span><span class="sxs-lookup"><span data-stu-id="06ac1-105">The classes for hardware drivers reside in the "root\\wmi namespace".</span></span>

<span data-ttu-id="06ac1-106">Классы WDM определяются преимущественно в WMI. mof.</span><span class="sxs-lookup"><span data-stu-id="06ac1-106">WDM classes are defined primarily in Wmi.mof.</span></span>

<span data-ttu-id="06ac1-107">WDM — это интерфейс операционной системы, с помощью которого аппаратные компоненты предоставляют сведения и уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="06ac1-107">WDM is an operating system interface through which hardware components provide information and event notification.</span></span> <span data-ttu-id="06ac1-108">Поставщик WDM является классом, экземпляром, событием и поставщиком метода, который позволяет приложениям управления получать доступ к данным и событиям из драйверов устройств с поддержкой интерфейса WMI для WDM.</span><span class="sxs-lookup"><span data-stu-id="06ac1-108">The WDM provider is a class, instance, event, and method provider that allows management applications access to data and events from WMI-for-WDM enabled device drivers.</span></span> <span data-ttu-id="06ac1-109">Классы, созданные поставщиком WDM для представления данных драйвера устройства, находятся только в \\ пространстве имен root WMI.</span><span class="sxs-lookup"><span data-stu-id="06ac1-109">The classes created by the WDM provider to represent device driver data reside only in the "Root\\WMI" namespace.</span></span> <span data-ttu-id="06ac1-110">Это пространство имен уже должно существовать до того, как поставщик WDM будет обрабатывать установленные драйверы WDM.</span><span class="sxs-lookup"><span data-stu-id="06ac1-110">This namespace must already exist before the WDM provider will process the installed WDM drivers.</span></span>

<span data-ttu-id="06ac1-111">Поставщик WDM записывает сведения о операциях WDM в файл Вмипров. log.</span><span class="sxs-lookup"><span data-stu-id="06ac1-111">The WDM provider records information about WDM operations in the WmiProv.log file.</span></span> <span data-ttu-id="06ac1-112">Дополнительные сведения см. в разделе [файлы журналов WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="06ac1-112">For more information, see [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span>

<span data-ttu-id="06ac1-113">Как класс, экземпляр, метод и поставщик событий, Поставщик WDM реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) , а также следующие методы [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="06ac1-113">As a class, instance, method, and event provider, the WDM provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the following [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="06ac1-114">**креатеклассенумасинк**</span><span class="sxs-lookup"><span data-stu-id="06ac1-114">**CreateClassEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="06ac1-115">**креатеинстанцеенумасинк**</span><span class="sxs-lookup"><span data-stu-id="06ac1-115">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="06ac1-116">**жетобжектасинк**</span><span class="sxs-lookup"><span data-stu-id="06ac1-116">**GetObjectAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="06ac1-117">**ексекмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="06ac1-117">**ExecMethodAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="06ac1-118">**ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="06ac1-118">**ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="06ac1-119">**ексеккуерясинк**</span><span class="sxs-lookup"><span data-stu-id="06ac1-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="06ac1-120">**путинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="06ac1-120">**PutInstanceAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="06ac1-121">Поставщик WDM поддерживает событие внешних событий [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) , которое УВЕДОМЛЯет Инструментарий WMI о событиях из драйверов на основе WDM.</span><span class="sxs-lookup"><span data-stu-id="06ac1-121">The WDM provider supports the [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) extrinsic event, which notifies WMI regarding events from WDM-based drivers.</span></span> <span data-ttu-id="06ac1-122">Вы можете зарегистрировать потребителей событий для событий **WMIEvent** , как и любое другое событие.</span><span class="sxs-lookup"><span data-stu-id="06ac1-122">You can register your event consumers for **WMIEvent** events as you would any other event.</span></span> <span data-ttu-id="06ac1-123">Дополнительные сведения см. [в разделе Получение WMI-события](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span><span class="sxs-lookup"><span data-stu-id="06ac1-123">For more information, see [Receiving a WMI Event](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span></span> <span data-ttu-id="06ac1-124">При запуске драйвера не вызываются события создания класса.</span><span class="sxs-lookup"><span data-stu-id="06ac1-124">No class creation events are raised when starting a driver.</span></span>

<span data-ttu-id="06ac1-125">Поставщик WDM поддерживает следующий класс:</span><span class="sxs-lookup"><span data-stu-id="06ac1-125">The WDM provider supports the following class:</span></span>

-   [<span data-ttu-id="06ac1-126">**вмибинаримофресаурце**</span><span class="sxs-lookup"><span data-stu-id="06ac1-126">**WMIBinaryMofResource**</span></span>](wmibinarymofresource.md)

## <a name="related-topics"></a><span data-ttu-id="06ac1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="06ac1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06ac1-128">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="06ac1-128">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[<span data-ttu-id="06ac1-129">Доступ к данным из драйверов устройств</span><span class="sxs-lookup"><span data-stu-id="06ac1-129">Accessing Data from Device Drivers</span></span>](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
