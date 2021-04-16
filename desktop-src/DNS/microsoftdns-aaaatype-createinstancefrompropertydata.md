---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_AAAAType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса IPv6-адреса (AAAA).
ms.assetid: 3f2774d8-1eb6-4300-95e2-f918fc6612e0
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_AAAAType
- DNS класса MicrosoftDNS_AAAAType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9232506b52795521300e827701f685e351d8ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534169"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="a1362-106">Метод Креатеинстанцефромпропертидата \_ класса Аааатипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="a1362-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="a1362-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса IPv6-адреса (AAAA).</span><span class="sxs-lookup"><span data-stu-id="a1362-107">The **CreateInstanceFromPropertyData** method instantiates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1362-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1362-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a1362-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1362-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1362-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1362-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1362-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1362-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a1362-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1362-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1362-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1362-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a1362-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1362-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1362-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1362-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a1362-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a1362-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1362-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1362-117">Class of the RR.</span></span> <span data-ttu-id="a1362-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="a1362-118">Default value is 1.</span></span> <span data-ttu-id="a1362-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a1362-119">The following values are valid.</span></span>



| <span data-ttu-id="a1362-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a1362-120">Value</span></span>                                                                                                | <span data-ttu-id="a1362-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a1362-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a1362-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a1362-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a1362-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="a1362-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="a1362-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a1362-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a1362-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="a1362-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="a1362-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="a1362-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a1362-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="a1362-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="a1362-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="a1362-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a1362-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="a1362-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a1362-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a1362-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1362-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="a1362-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a1362-132">*IPv6Address* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1362-132">*IPv6Address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1362-133">IPv6-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="a1362-133">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="a1362-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="a1362-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a1362-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="a1362-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1362-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1362-136">Return value</span></span>

<span data-ttu-id="a1362-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a1362-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1362-138">Требования</span><span class="sxs-lookup"><span data-stu-id="a1362-138">Requirements</span></span>



| <span data-ttu-id="a1362-139">Требование</span><span class="sxs-lookup"><span data-stu-id="a1362-139">Requirement</span></span> | <span data-ttu-id="a1362-140">Значение</span><span class="sxs-lookup"><span data-stu-id="a1362-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1362-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1362-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a1362-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a1362-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a1362-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1362-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a1362-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1362-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a1362-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a1362-145">Namespace</span></span><br/>                | <span data-ttu-id="a1362-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="a1362-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a1362-147">MOF</span><span class="sxs-lookup"><span data-stu-id="a1362-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1362-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1362-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1362-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1362-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1362-150">**Микрософтднс \_ аааатипе**</span><span class="sxs-lookup"><span data-stu-id="a1362-150">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="a1362-151">**Метод Modify \_ класса микрософтднс аааатипе**</span><span class="sxs-lookup"><span data-stu-id="a1362-151">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="a1362-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="a1362-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





