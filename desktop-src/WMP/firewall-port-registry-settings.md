---
title: Параметры реестра для порта брандмауэра
description: Параметры реестра для порта брандмауэра
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Проигрыватель Windows Media, параметры реестра для порта брандмауэра
- Проигрыватель Windows Media, параметры реестра портов
- Проигрыватель Windows Media, реестр
- реестр, параметры порта брандмауэра
- реестр, параметры порта
- реестр, параметры для проигрывателя Windows Media
- параметры реестра для порта брандмауэра
- параметры реестра портов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887800"
---
# <a name="firewall-port-registry-settings"></a><span data-ttu-id="2d040-111">Параметры реестра для порта брандмауэра</span><span class="sxs-lookup"><span data-stu-id="2d040-111">Firewall Port Registry Settings</span></span>

<span data-ttu-id="2d040-112">Проигрыватель Windows Media размещает записи в реестре, чтобы брандмауэры могли определить, следует ли открывать или закрывать порты, используемые совместно используемыми библиотеками мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2d040-112">Windows Media Player places entries in the registry so that firewalls can determine whether to open or close the ports that are used by media library sharing.</span></span>

<span data-ttu-id="2d040-113">**Запись реестра Акцептедеула**</span><span class="sxs-lookup"><span data-stu-id="2d040-113">**AcceptedEULA Registry Entry**</span></span>

<span data-ttu-id="2d040-114">Проигрыватель Windows Media использует следующую запись реестра, чтобы указать, принял ли пользователь лицензионное соглашение (EULA).</span><span class="sxs-lookup"><span data-stu-id="2d040-114">Windows Media Player uses the following registry entry to indicate whether the user has accepted the end user license agreement (EULA).</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



<span data-ttu-id="2d040-115">Значение 1 указывает, что пользователь принял лицензионное соглашение.</span><span class="sxs-lookup"><span data-stu-id="2d040-115">A value of 1 indicates that the user has accepted the license agreement.</span></span> <span data-ttu-id="2d040-116">Значение 0 указывает, что пользователь не принял лицензионное соглашение.</span><span class="sxs-lookup"><span data-stu-id="2d040-116">A value of 0 indicates that the user has not accepted the license agreement.</span></span>

<span data-ttu-id="2d040-117">**Запись реестра Вмпнссфиреваллпортсопен**</span><span class="sxs-lookup"><span data-stu-id="2d040-117">**WMPNSSFirewallPortsOpen Registry Entry**</span></span>

<span data-ttu-id="2d040-118">Проигрыватель Windows Media использует следующую запись реестра, чтобы указать, что пользователь выбрал для предоставления общего доступа к своей библиотеке мультимедиа другим компьютерам в домашней сети.</span><span class="sxs-lookup"><span data-stu-id="2d040-118">Windows Media Player uses the following registry entry to indicate whether the user has chosen to share his or her media library with other computers on a home network.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



<span data-ttu-id="2d040-119">Значение 1 указывает, что пользователь выбрал общий доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2d040-119">A value of 1 indicates that the user has chosen to share the library.</span></span> <span data-ttu-id="2d040-120">Значение 0 указывает, что пользователь решил не предоставлять общий доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="2d040-120">A value of 0 indicates that the user has chosen not to share the library.</span></span>

<span data-ttu-id="2d040-121">**Порты, связанные с совместным доступом к библиотеке мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="2d040-121">**Ports Related to Media Library Sharing**</span></span>

