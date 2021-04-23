---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MDType
description: Метод Креатеинстанцефромпропертидата создает экземпляр почтового агента для записи ресурса домена (MD).
ms.assetid: 23155a49-e2b3-4a69-8572-5dee61019d8f
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MDType
- DNS класса MicrosoftDNS_MDType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b2e2cfdf3d2bb4b853a8e32716e51ca8e4c5b8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490494"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="07fb4-106">Метод Креатеинстанцефромпропертидата \_ класса Мдтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="07fb4-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="07fb4-107">Метод **креатеинстанцефромпропертидата** создает экземпляр почтового агента для записи ресурса домена (MD).</span><span class="sxs-lookup"><span data-stu-id="07fb4-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="07fb4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07fb4-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="07fb4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="07fb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07fb4-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb4-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="07fb4-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="07fb4-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb4-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="07fb4-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="07fb4-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb4-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="07fb4-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="07fb4-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb4-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="07fb4-117">Class of the RR.</span></span> <span data-ttu-id="07fb4-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="07fb4-118">Default value is 1.</span></span> <span data-ttu-id="07fb4-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="07fb4-119">The following values are valid.</span></span>



| <span data-ttu-id="07fb4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="07fb4-120">Value</span></span>                                                                                                | <span data-ttu-id="07fb4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="07fb4-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="07fb4-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="07fb4-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="07fb4-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="07fb4-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="07fb4-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="07fb4-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="07fb4-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="07fb4-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="07fb4-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="07fb4-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="07fb4-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="07fb4-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="07fb4-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="07fb4-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="07fb4-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="07fb4-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="07fb4-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb4-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="07fb4-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="07fb4-132">*Мдхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-132">*MDHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb4-133">Имя узла доставки почты.</span><span class="sxs-lookup"><span data-stu-id="07fb4-133">Mail delivery host name.</span></span>

</dd> <dt>

<span data-ttu-id="07fb4-134">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb4-135">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="07fb4-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07fb4-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07fb4-136">Return value</span></span>

<span data-ttu-id="07fb4-137">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="07fb4-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="07fb4-138">Требования</span><span class="sxs-lookup"><span data-stu-id="07fb4-138">Requirements</span></span>



| <span data-ttu-id="07fb4-139">Требование</span><span class="sxs-lookup"><span data-stu-id="07fb4-139">Requirement</span></span> | <span data-ttu-id="07fb4-140">Значение</span><span class="sxs-lookup"><span data-stu-id="07fb4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07fb4-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07fb4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="07fb4-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07fb4-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="07fb4-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07fb4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="07fb4-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07fb4-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="07fb4-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="07fb4-145">Namespace</span></span><br/>                | <span data-ttu-id="07fb4-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="07fb4-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="07fb4-147">MOF</span><span class="sxs-lookup"><span data-stu-id="07fb4-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07fb4-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07fb4-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07fb4-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07fb4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07fb4-150">**Микрософтднс \_ мдтипе**</span><span class="sxs-lookup"><span data-stu-id="07fb4-150">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="07fb4-151">**Метод Modify \_ класса микрософтднс мдтипе**</span><span class="sxs-lookup"><span data-stu-id="07fb4-151">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="07fb4-152">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="07fb4-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





