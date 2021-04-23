---
title: Параметры сети по умолчанию
description: Параметры сети по умолчанию
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK, параметры сети по умолчанию
- Расширенный системный формат (ASF), параметры сети по умолчанию
- ASF (Расширенный системный формат), параметры сети по умолчанию
- Windows Media Format SDK, параметры сети
- Расширенный формат систем (ASF), параметры сети
- ASF (расширенный формат систем), параметры сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889160"
---
# <a name="default-networking-settings"></a><span data-ttu-id="b7376-109">Параметры сети по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b7376-109">Default Networking Settings</span></span>

<span data-ttu-id="b7376-110">В следующих таблицах описаны параметры сетевых параметров по умолчанию в пакете SDK формата Windows Media, сгруппированные по интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="b7376-110">The following tables describe the default settings of the networking parameters in the Windows Media Format SDK, grouped by interface.</span></span>



| <span data-ttu-id="b7376-111">ивмреадернетворкконфиг</span><span class="sxs-lookup"><span data-stu-id="b7376-111">IWMReaderNetworkConfig</span></span>                | <span data-ttu-id="b7376-112">Параметр по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b7376-112">Default setting</span></span>              |
|---------------------------------------|------------------------------|
| <span data-ttu-id="b7376-113">Время буферизации</span><span class="sxs-lookup"><span data-stu-id="b7376-113">Buffering time</span></span>                        | <span data-ttu-id="b7376-114">5 с</span><span class="sxs-lookup"><span data-stu-id="b7376-114">5 seconds</span></span>                    |
| <span data-ttu-id="b7376-115">усефикседудппорт</span><span class="sxs-lookup"><span data-stu-id="b7376-115">UseFixedUDPPort</span></span>                       | <span data-ttu-id="b7376-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="b7376-116">FALSE</span></span>                        |
| <span data-ttu-id="b7376-117">фикседудппорт</span><span class="sxs-lookup"><span data-stu-id="b7376-117">FixedUDPPort</span></span>                          | <span data-ttu-id="b7376-118">0 (недопустимо)</span><span class="sxs-lookup"><span data-stu-id="b7376-118">0 (not valid)</span></span>                |
| <span data-ttu-id="b7376-119">Проксисеттинг: HTTP</span><span class="sxs-lookup"><span data-stu-id="b7376-119">ProxySetting: HTTP</span></span>                    | <span data-ttu-id="b7376-120">\_браузер параметров прокси-сервера ВМТ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b7376-120">WMT\_PROXY\_SETTING\_BROWSER</span></span> |
| <span data-ttu-id="b7376-121">Проксисеттинг: MMS</span><span class="sxs-lookup"><span data-stu-id="b7376-121">ProxySetting: MMS</span></span>                     | <span data-ttu-id="b7376-122">\_параметр прокси-сервера ВМТ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b7376-122">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="b7376-123">Проксисеттинг: RTSP</span><span class="sxs-lookup"><span data-stu-id="b7376-123">ProxySetting: RTSP</span></span>                    | <span data-ttu-id="b7376-124">\_параметр прокси-сервера ВМТ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="b7376-124">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="b7376-125">Проксихостнаме (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="b7376-125">ProxyHostName (HTTP, MMS, RTSP)</span></span>       | <span data-ttu-id="b7376-126">""</span><span class="sxs-lookup"><span data-stu-id="b7376-126">""</span></span>                           |
| <span data-ttu-id="b7376-127">Проксипорт: HTTP</span><span class="sxs-lookup"><span data-stu-id="b7376-127">ProxyPort: HTTP</span></span>                       | <span data-ttu-id="b7376-128">80</span><span class="sxs-lookup"><span data-stu-id="b7376-128">80</span></span>                           |
| <span data-ttu-id="b7376-129">Проксипорт: MMS</span><span class="sxs-lookup"><span data-stu-id="b7376-129">ProxyPort: MMS</span></span>                        | <span data-ttu-id="b7376-130">1755</span><span class="sxs-lookup"><span data-stu-id="b7376-130">1755</span></span>                         |
| <span data-ttu-id="b7376-131">Прокстпорт: RTSP</span><span class="sxs-lookup"><span data-stu-id="b7376-131">ProxtPort: RTSP</span></span>                       | <span data-ttu-id="b7376-132">554</span><span class="sxs-lookup"><span data-stu-id="b7376-132">554</span></span>                          |
| <span data-ttu-id="b7376-133">Проксексцептионлист (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="b7376-133">ProxyExceptionList (HTTP, MMS, RTSP)</span></span>  | <span data-ttu-id="b7376-134">""</span><span class="sxs-lookup"><span data-stu-id="b7376-134">""</span></span>                           |
| <span data-ttu-id="b7376-135">Проксибипассфорлокал (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="b7376-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span></span> | <span data-ttu-id="b7376-136">FALSE</span><span class="sxs-lookup"><span data-stu-id="b7376-136">FALSE</span></span>                        |
| <span data-ttu-id="b7376-137">форцерерунаутодетектион</span><span class="sxs-lookup"><span data-stu-id="b7376-137">ForceRerunAutoDetection</span></span>               | <span data-ttu-id="b7376-138">FALSE</span><span class="sxs-lookup"><span data-stu-id="b7376-138">FALSE</span></span>                        |
| <span data-ttu-id="b7376-139">енаблемултикаст</span><span class="sxs-lookup"><span data-stu-id="b7376-139">EnableMulticast</span></span>                       | <span data-ttu-id="b7376-140">true</span><span class="sxs-lookup"><span data-stu-id="b7376-140">TRUE</span></span>                         |
| <span data-ttu-id="b7376-141">енаблехттп</span><span class="sxs-lookup"><span data-stu-id="b7376-141">EnableHTTP</span></span>                            | <span data-ttu-id="b7376-142">true</span><span class="sxs-lookup"><span data-stu-id="b7376-142">TRUE</span></span>                         |
| <span data-ttu-id="b7376-143">енаблеткп</span><span class="sxs-lookup"><span data-stu-id="b7376-143">EnableTCP</span></span>                             | <span data-ttu-id="b7376-144">true</span><span class="sxs-lookup"><span data-stu-id="b7376-144">TRUE</span></span>                         |
| <span data-ttu-id="b7376-145">енаблеудп</span><span class="sxs-lookup"><span data-stu-id="b7376-145">EnableUDP</span></span>                             | <span data-ttu-id="b7376-146">true</span><span class="sxs-lookup"><span data-stu-id="b7376-146">TRUE</span></span>                         |
| <span data-ttu-id="b7376-147">Пропускная способность подключения</span><span class="sxs-lookup"><span data-stu-id="b7376-147">Connection Bandwidth</span></span>                  | <span data-ttu-id="b7376-148">0 (автоматическое определение)</span><span class="sxs-lookup"><span data-stu-id="b7376-148">0 (auto-detect)</span></span>              |



 



| <span data-ttu-id="b7376-149">IWMReaderNetworkConfig2</span><span class="sxs-lookup"><span data-stu-id="b7376-149">IWMReaderNetworkConfig2</span></span>        | <span data-ttu-id="b7376-150">Параметр по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b7376-150">Default setting</span></span>        |
|--------------------------------|------------------------|
| <span data-ttu-id="b7376-151">Длительность ускоренной потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="b7376-151">Accelerated streaming duration</span></span> | <span data-ttu-id="b7376-152">100000000 (10 секунд)</span><span class="sxs-lookup"><span data-stu-id="b7376-152">100000000 (10 seconds)</span></span> |
| <span data-ttu-id="b7376-153">Включить кэширование содержимого</span><span class="sxs-lookup"><span data-stu-id="b7376-153">Enable content caching</span></span>         | <span data-ttu-id="b7376-154">true</span><span class="sxs-lookup"><span data-stu-id="b7376-154">TRUE</span></span>                   |
| <span data-ttu-id="b7376-155">Включить быстрый кэш</span><span class="sxs-lookup"><span data-stu-id="b7376-155">Enable fast cache</span></span>              | <span data-ttu-id="b7376-156">true</span><span class="sxs-lookup"><span data-stu-id="b7376-156">TRUE</span></span>                   |
| <span data-ttu-id="b7376-157">Включить повторные отправки</span><span class="sxs-lookup"><span data-stu-id="b7376-157">Enable resends</span></span>                 | <span data-ttu-id="b7376-158">true</span><span class="sxs-lookup"><span data-stu-id="b7376-158">TRUE</span></span>                   |
| <span data-ttu-id="b7376-159">Включить тонкое содержимое</span><span class="sxs-lookup"><span data-stu-id="b7376-159">Enable content thinning</span></span>        | <span data-ttu-id="b7376-160">true</span><span class="sxs-lookup"><span data-stu-id="b7376-160">TRUE</span></span>                   |
| <span data-ttu-id="b7376-161">Предел повторного подключения</span><span class="sxs-lookup"><span data-stu-id="b7376-161">Reconnect limit</span></span>                | <span data-ttu-id="b7376-162">25</span><span class="sxs-lookup"><span data-stu-id="b7376-162">25</span></span>                     |



 



| <span data-ttu-id="b7376-163">ивмвритернетворксинк</span><span class="sxs-lookup"><span data-stu-id="b7376-163">IWMWriterNetworkSink</span></span> | <span data-ttu-id="b7376-164">Параметр по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b7376-164">Default setting</span></span>         |
|----------------------|-------------------------|
| <span data-ttu-id="b7376-165">Максимум клиентов</span><span class="sxs-lookup"><span data-stu-id="b7376-165">Maximum clients</span></span>      | <span data-ttu-id="b7376-166">5</span><span class="sxs-lookup"><span data-stu-id="b7376-166">5</span></span>                       |
| <span data-ttu-id="b7376-167">Сетевой протокол</span><span class="sxs-lookup"><span data-stu-id="b7376-167">Network protocol</span></span>     | <span data-ttu-id="b7376-168">0 (ВМТ \_ протокол \_ http)</span><span class="sxs-lookup"><span data-stu-id="b7376-168">0 (WMT\_PROTOCOL\_HTTP)</span></span> |
| <span data-ttu-id="b7376-169">URL-адрес узла</span><span class="sxs-lookup"><span data-stu-id="b7376-169">Host URL</span></span>             | <span data-ttu-id="b7376-170">0 (недопустимо)</span><span class="sxs-lookup"><span data-stu-id="b7376-170">0 (not valid)</span></span>           |



 



| <span data-ttu-id="b7376-171">IWMWriterAdvanced2</span><span class="sxs-lookup"><span data-stu-id="b7376-171">IWMWriterAdvanced2</span></span>  | <span data-ttu-id="b7376-172">Параметр по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b7376-172">Default setting</span></span>             |
|---------------------|-----------------------------|
| <span data-ttu-id="b7376-173">Максимальный размер пакета</span><span class="sxs-lookup"><span data-stu-id="b7376-173">Maximum packet size</span></span> | <span data-ttu-id="b7376-174">1400</span><span class="sxs-lookup"><span data-stu-id="b7376-174">1400</span></span>                        |
| <span data-ttu-id="b7376-175">Идентификатор клиента журнала</span><span class="sxs-lookup"><span data-stu-id="b7376-175">Log client ID</span></span>       | <span data-ttu-id="b7376-176">FALSE</span><span class="sxs-lookup"><span data-stu-id="b7376-176">FALSE</span></span>                       |
| <span data-ttu-id="b7376-177">Режим воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b7376-177">Play mode</span></span>           | <span data-ttu-id="b7376-178">\_Автовыбор \_ режима воспроизведения ВМТ \_</span><span class="sxs-lookup"><span data-stu-id="b7376-178">WMT\_PLAY\_MODE\_AUTOSELECT</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b7376-179">См. также</span><span class="sxs-lookup"><span data-stu-id="b7376-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7376-180">**Реализация функций сети**</span><span class="sxs-lookup"><span data-stu-id="b7376-180">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




