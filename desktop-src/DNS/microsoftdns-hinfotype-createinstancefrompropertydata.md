---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_HINFOType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса сведений об узле (HINFO).
ms.assetid: dfc11ae8-5013-4b48-a1e9-78566dc32297
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_HINFOType
- DNS класса MicrosoftDNS_HINFOType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2c8386a9c66ec94436fe4ae4c886ec62ff5b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803520"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="26b7c-106">Метод Креатеинстанцефромпропертидата \_ класса Хинфотипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="26b7c-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="26b7c-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса сведений об узле (HINFO).</span><span class="sxs-lookup"><span data-stu-id="26b7c-107">The **CreateInstanceFromPropertyData** method instantiates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b7c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26b7c-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="26b7c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="26b7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b7c-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="26b7c-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="26b7c-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="26b7c-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="26b7c-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="26b7c-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="26b7c-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="26b7c-117">Class of the RR.</span></span> <span data-ttu-id="26b7c-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="26b7c-118">Default value is 1.</span></span> <span data-ttu-id="26b7c-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="26b7c-119">The following values are valid.</span></span>



| <span data-ttu-id="26b7c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="26b7c-120">Value</span></span>                                                                                                | <span data-ttu-id="26b7c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="26b7c-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="26b7c-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="26b7c-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="26b7c-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="26b7c-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="26b7c-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="26b7c-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="26b7c-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="26b7c-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="26b7c-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="26b7c-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="26b7c-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="26b7c-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="26b7c-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="26b7c-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="26b7c-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="26b7c-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="26b7c-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="26b7c-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="26b7c-132">*ЦП* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-132">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-133">Тип ЦП владельца записи.</span><span class="sxs-lookup"><span data-stu-id="26b7c-133">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="26b7c-134">*Операционная система* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-134">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-135">Операционная система владельца записи.</span><span class="sxs-lookup"><span data-stu-id="26b7c-135">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="26b7c-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="26b7c-137">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="26b7c-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b7c-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26b7c-138">Return value</span></span>

<span data-ttu-id="26b7c-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="26b7c-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b7c-140">Требования</span><span class="sxs-lookup"><span data-stu-id="26b7c-140">Requirements</span></span>



| <span data-ttu-id="26b7c-141">Требование</span><span class="sxs-lookup"><span data-stu-id="26b7c-141">Requirement</span></span> | <span data-ttu-id="26b7c-142">Значение</span><span class="sxs-lookup"><span data-stu-id="26b7c-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26b7c-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26b7c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="26b7c-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="26b7c-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="26b7c-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26b7c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="26b7c-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26b7c-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26b7c-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26b7c-147">Namespace</span></span><br/>                | <span data-ttu-id="26b7c-148">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="26b7c-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="26b7c-149">MOF</span><span class="sxs-lookup"><span data-stu-id="26b7c-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26b7c-150"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26b7c-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b7c-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26b7c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b7c-152">**Микрософтднс \_ хинфотипе**</span><span class="sxs-lookup"><span data-stu-id="26b7c-152">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="26b7c-153">**Метод Modify \_ класса микрософтднс хинфотипе**</span><span class="sxs-lookup"><span data-stu-id="26b7c-153">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="26b7c-154">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="26b7c-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





