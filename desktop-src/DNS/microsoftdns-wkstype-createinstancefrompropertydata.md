---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_WKSType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса Well-Known Services (WKS).
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_WKSType
- DNS класса MicrosoftDNS_WKSType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892214"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="5a00e-106">Метод Креатеинстанцефромпропертидата \_ класса Вкстипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="5a00e-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="5a00e-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="5a00e-107">The **CreateInstanceFromPropertyData** method instantiates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a00e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a00e-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5a00e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a00e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a00e-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a00e-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="5a00e-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a00e-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="5a00e-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a00e-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="5a00e-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a00e-117">Class of the RR.</span></span> <span data-ttu-id="5a00e-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="5a00e-118">Default value is 1.</span></span> <span data-ttu-id="5a00e-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="5a00e-119">The following values are valid.</span></span>



| <span data-ttu-id="5a00e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5a00e-120">Value</span></span>                                                                                                | <span data-ttu-id="5a00e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5a00e-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="5a00e-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5a00e-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="5a00e-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="5a00e-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="5a00e-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5a00e-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="5a00e-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="5a00e-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="5a00e-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="5a00e-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="5a00e-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="5a00e-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="5a00e-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="5a00e-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="5a00e-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="5a00e-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="5a00e-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="5a00e-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5a00e-132">*Интернетаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-132">*InternetAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-133">IP-адрес владельца записи.</span><span class="sxs-lookup"><span data-stu-id="5a00e-133">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="5a00e-134">*Иппротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-134">*IPProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-135">Строка, представляющая протокол IP для этой записи.</span><span class="sxs-lookup"><span data-stu-id="5a00e-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="5a00e-136">Допустимые значения: UDP или TCP.</span><span class="sxs-lookup"><span data-stu-id="5a00e-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="5a00e-137">*Службы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-137">*Services* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-138">Строка, содержащая все службы, используемые записью службы хорошо известных служб (WKS).</span><span class="sxs-lookup"><span data-stu-id="5a00e-138">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="5a00e-139">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5a00e-140">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="5a00e-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a00e-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a00e-141">Return value</span></span>

<span data-ttu-id="5a00e-142">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5a00e-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a00e-143">Требования</span><span class="sxs-lookup"><span data-stu-id="5a00e-143">Requirements</span></span>



| <span data-ttu-id="5a00e-144">Требование</span><span class="sxs-lookup"><span data-stu-id="5a00e-144">Requirement</span></span> | <span data-ttu-id="5a00e-145">Значение</span><span class="sxs-lookup"><span data-stu-id="5a00e-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a00e-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a00e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5a00e-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5a00e-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5a00e-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a00e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5a00e-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a00e-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a00e-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5a00e-150">Namespace</span></span><br/>                | <span data-ttu-id="5a00e-151">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="5a00e-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5a00e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="5a00e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a00e-153"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a00e-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a00e-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a00e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a00e-155">**Микрософтднс \_ вкстипе**</span><span class="sxs-lookup"><span data-stu-id="5a00e-155">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="5a00e-156">**Метод Modify \_ класса микрософтднс вкстипе**</span><span class="sxs-lookup"><span data-stu-id="5a00e-156">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="5a00e-157">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="5a00e-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





