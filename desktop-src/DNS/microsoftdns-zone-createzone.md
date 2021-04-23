---
title: Метод Креатезоне класса MicrosoftDNS_Zone
description: Метод Креатезоне создает зону DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- DNS-метод Креатезоне
- Креатезоне метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Креатезоне
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071800"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="93d99-106">Метод Креатезоне \_ класса зоны микрософтднс</span><span class="sxs-lookup"><span data-stu-id="93d99-106">CreateZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="93d99-107">Метод **креатезоне** создает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="93d99-107">The **CreateZone** method creates a DNS zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d99-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93d99-108">Syntax</span></span>


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="93d99-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="93d99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d99-110">*Имя_зоны* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d99-110">*ZoneName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d99-111">Строка, представляющая имя зоны.</span><span class="sxs-lookup"><span data-stu-id="93d99-111">String representing the name of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="93d99-112">*ZoneType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d99-112">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d99-113">Тип зоны.</span><span class="sxs-lookup"><span data-stu-id="93d99-113">Type of zone.</span></span> <span data-ttu-id="93d99-114">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="93d99-114">Valid values are the following:</span></span>



| <span data-ttu-id="93d99-115">Значение</span><span class="sxs-lookup"><span data-stu-id="93d99-115">Value</span></span>                                                                        | <span data-ttu-id="93d99-116">Значение</span><span class="sxs-lookup"><span data-stu-id="93d99-116">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93d99-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="93d99-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="93d99-118">Интегрированная служба AD.</span><span class="sxs-lookup"><span data-stu-id="93d99-118">AD integrated.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="93d99-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93d99-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="93d99-120">Дополнительная зона.</span><span class="sxs-lookup"><span data-stu-id="93d99-120">Secondary zone.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="93d99-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="93d99-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="93d99-122">Зона-заглушка.</span><span class="sxs-lookup"><span data-stu-id="93d99-122">Stub zone.</span></span><br/> <span data-ttu-id="93d99-123">**Windows Server 2003:** Этот тип зоны появился в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="93d99-123">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/>      |
| <dl> <span data-ttu-id="93d99-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="93d99-124"><dt>4</dt></span></span> </dl> | <span data-ttu-id="93d99-125">Сервер пересылки зоны.</span><span class="sxs-lookup"><span data-stu-id="93d99-125">Zone forwarder.</span></span><br/> <span data-ttu-id="93d99-126">**Windows Server 2003:** Этот тип зоны появился в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="93d99-126">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="93d99-127">*Дсинтегратед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d99-127">*DsIntegrated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d99-128">Указывает, хранятся ли данные зоны в Active Directory или в файлах.</span><span class="sxs-lookup"><span data-stu-id="93d99-128">Indicates whether zone data is stored in the Active Directory or in files.</span></span> <span data-ttu-id="93d99-129">Если значение — TRUE, данные хранятся в Active Directory; Если значение равно FALSE, данные хранятся в файлах.</span><span class="sxs-lookup"><span data-stu-id="93d99-129">If TRUE, the data is stored in the Active Directory; if FALSE, the data is stored in files.</span></span>

</dd> <dt>

<span data-ttu-id="93d99-130">*Имя файла* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="93d99-130">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93d99-131">Имя файла данных, связанного с зоной.</span><span class="sxs-lookup"><span data-stu-id="93d99-131">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="93d99-132">*Reduce* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="93d99-132">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93d99-133">IP-адрес главного DNS-сервера зоны.</span><span class="sxs-lookup"><span data-stu-id="93d99-133">IP address of the master DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="93d99-134">*Админемаилнаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="93d99-134">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93d99-135">Адрес электронной почты администратора, ответственного за зону.</span><span class="sxs-lookup"><span data-stu-id="93d99-135">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="93d99-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="93d99-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="93d99-137">RR типа **микрософтднс \_ Zone**.</span><span class="sxs-lookup"><span data-stu-id="93d99-137">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d99-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93d99-138">Return value</span></span>

<span data-ttu-id="93d99-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="93d99-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="93d99-140">Требования</span><span class="sxs-lookup"><span data-stu-id="93d99-140">Requirements</span></span>



| <span data-ttu-id="93d99-141">Требование</span><span class="sxs-lookup"><span data-stu-id="93d99-141">Requirement</span></span> | <span data-ttu-id="93d99-142">Значение</span><span class="sxs-lookup"><span data-stu-id="93d99-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93d99-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93d99-143">Minimum supported client</span></span><br/> | <span data-ttu-id="93d99-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="93d99-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="93d99-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93d99-145">Minimum supported server</span></span><br/> | <span data-ttu-id="93d99-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="93d99-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="93d99-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93d99-147">Namespace</span></span><br/>                | <span data-ttu-id="93d99-148">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="93d99-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="93d99-149">MOF</span><span class="sxs-lookup"><span data-stu-id="93d99-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93d99-150"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93d99-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93d99-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93d99-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d99-152">**\_Зона микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-152">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="93d99-153">**Метод Ажеаллрекордс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-153">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="93d99-154">**Метод Чанжезонетипе \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-154">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="93d99-155">**Метод Форцерефреш \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-155">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="93d99-156">**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-156">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="93d99-157">**Метод Паусезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-157">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="93d99-158">**Метод Релоадзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-158">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="93d99-159">**Метод Ресетсекондариес \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-159">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="93d99-160">**Метод Ресумезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-160">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="93d99-161">**Метод Упдатефромдс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-161">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="93d99-162">**Метод Вритебаккзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="93d99-162">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





