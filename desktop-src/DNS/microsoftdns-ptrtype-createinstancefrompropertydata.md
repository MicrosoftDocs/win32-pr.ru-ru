---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_PTRType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса указателя (PTR).
ms.assetid: ff8beaca-fa0d-4294-8dab-3aa62baa3fe3
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_PTRType
- DNS класса MicrosoftDNS_PTRType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6123b503fff1548b7fee3f643920b49ebacf636c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135842"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="945b9-106">Метод Креатеинстанцефромпропертидата \_ класса Птртипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="945b9-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="945b9-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="945b9-107">The **CreateInstanceFromPropertyData** method instantiates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="945b9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="945b9-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="945b9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="945b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="945b9-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="945b9-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945b9-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="945b9-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="945b9-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="945b9-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945b9-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="945b9-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="945b9-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="945b9-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945b9-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="945b9-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="945b9-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="945b9-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="945b9-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="945b9-117">Class of the RR.</span></span> <span data-ttu-id="945b9-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="945b9-118">Default value is 1.</span></span> <span data-ttu-id="945b9-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="945b9-119">The following values are valid.</span></span>



| <span data-ttu-id="945b9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="945b9-120">Value</span></span>                                                                                                | <span data-ttu-id="945b9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="945b9-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="945b9-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="945b9-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="945b9-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="945b9-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="945b9-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="945b9-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="945b9-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="945b9-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="945b9-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="945b9-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="945b9-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="945b9-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="945b9-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="945b9-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="945b9-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="945b9-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="945b9-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="945b9-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="945b9-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="945b9-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="945b9-132">*Птрдомаиннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="945b9-132">*PTRDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="945b9-133">Строка, представляющая адрес имени домена записи PTR.</span><span class="sxs-lookup"><span data-stu-id="945b9-133">String representing the domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="945b9-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="945b9-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="945b9-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="945b9-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="945b9-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="945b9-136">Return value</span></span>

<span data-ttu-id="945b9-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="945b9-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="945b9-138">Требования</span><span class="sxs-lookup"><span data-stu-id="945b9-138">Requirements</span></span>



| <span data-ttu-id="945b9-139">Требование</span><span class="sxs-lookup"><span data-stu-id="945b9-139">Requirement</span></span> | <span data-ttu-id="945b9-140">Значение</span><span class="sxs-lookup"><span data-stu-id="945b9-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="945b9-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="945b9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="945b9-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="945b9-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="945b9-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="945b9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="945b9-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="945b9-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="945b9-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="945b9-145">Namespace</span></span><br/>                | <span data-ttu-id="945b9-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="945b9-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="945b9-147">MOF</span><span class="sxs-lookup"><span data-stu-id="945b9-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="945b9-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="945b9-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945b9-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="945b9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945b9-150">**Микрософтднс \_ птртипе**</span><span class="sxs-lookup"><span data-stu-id="945b9-150">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="945b9-151">**Метод Modify \_ класса микрософтднс птртипе**</span><span class="sxs-lookup"><span data-stu-id="945b9-151">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="945b9-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="945b9-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





