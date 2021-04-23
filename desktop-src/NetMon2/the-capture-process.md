---
description: Процесс отслеживания одинаков для каждого из четырех интерфейсов НПП.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Процесс отслеживания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558262"
---
# <a name="the-capture-process"></a><span data-ttu-id="db6db-103">Процесс отслеживания</span><span class="sxs-lookup"><span data-stu-id="db6db-103">The Capture Process</span></span>

<span data-ttu-id="db6db-104">Процесс отслеживания одинаков для каждого из четырех интерфейсов НПП.</span><span class="sxs-lookup"><span data-stu-id="db6db-104">The capture process is the same for each of the four NPP interfaces.</span></span> <span data-ttu-id="db6db-105">В каждом случае процесс включает:</span><span class="sxs-lookup"><span data-stu-id="db6db-105">In each case, the process includes:</span></span>

-   <span data-ttu-id="db6db-106">Получение объекта интерфейса НПП для использования</span><span class="sxs-lookup"><span data-stu-id="db6db-106">Obtaining the NPP interface object to use</span></span>
-   <span data-ttu-id="db6db-107">Подключение к сети</span><span class="sxs-lookup"><span data-stu-id="db6db-107">Connecting to the network</span></span>
-   <span data-ttu-id="db6db-108">Запуск и остановка [ *записи*](c.md)</span><span class="sxs-lookup"><span data-stu-id="db6db-108">Starting and then stopping the [*capture*](c.md)</span></span>
-   <span data-ttu-id="db6db-109">Отключение от сети</span><span class="sxs-lookup"><span data-stu-id="db6db-109">Disconnecting from the network</span></span>

> [!Note]  
> <span data-ttu-id="db6db-110">При получении нужного объекта интерфейса убедитесь, что вызываются только методы, входящие в этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="db6db-110">When you obtain the interface object that you want, ensure you call only the methods included in that interface.</span></span> <span data-ttu-id="db6db-111">На следующем рисунке показано, как каждый интерфейс предоставляет аналогичные методы для записи сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="db6db-111">The following illustration shows each interface provides similar methods for capturing network data.</span></span> <span data-ttu-id="db6db-112">Если подключение к сети осуществляется с помощью одного интерфейса, а затем попытка запуска записи с использованием методов другого интерфейса, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="db6db-112">An error is returned if you connect to the network with one interface and then try to run a capture using the methods from another interface.</span></span>

 

<span data-ttu-id="db6db-113">На следующих иллюстрациях показаны два разных способа выполнения записи.</span><span class="sxs-lookup"><span data-stu-id="db6db-113">The following illustrations show two different ways you could run a capture.</span></span> <span data-ttu-id="db6db-114">На первой иллюстрации показано, как выполнить одно или несколько последовательных захватов, что позволяет создать любое количество независимых захватов.</span><span class="sxs-lookup"><span data-stu-id="db6db-114">The first illustration shows how to run one or more sequential captures, allowing you to create any number of independent captures.</span></span>

![последовательный захват](images/capt1.png)

<span data-ttu-id="db6db-116">Как показано выше, после подключения к сети вы можете запускать и прекращать запись сколько угодно раз, запуская новую запись и создавая новую статистику каждый раз при перезапуске записи.</span><span class="sxs-lookup"><span data-stu-id="db6db-116">As shown above, after you connect to the network you can start and stop a capture as many times as you wish, starting a new capture and generating new statistics every time you restart the capture.</span></span> <span data-ttu-id="db6db-117">Например, для отложенной записи с помощью интерфейса [**иделайдк**](idelaydc.md) новый [*файл записи*](c.md) создается при каждом перезапуске записи.</span><span class="sxs-lookup"><span data-stu-id="db6db-117">For example, for a delayed capture using the [**IDelaydC**](idelaydc.md) interface, a new [*capture file*](c.md) would be created each time you restarted the capture.</span></span>

<span data-ttu-id="db6db-118">Однако имейте в виду, что при каждом перезапуске процесса записи необходимо вызвать соответствующий метод настройки для повторной настройки соединения.</span><span class="sxs-lookup"><span data-stu-id="db6db-118">However, also be aware that every time you restart the capture process you must call the appropriate configure method to reconfigure the connection.</span></span> <span data-ttu-id="db6db-119">Для начального вызова для запуска записи подключение настраивается вызовом для подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="db6db-119">For the initial call to start the capture, the connection is configured by the call to connect to the network.</span></span>

<span data-ttu-id="db6db-120">На втором рисунке показано, как можно выполнить одну запись путем приостановки и перезапуска.</span><span class="sxs-lookup"><span data-stu-id="db6db-120">The second illustration shows how you could run a single capture by pausing and restarting.</span></span>

