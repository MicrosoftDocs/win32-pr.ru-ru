---
description: Если клиент и узел не могут видеть друг друга в сети, то для пользовательского узла и клиента можно заменить универсальный узел и клиент, чтобы помочь устранить проблему.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Использование универсального узла и клиента для UDP-WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263457"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a><span data-ttu-id="3f2d0-103">Использование универсального узла и клиента для UDP-WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="3f2d0-103">Using a Generic Host and Client for UDP WS-Discovery</span></span>

<span data-ttu-id="3f2d0-104">Если клиент и узел не могут видеть друг друга в сети, то для пользовательского узла и клиента можно заменить универсальный узел и клиент, чтобы помочь устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-104">If the client and host cannot see each other on the network, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="3f2d0-105">Если адрес устройства не отображается в выходных данных клиента отладки WSD, то, вероятно, причиной сбоя является сетевая среда.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-105">If the device address does not appear in the WSD Debug Client output, then the network environment is probably causing the failure.</span></span> <span data-ttu-id="3f2d0-106">Дополнительные сведения об универсальном узле и клиенте см. в разделе [средства отладки](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3f2d0-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="3f2d0-107">Если узел или клиент является приложением, запущенным на компьютере, универсальный узел или клиент должны быть запущены в том же контексте безопасности, что и фактический узел или клиент.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-107">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="3f2d0-108">Например, если фактический узел или клиент работает от имени администратора, то универсальный узел или клиент должен работать от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-108">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="3f2d0-109">Кроме того, если узел или клиент является автономным устройством, он должен быть полностью заменен ПК, на котором работает универсальный узел или клиент.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-109">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client.</span></span>

<span data-ttu-id="3f2d0-110">**Использование универсального узла и клиента для устранения неполадок при использовании протокола UDP WS-Discovery**</span><span class="sxs-lookup"><span data-stu-id="3f2d0-110">**To using a generic host and client to troubleshoot UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="3f2d0-111">Откройте окно командной строки.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-111">Open a command prompt window.</span></span>
2.  <span data-ttu-id="3f2d0-112">Выполните следующую команду: **всддебуг \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="3f2d0-112">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="3f2d0-113">Может появиться диалоговое окно **оповещение системы безопасности Windows** .</span><span class="sxs-lookup"><span data-stu-id="3f2d0-113">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="3f2d0-114">Если это так, нажмите кнопку **разблокировать** , чтобы разрешить запуск узла отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-114">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="3f2d0-115">Эта команда создает выходные данные, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-115">This command generates output similar to the following.</span></span> <span data-ttu-id="3f2d0-116">Запишите идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-116">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="3f2d0-117">Выполните следующую команду: **всддебуг \_client.exe/Mode Metadata/Хелло/ресолве** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="3f2d0-117">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="3f2d0-118">Замените *<id>* идентификатором устройства, указанным на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-118">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="3f2d0-119">Может появиться диалоговое окно **оповещение системы безопасности Windows** .</span><span class="sxs-lookup"><span data-stu-id="3f2d0-119">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="3f2d0-120">Если это так, нажмите кнопку **разблокировать** , чтобы разрешить запуск клиента отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-120">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="3f2d0-121">Клиент отладки WSD создает выходные данные, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-121">WSD Debug Client generates output similar to the following.</span></span>

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
```

<span data-ttu-id="3f2d0-122">Клиент отладки WSD может создавать большой объем выходных данных в сети с множеством устройств DPWS.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-122">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="3f2d0-123">Выходные данные можно перенаправить в файл для упрощения анализа.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-123">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="3f2d0-124">Введите **log tee** *<filename>* в командной строке клиента отладки WSD, чтобы перенаправить вывод в файл.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-124">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="3f2d0-125">Перенаправление выходных данных можно остановить, введя **log tee остановиться** в командной строке клиента отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-125">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="3f2d0-126">Запишите адрес ссылки на конечную точку (EPR).</span><span class="sxs-lookup"><span data-stu-id="3f2d0-126">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="3f2d0-127">Этот адрес EPR должен соответствовать ИДЕНТИФИКАТОРу устройства, указанному на шаге 2 выше.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-127">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="3f2d0-128">В этом случае сбой приложения, скорее всего, не связан с операционной системой или сетевой средой.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-128">If this is the case, then the application failure is likely not related to the operating system or the network environment.</span></span> <span data-ttu-id="3f2d0-129">Замените универсальный узел и клиент пользовательским узлом и клиентом и продолжайте устранение неполадок, выполнив процедуры, описанные в статье [Использование клиента отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="3f2d0-129">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

<span data-ttu-id="3f2d0-130">Если идентификатор устройства не совпадает с адресом EPR, вероятно, сбой приложения связан с операционной системой или сетевой средой.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-130">If the device ID does not match the EPR address, then the application failure is probably related to the operating system or the network environment.</span></span> <span data-ttu-id="3f2d0-131">Сбой может быть вызван одной или несколькими из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="3f2d0-131">The failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="3f2d0-132">Приложение выполняется в неправильном контексте безопасности.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-132">The application is running in the wrong security context.</span></span> <span data-ttu-id="3f2d0-133">Убедитесь, что приложение использует правильные учетные данные, а клиент и узел имеют достаточные разрешения для доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-133">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="3f2d0-134">Неправильная конфигурация брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-134">The firewall configuration is wrong.</span></span> <span data-ttu-id="3f2d0-135">Следуйте инструкциям в разделе [Проверка параметров адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md) , чтобы убедиться в правильности параметров брандмауэра Windows и отсутствии других правил удаления пакетов.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-135">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="3f2d0-136">Клиент и узел также можно скопировать на компьютер "поддерживалась" (один с установкой операционной системы по умолчанию, которая никогда не присоединяется к домену), чтобы попытаться воспроизвести сбой.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-136">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="3f2d0-137">Политика IPSec блокирует приложение.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-137">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="3f2d0-138">Скопируйте клиент и узел на компьютер, не подчиняются политикам IPSec, и попробуйте воспроизвести сбой.</span><span class="sxs-lookup"><span data-stu-id="3f2d0-138">Copy the client and host onto a machine not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f2d0-139">См. также</span><span class="sxs-lookup"><span data-stu-id="3f2d0-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f2d0-140">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="3f2d0-140">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="3f2d0-141">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="3f2d0-141">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



