---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MBType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса почтового ящика (МБ).
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MBType
- DNS класса MicrosoftDNS_MBType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e340d78057c12e58159a293468598da7dbf53e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892125"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="f800e-106">Метод Креатеинстанцефромпропертидата \_ класса Мбтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f800e-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="f800e-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса почтового ящика (МБ).</span><span class="sxs-lookup"><span data-stu-id="f800e-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f800e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f800e-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f800e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f800e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f800e-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f800e-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f800e-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="f800e-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f800e-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f800e-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f800e-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="f800e-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f800e-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f800e-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f800e-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f800e-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f800e-116">*Рекордкласс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f800e-116">*RecordClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f800e-117">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f800e-117">Optional.</span></span> <span data-ttu-id="f800e-118">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f800e-118">Class of the RR.</span></span> <span data-ttu-id="f800e-119">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="f800e-119">Default value is 1.</span></span> <span data-ttu-id="f800e-120">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f800e-120">The following values are valid.</span></span>



| <span data-ttu-id="f800e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f800e-121">Value</span></span>                                                                                                | <span data-ttu-id="f800e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f800e-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f800e-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f800e-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f800e-124">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="f800e-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f800e-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f800e-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f800e-126">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="f800e-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f800e-127"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="f800e-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f800e-128">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="f800e-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f800e-129"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="f800e-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f800e-130">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="f800e-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f800e-131">*Срок жизни* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f800e-131">*TTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f800e-132">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f800e-132">Optional.</span></span> <span data-ttu-id="f800e-133">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="f800e-133">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f800e-134">*Мбхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f800e-134">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f800e-135">Имя узла почтового ящика для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f800e-135">Mailbox host name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f800e-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="f800e-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f800e-137">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="f800e-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f800e-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f800e-138">Return value</span></span>

<span data-ttu-id="f800e-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f800e-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f800e-140">Требования</span><span class="sxs-lookup"><span data-stu-id="f800e-140">Requirements</span></span>



| <span data-ttu-id="f800e-141">Требование</span><span class="sxs-lookup"><span data-stu-id="f800e-141">Requirement</span></span> | <span data-ttu-id="f800e-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f800e-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f800e-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f800e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f800e-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f800e-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f800e-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f800e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f800e-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f800e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f800e-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f800e-147">Namespace</span></span><br/>                | <span data-ttu-id="f800e-148">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f800e-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f800e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f800e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f800e-150"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f800e-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f800e-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f800e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f800e-152">**Микрософтднс \_ мбтипе**</span><span class="sxs-lookup"><span data-stu-id="f800e-152">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="f800e-153">**Метод Modify \_ класса микрософтднс мбтипе**</span><span class="sxs-lookup"><span data-stu-id="f800e-153">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="f800e-154">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="f800e-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





