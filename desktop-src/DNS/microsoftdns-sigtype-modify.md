---
title: Метод Modify класса MicrosoftDNS_SIGType
description: Метод Modify обновляет запись подписи (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_SIGType класс
- MicrosoftDNS_SIGType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489435"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="18b38-106">Метод Modify \_ класса микрософтднс сигтипе</span><span class="sxs-lookup"><span data-stu-id="18b38-106">Modify method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="18b38-107">Метод **Modify** обновляет запись подписи (SIG).</span><span class="sxs-lookup"><span data-stu-id="18b38-107">The **Modify** method updates a Signature (SIG) RR.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b38-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18b38-108">Syntax</span></span>


```mof
void Modify(
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



## <a name="parameters"></a><span data-ttu-id="18b38-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18b38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b38-110">*Срок жизни* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="18b38-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-111">Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.</span><span class="sxs-lookup"><span data-stu-id="18b38-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-112">*Типековеред* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-112">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-113">Тип записи ресурса, охватываемый этой ПОДПИСЬю.</span><span class="sxs-lookup"><span data-stu-id="18b38-113">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-114">*Алгоритм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-114">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-115">Алгоритм, используемый с ключом, указанным в записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="18b38-115">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="18b38-116">Назначенные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="18b38-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="18b38-117">Значение</span><span class="sxs-lookup"><span data-stu-id="18b38-117">Value</span></span>                                                                                                | <span data-ttu-id="18b38-118">Значение</span><span class="sxs-lookup"><span data-stu-id="18b38-118">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="18b38-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="18b38-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="18b38-120">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="18b38-120">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="18b38-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="18b38-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="18b38-122">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="18b38-122">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="18b38-123"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="18b38-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="18b38-124">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="18b38-124">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="18b38-125"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="18b38-125"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="18b38-126">Шифрование на основе эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="18b38-126">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18b38-127">*Метки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-127">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-128">Число меток без знака в исходном имени владельца RR.</span><span class="sxs-lookup"><span data-stu-id="18b38-128">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="18b38-129">Число не включает метку NULL для корня или любые начальные подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="18b38-129">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-130">*Оригиналттл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-130">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-131">Срок жизни набора записей RR, подписанный SIG.</span><span class="sxs-lookup"><span data-stu-id="18b38-131">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-132">*Сигнатурикспиратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-132">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-133">Дата окончания срока действия подписи, выраженная в секундах с начала 1 января 1970 г., время по Гринвичу (GMT), за исключением високосных секунд.</span><span class="sxs-lookup"><span data-stu-id="18b38-133">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-134">*Сигнатуреинцептион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-134">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-135">Дата и время, когда подпись действительна, выраженная в секундах с начала 1 января 1970 г., время по Гринвичу (GMT), за исключением високосных секунд.</span><span class="sxs-lookup"><span data-stu-id="18b38-135">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-136">*Кэйтаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-136">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-137">Метод, используемый для выбора ключа, который проверяет подпись.</span><span class="sxs-lookup"><span data-stu-id="18b38-137">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="18b38-138">Метод, используемый для вычисления Кэйтаг, см. в документе RFC 2535 в приложении C.</span><span class="sxs-lookup"><span data-stu-id="18b38-138">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-139">*Сигнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-139">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-140">Доменное имя подписывающий, создавшего RR SIG.</span><span class="sxs-lookup"><span data-stu-id="18b38-140">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-141">*Сигнатура* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18b38-141">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-142">Сигнатура, представленная в базовом 64, в формате, определенном в RFC 2535, приложение а.</span><span class="sxs-lookup"><span data-stu-id="18b38-142">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="18b38-143">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="18b38-143">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="18b38-144">Ссылка на новый объект.</span><span class="sxs-lookup"><span data-stu-id="18b38-144">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b38-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18b38-145">Return value</span></span>

<span data-ttu-id="18b38-146">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="18b38-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b38-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18b38-147">Remarks</span></span>

<span data-ttu-id="18b38-148">Любой параметр, не указанный, остается неизменным в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="18b38-148">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b38-149">Требования</span><span class="sxs-lookup"><span data-stu-id="18b38-149">Requirements</span></span>



| <span data-ttu-id="18b38-150">Требование</span><span class="sxs-lookup"><span data-stu-id="18b38-150">Requirement</span></span> | <span data-ttu-id="18b38-151">Значение</span><span class="sxs-lookup"><span data-stu-id="18b38-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18b38-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18b38-152">Minimum supported client</span></span><br/> | <span data-ttu-id="18b38-153">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="18b38-153">None supported</span></span><br/>                                                              |
| <span data-ttu-id="18b38-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18b38-154">Minimum supported server</span></span><br/> | <span data-ttu-id="18b38-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18b38-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="18b38-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18b38-156">Namespace</span></span><br/>                | <span data-ttu-id="18b38-157">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="18b38-157">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="18b38-158">MOF</span><span class="sxs-lookup"><span data-stu-id="18b38-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18b38-159"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18b38-159"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b38-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18b38-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b38-161">**Микрософтднс \_ сигтипе**</span><span class="sxs-lookup"><span data-stu-id="18b38-161">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="18b38-162">**Метод Креатеинстанцефромпропертидата \_ класса Сигтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="18b38-162">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="18b38-163">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="18b38-163">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





