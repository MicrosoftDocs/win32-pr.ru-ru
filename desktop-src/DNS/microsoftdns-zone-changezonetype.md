---
title: Метод Чанжезонетипе класса MicrosoftDNS_Zone
description: Метод Чанжезонетипе изменяет тип зоны.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- DNS-метод Чанжезонетипе
- Чанжезонетипе метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Чанжезонетипе
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071502"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="060e0-106">Метод Чанжезонетипе \_ класса зоны микрософтднс</span><span class="sxs-lookup"><span data-stu-id="060e0-106">ChangeZoneType method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="060e0-107">Метод **чанжезонетипе** изменяет тип зоны.</span><span class="sxs-lookup"><span data-stu-id="060e0-107">The **ChangeZoneType** method changes the type of a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="060e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="060e0-108">Syntax</span></span>


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="060e0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="060e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060e0-110">*ZoneType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="060e0-110">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060e0-111">Тип зоны.</span><span class="sxs-lookup"><span data-stu-id="060e0-111">Type of zone.</span></span> <span data-ttu-id="060e0-112">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="060e0-112">Valid values are the following:</span></span>



| <span data-ttu-id="060e0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="060e0-113">Value</span></span>                                                                        | <span data-ttu-id="060e0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="060e0-114">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="060e0-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="060e0-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="060e0-116">Основная зона.</span><span class="sxs-lookup"><span data-stu-id="060e0-116">Primary zone.</span></span><br/>   |
| <dl> <span data-ttu-id="060e0-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="060e0-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="060e0-118">Дополнительная зона.</span><span class="sxs-lookup"><span data-stu-id="060e0-118">Secondary zone.</span></span><br/> |
| <dl> <span data-ttu-id="060e0-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="060e0-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="060e0-120">Зона-заглушка.</span><span class="sxs-lookup"><span data-stu-id="060e0-120">Stub zone.</span></span><br/>      |
| <dl> <span data-ttu-id="060e0-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="060e0-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="060e0-122">Сервер пересылки зоны.</span><span class="sxs-lookup"><span data-stu-id="060e0-122">Zone forwarder.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="060e0-123">*Имя файла* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="060e0-123">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="060e0-124">Имя файла данных, связанного с зоной.</span><span class="sxs-lookup"><span data-stu-id="060e0-124">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="060e0-125">*Reduce* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="060e0-125">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="060e0-126">IP-адрес DNS-сервера главном для зоны.</span><span class="sxs-lookup"><span data-stu-id="060e0-126">IP address of the mater DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="060e0-127">*Админемаилнаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="060e0-127">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="060e0-128">Адрес электронной почты администратора, ответственного за зону.</span><span class="sxs-lookup"><span data-stu-id="060e0-128">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="060e0-129">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="060e0-129">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="060e0-130">RR типа **микрософтднс \_ Zone**.</span><span class="sxs-lookup"><span data-stu-id="060e0-130">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060e0-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="060e0-131">Return value</span></span>

<span data-ttu-id="060e0-132">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="060e0-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="060e0-133">Требования</span><span class="sxs-lookup"><span data-stu-id="060e0-133">Requirements</span></span>



| <span data-ttu-id="060e0-134">Требование</span><span class="sxs-lookup"><span data-stu-id="060e0-134">Requirement</span></span> | <span data-ttu-id="060e0-135">Значение</span><span class="sxs-lookup"><span data-stu-id="060e0-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="060e0-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="060e0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="060e0-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="060e0-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="060e0-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="060e0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="060e0-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="060e0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="060e0-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="060e0-140">Namespace</span></span><br/>                | <span data-ttu-id="060e0-141">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="060e0-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="060e0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="060e0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="060e0-143"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="060e0-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="060e0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="060e0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060e0-145">**\_Зона микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-145">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="060e0-146">**Метод Ажеаллрекордс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-146">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="060e0-147">**Метод Креатезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-147">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="060e0-148">**Метод Форцерефреш \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-148">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="060e0-149">**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-149">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="060e0-150">**Метод Паусезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-150">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="060e0-151">**Метод Релоадзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-151">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="060e0-152">**Метод Ресетсекондариес \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-152">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="060e0-153">**Метод Ресумезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-153">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="060e0-154">**Метод Упдатефромдс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-154">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="060e0-155">**Метод Вритебаккзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="060e0-155">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





