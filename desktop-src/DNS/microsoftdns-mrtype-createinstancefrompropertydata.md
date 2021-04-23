---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MRType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса переименования почтового ящика (MR).
ms.assetid: 7dab86e0-bf05-4e98-b1f8-e1daecd4425c
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MRType
- DNS класса MicrosoftDNS_MRType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f41478d4ff59ff7999f6f3b052f203aeda78803
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891977"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="cc484-106">Метод Креатеинстанцефромпропертидата \_ класса Мртипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="cc484-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="cc484-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса переименования почтового ящика (MR).</span><span class="sxs-lookup"><span data-stu-id="cc484-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc484-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc484-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cc484-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc484-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc484-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc484-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc484-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc484-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="cc484-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc484-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc484-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc484-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="cc484-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc484-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc484-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc484-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="cc484-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cc484-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc484-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc484-117">Class of the RR.</span></span> <span data-ttu-id="cc484-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="cc484-118">Default value is 1.</span></span> <span data-ttu-id="cc484-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="cc484-119">The following values are valid.</span></span>



| <span data-ttu-id="cc484-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cc484-120">Value</span></span>                                                                                                | <span data-ttu-id="cc484-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cc484-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="cc484-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cc484-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="cc484-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="cc484-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="cc484-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cc484-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="cc484-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="cc484-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="cc484-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="cc484-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="cc484-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="cc484-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="cc484-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="cc484-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="cc484-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="cc484-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="cc484-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="cc484-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc484-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="cc484-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cc484-132">*Мрмаилбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc484-132">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc484-133">Полное доменное имя, указывающее почтовый ящик, который является правильным именем почтового ящика, указанного в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="cc484-133">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="cc484-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="cc484-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cc484-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="cc484-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc484-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc484-136">Return value</span></span>

<span data-ttu-id="cc484-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cc484-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc484-138">Требования</span><span class="sxs-lookup"><span data-stu-id="cc484-138">Requirements</span></span>



| <span data-ttu-id="cc484-139">Требование</span><span class="sxs-lookup"><span data-stu-id="cc484-139">Requirement</span></span> | <span data-ttu-id="cc484-140">Значение</span><span class="sxs-lookup"><span data-stu-id="cc484-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc484-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc484-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cc484-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc484-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cc484-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc484-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cc484-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc484-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc484-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cc484-145">Namespace</span></span><br/>                | <span data-ttu-id="cc484-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="cc484-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cc484-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cc484-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc484-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc484-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc484-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc484-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc484-150">**Микрософтднс \_ мртипе**</span><span class="sxs-lookup"><span data-stu-id="cc484-150">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="cc484-151">**Метод Modify \_ класса микрософтднс мртипе**</span><span class="sxs-lookup"><span data-stu-id="cc484-151">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="cc484-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="cc484-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





