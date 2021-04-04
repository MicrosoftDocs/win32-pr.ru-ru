---
title: Метод Ресетсекондариес класса MicrosoftDNS_Zone
description: Метод Ресетсекондариес сбрасывает IP-адреса для дополнительных DNS-серверов в зоне.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- DNS-метод Ресетсекондариес
- Ресетсекондариес метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Ресетсекондариес
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988974"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="d4f46-106">Метод Ресетсекондариес \_ класса зоны микрософтднс</span><span class="sxs-lookup"><span data-stu-id="d4f46-106">ResetSecondaries method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="d4f46-107">Метод **ресетсекондариес** сбрасывает IP-адреса для дополнительных DNS-серверов в зоне.</span><span class="sxs-lookup"><span data-stu-id="d4f46-107">The **ResetSecondaries** method resets the IP addresses for secondary DNS Servers in the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f46-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4f46-108">Syntax</span></span>


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d4f46-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4f46-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f46-110">*Секондарисерверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4f46-110">*SecondaryServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f46-111">Массив IP-адресов для дополнительных DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="d4f46-111">Array of IP addresses for secondary DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="d4f46-112">*Секуресекондариес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4f46-112">*SecureSecondaries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f46-113">Задает применяемый уровень безопасности и должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="d4f46-113">Specifies the security to be applied and must be one of the following:</span></span>

-   <span data-ttu-id="d4f46-114">ЗОНА \_ сексекуре \_ без \_ безопасности</span><span class="sxs-lookup"><span data-stu-id="d4f46-114">ZONE\_SECSECURE\_NO\_SECURITY</span></span>
-   <span data-ttu-id="d4f46-115">\_только зона сексекуре \_ NS \_</span><span class="sxs-lookup"><span data-stu-id="d4f46-115">ZONE\_SECSECURE\_NS\_ONLY</span></span>
-   <span data-ttu-id="d4f46-116">\_ \_ только список сексекуре \_ зоны</span><span class="sxs-lookup"><span data-stu-id="d4f46-116">ZONE\_SECSECURE\_LIST\_ONLY</span></span>
-   <span data-ttu-id="d4f46-117">ЗОНА \_ сексекуре \_ No \_ ксфр</span><span class="sxs-lookup"><span data-stu-id="d4f46-117">ZONE\_SECSECURE\_NO\_XFR</span></span>

</dd> <dt>

<span data-ttu-id="d4f46-118">*Нотифисерверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4f46-118">*NotifyServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f46-119">IP-адрес DNS-серверов для уведомления при изменении зоны.</span><span class="sxs-lookup"><span data-stu-id="d4f46-119">IP address of DNS Servers to be notified when the zone changes.</span></span>

</dd> <dt>

<span data-ttu-id="d4f46-120">*Уведомление* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4f46-120">*Notify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f46-121">Параметр уведомления и должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d4f46-121">Notification setting and must be one of the following:</span></span>

-   <span data-ttu-id="d4f46-122">\_уведомление зоны \_ отключено</span><span class="sxs-lookup"><span data-stu-id="d4f46-122">ZONE\_NOTIFY\_OFF</span></span>
-   <span data-ttu-id="d4f46-123">уведомление зоны для \_ \_ всех \_ получателей</span><span class="sxs-lookup"><span data-stu-id="d4f46-123">ZONE\_NOTIFY\_ALL\_SECONDARIES</span></span>
-   <span data-ttu-id="d4f46-124">\_только список уведомлений о зонах \_ \_</span><span class="sxs-lookup"><span data-stu-id="d4f46-124">ZONE\_NOTIFY\_LIST\_ONLY</span></span>

</dd> <dt>

<span data-ttu-id="d4f46-125">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="d4f46-125">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f46-126">RR типа [**микрософтднс \_ Zone**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="d4f46-126">RR of type [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f46-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4f46-127">Return value</span></span>

<span data-ttu-id="d4f46-128">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d4f46-128">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f46-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d4f46-129">Requirements</span></span>



| <span data-ttu-id="d4f46-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d4f46-130">Requirement</span></span> | <span data-ttu-id="d4f46-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d4f46-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f46-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4f46-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f46-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4f46-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d4f46-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4f46-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f46-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4f46-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d4f46-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d4f46-136">Namespace</span></span><br/>                | <span data-ttu-id="d4f46-137">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="d4f46-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d4f46-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d4f46-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4f46-139"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4f46-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f46-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4f46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f46-141">**\_Зона микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-141">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="d4f46-142">**Метод Ажеаллрекордс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-142">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="d4f46-143">**Метод Чанжезонетипе \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-143">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="d4f46-144">**Метод Креатезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-144">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="d4f46-145">**Метод Форцерефреш \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-145">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="d4f46-146">**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-146">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="d4f46-147">**Метод Паусезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-147">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="d4f46-148">**Метод Релоадзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-148">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="d4f46-149">**Метод Ресумезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-149">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="d4f46-150">**Метод Упдатефромдс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-150">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="d4f46-151">**Метод Вритебаккзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d4f46-151">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





