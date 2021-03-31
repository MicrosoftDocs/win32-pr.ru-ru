---
title: Метод Modify класса MicrosoftDNS_SOAType
description: Метод Modify обновляет запись ресурса начальной записи зоны (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_SOAType класс
- MicrosoftDNS_SOAType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071243"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a><span data-ttu-id="8fec1-106">Метод Modify \_ класса микрософтднс соатипе</span><span class="sxs-lookup"><span data-stu-id="8fec1-106">Modify method of the MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="8fec1-107">Метод **Modify** обновляет запись ресурса начальной записи зоны (SOA).</span><span class="sxs-lookup"><span data-stu-id="8fec1-107">The **Modify** method updates a Start Of Authority (SOA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fec1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fec1-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8fec1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fec1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fec1-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="8fec1-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-112">*Серийный* \[ номер в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-112">*SerialNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-113">Серийный номер SOA, представляющий количество обновлений зоны, используемых [*серверами-получателями*](s-gly.md) для определения необходимости передачи зоны.</span><span class="sxs-lookup"><span data-stu-id="8fec1-113">SOA serial number representing the number of times the zone has been updated, used by [*secondary servers*](s-gly.md) to determine whether zone transfer is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-114">*Сервер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-114">*PrimaryServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-115">Имя сервера источника.</span><span class="sxs-lookup"><span data-stu-id="8fec1-115">Name of the primary server.</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-116">*Респонсиблепарти* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-116">*ResponsibleParty* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-117">Адрес почтового ящика ответственного лица в виде псевдонима. домен, например xyz.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8fec1-117">Mailbox address of the responsible party, in the form of alias.domain, such as xyz.microsoft.com.</span></span> <span data-ttu-id="8fec1-118">Обратите внимание на использование точки, а не символа @.</span><span class="sxs-lookup"><span data-stu-id="8fec1-118">Note the use of a period rather than an at symbol (@).</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-119">*RefreshInterval* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-119">*RefreshInterval* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-120">Время в секундах до обновления зоны, содержащей эту запись.</span><span class="sxs-lookup"><span data-stu-id="8fec1-120">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-121">*Ретриделай* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-121">*RetryDelay* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-122">Время в секундах, в течение которого DNS-сервер должен откладывать задержку между попытками разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="8fec1-122">Time, in seconds, the DNS Server should delay between name resolution attempts.</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-123">*Експирелимит* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-123">*ExpireLimit* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-124">Время в секундах, в течение которого серверы-получатели должны ожидать ответа от сервера-источника, прежде чем отменять их копии файла зоны как недопустимые.</span><span class="sxs-lookup"><span data-stu-id="8fec1-124">Time, in seconds, that secondary servers should wait for a response from the primary server before discarding their copies of the zone file as invalid.</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-125">*Минимумттл* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-125">*MinimumTTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-126">Время жизни (в секундах), применяемое к записям ресурсов в зоне, которые не указывают собственный срок жизни.</span><span class="sxs-lookup"><span data-stu-id="8fec1-126">TTL time, in seconds, applied to resource records in the zone that do not specify their own TTL.</span></span>

</dd> <dt>

<span data-ttu-id="8fec1-127">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-127">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8fec1-128">Ссылка на измененный объект</span><span class="sxs-lookup"><span data-stu-id="8fec1-128">Reference to the modified object</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fec1-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fec1-129">Return value</span></span>

<span data-ttu-id="8fec1-130">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8fec1-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fec1-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fec1-131">Remarks</span></span>

<span data-ttu-id="8fec1-132">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="8fec1-132">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fec1-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8fec1-133">Requirements</span></span>



| <span data-ttu-id="8fec1-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8fec1-134">Requirement</span></span> | <span data-ttu-id="8fec1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8fec1-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fec1-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fec1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8fec1-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8fec1-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8fec1-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fec1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8fec1-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8fec1-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8fec1-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8fec1-140">Namespace</span></span><br/>                | <span data-ttu-id="8fec1-141">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="8fec1-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8fec1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8fec1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fec1-143"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fec1-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fec1-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fec1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fec1-145">**Микрософтднс \_ соатипе**</span><span class="sxs-lookup"><span data-stu-id="8fec1-145">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)
</dt> <dt>

[<span data-ttu-id="8fec1-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="8fec1-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





