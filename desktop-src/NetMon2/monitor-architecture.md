---
description: На следующем рисунке показана связь между мониторами и другими компонентами архитектуры сетевой монитор.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Мониторинг архитектуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551901"
---
# <a name="monitor-architecture"></a><span data-ttu-id="f4485-103">Мониторинг архитектуры</span><span class="sxs-lookup"><span data-stu-id="f4485-103">Monitor Architecture</span></span>

<span data-ttu-id="f4485-104">На следующем рисунке показана связь между [*мониторами*](m.md) и другими компонентами архитектуры сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="f4485-104">The following figure shows the relationship between [*monitors*](m.md) and other components of the Network Monitor architecture.</span></span>

![связь между мониторами и другими компонентами сетевого монитора](images/nmarch2.png)

<span data-ttu-id="f4485-106">Сетевой трафик собираются (отдельные кадры) из драйвера NDIS.</span><span class="sxs-lookup"><span data-stu-id="f4485-106">The network traffic is collected (as individual frames) from the NDIS driver.</span></span> <span data-ttu-id="f4485-107">Затем драйвер сетевой монитор (Nmnt.sys) направляет кадры в поставщик сетевых пакетов (НПП), который, в свою очередь, захватывает данные в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="f4485-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which in turn captures the data in real-time mode.</span></span> <span data-ttu-id="f4485-108">НПП — это коллекция COM-интерфейсов, используемых для сбора данных.</span><span class="sxs-lookup"><span data-stu-id="f4485-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="f4485-109">В этом случае для выполнения записи в режиме реального времени используется интерфейс [**ИРТК**](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="f4485-109">In this case, the [**IRTC**](irtc.md) interface is used to perform a real-time capture.</span></span>

> [!Note]  
> <span data-ttu-id="f4485-110">НПП используется для отложенных и в реальном времени записей.</span><span class="sxs-lookup"><span data-stu-id="f4485-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="f4485-111">Для отложенных захватов, используемых экспертами и анализаторами, используется интерфейс [**иделайдк**](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="f4485-111">For delayed captures used by experts and parsers, the [**IDelaydC**](idelaydc.md) interface is used.</span></span>

 

<span data-ttu-id="f4485-112">Затем монитор проверяет захваченные данные в режиме реального времени, выявляя определенные условия сети и создавая события по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="f4485-112">The monitor then examines the captured data in real-time mode, detecting specific network conditions and generating events as required.</span></span>

<span data-ttu-id="f4485-113">Для мониторинга приложений используются три других компонента: средство управления монитором, служба контроля мониторинга (МКСВК) и Просмотр событий:</span><span class="sxs-lookup"><span data-stu-id="f4485-113">Three other components are used by monitor applications: the Monitor Control Tool, the Monitor Control Service (MCSVC), and the Event Viewer:</span></span>

-   <span data-ttu-id="f4485-114">Средство управления монитором используется для управления приложениями мониторинга.</span><span class="sxs-lookup"><span data-stu-id="f4485-114">The Monitor Control Tool is used to manage your monitor applications.</span></span> <span data-ttu-id="f4485-115">Сюда входит настройка и запуск всех приложений мониторинга.</span><span class="sxs-lookup"><span data-stu-id="f4485-115">This includes configuring and running all your monitor applications.</span></span>
-   <span data-ttu-id="f4485-116">Служба управления монитором (МКСВК) запускает события, предоставляет ссылку для обмена данными на WMI для просмотра событий и координирует обработку операций мониторинга.</span><span class="sxs-lookup"><span data-stu-id="f4485-116">The Monitor Control Service (MCSVC) fires events, provides a communications link to WMI for event viewing, and coordinates the processing of monitor operations.</span></span>
-   <span data-ttu-id="f4485-117">В Просмотр событий отображаются события, инициированные службой управления монитором.</span><span class="sxs-lookup"><span data-stu-id="f4485-117">The Event Viewer displays the events fired by the Monitor Control Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4485-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f4485-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4485-119">**имонитор**</span><span class="sxs-lookup"><span data-stu-id="f4485-119">**IMonitor**</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="f4485-120">**имониторевентер**</span><span class="sxs-lookup"><span data-stu-id="f4485-120">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="f4485-121">**иртк**</span><span class="sxs-lookup"><span data-stu-id="f4485-121">**IRTC**</span></span>](irtc.md)
</dt> </dl>

 

 



