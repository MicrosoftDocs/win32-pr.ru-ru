---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_CNAMEType
description: Метод Креатеинстанцефромпропертидата создает запись ресурса канонического имени (CNAME).
ms.assetid: b5a5e14a-fb30-4cdf-90d0-7ef446350ac6
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_CNAMEType
- DNS класса MicrosoftDNS_CNAMEType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceb65a76002651e98dd8751e0a5c0c56aca3e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988659"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="32642-106">Метод Креатеинстанцефромпропертидата \_ класса Кнаметипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="32642-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="32642-107">Метод **креатеинстанцефромпропертидата** создает запись ресурса канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="32642-107">The **CreateInstanceFromPropertyData** method instantiates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="32642-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32642-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="32642-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="32642-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32642-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32642-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32642-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="32642-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="32642-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32642-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32642-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="32642-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="32642-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32642-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32642-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="32642-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="32642-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="32642-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32642-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="32642-117">Class of the RR.</span></span> <span data-ttu-id="32642-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="32642-118">Default value is 1.</span></span> <span data-ttu-id="32642-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="32642-119">The following values are valid.</span></span>



| <span data-ttu-id="32642-120">Значение</span><span class="sxs-lookup"><span data-stu-id="32642-120">Value</span></span>                                                                                                | <span data-ttu-id="32642-121">Значение</span><span class="sxs-lookup"><span data-stu-id="32642-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="32642-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="32642-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="32642-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="32642-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="32642-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="32642-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="32642-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="32642-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="32642-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="32642-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="32642-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="32642-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="32642-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="32642-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="32642-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="32642-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="32642-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="32642-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32642-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="32642-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="32642-132">*Примаринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32642-132">*PrimaryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32642-133">Основное имя RR CNAME.</span><span class="sxs-lookup"><span data-stu-id="32642-133">Primary name of the CNAME RR.</span></span>

</dd> <dt>

<span data-ttu-id="32642-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="32642-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="32642-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="32642-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32642-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32642-136">Return value</span></span>

<span data-ttu-id="32642-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="32642-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32642-138">Требования</span><span class="sxs-lookup"><span data-stu-id="32642-138">Requirements</span></span>



| <span data-ttu-id="32642-139">Требование</span><span class="sxs-lookup"><span data-stu-id="32642-139">Requirement</span></span> | <span data-ttu-id="32642-140">Значение</span><span class="sxs-lookup"><span data-stu-id="32642-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32642-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32642-141">Minimum supported client</span></span><br/> | <span data-ttu-id="32642-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="32642-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="32642-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32642-143">Minimum supported server</span></span><br/> | <span data-ttu-id="32642-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="32642-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="32642-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="32642-145">Namespace</span></span><br/>                | <span data-ttu-id="32642-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="32642-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="32642-147">MOF</span><span class="sxs-lookup"><span data-stu-id="32642-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32642-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32642-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32642-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32642-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32642-150">**Микрософтднс \_ кнаметипе**</span><span class="sxs-lookup"><span data-stu-id="32642-150">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="32642-151">**Метод Modify \_ класса микрософтднс кнаметипе**</span><span class="sxs-lookup"><span data-stu-id="32642-151">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="32642-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="32642-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