<span data-ttu-id="2d040-122">В Windows Vista, если параметр реестра **вмпнссфиреваллпортсопен** имеет значение 1, должны быть открыты следующие порты.</span><span class="sxs-lookup"><span data-stu-id="2d040-122">On Windows Vista, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="2d040-123">Порт</span><span class="sxs-lookup"><span data-stu-id="2d040-123">Port</span></span>          | <span data-ttu-id="2d040-124">Протокол</span><span class="sxs-lookup"><span data-stu-id="2d040-124">Protocol</span></span>                  | <span data-ttu-id="2d040-125">Процесс</span><span class="sxs-lookup"><span data-stu-id="2d040-125">Process</span></span>                         | <span data-ttu-id="2d040-126">Направление</span><span class="sxs-lookup"><span data-stu-id="2d040-126">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="2d040-127">554</span><span class="sxs-lookup"><span data-stu-id="2d040-127">554</span></span>           | <span data-ttu-id="2d040-128">TCP RTSP</span><span class="sxs-lookup"><span data-stu-id="2d040-128">TCP RTSP</span></span>                  | <span data-ttu-id="2d040-129">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-129">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-130">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-130">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-131">8554-8558</span><span class="sxs-lookup"><span data-stu-id="2d040-131">8554 - 8558</span></span>   | <span data-ttu-id="2d040-132">TCP RTSP</span><span class="sxs-lookup"><span data-stu-id="2d040-132">TCP RTSP</span></span>                  | <span data-ttu-id="2d040-133">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-133">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-134">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-134">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-135">5004, 5005</span><span class="sxs-lookup"><span data-stu-id="2d040-135">5004, 5005</span></span>    | <span data-ttu-id="2d040-136">UDP РТКП/RTP</span><span class="sxs-lookup"><span data-stu-id="2d040-136">UDP RTCP/RTP</span></span>              | <span data-ttu-id="2d040-137">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-137">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-138">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-138">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-139">50004-50013</span><span class="sxs-lookup"><span data-stu-id="2d040-139">50004 - 50013</span></span> | <span data-ttu-id="2d040-140">UDP РТКП/RTP</span><span class="sxs-lookup"><span data-stu-id="2d040-140">UDP RTCP/RTP</span></span>              | <span data-ttu-id="2d040-141">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-141">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-142">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-142">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-143">1900</span><span class="sxs-lookup"><span data-stu-id="2d040-143">1900</span></span>          | <span data-ttu-id="2d040-144">UDP SSDP</span><span class="sxs-lookup"><span data-stu-id="2d040-144">UDP SSDP</span></span>                  | <span data-ttu-id="2d040-145">Ссдпсрв в svchost.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-145">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="2d040-146">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-146">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-147">2869</span><span class="sxs-lookup"><span data-stu-id="2d040-147">2869</span></span>          | <span data-ttu-id="2d040-148">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="2d040-148">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="2d040-149">Ссдпсрв или UPnPHost в svchost.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-149">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="2d040-150">Въезд</span><span class="sxs-lookup"><span data-stu-id="2d040-150">inbound</span></span>              |
| <span data-ttu-id="2d040-151">10280-10284</span><span class="sxs-lookup"><span data-stu-id="2d040-151">10280 - 10284</span></span> | <span data-ttu-id="2d040-152">Регистрация UDP WMDRM-ND</span><span class="sxs-lookup"><span data-stu-id="2d040-152">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="2d040-153">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-153">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-154">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-154">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-155">10243</span><span class="sxs-lookup"><span data-stu-id="2d040-155">10243</span></span>         | <span data-ttu-id="2d040-156">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="2d040-156">TCP HTTP</span></span>                  | <span data-ttu-id="2d040-157">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-157">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-158">Въезд</span><span class="sxs-lookup"><span data-stu-id="2d040-158">inbound</span></span>              |
| <span data-ttu-id="2d040-159">2177</span><span class="sxs-lookup"><span data-stu-id="2d040-159">2177</span></span>          | <span data-ttu-id="2d040-160">QWAVE TCP UDP</span><span class="sxs-lookup"><span data-stu-id="2d040-160">TCP UDP qWAVE</span></span>             | <span data-ttu-id="2d040-161">svchost.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-161">svchost.exe</span></span>                     | <span data-ttu-id="2d040-162">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-162">inbound and outbound</span></span> |



 

