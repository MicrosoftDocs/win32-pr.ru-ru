---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_AType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса адреса (A).
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_AType
- DNS класса MicrosoftDNS_AType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d8d3e5c9d0ad4302da2243a3ef9611e295c86e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135922"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="699f0-106">Метод Креатеинстанцефромпропертидата \_ класса Атипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="699f0-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="699f0-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса адреса (A).</span><span class="sxs-lookup"><span data-stu-id="699f0-107">The **CreateInstanceFromPropertyData** method instantiates an Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="699f0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="699f0-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="699f0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="699f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="699f0-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="699f0-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="699f0-111">Полное доменное имя (FQDN) или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="699f0-111">Fully Qualified Domain Name (FQDN) or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="699f0-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="699f0-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="699f0-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="699f0-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="699f0-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="699f0-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="699f0-115">Полное доменное имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="699f0-115">Owner FQDN for the RR.</span></span>

> [!Note]  
> <span data-ttu-id="699f0-116">Не используйте NetBIOS-имя владельца.</span><span class="sxs-lookup"><span data-stu-id="699f0-116">Do not use the owner NetBIOS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="699f0-117">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="699f0-117">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="699f0-118">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="699f0-118">Class of the RR.</span></span> <span data-ttu-id="699f0-119">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="699f0-119">Default value is 1.</span></span> <span data-ttu-id="699f0-120">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="699f0-120">The following values are valid.</span></span>



| <span data-ttu-id="699f0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="699f0-121">Value</span></span>                                                                                                | <span data-ttu-id="699f0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="699f0-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="699f0-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="699f0-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="699f0-124">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="699f0-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="699f0-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="699f0-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="699f0-126">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="699f0-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="699f0-127"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="699f0-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="699f0-128">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="699f0-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="699f0-129"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="699f0-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="699f0-130">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="699f0-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="699f0-131">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="699f0-131">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="699f0-132">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="699f0-132">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="699f0-133">*IP-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="699f0-133">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="699f0-134">Строка, представляющая IP-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="699f0-134">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="699f0-135">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="699f0-135">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="699f0-136">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="699f0-136">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="699f0-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="699f0-137">Return value</span></span>

<span data-ttu-id="699f0-138">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="699f0-138">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="699f0-139">Требования</span><span class="sxs-lookup"><span data-stu-id="699f0-139">Requirements</span></span>



| <span data-ttu-id="699f0-140">Требование</span><span class="sxs-lookup"><span data-stu-id="699f0-140">Requirement</span></span> | <span data-ttu-id="699f0-141">Значение</span><span class="sxs-lookup"><span data-stu-id="699f0-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="699f0-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="699f0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="699f0-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="699f0-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="699f0-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="699f0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="699f0-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="699f0-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="699f0-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="699f0-146">Namespace</span></span><br/>                | <span data-ttu-id="699f0-147">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="699f0-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="699f0-148">MOF</span><span class="sxs-lookup"><span data-stu-id="699f0-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="699f0-149"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="699f0-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="699f0-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="699f0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="699f0-151">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="699f0-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="699f0-152">**Метод Modify \_ класса микрософтднс атипе**</span><span class="sxs-lookup"><span data-stu-id="699f0-152">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





