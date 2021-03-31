---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_WINSRType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса обратного просмотра WINS (WINSR).
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_WINSRType
- DNS класса MicrosoftDNS_WINSRType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c35863e00ace6c0772383604d0fbdfd7915cd02c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136599"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="dd2e5-106">Метод Креатеинстанцефромпропертидата \_ класса Винсртипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="dd2e5-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="dd2e5-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса обратного просмотра WINS (WINSR).</span><span class="sxs-lookup"><span data-stu-id="dd2e5-107">The **CreateInstanceFromPropertyData** method instantiates a WINS Reverse Lookup (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2e5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd2e5-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="dd2e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd2e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2e5-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-117">Class of the RR.</span></span> <span data-ttu-id="dd2e5-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-118">Default value is 1.</span></span> <span data-ttu-id="dd2e5-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-119">The following values are valid.</span></span>



| <span data-ttu-id="dd2e5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dd2e5-120">Value</span></span>                                                                                                | <span data-ttu-id="dd2e5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dd2e5-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="dd2e5-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2e5-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dd2e5-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="dd2e5-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="dd2e5-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2e5-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dd2e5-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="dd2e5-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="dd2e5-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2e5-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dd2e5-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="dd2e5-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="dd2e5-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="dd2e5-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dd2e5-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="dd2e5-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="dd2e5-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-132">*Маппингфлаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-133">Флаг сопоставления WINSR, указывающий, следует ли включать запись в репликацию зоны.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-133">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="dd2e5-134">Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-135">*Лукуптимеаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-135">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-136">Время ожидания (в секундах) для DNS-сервера, использующего обратный поиск WINS.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-136">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-137">*CacheTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-137">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-138">Время (в секундах), в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-138">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-139">*Ресултдомаин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-139">*ResultDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-140">Имя домена, добавляемое к возвращенным NetBIOS-именам.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-140">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="dd2e5-141">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-141">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2e5-142">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-142">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd2e5-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd2e5-143">Return value</span></span>

<span data-ttu-id="dd2e5-144">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dd2e5-144">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2e5-145">Требования</span><span class="sxs-lookup"><span data-stu-id="dd2e5-145">Requirements</span></span>



| <span data-ttu-id="dd2e5-146">Требование</span><span class="sxs-lookup"><span data-stu-id="dd2e5-146">Requirement</span></span> | <span data-ttu-id="dd2e5-147">Значение</span><span class="sxs-lookup"><span data-stu-id="dd2e5-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2e5-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd2e5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2e5-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd2e5-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dd2e5-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd2e5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2e5-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd2e5-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dd2e5-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd2e5-152">Namespace</span></span><br/>                | <span data-ttu-id="dd2e5-153">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="dd2e5-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dd2e5-154">MOF</span><span class="sxs-lookup"><span data-stu-id="dd2e5-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd2e5-155"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd2e5-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2e5-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd2e5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2e5-157">**Микрософтднс \_ винсртипе**</span><span class="sxs-lookup"><span data-stu-id="dd2e5-157">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="dd2e5-158">**Метод Modify \_ класса микрософтднс винсртипе**</span><span class="sxs-lookup"><span data-stu-id="dd2e5-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="dd2e5-159">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="dd2e5-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





