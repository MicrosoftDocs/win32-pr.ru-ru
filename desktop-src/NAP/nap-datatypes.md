---
title: Типы защиты доступа к сети (Наптипес. h)
description: Примечание. Платформа защиты доступа к сети недоступна начиная с Windows 10 типы данными для API защиты доступа к сети (NAP) приведены ниже.
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- пробатионтиме
- протоколмакссизе
- напкомпонентид
- системхеалсентитид
- енфорцементентитид
- системхеалсентитикаунт
- енфорцементентитикаунт
- стрингкоррелатионид
- ConnectionId
- Процент
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989153"
---
# <a name="nap-datatypes"></a><span data-ttu-id="e6c6f-114">Типы типов защиты доступа к сети</span><span class="sxs-lookup"><span data-stu-id="e6c6f-114">NAP Datatypes</span></span>

> [!Note]  
> <span data-ttu-id="e6c6f-115">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e6c6f-115">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e6c6f-116">Для API защиты доступа к сети (NAP) доступны следующие типы типов:</span><span class="sxs-lookup"><span data-stu-id="e6c6f-116">The datatypes for the Network Access Protection (NAP) API are as follows.</span></span>


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

<span data-ttu-id="e6c6f-117">**пробатионтиме**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-117">**ProbationTime**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-118">Структура [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , которая содержит время, относящееся к надзору на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-118">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains a time related to a client machine's probation.</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-119">**протоколмакссизе**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-119">**ProtocolMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-120">Значение, указывающее диапазон возможных значений для максимального размера пакета [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) в байтах, определенного диапазоном ([**минпротоколмакссизе, макспротоколмакссизе**](nap-type-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="e6c6f-120">A value that specifies the range of possible values for the maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet as defined by range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-121">**напкомпонентид**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-121">**NapComponentId**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-122">Уникальный 4-байтовый идентификатор, используемый SHA, SHV и клиенты принудительного применения для самостоятельной идентификации.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-122">A unique 4-byte identifier used by SHAs, SHVs and enforcement clients to identify themselves.</span></span> <span data-ttu-id="e6c6f-123">Первые три байта — это код SMI поставщика, назначенный IETF, а последний байт идентифицирует сам компонент.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-123">The first three bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-124">**системхеалсентитид**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-124">**SystemHealthEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-125">Значение **напкомпонентид** , используемое для распознавания пар SHA/SHV.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-125">A **NapComponentId** value used to identify SHA/SHV pairs.</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-126">**енфорцементентитид**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-126">**EnforcementEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-127">Значение **напкомпонентид** , используемое для распознавания клиентов принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-127">A **NapComponentId** value used to identify enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-128">**системхеалсентитикаунт**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-128">**SystemHealthEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-129">Значение, указывающее число зарегистрированных SHA в системе защиты доступа к сети в диапазоне 0 (ноль) до [**макссистемхеалсентитикаунт**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e6c6f-129">A value that specifies the number of registered SHAs in the NAP system in the range 0 (zero) to [**maxSystemHealthEntityCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-130">**енфорцементентитикаунт**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-130">**EnforcementEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-131">Значение, указывающее число клиентов принудительного применения в системе защиты доступа к сети в диапазоне 0 (ноль) до [**максенфорцеркаунт**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e6c6f-131">A value that specifies the number of enforcement clients in the NAP system in the range 0 (zero) to [**maxEnforcerCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-132">**стрингкоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-132">**StringCorrelationId**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-133">[**Каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) версия структуры [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) , используемая для связывания [**сохрекуестс**](/windows/win32/api/naptypes/ns-naptypes-soh) с **сохреспонсес**.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-133">The [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) version of a [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure used to pair [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) to **SoHResponses**.</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-134">**ConnectionId**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-134">**ConnectionId**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-135">Уникальный глобальный уникальный идентификатор (GUID), используемый для идентификации подключений NAP, обслуживаемых клиентами принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-135">A unique Globally Unique Identifier (GUID) used to identify a NAP connections maintained by enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-136">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-136">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-137">Значение, содержащее процент от 0 (нуля) до 100 исправления, которое завершено</span><span class="sxs-lookup"><span data-stu-id="e6c6f-137">A value that contains the percentage between 0 (zero) and 100 of remediation that is complete</span></span>

</dd> <dt>

<span data-ttu-id="e6c6f-138">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-138">**MessageId**</span></span>
</dt> <dd>

<span data-ttu-id="e6c6f-139">Уникальное значение, используемое для распознавания системных сообщений NAP.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-139">A unique value used to identify NAP system messages.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6c6f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="e6c6f-140">Requirements</span></span>



| <span data-ttu-id="e6c6f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="e6c6f-141">Requirement</span></span> | <span data-ttu-id="e6c6f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="e6c6f-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c6f-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6c6f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c6f-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6c6f-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="e6c6f-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6c6f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c6f-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6c6f-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="e6c6f-147">Header</span><span class="sxs-lookup"><span data-stu-id="e6c6f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c6f-148"><dt>Наптипес. h; </dt> <dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c6f-148"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



 