<span data-ttu-id="2d040-163">В Windows Vista, если параметр реестра **акцептедеула** имеет значение 1, должны быть открыты следующие порты.</span><span class="sxs-lookup"><span data-stu-id="2d040-163">On Windows Vista, if the **AcceptedEULA** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="2d040-164">Порт</span><span class="sxs-lookup"><span data-stu-id="2d040-164">Port</span></span>          | <span data-ttu-id="2d040-165">Протокол</span><span class="sxs-lookup"><span data-stu-id="2d040-165">Protocol</span></span>       | <span data-ttu-id="2d040-166">Процесс</span><span class="sxs-lookup"><span data-stu-id="2d040-166">Process</span></span>                         | <span data-ttu-id="2d040-167">Направление</span><span class="sxs-lookup"><span data-stu-id="2d040-167">Direction</span></span>            |
|---------------|----------------|---------------------------------|----------------------|
| <span data-ttu-id="2d040-168">Все UDP-порты</span><span class="sxs-lookup"><span data-stu-id="2d040-168">All UDP ports</span></span> | <span data-ttu-id="2d040-169">UDP-RTP, ТО ЕСТЬ</span><span class="sxs-lookup"><span data-stu-id="2d040-169">UDP RTP, MSB</span></span>   | <span data-ttu-id="2d040-170">wmplayer.exe, любая подсеть</span><span class="sxs-lookup"><span data-stu-id="2d040-170">wmplayer.exe, any subnet</span></span>        | <span data-ttu-id="2d040-171">Въезд</span><span class="sxs-lookup"><span data-stu-id="2d040-171">inbound</span></span>              |
| <span data-ttu-id="2d040-172">1900</span><span class="sxs-lookup"><span data-stu-id="2d040-172">1900</span></span>          | <span data-ttu-id="2d040-173">UDP SSDP</span><span class="sxs-lookup"><span data-stu-id="2d040-173">UDP SSDP</span></span>       | <span data-ttu-id="2d040-174">Ссдпсрв или UPnPHost в svchost.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-174">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="2d040-175">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-175">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-176">2869</span><span class="sxs-lookup"><span data-stu-id="2d040-176">2869</span></span>          | <span data-ttu-id="2d040-177">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="2d040-177">TCP SSDP, UPnP</span></span> | <span data-ttu-id="2d040-178">Ссдпсрв, UPnPHost</span><span class="sxs-lookup"><span data-stu-id="2d040-178">SSDPsrv, UPnPHost</span></span>               | <span data-ttu-id="2d040-179">Въезд</span><span class="sxs-lookup"><span data-stu-id="2d040-179">inbound</span></span>              |



 

<span data-ttu-id="2d040-180">В Microsoft Windows XP, если параметру реестра **вмпнссфиреваллпортсопен** присвоено значение 1, то должны быть открыты следующие порты.</span><span class="sxs-lookup"><span data-stu-id="2d040-180">On Microsoft Windows XP, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="2d040-181">Порт</span><span class="sxs-lookup"><span data-stu-id="2d040-181">Port</span></span>          | <span data-ttu-id="2d040-182">Протокол</span><span class="sxs-lookup"><span data-stu-id="2d040-182">Protocol</span></span>                  | <span data-ttu-id="2d040-183">Процесс</span><span class="sxs-lookup"><span data-stu-id="2d040-183">Process</span></span>                         | <span data-ttu-id="2d040-184">Направление</span><span class="sxs-lookup"><span data-stu-id="2d040-184">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="2d040-185">1900</span><span class="sxs-lookup"><span data-stu-id="2d040-185">1900</span></span>          | <span data-ttu-id="2d040-186">UDP SSDP</span><span class="sxs-lookup"><span data-stu-id="2d040-186">UDP SSDP</span></span>                  | <span data-ttu-id="2d040-187">Ссдпсрв в svchost.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-187">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="2d040-188">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-188">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-189">2869</span><span class="sxs-lookup"><span data-stu-id="2d040-189">2869</span></span>          | <span data-ttu-id="2d040-190">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="2d040-190">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="2d040-191">Ссдпсрв или UPnPHost в svchost.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-191">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="2d040-192">Въезд</span><span class="sxs-lookup"><span data-stu-id="2d040-192">inbound</span></span>              |
| <span data-ttu-id="2d040-193">10280-10284</span><span class="sxs-lookup"><span data-stu-id="2d040-193">10280 - 10284</span></span> | <span data-ttu-id="2d040-194">Регистрация UDP WMDRM-ND</span><span class="sxs-lookup"><span data-stu-id="2d040-194">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="2d040-195">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-195">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-196">входящие и исходящие</span><span class="sxs-lookup"><span data-stu-id="2d040-196">inbound and outbound</span></span> |
| <span data-ttu-id="2d040-197">10243</span><span class="sxs-lookup"><span data-stu-id="2d040-197">10243</span></span>         | <span data-ttu-id="2d040-198">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="2d040-198">TCP HTTP</span></span>                  | <span data-ttu-id="2d040-199">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="2d040-199">wmpnetwk.exe</span></span>                    | <span data-ttu-id="2d040-200">Въезд</span><span class="sxs-lookup"><span data-stu-id="2d040-200">inbound</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="2d040-201">См. также</span><span class="sxs-lookup"><span data-stu-id="2d040-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d040-202">**Параметры реестра**</span><span class="sxs-lookup"><span data-stu-id="2d040-202">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




