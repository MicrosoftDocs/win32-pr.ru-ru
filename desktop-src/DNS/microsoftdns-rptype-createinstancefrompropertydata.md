---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_RPType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса ответственного лица (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_RPType
- DNS класса MicrosoftDNS_RPType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262198"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="b0206-106">Метод Креатеинстанцефромпропертидата \_ класса Рптипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="b0206-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="b0206-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса ответственного лица (RP).</span><span class="sxs-lookup"><span data-stu-id="b0206-107">The **CreateInstanceFromPropertyData** method instantiates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0206-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0206-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b0206-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0206-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0206-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0206-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0206-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b0206-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0206-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0206-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b0206-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0206-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0206-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="b0206-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b0206-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0206-117">Class of the RR.</span></span> <span data-ttu-id="b0206-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="b0206-118">Default value is 1.</span></span> <span data-ttu-id="b0206-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b0206-119">The following values are valid.</span></span>



| <span data-ttu-id="b0206-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b0206-120">Value</span></span>                                                                                                | <span data-ttu-id="b0206-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b0206-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="b0206-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b0206-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b0206-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="b0206-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="b0206-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b0206-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b0206-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="b0206-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="b0206-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="b0206-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="b0206-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="b0206-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="b0206-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="b0206-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="b0206-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="b0206-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="b0206-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b0206-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="b0206-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b0206-132">*Рпмаилбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0206-132">*RPMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-133">Полное доменное имя, указывающее почтовый ящик ответственного лица.</span><span class="sxs-lookup"><span data-stu-id="b0206-133">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="b0206-134">*Ткстдомаиннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0206-134">*TXTDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-135">Полное доменное имя, для которого существуют записи ресурсов TXT.</span><span class="sxs-lookup"><span data-stu-id="b0206-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="b0206-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="b0206-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b0206-137">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="b0206-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0206-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0206-138">Return value</span></span>

<span data-ttu-id="b0206-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b0206-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0206-140">Требования</span><span class="sxs-lookup"><span data-stu-id="b0206-140">Requirements</span></span>



| <span data-ttu-id="b0206-141">Требование</span><span class="sxs-lookup"><span data-stu-id="b0206-141">Requirement</span></span> | <span data-ttu-id="b0206-142">Значение</span><span class="sxs-lookup"><span data-stu-id="b0206-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0206-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0206-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b0206-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b0206-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b0206-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0206-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b0206-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0206-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b0206-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0206-147">Namespace</span></span><br/>                | <span data-ttu-id="b0206-148">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="b0206-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b0206-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b0206-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0206-150"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0206-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0206-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0206-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0206-152">**Микрософтднс \_ рптипе**</span><span class="sxs-lookup"><span data-stu-id="b0206-152">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="b0206-153">**Метод Modify \_ класса микрософтднс рптипе**</span><span class="sxs-lookup"><span data-stu-id="b0206-153">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="b0206-154">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="b0206-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





