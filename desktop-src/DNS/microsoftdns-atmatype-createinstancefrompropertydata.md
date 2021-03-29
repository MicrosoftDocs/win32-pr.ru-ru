---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_ATMAType
description: Метод Креатеинстанцефромпропертидата создает запись ресурса ATM Address to Name (ATMA).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_ATMAType
- DNS класса MicrosoftDNS_ATMAType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654492"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="e6070-106">Метод Креатеинстанцефромпропертидата \_ класса Атматипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="e6070-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="e6070-107">Метод **креатеинстанцефромпропертидата** создает запись ресурса ATM Address to Name (ATMA).</span><span class="sxs-lookup"><span data-stu-id="e6070-107">The **CreateInstanceFromPropertyData** method instantiates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6070-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6070-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="e6070-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6070-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6070-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6070-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6070-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e6070-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6070-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6070-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="e6070-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6070-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6070-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="e6070-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e6070-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6070-117">Class of the RR.</span></span> <span data-ttu-id="e6070-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="e6070-118">Default value is 1.</span></span> <span data-ttu-id="e6070-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e6070-119">The following values are valid.</span></span>



| <span data-ttu-id="e6070-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e6070-120">Value</span></span>                                                                                                | <span data-ttu-id="e6070-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e6070-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="e6070-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e6070-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="e6070-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="e6070-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e6070-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="e6070-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="e6070-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="e6070-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="e6070-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="e6070-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="e6070-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="e6070-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e6070-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e6070-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="e6070-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="e6070-132">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6070-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-133">Формат адреса ATM.</span><span class="sxs-lookup"><span data-stu-id="e6070-133">ATM address format.</span></span> <span data-ttu-id="e6070-134">ФОРМАТ имеет два возможных значения: 0, указывающий формат адреса конечной системы (АЕСА) ATM, а 1 — формат E. 164.</span><span class="sxs-lookup"><span data-stu-id="e6070-134">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="e6070-135">*Атмаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6070-135">*ATMAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-136">Строка переменной длины октетов, содержащая ATM-адрес узла или владельца, к которому относится эта запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6070-136">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="e6070-137">Первые четыре байта массива используются для хранения размера строки октета.</span><span class="sxs-lookup"><span data-stu-id="e6070-137">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="e6070-138">Наиболее значимый байт хранится в байте 0.</span><span class="sxs-lookup"><span data-stu-id="e6070-138">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="e6070-139">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="e6070-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-140">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="e6070-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6070-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6070-141">Return value</span></span>

<span data-ttu-id="e6070-142">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e6070-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6070-143">Требования</span><span class="sxs-lookup"><span data-stu-id="e6070-143">Requirements</span></span>



| <span data-ttu-id="e6070-144">Требование</span><span class="sxs-lookup"><span data-stu-id="e6070-144">Requirement</span></span> | <span data-ttu-id="e6070-145">Значение</span><span class="sxs-lookup"><span data-stu-id="e6070-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6070-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6070-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e6070-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6070-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e6070-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6070-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e6070-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6070-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e6070-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e6070-150">Namespace</span></span><br/>                | <span data-ttu-id="e6070-151">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="e6070-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e6070-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e6070-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6070-153"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6070-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6070-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6070-155">**Микрософтднс \_ атматипе**</span><span class="sxs-lookup"><span data-stu-id="e6070-155">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="e6070-156">**Метод Modify \_ класса микрософтднс атматипе**</span><span class="sxs-lookup"><span data-stu-id="e6070-156">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="e6070-157">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="e6070-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





