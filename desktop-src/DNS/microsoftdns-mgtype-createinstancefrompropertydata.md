---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MGType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса почтовой группы (MG).
ms.assetid: 98e2ecb3-bf2f-42db-8a8b-de10a29f5a5a
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MGType
- DNS класса MicrosoftDNS_MGType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 313f6d14a10b1de9bc1d3b3b8042020ea5b0a522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136602"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="23b3e-106">Метод Креатеинстанцефромпропертидата \_ класса Мгтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="23b3e-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="23b3e-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса почтовой группы (MG).</span><span class="sxs-lookup"><span data-stu-id="23b3e-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b3e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23b3e-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="23b3e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="23b3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b3e-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b3e-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="23b3e-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="23b3e-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b3e-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="23b3e-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="23b3e-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b3e-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="23b3e-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="23b3e-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23b3e-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="23b3e-117">Class of the RR.</span></span> <span data-ttu-id="23b3e-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="23b3e-118">Default value is 1.</span></span> <span data-ttu-id="23b3e-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="23b3e-119">The following values are valid.</span></span>



| <span data-ttu-id="23b3e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="23b3e-120">Value</span></span>                                                                                                | <span data-ttu-id="23b3e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="23b3e-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="23b3e-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="23b3e-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="23b3e-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="23b3e-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="23b3e-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="23b3e-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="23b3e-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="23b3e-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="23b3e-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="23b3e-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="23b3e-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="23b3e-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="23b3e-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="23b3e-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="23b3e-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="23b3e-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="23b3e-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23b3e-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="23b3e-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="23b3e-132">*Мгмаилбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-132">*MGMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b3e-133">Полное доменное имя, указывающее почтовый ящик, который является членом почтовой группы, указанной в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="23b3e-133">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="23b3e-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="23b3e-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="23b3e-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b3e-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23b3e-136">Return value</span></span>

<span data-ttu-id="23b3e-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="23b3e-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b3e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="23b3e-138">Requirements</span></span>



| <span data-ttu-id="23b3e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="23b3e-139">Requirement</span></span> | <span data-ttu-id="23b3e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="23b3e-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23b3e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23b3e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="23b3e-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="23b3e-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="23b3e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23b3e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="23b3e-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="23b3e-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="23b3e-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="23b3e-145">Namespace</span></span><br/>                | <span data-ttu-id="23b3e-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="23b3e-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="23b3e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="23b3e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23b3e-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23b3e-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b3e-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23b3e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b3e-150">**Микрософтднс \_ мгтипе**</span><span class="sxs-lookup"><span data-stu-id="23b3e-150">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="23b3e-151">**Метод Modify \_ класса микрософтднс мгтипе**</span><span class="sxs-lookup"><span data-stu-id="23b3e-151">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="23b3e-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="23b3e-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





