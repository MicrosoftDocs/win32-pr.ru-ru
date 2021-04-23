---
description: Если клиент и узел не могут обмениваться метаданными, то для пользовательского узла и клиента можно заменить универсальный узел и клиент, чтобы помочь устранить проблему.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Использование универсального узла и клиента для обмена метаданными HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701783"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a><span data-ttu-id="00ecc-103">Использование универсального узла и клиента для обмена метаданными HTTP</span><span class="sxs-lookup"><span data-stu-id="00ecc-103">Using a Generic Host and Client for HTTP Metadata Exchange</span></span>

<span data-ttu-id="00ecc-104">Если клиент и узел не могут обмениваться метаданными, то для пользовательского узла и клиента можно заменить универсальный узел и клиент, чтобы помочь устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="00ecc-104">If the client and host cannot exchange metadata, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="00ecc-105">Если адрес устройства или метаданные устройства не отображаются в выходных данных клиента отладки WSD, указанные адреса транспорта или сетевая среда могут вызвать сбой.</span><span class="sxs-lookup"><span data-stu-id="00ecc-105">If the device address or device metadata does not appear in the WSD Debug Client output, then the supplied transport addresses or the network environment may be causing the failure.</span></span> <span data-ttu-id="00ecc-106">Дополнительные сведения об универсальном узле и клиенте см. в разделе [средства отладки](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="00ecc-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="00ecc-107">Если вы проверили, что универсальный узел и клиент могут завершить как WS-Discovery, так и обмен метаданными HTTP, эту диагностическую процедуру можно пропустить, а устранение неполадок можно продолжить, выполнив процедуры, описанные в статье [Использование ведения журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="00ecc-107">If it has been verified that a generic host and client can complete both WS-Discovery and HTTP metadata exchange, then this diagnostic procedure can be skipped and troubleshooting can be continued by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="00ecc-108">Если узел или клиент является приложением, запущенным на компьютере, универсальный узел или клиент должны быть запущены в том же контексте безопасности, что и фактический узел или клиент.</span><span class="sxs-lookup"><span data-stu-id="00ecc-108">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="00ecc-109">Например, если фактический узел или клиент работает от имени администратора, то универсальный узел или клиент должен работать от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="00ecc-109">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="00ecc-110">Кроме того, если узел или клиент является автономным устройством, он должен быть полностью заменен ПК, на котором работает универсальный узел или клиент, в контексте безопасности, который обеспечивает неограниченный доступ к сети (например, Запуск от имени администратора).</span><span class="sxs-lookup"><span data-stu-id="00ecc-110">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client in a security context that guarantees unlimited network access (for example, running as Administrator).</span></span>

<span data-ttu-id="00ecc-111">**Использование универсального узла и клиента для устранения неполадок при обмене метаданными HTTP**</span><span class="sxs-lookup"><span data-stu-id="00ecc-111">**To using a generic host and client to troubleshoot HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="00ecc-112">Откройте окно командной строки.</span><span class="sxs-lookup"><span data-stu-id="00ecc-112">Open a command prompt window.</span></span>
2.  <span data-ttu-id="00ecc-113">Выполните следующую команду: **всддебуг \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="00ecc-113">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="00ecc-114">Может появиться диалоговое окно **оповещение системы безопасности Windows** .</span><span class="sxs-lookup"><span data-stu-id="00ecc-114">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="00ecc-115">Если это так, нажмите кнопку **разблокировать** , чтобы разрешить запуск узла отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="00ecc-115">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="00ecc-116">Эта команда создает выходные данные, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="00ecc-116">This command generates output similar to the following.</span></span> <span data-ttu-id="00ecc-117">Запишите идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="00ecc-117">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="00ecc-118">Выполните следующую команду: **всддебуг \_client.exe/Mode Metadata/Хелло/ресолве** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="00ecc-118">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="00ecc-119">Замените *<id>* идентификатором устройства, указанным на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="00ecc-119">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="00ecc-120">Может появиться диалоговое окно **оповещение системы безопасности Windows** .</span><span class="sxs-lookup"><span data-stu-id="00ecc-120">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="00ecc-121">Если это так, нажмите кнопку **разблокировать** , чтобы разрешить запуск клиента отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="00ecc-121">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="00ecc-122">Клиент отладки WSD создает выходные данные, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="00ecc-122">WSD Debug Client generates output similar to the following.</span></span>

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

<span data-ttu-id="00ecc-123">Клиент отладки WSD может создавать большой объем выходных данных в сети с множеством устройств DPWS.</span><span class="sxs-lookup"><span data-stu-id="00ecc-123">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="00ecc-124">Выходные данные можно перенаправить в файл для упрощения анализа.</span><span class="sxs-lookup"><span data-stu-id="00ecc-124">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="00ecc-125">Введите **log tee** *<filename>* в командной строке клиента отладки WSD, чтобы перенаправить вывод в файл.</span><span class="sxs-lookup"><span data-stu-id="00ecc-125">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="00ecc-126">Перенаправление выходных данных можно остановить, введя **log tee остановиться** в командной строке клиента отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="00ecc-126">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="00ecc-127">Запишите адрес ссылки на конечную точку (EPR).</span><span class="sxs-lookup"><span data-stu-id="00ecc-127">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="00ecc-128">Этот адрес EPR должен соответствовать ИДЕНТИФИКАТОРу устройства, указанному на шаге 2 выше.</span><span class="sxs-lookup"><span data-stu-id="00ecc-128">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="00ecc-129">Кроме того, убедитесь, что клиент отладки WSD полностью выпечатал метаданные для устройства.</span><span class="sxs-lookup"><span data-stu-id="00ecc-129">Also, verify that the WSD Debug Client completely printed the metadata for the device.</span></span> <span data-ttu-id="00ecc-130">Метаданные устройства начинаются с `Metadata for host` и заканчиваются на `End of metadata` .</span><span class="sxs-lookup"><span data-stu-id="00ecc-130">The device metadata begins with `Metadata for host` and ends with `End of metadata`.</span></span>

<span data-ttu-id="00ecc-131">Если идентификатор устройства и метаданные устройства правильно отображаются в выходных данных клиента отладки WSD, то, скорее всего, сбой приложения не связан с переданными адресами транспорта, операционной системой или сетевой средой.</span><span class="sxs-lookup"><span data-stu-id="00ecc-131">If the device ID and device metadata appears correctly in the WSD Debug Client output, then the application failure is likely not related to the supplied transport addresses, the operating system, or the network environment.</span></span> <span data-ttu-id="00ecc-132">Замените универсальный узел и клиент пользовательским узлом и клиентом и продолжайте устранение неполадок, выполнив процедуры, описанные в статье [Использование ведения журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="00ecc-132">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="00ecc-133">Если адрес устройства и метаданные устройства не отображаются в выходных данных клиента отладки WSD, то ошибка может быть вызвана одной или несколькими из следующих причин.</span><span class="sxs-lookup"><span data-stu-id="00ecc-133">If the device address and device metadata do not appear in the WSD Debug Client output, then the failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="00ecc-134">Адрес транспорта, объявленный узлом, неверен или имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="00ecc-134">The transport address advertised by the host is incorrect or malformed.</span></span> <span data-ttu-id="00ecc-135">Клиент отладки WSD пытается получить метаданные устройства из URL-адреса, указанного в элементе **ксаддрс** сообщения [ProbeMatch](probematches-message.md) или [ресолвематчес](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="00ecc-135">WSD Debug Client attempts to get device metadata from the URL provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="00ecc-136">URL-адрес, используемый для обмена метаданными, отображается в выходных данных клиента отладки WSD с префиксом фразы `Using xAddr` .</span><span class="sxs-lookup"><span data-stu-id="00ecc-136">The URL used for metadata exchange appears in the WSD Debug Client output, prefixed by the phrase `Using xAddr`.</span></span> <span data-ttu-id="00ecc-137">В следующем примере показан Ксаддрс, используемый для обмена метаданными в приведенном выше выходных данных клиента отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="00ecc-137">The following example shows the XAddrs used for metadata exchange in the above WSD Debug Client output.</span></span>

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    <span data-ttu-id="00ecc-138">Если указанный Ксаддрс не соответствует [правилам проверки ксаддр](xaddr-validation-rules.md), то клиент отладки WSD не сможет получить метаданные устройства.</span><span class="sxs-lookup"><span data-stu-id="00ecc-138">If the supplied XAddrs do not conform to the [XAddr validation rules](xaddr-validation-rules.md), then the WSD Debug Client cannot get the device's metadata.</span></span>

-   <span data-ttu-id="00ecc-139">Приложение выполняется в неправильном контексте безопасности.</span><span class="sxs-lookup"><span data-stu-id="00ecc-139">The application is running in the wrong security context.</span></span> <span data-ttu-id="00ecc-140">Убедитесь, что приложение использует правильные учетные данные, а клиент и узел имеют достаточные разрешения для доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="00ecc-140">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="00ecc-141">Неправильная конфигурация брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="00ecc-141">The firewall configuration is wrong.</span></span> <span data-ttu-id="00ecc-142">Следуйте инструкциям в разделе [Проверка параметров адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md) , чтобы убедиться в правильности параметров брандмауэра Windows и отсутствии других правил удаления пакетов.</span><span class="sxs-lookup"><span data-stu-id="00ecc-142">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="00ecc-143">Клиент и узел также можно скопировать на компьютер "поддерживалась" (один с установкой операционной системы по умолчанию, которая никогда не присоединяется к домену), чтобы попытаться воспроизвести сбой.</span><span class="sxs-lookup"><span data-stu-id="00ecc-143">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="00ecc-144">Политика IPSec блокирует приложение.</span><span class="sxs-lookup"><span data-stu-id="00ecc-144">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="00ecc-145">Скопируйте клиент и узел на компьютер, который не подчиняется политикам IPSec, и попробуйте воспроизвести ошибку.</span><span class="sxs-lookup"><span data-stu-id="00ecc-145">Copy the client and host onto a machine that is not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00ecc-146">См. также</span><span class="sxs-lookup"><span data-stu-id="00ecc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ecc-147">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="00ecc-147">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="00ecc-148">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="00ecc-148">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



