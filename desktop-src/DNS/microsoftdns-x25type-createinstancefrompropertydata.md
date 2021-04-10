---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_X25Type
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса X. 25 (X25).
ms.assetid: fe89f829-79b9-457e-b455-899b2706ef04
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_X25Type
- DNS класса MicrosoftDNS_X25Type, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f198bf7b843b5633acd0b1515e9e3573f5ebb55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071771"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="04ea5-106">Метод Креатеинстанцефромпропертидата \_ класса X25Type микрософтднс</span><span class="sxs-lookup"><span data-stu-id="04ea5-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="04ea5-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="04ea5-107">The **CreateInstanceFromPropertyData** method instantiates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ea5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04ea5-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="04ea5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="04ea5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ea5-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ea5-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="04ea5-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="04ea5-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ea5-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="04ea5-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="04ea5-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ea5-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="04ea5-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="04ea5-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04ea5-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="04ea5-117">Class of the RR.</span></span> <span data-ttu-id="04ea5-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="04ea5-118">Default value is 1.</span></span> <span data-ttu-id="04ea5-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="04ea5-119">The following values are valid.</span></span>



| <span data-ttu-id="04ea5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="04ea5-120">Value</span></span>                                                                                                | <span data-ttu-id="04ea5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="04ea5-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="04ea5-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="04ea5-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="04ea5-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="04ea5-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="04ea5-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="04ea5-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="04ea5-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="04ea5-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="04ea5-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="04ea5-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="04ea5-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="04ea5-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="04ea5-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="04ea5-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="04ea5-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="04ea5-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="04ea5-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04ea5-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="04ea5-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="04ea5-132">*Псднаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-132">*PSDNAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ea5-133">Адрес PSDN владельца записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="04ea5-133">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="04ea5-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="04ea5-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="04ea5-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ea5-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04ea5-136">Return value</span></span>

<span data-ttu-id="04ea5-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="04ea5-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ea5-138">Требования</span><span class="sxs-lookup"><span data-stu-id="04ea5-138">Requirements</span></span>



| <span data-ttu-id="04ea5-139">Требование</span><span class="sxs-lookup"><span data-stu-id="04ea5-139">Requirement</span></span> | <span data-ttu-id="04ea5-140">Значение</span><span class="sxs-lookup"><span data-stu-id="04ea5-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04ea5-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04ea5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="04ea5-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="04ea5-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="04ea5-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04ea5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="04ea5-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04ea5-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04ea5-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="04ea5-145">Namespace</span></span><br/>                | <span data-ttu-id="04ea5-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="04ea5-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="04ea5-147">MOF</span><span class="sxs-lookup"><span data-stu-id="04ea5-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04ea5-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04ea5-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ea5-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04ea5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ea5-150">**Микрософтднс \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="04ea5-150">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="04ea5-151">**Метод Modify \_ класса микрософтднс X25Type**</span><span class="sxs-lookup"><span data-stu-id="04ea5-151">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="04ea5-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="04ea5-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





