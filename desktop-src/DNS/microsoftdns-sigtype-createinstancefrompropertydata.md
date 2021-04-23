---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_SIGType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса подписи (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_SIGType
- DNS класса MicrosoftDNS_SIGType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071245"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="7449b-106">Метод Креатеинстанцефромпропертидата \_ класса Сигтипе микрософтднс</span><span class="sxs-lookup"><span data-stu-id="7449b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="7449b-107">Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса подписи (SIG).</span><span class="sxs-lookup"><span data-stu-id="7449b-107">The **CreateInstanceFromPropertyData** method instantiates a Signature (SIG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7449b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7449b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="7449b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7449b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7449b-110">*Днссервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-111">FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="7449b-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-112">*ContainerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-113">Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="7449b-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-114">*OwnerName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-115">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="7449b-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-116">*Рекордкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7449b-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-117">Класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="7449b-117">Class of the RR.</span></span> <span data-ttu-id="7449b-118">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="7449b-118">Default value is 1.</span></span> <span data-ttu-id="7449b-119">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7449b-119">The following values are valid.</span></span>



| <span data-ttu-id="7449b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7449b-120">Value</span></span>                                                                                                | <span data-ttu-id="7449b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7449b-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="7449b-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7449b-123">В (Интернет)</span><span class="sxs-lookup"><span data-stu-id="7449b-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="7449b-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7449b-125">CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="7449b-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="7449b-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="7449b-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="7449b-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="7449b-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="7449b-129">HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="7449b-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="7449b-130">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7449b-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-131">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="7449b-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-132">*Типековеред* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-132">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-133">Тип записи ресурса, охватываемый этой ПОДПИСЬю.</span><span class="sxs-lookup"><span data-stu-id="7449b-133">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-134">*Алгоритм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-134">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-135">Алгоритм, используемый с ключом, указанным в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="7449b-135">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="7449b-136">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7449b-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="7449b-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7449b-137">Value</span></span>                                                                                                | <span data-ttu-id="7449b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7449b-138">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="7449b-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-139"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7449b-140">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="7449b-140">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="7449b-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-141"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7449b-142">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="7449b-142">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="7449b-143"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-143"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="7449b-144">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="7449b-144">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="7449b-145"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-145"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="7449b-146">Шифрование на основе эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="7449b-146">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7449b-147">*Метки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-147">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-148">Число меток без знака в исходном имени владельца RR.</span><span class="sxs-lookup"><span data-stu-id="7449b-148">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="7449b-149">Число не включает метку NULL для корня или любые начальные подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="7449b-149">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-150">*Оригиналттл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-150">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-151">Срок жизни набора записей RR, подписанный SIG.</span><span class="sxs-lookup"><span data-stu-id="7449b-151">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-152">*Сигнатурикспиратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-152">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-153">Дата окончания срока действия подписи, выраженная в секундах с начала 1 января 1970 г., время по Гринвичу (GMT), за исключением високосных секунд.</span><span class="sxs-lookup"><span data-stu-id="7449b-153">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-154">*Сигнатуреинцептион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-154">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-155">Дата и время, когда подпись действительна, выраженная в секундах с начала 1 января 1970 г., время по Гринвичу (GMT), за исключением високосных секунд.</span><span class="sxs-lookup"><span data-stu-id="7449b-155">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-156">*Кэйтаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-156">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-157">Метод, используемый для выбора ключа, который проверяет подпись.</span><span class="sxs-lookup"><span data-stu-id="7449b-157">Method used to choose a key that verifies an SIG.</span></span> <span data-ttu-id="7449b-158">Метод, используемый для вычисления Кэйтаг, см. в документе RFC 2535 в приложении C.</span><span class="sxs-lookup"><span data-stu-id="7449b-158">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-159">*Сигнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-159">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-160">Доменное имя подписывающий, создавшего RR SIG.</span><span class="sxs-lookup"><span data-stu-id="7449b-160">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-161">*Сигнатура* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7449b-161">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-162">Сигнатура, представленная в базовом 64, в формате, определенном в RFC 2535, приложение а.</span><span class="sxs-lookup"><span data-stu-id="7449b-162">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="7449b-163">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="7449b-163">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7449b-164">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="7449b-164">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7449b-165">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7449b-165">Return value</span></span>

<span data-ttu-id="7449b-166">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7449b-166">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7449b-167">Требования</span><span class="sxs-lookup"><span data-stu-id="7449b-167">Requirements</span></span>



| <span data-ttu-id="7449b-168">Требование</span><span class="sxs-lookup"><span data-stu-id="7449b-168">Requirement</span></span> | <span data-ttu-id="7449b-169">Значение</span><span class="sxs-lookup"><span data-stu-id="7449b-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7449b-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7449b-170">Minimum supported client</span></span><br/> | <span data-ttu-id="7449b-171">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7449b-171">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7449b-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7449b-172">Minimum supported server</span></span><br/> | <span data-ttu-id="7449b-173">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7449b-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7449b-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7449b-174">Namespace</span></span><br/>                | <span data-ttu-id="7449b-175">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="7449b-175">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7449b-176">MOF</span><span class="sxs-lookup"><span data-stu-id="7449b-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7449b-177"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7449b-177"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7449b-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7449b-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7449b-179">**Микрософтднс \_ сигтипе**</span><span class="sxs-lookup"><span data-stu-id="7449b-179">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="7449b-180">**Метод Modify \_ класса микрософтднс сигтипе**</span><span class="sxs-lookup"><span data-stu-id="7449b-180">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="7449b-181">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="7449b-181">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





