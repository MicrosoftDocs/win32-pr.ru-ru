---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_TXTType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса Text (TXT).
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_TXTType
- DNS класса MicrosoftDNS_TXTType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23f9790189ca182cd65d9fe34890c31a90921d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654637"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="12f26-106">Метод Креатеинстанцефромпропертидата \_ класса Тксттипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="12f26-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="12f26-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса Text (txt).</span><span class="sxs-lookup"><span data-stu-id="12f26-107">The **CreateInstanceFromPropertyData** method instantiates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f26-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12f26-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="12f26-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="12f26-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f26-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12f26-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f26-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="12f26-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="12f26-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12f26-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f26-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="12f26-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="12f26-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12f26-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f26-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="12f26-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="12f26-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="12f26-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12f26-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="12f26-117">Class of the RR.</span></span> <span data-ttu-id="12f26-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="12f26-118">Default value is 1.</span></span> <span data-ttu-id="12f26-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="12f26-119">The following values are valid.</span></span>



| <span data-ttu-id="12f26-120">Значение</span><span class="sxs-lookup"><span data-stu-id="12f26-120">Value</span></span>                                                                                                | <span data-ttu-id="12f26-121">Значение</span><span class="sxs-lookup"><span data-stu-id="12f26-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="12f26-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="12f26-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="12f26-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="12f26-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="12f26-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="12f26-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="12f26-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="12f26-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="12f26-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="12f26-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="12f26-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="12f26-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="12f26-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="12f26-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="12f26-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="12f26-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="12f26-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="12f26-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12f26-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="12f26-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="12f26-132">*Дескриптиветекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12f26-132">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f26-133">Описательный текст, семантика которого зависит от домена владельца.</span><span class="sxs-lookup"><span data-stu-id="12f26-133">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="12f26-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="12f26-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="12f26-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="12f26-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f26-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12f26-136">Return value</span></span>

<span data-ttu-id="12f26-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="12f26-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f26-138">Требования</span><span class="sxs-lookup"><span data-stu-id="12f26-138">Requirements</span></span>



| <span data-ttu-id="12f26-139">Требование</span><span class="sxs-lookup"><span data-stu-id="12f26-139">Requirement</span></span> | <span data-ttu-id="12f26-140">Значение</span><span class="sxs-lookup"><span data-stu-id="12f26-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12f26-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12f26-141">Minimum supported client</span></span><br/> | <span data-ttu-id="12f26-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="12f26-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="12f26-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12f26-143">Minimum supported server</span></span><br/> | <span data-ttu-id="12f26-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="12f26-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="12f26-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="12f26-145">Namespace</span></span><br/>                | <span data-ttu-id="12f26-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="12f26-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="12f26-147">MOF</span><span class="sxs-lookup"><span data-stu-id="12f26-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12f26-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12f26-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12f26-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12f26-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f26-150">**Микрософтднс \_ тксттипе**</span><span class="sxs-lookup"><span data-stu-id="12f26-150">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="12f26-151">**Метод Modify \_ класса микрософтднс тксттипе**</span><span class="sxs-lookup"><span data-stu-id="12f26-151">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="12f26-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="12f26-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





