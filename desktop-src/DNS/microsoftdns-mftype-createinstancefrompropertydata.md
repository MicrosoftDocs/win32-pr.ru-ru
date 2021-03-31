---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MFType
description: Метод Креатеинстанцефромпропертидата создает экземпляр агента переадресации почты для записи ресурса домена (MF).
ms.assetid: e669d065-bfba-4a86-8519-2317e03ed4ee
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MFType
- DNS класса MicrosoftDNS_MFType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26cafc766a6ea6419432b279f5389721f6572b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988631"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="60184-106">Метод Креатеинстанцефромпропертидата \_ класса Мфтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="60184-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="60184-107">Метод **креатеинстанцефромпропертидата** создает экземпляр агента переадресации почты для записи ресурса домена (MF).</span><span class="sxs-lookup"><span data-stu-id="60184-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="60184-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60184-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="60184-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="60184-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60184-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60184-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60184-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="60184-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="60184-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60184-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60184-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="60184-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="60184-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60184-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60184-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="60184-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="60184-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="60184-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60184-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="60184-117">Class of the RR.</span></span> <span data-ttu-id="60184-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="60184-118">Default value is 1.</span></span> <span data-ttu-id="60184-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="60184-119">The following values are valid.</span></span>



| <span data-ttu-id="60184-120">Значение</span><span class="sxs-lookup"><span data-stu-id="60184-120">Value</span></span>                                                                                                | <span data-ttu-id="60184-121">Значение</span><span class="sxs-lookup"><span data-stu-id="60184-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="60184-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="60184-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="60184-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="60184-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="60184-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="60184-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="60184-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="60184-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="60184-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="60184-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="60184-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="60184-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="60184-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="60184-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="60184-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="60184-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="60184-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="60184-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60184-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="60184-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="60184-132">*Мфхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60184-132">*MFHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60184-133">Имя узла, предоставляющего агент пересылки почты.</span><span class="sxs-lookup"><span data-stu-id="60184-133">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="60184-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="60184-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="60184-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="60184-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60184-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60184-136">Return value</span></span>

<span data-ttu-id="60184-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="60184-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="60184-138">Требования</span><span class="sxs-lookup"><span data-stu-id="60184-138">Requirements</span></span>



| <span data-ttu-id="60184-139">Требование</span><span class="sxs-lookup"><span data-stu-id="60184-139">Requirement</span></span> | <span data-ttu-id="60184-140">Значение</span><span class="sxs-lookup"><span data-stu-id="60184-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60184-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60184-141">Minimum supported client</span></span><br/> | <span data-ttu-id="60184-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60184-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="60184-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60184-143">Minimum supported server</span></span><br/> | <span data-ttu-id="60184-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="60184-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="60184-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60184-145">Namespace</span></span><br/>                | <span data-ttu-id="60184-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="60184-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="60184-147">MOF</span><span class="sxs-lookup"><span data-stu-id="60184-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60184-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60184-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60184-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60184-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60184-150">**Микрософтднс \_ мфтипе**</span><span class="sxs-lookup"><span data-stu-id="60184-150">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="60184-151">**Метод Modify \_ класса микрософтднс мфтипе**</span><span class="sxs-lookup"><span data-stu-id="60184-151">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="60184-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="60184-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





