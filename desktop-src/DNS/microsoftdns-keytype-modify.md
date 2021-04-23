---
title: Метод Modify класса MicrosoftDNS_KEYType
description: Метод Modify обновляет запись ресурса ключа.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_KEYType класс
- MicrosoftDNS_KEYType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137530"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="ddc5e-106">Метод Modify \_ класса микрософтднс KEYType</span><span class="sxs-lookup"><span data-stu-id="ddc5e-106">Modify method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="ddc5e-107">Метод **Modify** обновляет запись ресурса ключа.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-107">The **Modify** method updates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc5e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddc5e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ddc5e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddc5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc5e-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddc5e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc5e-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ddc5e-112">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddc5e-112">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc5e-113">Флаги, используемые для определения сопоставления, как описано в документе IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-113">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="ddc5e-114">*Протокол* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddc5e-114">*Protocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc5e-115">Протокол, для которого можно использовать ключ, указанный в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-115">Protocol for which the key specified in the RR can be used.</span></span> <span data-ttu-id="ddc5e-116">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="ddc5e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc5e-117">Value</span></span>                                                                                                    | <span data-ttu-id="ddc5e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc5e-118">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ddc5e-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-119"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="ddc5e-120">TLS</span><span class="sxs-lookup"><span data-stu-id="ddc5e-120">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="ddc5e-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-121"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="ddc5e-122">E-Mail</span><span class="sxs-lookup"><span data-stu-id="ddc5e-122">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="ddc5e-123"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-123"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="ddc5e-124">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="ddc5e-124">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="ddc5e-125"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-125"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="ddc5e-126">IPsec</span><span class="sxs-lookup"><span data-stu-id="ddc5e-126">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="ddc5e-127"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-127"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="ddc5e-128">Все протоколы</span><span class="sxs-lookup"><span data-stu-id="ddc5e-128">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ddc5e-129">*Алгоритм* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddc5e-129">*Algorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc5e-130">Алгоритм, используемый с ключом, указанным в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-130">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="ddc5e-131">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-131">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="ddc5e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc5e-132">Value</span></span>                                                                                                | <span data-ttu-id="ddc5e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc5e-133">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ddc5e-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ddc5e-135">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="ddc5e-135">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="ddc5e-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ddc5e-137">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="ddc5e-137">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="ddc5e-138"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-138"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ddc5e-139">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="ddc5e-139">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="ddc5e-140"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-140"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ddc5e-141">Шифрование на основе эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="ddc5e-141">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ddc5e-142">*PublicKey* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddc5e-142">*PublicKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc5e-143">Открытый ключ, представленный в базовом 64, как описано в приложении A из RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-143">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="ddc5e-144">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="ddc5e-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc5e-145">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc5e-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddc5e-146">Return value</span></span>

<span data-ttu-id="ddc5e-147">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddc5e-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddc5e-148">Remarks</span></span>

<span data-ttu-id="ddc5e-149">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-149">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc5e-150">Требования</span><span class="sxs-lookup"><span data-stu-id="ddc5e-150">Requirements</span></span>



| <span data-ttu-id="ddc5e-151">Требование</span><span class="sxs-lookup"><span data-stu-id="ddc5e-151">Requirement</span></span> | <span data-ttu-id="ddc5e-152">Значение</span><span class="sxs-lookup"><span data-stu-id="ddc5e-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc5e-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddc5e-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc5e-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ddc5e-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ddc5e-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddc5e-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc5e-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ddc5e-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ddc5e-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ddc5e-157">Namespace</span></span><br/>                | <span data-ttu-id="ddc5e-158">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="ddc5e-158">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ddc5e-159">MOF</span><span class="sxs-lookup"><span data-stu-id="ddc5e-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddc5e-160"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddc5e-160"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc5e-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddc5e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc5e-162">**Микрософтднс \_ KEYType**</span><span class="sxs-lookup"><span data-stu-id="ddc5e-162">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="ddc5e-163">**Метод Креатеинстанцефромпропертидата \_ класса KEYType микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="ddc5e-163">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ddc5e-164">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="ddc5e-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





