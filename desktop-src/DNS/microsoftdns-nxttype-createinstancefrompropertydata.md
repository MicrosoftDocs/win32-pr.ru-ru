---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_NXTType
description: Метод Креатеинстанцефромпропертидата создает экземпляр следующей записи ресурса (NXT).
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_NXTType
- DNS класса MicrosoftDNS_NXTType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491415"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="8efcc-106">Метод Креатеинстанцефромпропертидата \_ класса Нксттипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="8efcc-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="8efcc-107">Метод **креатеинстанцефромпропертидата** создает экземпляр следующей записи ресурса (NXT).</span><span class="sxs-lookup"><span data-stu-id="8efcc-107">The **CreateInstanceFromPropertyData** method instantiates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8efcc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8efcc-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8efcc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8efcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8efcc-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="8efcc-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8efcc-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="8efcc-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8efcc-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="8efcc-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8efcc-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="8efcc-117">Class of the RR.</span></span> <span data-ttu-id="8efcc-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="8efcc-118">Default value is 1.</span></span> <span data-ttu-id="8efcc-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8efcc-119">The following values are valid.</span></span>



| <span data-ttu-id="8efcc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8efcc-120">Value</span></span>                                                                                                | <span data-ttu-id="8efcc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8efcc-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8efcc-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8efcc-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8efcc-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="8efcc-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8efcc-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8efcc-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8efcc-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="8efcc-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8efcc-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="8efcc-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8efcc-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="8efcc-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8efcc-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="8efcc-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8efcc-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="8efcc-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8efcc-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="8efcc-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8efcc-132">*Некстдомаиннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-132">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-133">Следующее имя домена.</span><span class="sxs-lookup"><span data-stu-id="8efcc-133">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8efcc-134">*Типы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-134">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-135">Разделенный пробелами список назначенных пространств имен для имени владельца записи ресурса NXT.</span><span class="sxs-lookup"><span data-stu-id="8efcc-135">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="8efcc-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8efcc-137">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="8efcc-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8efcc-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8efcc-138">Return value</span></span>

<span data-ttu-id="8efcc-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8efcc-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8efcc-140">Требования</span><span class="sxs-lookup"><span data-stu-id="8efcc-140">Requirements</span></span>



| <span data-ttu-id="8efcc-141">Требование</span><span class="sxs-lookup"><span data-stu-id="8efcc-141">Requirement</span></span> | <span data-ttu-id="8efcc-142">Значение</span><span class="sxs-lookup"><span data-stu-id="8efcc-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8efcc-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8efcc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8efcc-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8efcc-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8efcc-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8efcc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8efcc-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8efcc-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8efcc-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8efcc-147">Namespace</span></span><br/>                | <span data-ttu-id="8efcc-148">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="8efcc-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8efcc-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8efcc-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8efcc-150"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8efcc-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8efcc-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8efcc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8efcc-152">**Микрософтднс \_ нксттипе**</span><span class="sxs-lookup"><span data-stu-id="8efcc-152">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="8efcc-153">**Метод Modify \_ класса микрософтднс нксттипе**</span><span class="sxs-lookup"><span data-stu-id="8efcc-153">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="8efcc-154">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="8efcc-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





