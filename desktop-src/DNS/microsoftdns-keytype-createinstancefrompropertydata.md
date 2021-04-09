---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_KEYType
description: Метод Креатеинстанцефромпропертидата создает запись ресурса ключа.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_KEYType
- DNS класса MicrosoftDNS_KEYType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071991"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="f6450-106">Метод Креатеинстанцефромпропертидата \_ класса KEYType микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f6450-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="f6450-107">Метод **креатеинстанцефромпропертидата** создает запись ресурса ключа.</span><span class="sxs-lookup"><span data-stu-id="f6450-107">The **CreateInstanceFromPropertyData** method instantiates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6450-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6450-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f6450-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6450-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6450-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6450-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6450-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6450-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6450-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6450-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6450-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6450-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6450-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6450-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f6450-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6450-117">Class of the RR.</span></span> <span data-ttu-id="f6450-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="f6450-118">Default value is 1.</span></span> <span data-ttu-id="f6450-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f6450-119">The following values are valid.</span></span>



| <span data-ttu-id="f6450-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f6450-120">Value</span></span>                                                                                                | <span data-ttu-id="f6450-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f6450-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f6450-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f6450-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="f6450-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f6450-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f6450-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="f6450-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f6450-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f6450-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="f6450-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f6450-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f6450-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="f6450-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f6450-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f6450-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="f6450-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f6450-132">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6450-132">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-133">Флаги, используемые для определения сопоставления, как описано в документе IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="f6450-133">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="f6450-134">*Протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6450-134">*Protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-135">Протокол, для которого можно использовать ключ, указанный в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6450-135">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="f6450-136">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f6450-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="f6450-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f6450-137">Value</span></span>                                                                                                    | <span data-ttu-id="f6450-138">Значение</span><span class="sxs-lookup"><span data-stu-id="f6450-138">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f6450-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-139"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="f6450-140">TLS</span><span class="sxs-lookup"><span data-stu-id="f6450-140">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="f6450-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-141"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="f6450-142">E-Mail</span><span class="sxs-lookup"><span data-stu-id="f6450-142">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="f6450-143"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-143"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="f6450-144">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="f6450-144">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="f6450-145"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-145"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="f6450-146">IPsec</span><span class="sxs-lookup"><span data-stu-id="f6450-146">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="f6450-147"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-147"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="f6450-148">Все протоколы</span><span class="sxs-lookup"><span data-stu-id="f6450-148">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f6450-149">*Алгоритм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6450-149">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-150">Алгоритм, используемый с ключом, указанным в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6450-150">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="f6450-151">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f6450-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="f6450-152">Значение</span><span class="sxs-lookup"><span data-stu-id="f6450-152">Value</span></span>                                                                                                | <span data-ttu-id="f6450-153">Значение</span><span class="sxs-lookup"><span data-stu-id="f6450-153">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f6450-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-154"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f6450-155">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="f6450-155">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="f6450-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-156"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f6450-157">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="f6450-157">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="f6450-158"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-158"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f6450-159">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="f6450-159">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="f6450-160"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-160"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f6450-161">Шифрование на основе эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="f6450-161">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f6450-162">*PublicKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6450-162">*PublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-163">Открытый ключ, представленный в базовом 64, как описано в приложении A из RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="f6450-163">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="f6450-164">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="f6450-164">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f6450-165">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="f6450-165">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6450-166">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6450-166">Return value</span></span>

<span data-ttu-id="f6450-167">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f6450-167">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6450-168">Требования</span><span class="sxs-lookup"><span data-stu-id="f6450-168">Requirements</span></span>



| <span data-ttu-id="f6450-169">Требование</span><span class="sxs-lookup"><span data-stu-id="f6450-169">Requirement</span></span> | <span data-ttu-id="f6450-170">Значение</span><span class="sxs-lookup"><span data-stu-id="f6450-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6450-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6450-171">Minimum supported client</span></span><br/> | <span data-ttu-id="f6450-172">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6450-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6450-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6450-173">Minimum supported server</span></span><br/> | <span data-ttu-id="f6450-174">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6450-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6450-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6450-175">Namespace</span></span><br/>                | <span data-ttu-id="f6450-176">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="f6450-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f6450-177">MOF</span><span class="sxs-lookup"><span data-stu-id="f6450-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6450-178"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6450-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6450-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6450-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6450-180">**Микрософтднс \_ KEYType**</span><span class="sxs-lookup"><span data-stu-id="f6450-180">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="f6450-181">**Метод Modify \_ класса микрософтднс KEYType**</span><span class="sxs-lookup"><span data-stu-id="f6450-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="f6450-182">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="f6450-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





