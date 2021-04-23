---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_WINSType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса службы Windows Internet Name Service (WINS).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_WINSType
- DNS класса MicrosoftDNS_WINSType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802836"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="37bad-106">Метод Креатеинстанцефромпропертидата \_ класса Винстипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="37bad-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="37bad-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса службы Windows Internet Name Service (WINS).</span><span class="sxs-lookup"><span data-stu-id="37bad-107">The **CreateInstanceFromPropertyData** method instantiates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="37bad-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37bad-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="37bad-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="37bad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37bad-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37bad-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="37bad-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="37bad-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37bad-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="37bad-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="37bad-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37bad-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="37bad-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="37bad-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="37bad-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="37bad-117">Class of the RR.</span></span> <span data-ttu-id="37bad-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="37bad-118">Default value is 1.</span></span> <span data-ttu-id="37bad-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="37bad-119">The following values are valid.</span></span>



| <span data-ttu-id="37bad-120">Значение</span><span class="sxs-lookup"><span data-stu-id="37bad-120">Value</span></span>                                                                                                | <span data-ttu-id="37bad-121">Значение</span><span class="sxs-lookup"><span data-stu-id="37bad-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="37bad-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="37bad-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="37bad-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="37bad-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="37bad-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="37bad-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="37bad-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="37bad-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="37bad-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="37bad-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="37bad-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="37bad-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="37bad-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="37bad-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="37bad-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="37bad-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="37bad-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="37bad-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="37bad-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="37bad-132">*Маппингфлаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37bad-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-133">Флаг сопоставления WINS, указывающий, следует ли включать запись в репликацию зоны.</span><span class="sxs-lookup"><span data-stu-id="37bad-133">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="37bad-134">Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно.</span><span class="sxs-lookup"><span data-stu-id="37bad-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="37bad-135">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="37bad-135">The following values are valid.</span></span>



| <span data-ttu-id="37bad-136">Значение</span><span class="sxs-lookup"><span data-stu-id="37bad-136">Value</span></span>                                                                                                                                               | <span data-ttu-id="37bad-137">Значение</span><span class="sxs-lookup"><span data-stu-id="37bad-137">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="37bad-138"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="37bad-138"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="37bad-139">Флаг репликации</span><span class="sxs-lookup"><span data-stu-id="37bad-139">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="37bad-140"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="37bad-140"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="37bad-141">Флаг отсутствия репликации (локальная запись)</span><span class="sxs-lookup"><span data-stu-id="37bad-141">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37bad-142">*Лукуптимеаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37bad-142">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-143">Время в секундах, в течение которого DNS-сервер пытается выполнить разрешение с помощью поиска WINS.</span><span class="sxs-lookup"><span data-stu-id="37bad-143">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="37bad-144">*CacheTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37bad-144">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-145">Время в секундах, в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="37bad-145">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="37bad-146">*Винссерверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37bad-146">*WinsServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-147">Список разделенных запятыми IP-адресов WINS-серверов, используемых при поиске WINS.</span><span class="sxs-lookup"><span data-stu-id="37bad-147">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="37bad-148">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="37bad-148">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="37bad-149">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="37bad-149">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37bad-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37bad-150">Return value</span></span>

<span data-ttu-id="37bad-151">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="37bad-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="37bad-152">Требования</span><span class="sxs-lookup"><span data-stu-id="37bad-152">Requirements</span></span>



| <span data-ttu-id="37bad-153">Требование</span><span class="sxs-lookup"><span data-stu-id="37bad-153">Requirement</span></span> | <span data-ttu-id="37bad-154">Значение</span><span class="sxs-lookup"><span data-stu-id="37bad-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37bad-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37bad-155">Minimum supported client</span></span><br/> | <span data-ttu-id="37bad-156">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="37bad-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="37bad-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37bad-157">Minimum supported server</span></span><br/> | <span data-ttu-id="37bad-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="37bad-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="37bad-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="37bad-159">Namespace</span></span><br/>                | <span data-ttu-id="37bad-160">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="37bad-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="37bad-161">MOF</span><span class="sxs-lookup"><span data-stu-id="37bad-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37bad-162"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37bad-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37bad-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37bad-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37bad-164">**Микрософтднс \_ винстипе**</span><span class="sxs-lookup"><span data-stu-id="37bad-164">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="37bad-165">**Метод Modify \_ класса микрософтднс винстипе**</span><span class="sxs-lookup"><span data-stu-id="37bad-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="37bad-166">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="37bad-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





