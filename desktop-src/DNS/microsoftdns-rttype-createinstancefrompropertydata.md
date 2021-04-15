---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_RTType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса маршрута (RT).
ms.assetid: 1ebb0543-d031-4430-acbe-708c4931b7a4
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_RTType
- DNS класса MicrosoftDNS_RTType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c3b8d71c41fefa9b78aa9a469ee1426c553e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534328"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="e32a6-106">Метод Креатеинстанцефромпропертидата \_ класса Рттипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="e32a6-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="e32a6-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса маршрута (RT).</span><span class="sxs-lookup"><span data-stu-id="e32a6-107">The **CreateInstanceFromPropertyData** method instantiates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32a6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e32a6-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e32a6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e32a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32a6-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="e32a6-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e32a6-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="e32a6-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e32a6-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="e32a6-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="e32a6-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="e32a6-117">Class of the RR.</span></span> <span data-ttu-id="e32a6-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="e32a6-118">Default value is 1.</span></span> <span data-ttu-id="e32a6-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e32a6-119">The following values are valid.</span></span>



| <span data-ttu-id="e32a6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e32a6-120">Value</span></span>                                                                                                | <span data-ttu-id="e32a6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e32a6-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="e32a6-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e32a6-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e32a6-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="e32a6-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="e32a6-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e32a6-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e32a6-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="e32a6-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="e32a6-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="e32a6-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="e32a6-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="e32a6-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="e32a6-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="e32a6-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="e32a6-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="e32a6-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e32a6-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="e32a6-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e32a6-132">*Настройка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-133">Предпочтение данной записи ресурса между другими пользователями того же владельца.</span><span class="sxs-lookup"><span data-stu-id="e32a6-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="e32a6-134">Более низкие значения являются предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="e32a6-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="e32a6-135">*Интермедиатехост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-135">*IntermediateHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-136">Полное доменное имя, указывающее узел, который будет выступать в качестве промежуточного в достижение узла, указанного владельцем.</span><span class="sxs-lookup"><span data-stu-id="e32a6-136">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="e32a6-137">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e32a6-138">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="e32a6-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e32a6-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e32a6-139">Return value</span></span>

<span data-ttu-id="e32a6-140">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e32a6-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e32a6-141">Требования</span><span class="sxs-lookup"><span data-stu-id="e32a6-141">Requirements</span></span>



| <span data-ttu-id="e32a6-142">Требование</span><span class="sxs-lookup"><span data-stu-id="e32a6-142">Requirement</span></span> | <span data-ttu-id="e32a6-143">Значение</span><span class="sxs-lookup"><span data-stu-id="e32a6-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e32a6-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e32a6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e32a6-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e32a6-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e32a6-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e32a6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e32a6-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e32a6-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e32a6-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e32a6-148">Namespace</span></span><br/>                | <span data-ttu-id="e32a6-149">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="e32a6-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e32a6-150">MOF</span><span class="sxs-lookup"><span data-stu-id="e32a6-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e32a6-151"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e32a6-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e32a6-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e32a6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32a6-153">**Микрософтднс \_ рттипе**</span><span class="sxs-lookup"><span data-stu-id="e32a6-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="e32a6-154">**Метод Modify \_ класса микрософтднс рттипе**</span><span class="sxs-lookup"><span data-stu-id="e32a6-154">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="e32a6-155">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="e32a6-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





