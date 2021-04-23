---
title: Метод Ажеаллрекордс класса MicrosoftDNS_Zone
description: Метод Ажеаллрекордс включает устаревание для некоторых или всех записей, отличных от NS и не являющихся SOA, в зоне.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- DNS-метод Ажеаллрекордс
- Ажеаллрекордс метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Ажеаллрекордс
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492369"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="d7b5c-106">Метод Ажеаллрекордс \_ класса зоны микрософтднс</span><span class="sxs-lookup"><span data-stu-id="d7b5c-106">AgeAllRecords method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="d7b5c-107">Метод **ажеаллрекордс** включает устаревание для некоторых или всех записей, отличных от NS и не являющихся SOA, в зоне.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-107">The **AgeAllRecords** method enables aging for some or all non-NS and non-SOA records in a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b5c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b5c-108">Syntax</span></span>


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a><span data-ttu-id="d7b5c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7b5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b5c-110">*NodeName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d7b5c-110">*NodeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b5c-111">Имя узла, которому будет присвоено значение Age.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-111">Name of the node to age.</span></span>

</dd> <dt>

<span data-ttu-id="d7b5c-112">*Апплитосубтри* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d7b5c-112">*ApplyToSubtree* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b5c-113">Указывает, следует ли применять устаревание ко всем записям в поддереве.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-113">Specifies whether aging should apply to all records in the subtree.</span></span> <span data-ttu-id="d7b5c-114">Задайте значение TRUE, чтобы применить устаревание ко всем записям в поддереве, начиная с NodeName.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-114">Set to TRUE to apply aging to all records in the subtree, beginning with NodeName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b5c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7b5c-115">Return value</span></span>

<span data-ttu-id="d7b5c-116">Ошибка \_ указывает, что устаревание успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-116">ERROR\_SUCCESS indicates the aging was successfully completed.</span></span> <span data-ttu-id="d7b5c-117">Любое другое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-117">Any other value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7b5c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7b5c-118">Remarks</span></span>

<span data-ttu-id="d7b5c-119">Если значение *nodeName* не указано, все записи будут подвергаться старению и очистке.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-119">If *NodeName* is not specified, all records will be subject to aging and scavenging.</span></span>

<span data-ttu-id="d7b5c-120">Если указан параметр *nodeName* и параметр *апплитосубтри* не задан или равен нулю, записи на указанном узле будут подвергаться старению и очистке.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-120">If *NodeName* is specified and *ApplyToSubtree* is not specified or set to zero, records at the specified node will be subjected to aging and scavenging.</span></span>

<span data-ttu-id="d7b5c-121">Если задан параметр *nodeName* и для *апплитосубтри* задано значение 1, то все записи поддерева, начинающиеся с *nodeName* , будут подвергаться старению и очистке.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-121">If *NodeName* is specified and *ApplyToSubtree* is set to 1, all records of the subtree starting at *NodeName* will be subjected to aging and scavenging.</span></span> <span data-ttu-id="d7b5c-122">В качестве метки времени задано текущее время для всех записей, не являющихся записями NS и не являющихся SOA, с именами владельцев, определяемыми входными параметрами.</span><span class="sxs-lookup"><span data-stu-id="d7b5c-122">The time stamp is set to the current time for all non-NS and non-SOA RRs with the owner name(s) identified by the input parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7b5c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d7b5c-123">Requirements</span></span>



| <span data-ttu-id="d7b5c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d7b5c-124">Requirement</span></span> | <span data-ttu-id="d7b5c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b5c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b5c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7b5c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b5c-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d7b5c-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d7b5c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7b5c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b5c-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7b5c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7b5c-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d7b5c-130">Namespace</span></span><br/>                | <span data-ttu-id="d7b5c-131">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="d7b5c-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d7b5c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d7b5c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7b5c-133"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7b5c-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b5c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7b5c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b5c-135">**\_Зона микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-135">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-136">**Метод Чанжезонетипе \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-136">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-137">**Метод Креатезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-137">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-138">**Метод Форцерефреш \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-138">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-139">**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-139">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-140">**Метод Паусезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-140">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-141">**Метод Релоадзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-141">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-142">**Метод Ресетсекондариес \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-142">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-143">**Метод Ресумезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-143">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-144">**Метод Упдатефромдс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-144">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="d7b5c-145">**Метод Вритебаккзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="d7b5c-145">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





