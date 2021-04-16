---
title: Константы типа NAP (Наптипес. h)
description: Определены следующие константы NAP.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672790"
---
# <a name="nap-type-constants"></a><span data-ttu-id="d8a66-103">Константы типа NAP</span><span class="sxs-lookup"><span data-stu-id="d8a66-103">NAP Type Constants</span></span>

> [!Note]  
> <span data-ttu-id="d8a66-104">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="d8a66-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d8a66-105">Определены следующие константы NAP.</span><span class="sxs-lookup"><span data-stu-id="d8a66-105">The following NAP constants are defined.</span></span>

<span data-ttu-id="d8a66-106">В Наптипес. h определены следующие константы NAP:</span><span class="sxs-lookup"><span data-stu-id="d8a66-106">The following NAP constants are defined in NapTypes.h:</span></span>

<dl> <dt>

<span data-ttu-id="d8a66-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**макссохаттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="d8a66-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-108">0x64</span><span class="sxs-lookup"><span data-stu-id="d8a66-108">0x64</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-109">Максимальное число [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) объектов типа "Длина-значение" (TLV), связанных с пакетом [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="d8a66-109">The maximum number of [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) objects associated with an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**макссохаттрибутесизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-111">0xFA0</span><span class="sxs-lookup"><span data-stu-id="d8a66-111">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-112">Максимальный размер (в байтах) объекта [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) , связанного с пакетом состояния работоспособности ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)).</span><span class="sxs-lookup"><span data-stu-id="d8a66-112">The maximum size, in bytes, of a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) object associated with a statement of health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**миннетворксохсизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-114">0xC</span><span class="sxs-lookup"><span data-stu-id="d8a66-114">0xC</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-115">Минимальный размер пакета [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) в байтах.</span><span class="sxs-lookup"><span data-stu-id="d8a66-115">The minimum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**макснетворксохсизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-117">0xFA0</span><span class="sxs-lookup"><span data-stu-id="d8a66-117">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-118">Максимальный размер пакета [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) в байтах.</span><span class="sxs-lookup"><span data-stu-id="d8a66-118">The maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**максдвордкаунтперсохаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="d8a66-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-120">Макссохаттрибутесизе/sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="d8a66-120">maxSoHAttributeSize / sizeof(DWORD)</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-121">Максимальное число значений типа DWORD, связанных с [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="d8a66-121">The maximum number of DWORD values associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="d8a66-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-123">Макссохаттрибутесизе/0x4</span><span class="sxs-lookup"><span data-stu-id="d8a66-123">maxSoHAttributeSize / 0x4</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-124">Максимальное число IPv4-адресов, связанных с [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="d8a66-124">The maximum number of IPv4 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="d8a66-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-126">Макссохаттрибутесизе/0x10</span><span class="sxs-lookup"><span data-stu-id="d8a66-126">maxSoHAttributeSize / 0x10</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-127">Максимальное число IPv6-адресов, связанных с [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="d8a66-127">The maximum number of IPv6 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**максстрингленгс**</span><span class="sxs-lookup"><span data-stu-id="d8a66-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-129">0x400</span><span class="sxs-lookup"><span data-stu-id="d8a66-129">0x400</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-130">Максимальная длина строки, заданной структурой [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="d8a66-130">The maximum length of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**максстрингленгсинбитес**</span><span class="sxs-lookup"><span data-stu-id="d8a66-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-132">(Максстрингленгс + 1) \* sizeof (WCHAR)</span><span class="sxs-lookup"><span data-stu-id="d8a66-132">(maxStringLength + 1) \* sizeof(WCHAR)</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-133">Максимальная длина строки в байтах, заданной структурой [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="d8a66-133">The maximum length, in bytes, of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**макссистемхеалсентитикаунт**</span><span class="sxs-lookup"><span data-stu-id="d8a66-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-135">0x14</span><span class="sxs-lookup"><span data-stu-id="d8a66-135">0x14</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-136">Максимальное число сущностей работоспособности системы, таких как SHV и SHA.</span><span class="sxs-lookup"><span data-stu-id="d8a66-136">The maximum number of system health entities, such as SHVs and SHAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**системхеалсентитикаунт**</span><span class="sxs-lookup"><span data-stu-id="d8a66-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-138">\[диапазон (0, Макссистемхеалсентитикаунт)\]</span><span class="sxs-lookup"><span data-stu-id="d8a66-138">\[range(0, maxSystemHealthEntityCount)\]</span></span> 
</dt> <dt>



<span data-ttu-id="d8a66-139">Диапазон возможных значений для числа сущностей работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="d8a66-139">The range of possible values for the number of system health entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**максенфорцеркаунт**</span><span class="sxs-lookup"><span data-stu-id="d8a66-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-141">0x14</span><span class="sxs-lookup"><span data-stu-id="d8a66-141">0x14</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-142">Максимальное число сущностей принудительного применения, например кекс.</span><span class="sxs-lookup"><span data-stu-id="d8a66-142">The maximum number of enforcement entities, such as QECs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**енфорцементентитикаунт**</span><span class="sxs-lookup"><span data-stu-id="d8a66-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-144">\[диапазон (0, Максенфорцеркаунт)\]</span><span class="sxs-lookup"><span data-stu-id="d8a66-144">\[range(0, maxEnforcerCount)\]</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-145">Диапазон возможных значений для числа сущностей принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="d8a66-145">The range of possible values for the number of enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**максприватедатасизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-147">0xC8</span><span class="sxs-lookup"><span data-stu-id="d8a66-147">0xC8</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-148">Максимальный размер (в байтах) структуры [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .</span><span class="sxs-lookup"><span data-stu-id="d8a66-148">The maximum size, in bytes, of a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**максконнектионкаунтперенфорцер**</span><span class="sxs-lookup"><span data-stu-id="d8a66-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-150">0x14</span><span class="sxs-lookup"><span data-stu-id="d8a66-150">0x14</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-151">Максимальное число объектов [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) , связанных с сущностью принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="d8a66-151">The maximum number of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) objects associated with an enforcement entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**макскачедсохкаунт**</span><span class="sxs-lookup"><span data-stu-id="d8a66-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-153">Макссистемхеалсентитикаунт \* максенфорцеркаунт \* максконнектионкаунтперенфорцер</span><span class="sxs-lookup"><span data-stu-id="d8a66-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-154">Максимальное количество кэшированных подключений SoH для всех сущностей работоспособности и принудительного применения системы.</span><span class="sxs-lookup"><span data-stu-id="d8a66-154">The maximum number of cached SoH connections for all system health and enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**фрешсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="d8a66-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-156">0x1</span><span class="sxs-lookup"><span data-stu-id="d8a66-156">0x1</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-157">Указывает, что [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-networksoh)из-за нового запроса, а не кэшированного запроса.</span><span class="sxs-lookup"><span data-stu-id="d8a66-157">Specifies that an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)is due to a new request, not a cached request.</span></span> <span data-ttu-id="d8a66-158">Этот флаг используется агентом NAP для объекта [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="d8a66-158">This flag is used by the NAP agent on an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**шафиксуп**</span><span class="sxs-lookup"><span data-stu-id="d8a66-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-160">0x1</span><span class="sxs-lookup"><span data-stu-id="d8a66-160">0x1</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-161">Указывает, что требуется исправление.</span><span class="sxs-lookup"><span data-stu-id="d8a66-161">Specifies that fix-up is required.</span></span> <span data-ttu-id="d8a66-162">Этот флаг используется SHA.</span><span class="sxs-lookup"><span data-stu-id="d8a66-162">This flag is used by a SHA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**фаилурекатегорикаунт**</span><span class="sxs-lookup"><span data-stu-id="d8a66-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-164">0x5</span><span class="sxs-lookup"><span data-stu-id="d8a66-164">0x5</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-165">Число категорий сбоев, содержащихся в структуре [**фаилурекатегоримаппинг**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="d8a66-165">The number of failure categories contained within a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**компоненттипинфорцементклиентсох**</span><span class="sxs-lookup"><span data-stu-id="d8a66-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-167">0x1</span><span class="sxs-lookup"><span data-stu-id="d8a66-167">0x1</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-168">Компонент является клиентом принудительного применения карантина (Кек), который отправляет пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) во время проверки подлинности подключения.</span><span class="sxs-lookup"><span data-stu-id="d8a66-168">The component is a quarantine enforcement client (QEC) that sends an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet in-band during connection authentication.</span></span>

> [!Note]  
> <span data-ttu-id="d8a66-169">Это значение не используется SHA и SHV.</span><span class="sxs-lookup"><span data-stu-id="d8a66-169">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**компоненттипинфорцементклиентрп**</span><span class="sxs-lookup"><span data-stu-id="d8a66-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-171">0x2</span><span class="sxs-lookup"><span data-stu-id="d8a66-171">0x2</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-172">Компонент — это Кек, который реализует [**инапцертрелингпарти**](inapcertrelyingparty.md) и должен взаимодействовать с сервером сертификатов работоспособности (HCS) для получения сертификата работоспособности.</span><span class="sxs-lookup"><span data-stu-id="d8a66-172">The component is a QEC that implements [**INapCertRelyingParty**](inapcertrelyingparty.md) and must interact with the Health Certificate Server (HCS) in order to obtain a health certificate.</span></span>

> [!Note]  
> <span data-ttu-id="d8a66-173">Это значение не используется SHA и SHV.</span><span class="sxs-lookup"><span data-stu-id="d8a66-173">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> </dl>

<span data-ttu-id="d8a66-174">Следующие константы NAP определены в Напенфорцементклиент. h.</span><span class="sxs-lookup"><span data-stu-id="d8a66-174">The following NAP constants are defined in NapEnforcementClient.h.</span></span>

<dl> <dt>

<span data-ttu-id="d8a66-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**дефаултпротоколмакссизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-176">0x0FA0</span><span class="sxs-lookup"><span data-stu-id="d8a66-176">0x0FA0</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-177">Максимальный размер пакета SoH (в байтах) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8a66-177">The default maximum size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**макспротоколмакссизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-179">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="d8a66-179">0xFFFF</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-180">Максимальный возможный размер пакета SoH в байтах.</span><span class="sxs-lookup"><span data-stu-id="d8a66-180">The maximum possible size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**минпротоколмакссизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-182">0x012C</span><span class="sxs-lookup"><span data-stu-id="d8a66-182">0x012C</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-183">Наименьший возможный максимальный размер пакета SoH в байтах.</span><span class="sxs-lookup"><span data-stu-id="d8a66-183">The smallest possible maximum size, in bytes, of an SoH packet.</span></span> <span data-ttu-id="d8a66-184">Фактический размер пакета SoH может быть меньше **минпротоколмакссизе**.</span><span class="sxs-lookup"><span data-stu-id="d8a66-184">The actual size of the SoH packet may be smaller than **minProtocolMaxSize**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8a66-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**протоколмакссизе**</span><span class="sxs-lookup"><span data-stu-id="d8a66-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8a66-186">Range (Минпротоколмакссизе, Макспротоколмакссизе)</span><span class="sxs-lookup"><span data-stu-id="d8a66-186">range(minProtocolMaxSize, maxProtocolMaxSize)</span></span>
</dt> <dt>



<span data-ttu-id="d8a66-187">Диапазон возможных значений для максимального размера пакета SoH.</span><span class="sxs-lookup"><span data-stu-id="d8a66-187">The range of possible values for the maximum size of a SoH packet.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8a66-188">Требования</span><span class="sxs-lookup"><span data-stu-id="d8a66-188">Requirements</span></span>



| <span data-ttu-id="d8a66-189">Требование</span><span class="sxs-lookup"><span data-stu-id="d8a66-189">Requirement</span></span> | <span data-ttu-id="d8a66-190">Значение</span><span class="sxs-lookup"><span data-stu-id="d8a66-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a66-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8a66-191">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a66-192">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8a66-192">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="d8a66-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8a66-193">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a66-194">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8a66-194">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="d8a66-195">Header</span><span class="sxs-lookup"><span data-stu-id="d8a66-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8a66-196"><dt>Наптипес. h; </dt> <dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8a66-196"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a66-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8a66-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a66-198">**Константы NAP**</span><span class="sxs-lookup"><span data-stu-id="d8a66-198">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





