---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MXType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса почтового обменника (MR).
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MXType
- DNS класса MicrosoftDNS_MXType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8154e8ccdc6ac18824e2d56597ac8e0f186f3912
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136014"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="ddd62-106">Метод Креатеинстанцефромпропертидата \_ класса Мкстипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="ddd62-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="ddd62-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса почтового обменника (MR).</span><span class="sxs-lookup"><span data-stu-id="ddd62-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddd62-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddd62-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ddd62-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddd62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddd62-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="ddd62-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ddd62-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="ddd62-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ddd62-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="ddd62-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ddd62-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="ddd62-117">Class of the RR.</span></span> <span data-ttu-id="ddd62-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="ddd62-118">Default value is 1.</span></span> <span data-ttu-id="ddd62-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="ddd62-119">The following values are valid.</span></span>



| <span data-ttu-id="ddd62-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd62-120">Value</span></span>                                                                                                | <span data-ttu-id="ddd62-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd62-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ddd62-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd62-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ddd62-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="ddd62-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ddd62-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd62-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ddd62-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="ddd62-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ddd62-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd62-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ddd62-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="ddd62-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ddd62-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd62-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ddd62-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="ddd62-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ddd62-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="ddd62-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ddd62-132">*Настройка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-133">Предпочтение данной записи ресурса между другими пользователями того же владельца.</span><span class="sxs-lookup"><span data-stu-id="ddd62-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="ddd62-134">Более низкие значения являются предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="ddd62-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="ddd62-135">*Маилексчанже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-135">*MailExchange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-136">Полное доменное имя с указанием узла, который будет использоваться в качестве почтового обмена для имени владельца.</span><span class="sxs-lookup"><span data-stu-id="ddd62-136">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="ddd62-137">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd62-138">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="ddd62-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddd62-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddd62-139">Return value</span></span>

<span data-ttu-id="ddd62-140">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ddd62-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd62-141">Требования</span><span class="sxs-lookup"><span data-stu-id="ddd62-141">Requirements</span></span>



| <span data-ttu-id="ddd62-142">Требование</span><span class="sxs-lookup"><span data-stu-id="ddd62-142">Requirement</span></span> | <span data-ttu-id="ddd62-143">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd62-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd62-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddd62-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd62-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ddd62-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ddd62-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddd62-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd62-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ddd62-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ddd62-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ddd62-148">Namespace</span></span><br/>                | <span data-ttu-id="ddd62-149">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="ddd62-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ddd62-150">MOF</span><span class="sxs-lookup"><span data-stu-id="ddd62-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddd62-151"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddd62-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddd62-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddd62-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd62-153">**Микрософтднс \_ мкстипе**</span><span class="sxs-lookup"><span data-stu-id="ddd62-153">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="ddd62-154">**Метод Modify \_ класса микрософтднс мкстипе**</span><span class="sxs-lookup"><span data-stu-id="ddd62-154">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ddd62-155">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="ddd62-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





