---
title: Параметры конфигурации
description: Поведение API точки управления и API узла устройства можно изменить, изменив параметры в реестре.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691162"
---
# <a name="configuration-settings"></a><span data-ttu-id="94158-103">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="94158-103">Configuration Settings</span></span>

<span data-ttu-id="94158-104">Поведение [API точки управления](control-point-api.md) и [API узла устройства](device-host-api.md) можно изменить, изменив параметры в реестре.</span><span class="sxs-lookup"><span data-stu-id="94158-104">The behavior of the [Control Point API](control-point-api.md) and [Device Host API](device-host-api.md) can be modified by changing settings in the registry.</span></span>

<span data-ttu-id="94158-105">Существует семь значений реестра, влияющих на поведение:</span><span class="sxs-lookup"><span data-stu-id="94158-105">There are seven registry values that affect behavior:</span></span>

-   <span data-ttu-id="94158-106">**довнлоадскопе**</span><span class="sxs-lookup"><span data-stu-id="94158-106">**DownloadScope**</span></span>
-   <span data-ttu-id="94158-107">**девицелифетиме**</span><span class="sxs-lookup"><span data-stu-id="94158-107">**DeviceLifeTime**</span></span>
-   <span data-ttu-id="94158-108">\\**Узел** \\ устройства UPnP **Ограничение размера файла**</span><span class="sxs-lookup"><span data-stu-id="94158-108">\\**UPnP Device Host**\\**File Size Limit**</span></span>
-   <span data-ttu-id="94158-109">\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Ограничение размера файла**</span><span class="sxs-lookup"><span data-stu-id="94158-109">\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
-   <span data-ttu-id="94158-110">**макскаче**</span><span class="sxs-lookup"><span data-stu-id="94158-110">**MaxCache**</span></span>
-   <span data-ttu-id="94158-111">**Срок жизни**</span><span class="sxs-lookup"><span data-stu-id="94158-111">**TTL**</span></span>
-   <span data-ttu-id="94158-112">**рецеивескопе**</span><span class="sxs-lookup"><span data-stu-id="94158-112">**ReceiveScope**</span></span>

<span data-ttu-id="94158-113">Существует два значения реестра под названием **ограничение размера файла**, один для документов описания, другой — для ответов, использующих протокол SOAP.</span><span class="sxs-lookup"><span data-stu-id="94158-113">There are two registry values called **File Size Limit**, one for description documents and the other for responses that use Simple Object Access Protocol (SOAP).</span></span>

<span data-ttu-id="94158-114">Расположение каждого из семи значений в реестре выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="94158-114">The location of each of the seven values in the registry is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a><span data-ttu-id="94158-115">Описание значения реестра</span><span class="sxs-lookup"><span data-stu-id="94158-115">Registry Value Descriptions</span></span>

<span data-ttu-id="94158-116">Значения реестра описаны в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="94158-116">The registry values are explained in the following list.</span></span> <span data-ttu-id="94158-117">Каждое значение реестра представляет собой **reg \_ DWORD** (32-разрядное целое число).</span><span class="sxs-lookup"><span data-stu-id="94158-117">Each registry value is a **REG\_DWORD** (a 32-bit integer).</span></span> <span data-ttu-id="94158-118">Результат каждого значения является глобальным.</span><span class="sxs-lookup"><span data-stu-id="94158-118">The effect of each value is global.</span></span>

<dl> <dt>

<span data-ttu-id="94158-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**довнлоадскопе**</span><span class="sxs-lookup"><span data-stu-id="94158-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span></span>
</dt> <dd>

<span data-ttu-id="94158-120">Указывает, какие IP-адреса являются допустимыми для URL-адреса документа описания устройства.</span><span class="sxs-lookup"><span data-stu-id="94158-120">Specifies which IP addresses are valid for the device description document URL.</span></span> <span data-ttu-id="94158-121">Если IP-адрес узла, указанный в URL-адресе документа описания, не входит в область, указанную параметром **довнлоадскопе**, то этот IP-адрес является недопустимым и объект устройства не будет создан.</span><span class="sxs-lookup"><span data-stu-id="94158-121">If the IP address of the host that is specified in the description document URL is not within the scope specified by **DownloadScope**, that IP address is not valid and the device object will not be created.</span></span>

<span data-ttu-id="94158-122">Допустимые значения приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="94158-122">The valid values are shown in the following table.</span></span> <span data-ttu-id="94158-123">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="94158-123">The default value is 1.</span></span>