![однократная запись путем приостановки и перезапуска](images/capt2.png)

<span data-ttu-id="db6db-122">В этом случае можно приостановить и перезапустить запись столько раз, сколько нужно.</span><span class="sxs-lookup"><span data-stu-id="db6db-122">In this case, you can pause and restart a capture as many times as you want.</span></span> <span data-ttu-id="db6db-123">При таком подходе можно запустить запись, данные которой (и связанная с ней статистика) записываются в виде одной записи.</span><span class="sxs-lookup"><span data-stu-id="db6db-123">With this approach, you can run a capture whose data (and its related statistics) are recorded as a single capture.</span></span> <span data-ttu-id="db6db-124">Например, чтобы выполнить отложенную запись с помощью интерфейса [**иделайдк**](idelaydc.md) , все записанные сведения о сети будут сохранены в одном [*файле записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="db6db-124">For example, to perform a delayed capture using the [**IDelaydC**](idelaydc.md) interface, all the captured network information would be saved in a single [*capture file*](c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db6db-125">См. также</span><span class="sxs-lookup"><span data-stu-id="db6db-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db6db-126">**креатенппинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="db6db-126">**CreateNPPInterface**</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="db6db-127">**Иделайдк:: Configure**</span><span class="sxs-lookup"><span data-stu-id="db6db-127">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="db6db-128">**Иделайдк:: Connect**</span><span class="sxs-lookup"><span data-stu-id="db6db-128">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="db6db-129">**Иделайдк::D подключение**</span><span class="sxs-lookup"><span data-stu-id="db6db-129">**IDelaydC::Disconnect**</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="db6db-130">**Иделайдк::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="db6db-130">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="db6db-131">**Иделайдк:: Resume**</span><span class="sxs-lookup"><span data-stu-id="db6db-131">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="db6db-132">**Иделайдк:: Start**</span><span class="sxs-lookup"><span data-stu-id="db6db-132">**IDelaydC::Start**</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="db6db-133">**Иделайдк:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="db6db-133">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> <dt>

[<span data-ttu-id="db6db-134">**ИЕСП:: Configure**</span><span class="sxs-lookup"><span data-stu-id="db6db-134">**IESP::Configure**</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="db6db-135">**ИЕСП:: Connect**</span><span class="sxs-lookup"><span data-stu-id="db6db-135">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="db6db-136">**ИЕСП::D подключение**</span><span class="sxs-lookup"><span data-stu-id="db6db-136">**IESP::Disconnect**</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="db6db-137">**ИЕСП::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="db6db-137">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="db6db-138">**ИЕСП:: Resume**</span><span class="sxs-lookup"><span data-stu-id="db6db-138">**IESP::Resume**</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="db6db-139">**ИЕСП:: Start**</span><span class="sxs-lookup"><span data-stu-id="db6db-139">**IESP::Start**</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="db6db-140">**ИЕСП:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="db6db-140">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> <dt>

[<span data-ttu-id="db6db-141">**ИРТК:: Configure**</span><span class="sxs-lookup"><span data-stu-id="db6db-141">**IRTC::Configure**</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="db6db-142">**ИРТК:: Connect**</span><span class="sxs-lookup"><span data-stu-id="db6db-142">**IRTC::Connect**</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="db6db-143">**ИРТК::D подключение**</span><span class="sxs-lookup"><span data-stu-id="db6db-143">**IRTC::Disconnect**</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="db6db-144">**ИРТК::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="db6db-144">**IRTC::Pause**</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="db6db-145">**ИРТК:: Resume**</span><span class="sxs-lookup"><span data-stu-id="db6db-145">**IRTC::Resume**</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="db6db-146">**ИРТК:: Start**</span><span class="sxs-lookup"><span data-stu-id="db6db-146">**IRTC::Start**</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="db6db-147">**ИРТК:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="db6db-147">**IRTC::Stop**</span></span>](irtc-stop.md)
</dt> <dt>

[<span data-ttu-id="db6db-148">**Истатс:: Configure**</span><span class="sxs-lookup"><span data-stu-id="db6db-148">**IStats::Configure**</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="db6db-149">**Истатс:: Connect**</span><span class="sxs-lookup"><span data-stu-id="db6db-149">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="db6db-150">**Истатс::D подключение**</span><span class="sxs-lookup"><span data-stu-id="db6db-150">**IStats::Disconnect**</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="db6db-151">**Истатс::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="db6db-151">**IStats::Pause**</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="db6db-152">**Истатс:: Resume**</span><span class="sxs-lookup"><span data-stu-id="db6db-152">**IStats::Resume**</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="db6db-153">**Истатс:: Start**</span><span class="sxs-lookup"><span data-stu-id="db6db-153">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="db6db-154">**Истатс:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="db6db-154">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 



