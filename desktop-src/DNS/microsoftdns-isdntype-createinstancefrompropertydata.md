---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_ISDNType
description: Метод Креатеинстанцефромпропертидата создает запись ресурса ISDN.
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_ISDNType
- DNS класса MicrosoftDNS_ISDNType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f6adaaf374cac56d7d29d04d83c8765b0080ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534643"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="0d0dd-106">Метод Креатеинстанцефромпропертидата \_ класса Исднтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="0d0dd-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="0d0dd-107">Метод **креатеинстанцефромпропертидата** создает запись ресурса ISDN.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-107">The **CreateInstanceFromPropertyData** method instantiates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0dd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d0dd-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="0d0dd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d0dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d0dd-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="0d0dd-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="0d0dd-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="0d0dd-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-117">Class of the RR.</span></span> <span data-ttu-id="0d0dd-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-118">Default value is 1.</span></span> <span data-ttu-id="0d0dd-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-119">The following values are valid.</span></span>



| <span data-ttu-id="0d0dd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0d0dd-120">Value</span></span>                                                                                                | <span data-ttu-id="0d0dd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0d0dd-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="0d0dd-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0d0dd-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0d0dd-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="0d0dd-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="0d0dd-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0d0dd-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0d0dd-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="0d0dd-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="0d0dd-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="0d0dd-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="0d0dd-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="0d0dd-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="0d0dd-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="0d0dd-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0d0dd-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="0d0dd-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="0d0dd-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="0d0dd-132">*Исдннумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-132">*ISDNNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-133">Номер ISDN и DDI владельца записи.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-133">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="0d0dd-134">*Подадрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-134">*SubAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-135">Подадрес владельца, если он определен.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-135">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="0d0dd-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0dd-137">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d0dd-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d0dd-138">Return value</span></span>

<span data-ttu-id="0d0dd-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0dd-140">Требования</span><span class="sxs-lookup"><span data-stu-id="0d0dd-140">Requirements</span></span>



| <span data-ttu-id="0d0dd-141">Требование</span><span class="sxs-lookup"><span data-stu-id="0d0dd-141">Requirement</span></span> | <span data-ttu-id="0d0dd-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0d0dd-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0dd-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d0dd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0dd-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0d0dd-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0d0dd-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d0dd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0dd-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d0dd-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0d0dd-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0d0dd-147">Namespace</span></span><br/>                | <span data-ttu-id="0d0dd-148">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="0d0dd-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="0d0dd-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0d0dd-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d0dd-150"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d0dd-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d0dd-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d0dd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0dd-152">**Микрософтднс \_ исднтипе**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-152">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="0d0dd-153">**Метод Modify \_ класса микрософтднс исднтипе**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-153">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="0d0dd-154">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