| <span data-ttu-id="94158-124">Значение **довнлоадскопе**</span><span class="sxs-lookup"><span data-stu-id="94158-124">Value of **DownloadScope**</span></span> | <span data-ttu-id="94158-125">Значение</span><span class="sxs-lookup"><span data-stu-id="94158-125">Meaning</span></span>                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94158-126">0</span><span class="sxs-lookup"><span data-stu-id="94158-126">0</span></span>                          | <span data-ttu-id="94158-127">IP-адрес узла должен быть адресом подсети.</span><span class="sxs-lookup"><span data-stu-id="94158-127">Host's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="94158-128">1</span><span class="sxs-lookup"><span data-stu-id="94158-128">1</span></span>                          | <span data-ttu-id="94158-129">IP-адрес узла должен быть адресом подсети или частным адресом, который является одним из 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (как указано в RFC 1918) или 169,254. *x*. *x* (как указано в RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="94158-129">Host's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="94158-130">2</span><span class="sxs-lookup"><span data-stu-id="94158-130">2</span></span>                          | <span data-ttu-id="94158-131">IP-адрес узла должен быть адресом подсети, частным адресом или адресом, который находится на прыжках срока жизни (TTL) от контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="94158-131">Host's IP address must be a subnet address, private address, or an address that is within the time-to-live (TTL) hops from the control point.</span></span>                                                              |
| <span data-ttu-id="94158-132">3</span><span class="sxs-lookup"><span data-stu-id="94158-132">3</span></span>                          | <span data-ttu-id="94158-133">IP-адрес узла может быть любым адресом.</span><span class="sxs-lookup"><span data-stu-id="94158-133">Host's IP address can be any address.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="94158-134">>3</span><span class="sxs-lookup"><span data-stu-id="94158-134">>3</span></span>                      | <span data-ttu-id="94158-135">То же, что и для значения 0.</span><span class="sxs-lookup"><span data-stu-id="94158-135">Same as that for the value 0.</span></span>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="94158-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**девицелифетиме**</span><span class="sxs-lookup"><span data-stu-id="94158-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span></span>
</dt> <dd>

<span data-ttu-id="94158-137">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="94158-137">Optional.</span></span> <span data-ttu-id="94158-138">Указывает время существования устройства (в секундах), переопределяющее значение, указанное в сообщении с объявлением устройства.</span><span class="sxs-lookup"><span data-stu-id="94158-138">Specifies a device's lifetime, in seconds, which overrides the value provided in the device's announcement message.</span></span> <span data-ttu-id="94158-139">Если указан параметр **девицелифетиме** , значение, указанное в объявлении устройства, игнорируется, а вместо него используется значение реестра.</span><span class="sxs-lookup"><span data-stu-id="94158-139">If **DeviceLifeTime** is present, the value specified in the device's announcement is ignored and the registry value is used instead.</span></span> <span data-ttu-id="94158-140">Это относится ко всем устройствам.</span><span class="sxs-lookup"><span data-stu-id="94158-140">This applies to all devices.</span></span>

<span data-ttu-id="94158-141">Допустимые значения находятся в диапазоне от 900 до **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="94158-141">Valid values range from 900 through **MAX\_DWORD**.</span></span> <span data-ttu-id="94158-142">Значение по умолчанию — 1800.</span><span class="sxs-lookup"><span data-stu-id="94158-142">The default value is 1800.</span></span> <span data-ttu-id="94158-143">Если для **девицелифетиме** задано значение 0, то используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94158-143">If **DeviceLifeTime** is set to 0, the default value is used.</span></span>

</dd> <dt>

<span data-ttu-id="94158-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**Узел** \\ устройства UPnP **Ограничение размера файла**</span><span class="sxs-lookup"><span data-stu-id="94158-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP Device Host**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="94158-145">Задает максимальный размер каждого документа описания в байтах.</span><span class="sxs-lookup"><span data-stu-id="94158-145">Specifies the maximum size, in bytes, of each description document.</span></span> <span data-ttu-id="94158-146">Этот параметр нельзя настроить в версиях Windows, предшествующих Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="94158-146">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="94158-147">В предыдущих версиях этот параметр жестко закодирован как 102400.</span><span class="sxs-lookup"><span data-stu-id="94158-147">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="94158-148">Допустимые значения находятся в диапазоне от 10240 до **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="94158-148">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="94158-149">Значение по умолчанию — 102400.</span><span class="sxs-lookup"><span data-stu-id="94158-149">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="94158-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Ограничение размера файла**</span><span class="sxs-lookup"><span data-stu-id="94158-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="94158-151">Указывает допустимый максимальный размер (в байтах) ответа SOAP.</span><span class="sxs-lookup"><span data-stu-id="94158-151">Specifies the maximum size, in bytes, of the SOAP response that is acceptable.</span></span> <span data-ttu-id="94158-152">Этот параметр нельзя настроить в версиях Windows, предшествующих Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="94158-152">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="94158-153">В предыдущих версиях этот параметр жестко закодирован как 102400.</span><span class="sxs-lookup"><span data-stu-id="94158-153">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="94158-154">Допустимые значения находятся в диапазоне от 10240 до **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="94158-154">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="94158-155">Значение по умолчанию — 102400.</span><span class="sxs-lookup"><span data-stu-id="94158-155">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="94158-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**макскаче**</span><span class="sxs-lookup"><span data-stu-id="94158-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span></span>
</dt> <dd>

