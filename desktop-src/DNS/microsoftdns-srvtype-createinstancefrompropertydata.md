---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_SRVType
description: Метод Креатеинстанцефромпропертидата создает запись ресурса службы (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_SRVType
- DNS класса MicrosoftDNS_SRVType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803688"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="f6605-106">Метод Креатеинстанцефромпропертидата \_ класса Срвтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f6605-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="f6605-107">Метод **креатеинстанцефромпропертидата** создает запись ресурса службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="f6605-107">The **CreateInstanceFromPropertyData** method instantiates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6605-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6605-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f6605-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6605-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6605-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6605-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6605-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6605-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6605-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6605-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6605-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f6605-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6605-117">Class of the RR.</span></span> <span data-ttu-id="f6605-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="f6605-118">Default value is 1.</span></span> <span data-ttu-id="f6605-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f6605-119">The following values are valid.</span></span>



| <span data-ttu-id="f6605-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f6605-120">Value</span></span>                                                                                                | <span data-ttu-id="f6605-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f6605-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f6605-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f6605-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f6605-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="f6605-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f6605-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f6605-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f6605-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="f6605-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f6605-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="f6605-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f6605-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="f6605-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f6605-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="f6605-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f6605-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="f6605-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f6605-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f6605-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="f6605-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-132">*Приоритет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6605-132">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-133">Приоритет целевого узла, указанного в имени владельца.</span><span class="sxs-lookup"><span data-stu-id="f6605-133">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="f6605-134">Более низкие значения подразумевают более высокие приоритеты.</span><span class="sxs-lookup"><span data-stu-id="f6605-134">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-135">*Вес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6605-135">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-136">Вес целевого узла.</span><span class="sxs-lookup"><span data-stu-id="f6605-136">Weight of the target host.</span></span> <span data-ttu-id="f6605-137">Это полезно при выборе между узлами с одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="f6605-137">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="f6605-138">Вероятность использования этого узла должна быть пропорциональна его весу.</span><span class="sxs-lookup"><span data-stu-id="f6605-138">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-139">*Порт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6605-139">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-140">Порт, используемый на целевом узле службы протокола.</span><span class="sxs-lookup"><span data-stu-id="f6605-140">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-141">*Срвдомаиннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6605-141">*SRVDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-142">Полное доменное имя целевого узла.</span><span class="sxs-lookup"><span data-stu-id="f6605-142">FQDN of the target host.</span></span> <span data-ttu-id="f6605-143">Целевой объект \\ . \\ означает, что служба не будет доступна в этом домене.</span><span class="sxs-lookup"><span data-stu-id="f6605-143">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="f6605-144">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="f6605-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f6605-145">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="f6605-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6605-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6605-146">Return value</span></span>

<span data-ttu-id="f6605-147">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f6605-147">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6605-148">Требования</span><span class="sxs-lookup"><span data-stu-id="f6605-148">Requirements</span></span>



| <span data-ttu-id="f6605-149">Требование</span><span class="sxs-lookup"><span data-stu-id="f6605-149">Requirement</span></span> | <span data-ttu-id="f6605-150">Значение</span><span class="sxs-lookup"><span data-stu-id="f6605-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6605-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6605-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f6605-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6605-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6605-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6605-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f6605-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6605-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6605-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6605-155">Namespace</span></span><br/>                | <span data-ttu-id="f6605-156">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f6605-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f6605-157">MOF</span><span class="sxs-lookup"><span data-stu-id="f6605-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6605-158"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6605-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6605-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6605-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6605-160">**Микрософтднс \_ срвтипе**</span><span class="sxs-lookup"><span data-stu-id="f6605-160">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="f6605-161">**Метод Modify \_ класса микрософтднс срвтипе**</span><span class="sxs-lookup"><span data-stu-id="f6605-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="f6605-162">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="f6605-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