<span data-ttu-id="94158-157">Указывает максимальное число записей, разрешенных в кэше SSDP.</span><span class="sxs-lookup"><span data-stu-id="94158-157">Specifies the maximum number of entries allowed in the Simple Service Discovery Protocol (SSDP) cache.</span></span>

<span data-ttu-id="94158-158">Допустимы значения в диапазоне от 10 до 30000.</span><span class="sxs-lookup"><span data-stu-id="94158-158">Valid values range from 10 through 30000.</span></span> <span data-ttu-id="94158-159">Значение по умолчанию ― 1000.</span><span class="sxs-lookup"><span data-stu-id="94158-159">The default value is 1000.</span></span>

</dd> <dt>

<span data-ttu-id="94158-160"><span id="TTL"></span><span id="ttl"></span>**ВЕЛИЧИН**</span><span class="sxs-lookup"><span data-stu-id="94158-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span></span>
</dt> <dd>

<span data-ttu-id="94158-161">Указывает срок жизни для пакета SSDP.</span><span class="sxs-lookup"><span data-stu-id="94158-161">Specifies the time-to-live for an SSDP packet.</span></span> <span data-ttu-id="94158-162">То есть **TTL** указывает число прыжков, разрешенное для пакета.</span><span class="sxs-lookup"><span data-stu-id="94158-162">That is, **TTL** specifies the number of hops allowed for a packet.</span></span>

<span data-ttu-id="94158-163">Допустимы значения в диапазоне от 1 до 255.</span><span class="sxs-lookup"><span data-stu-id="94158-163">Valid values range from 1 through 255.</span></span> <span data-ttu-id="94158-164">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="94158-164">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="94158-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**рецеивескопе**</span><span class="sxs-lookup"><span data-stu-id="94158-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span></span>
</dt> <dd>

<span data-ttu-id="94158-166">Указывает, какие IP-адреса являются допустимыми источниками сообщения.</span><span class="sxs-lookup"><span data-stu-id="94158-166">Specifies which IP addresses are valid sources of a message.</span></span> <span data-ttu-id="94158-167">Если входящее сообщение исходит из адреса, не находящегося в области, заданной параметром **рецеивескопе**, сообщение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="94158-167">If an incoming message originates from an address that is not within the scope specified by **ReceiveScope**, the message is ignored.</span></span> <span data-ttu-id="94158-168">Этот параметр нельзя настроить в версиях Windows, предшествующих Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="94158-168">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="94158-169">В предыдущих версиях сообщение принимается без учета его источника.</span><span class="sxs-lookup"><span data-stu-id="94158-169">In the previous versions, a message is accepted without regard to its source.</span></span>

<span data-ttu-id="94158-170">Допустимые значения приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="94158-170">The valid values are shown in the following table.</span></span> <span data-ttu-id="94158-171">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="94158-171">The default value is 1.</span></span>



| <span data-ttu-id="94158-172">Значение **рецеивескопе**</span><span class="sxs-lookup"><span data-stu-id="94158-172">Value of **ReceiveScope**</span></span> | <span data-ttu-id="94158-173">Значение</span><span class="sxs-lookup"><span data-stu-id="94158-173">Meaning</span></span>                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94158-174">0</span><span class="sxs-lookup"><span data-stu-id="94158-174">0</span></span>                         | <span data-ttu-id="94158-175">IP-адрес отправителя должен быть адресом подсети.</span><span class="sxs-lookup"><span data-stu-id="94158-175">Sender's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="94158-176">1</span><span class="sxs-lookup"><span data-stu-id="94158-176">1</span></span>                         | <span data-ttu-id="94158-177">IP-адрес отправителя должен быть адресом подсети или частным адресом, который является одним из 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (как указано в RFC 1918) или 169,254. *x*. *x* (как указано в RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="94158-177">Sender's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="94158-178">2</span><span class="sxs-lookup"><span data-stu-id="94158-178">2</span></span>                         | <span data-ttu-id="94158-179">Не используется.</span><span class="sxs-lookup"><span data-stu-id="94158-179">Not used.</span></span> <span data-ttu-id="94158-180">Если для **рецеивескопе** задано значение 2, то используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94158-180">If **ReceiveScope** is set to 2, the default value is used.</span></span>                                                                                                                                        |
| <span data-ttu-id="94158-181">3</span><span class="sxs-lookup"><span data-stu-id="94158-181">3</span></span>                         | <span data-ttu-id="94158-182">IP-адрес отправителя может быть любым адресом.</span><span class="sxs-lookup"><span data-stu-id="94158-182">Sender's IP address can be any address.</span></span>                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="94158-183">См. также</span><span class="sxs-lookup"><span data-stu-id="94158-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94158-184">Общие сведения об архитектуре UPnP</span><span class="sxs-lookup"><span data-stu-id="94158-184">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




