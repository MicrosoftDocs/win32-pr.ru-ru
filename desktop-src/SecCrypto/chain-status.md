---
description: Возвращает состояние допустимости цепочки или определенного сертификата в цепочке.
title: 'Свойство IChain2:: Status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688952"
---
# <a name="ichain2status-property"></a><span data-ttu-id="56d2e-103">Свойство IChain2:: Status</span><span class="sxs-lookup"><span data-stu-id="56d2e-103">IChain2::Status property</span></span>

<span data-ttu-id="56d2e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="56d2e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="56d2e-105">Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="56d2e-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="56d2e-106">Свойство **Status** получает состояние действия цепочки или определенного сертификата в цепочке.</span><span class="sxs-lookup"><span data-stu-id="56d2e-106">The **Status** property retrieves the validity status of the chain or a specific certificate in the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d2e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56d2e-107">Syntax</span></span>


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a><span data-ttu-id="56d2e-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="56d2e-108">Property value</span></span>

<span data-ttu-id="56d2e-109">Значение **типа Long** , представляющее индикатор состояния допустимости цепочки или указанного сертификата.</span><span class="sxs-lookup"><span data-stu-id="56d2e-109">A **LONG** value that represents the validity status indicator of the chain or the specified certificate.</span></span> <span data-ttu-id="56d2e-110">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="56d2e-110">The following table shows the possible values.</span></span> <span data-ttu-id="56d2e-111">Это свойство будет содержать нуль, если цепочка или указанный сертификат являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="56d2e-111">This property will contain zero if the chain or specified certificate is valid.</span></span> <span data-ttu-id="56d2e-112">В противном случае это свойство будет содержать сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="56d2e-112">Otherwise, this property will contain a combination of one or more of the following values.</span></span>

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span data-ttu-id="56d2e-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ \_ \_ \_ \_ Недопустимое время доверия** (&H00000001)</span><span class="sxs-lookup"><span data-stu-id="56d2e-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_VALID** (&H00000001)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-114">Этот сертификат или один из сертификатов в цепочке сертификатов имеет недопустимый срок действия.</span><span class="sxs-lookup"><span data-stu-id="56d2e-114">This certificate or one of the certificates in the certificate chain is not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span data-ttu-id="56d2e-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ ДОВЕРИЕ \_ не \_ является \_ \_ вложенным во временную** (&H00000002)</span><span class="sxs-lookup"><span data-stu-id="56d2e-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_NESTED** (&H00000002)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-116">Сертификаты в цепочке не вложены в неправильное время.</span><span class="sxs-lookup"><span data-stu-id="56d2e-116">Certificates in the chain are not properly time nested.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span data-ttu-id="56d2e-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ Отношение \_ доверия \_ отозвано** (&H00000004)</span><span class="sxs-lookup"><span data-stu-id="56d2e-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM\_TRUST\_IS\_REVOKED** (&H00000004)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-118">Отношение доверия для этого сертификата или одного из сертификатов в цепочке сертификатов было отозвано.</span><span class="sxs-lookup"><span data-stu-id="56d2e-118">Trust for this certificate or one of the certificates in the certificate chain has been revoked.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span data-ttu-id="56d2e-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ ДОВЕРИЕ \_ \_ не является \_ \_ допустимой сигнатурой** (&H00000008)</span><span class="sxs-lookup"><span data-stu-id="56d2e-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_SIGNATURE\_VALID** (&H00000008)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-120">Сертификат или один из сертификатов в цепочке сертификатов не имеет действительной подписи.</span><span class="sxs-lookup"><span data-stu-id="56d2e-120">The certificate or one of the certificates in the certificate chain does not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span data-ttu-id="56d2e-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ Отношение доверия недопустимо \_ \_ \_ \_ для \_ использования** (&H00000010)</span><span class="sxs-lookup"><span data-stu-id="56d2e-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00000010)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-122">Сертификат или цепочка сертификатов не являются допустимыми для предполагаемого использования.</span><span class="sxs-lookup"><span data-stu-id="56d2e-122">The certificate or certificate chain is not valid for its proposed usage.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span data-ttu-id="56d2e-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ ДОВЕРИЕ \_ является \_ недоверенным \_ корнем** (&H00000020)</span><span class="sxs-lookup"><span data-stu-id="56d2e-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM\_TRUST\_IS\_UNTRUSTED\_ROOT** (&H00000020)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-124">Сертификат или цепочка сертификатов основаны на недоверенном корне.</span><span class="sxs-lookup"><span data-stu-id="56d2e-124">The certificate or certificate chain is based on an untrusted root.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span data-ttu-id="56d2e-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_ \_ \_ Неизвестное состояние отзыва доверия** (&H00000040)</span><span class="sxs-lookup"><span data-stu-id="56d2e-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM\_TRUST\_REVOCATION\_STATUS\_UNKNOWN** (&H00000040)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-126">Состояние отзыва сертификата или одного из сертификатов в цепочке сертификатов неизвестно.</span><span class="sxs-lookup"><span data-stu-id="56d2e-126">The revocation status of the certificate or one of the certificates in the certificate chain is unknown.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span data-ttu-id="56d2e-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ Отношение доверия \_ является \_ циклическим** (&H00000080)</span><span class="sxs-lookup"><span data-stu-id="56d2e-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM\_TRUST\_IS\_CYCLIC** (&H00000080)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-128">Один из сертификатов в цепочке выдан [*центром сертификации*](../secgloss/c-gly.md) , которому был сертифицирован исходный сертификат.</span><span class="sxs-lookup"><span data-stu-id="56d2e-128">One of the certificates in the chain was issued by a [*certification authority*](../secgloss/c-gly.md) that the original certificate had certified.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span data-ttu-id="56d2e-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_Недопустимое \_ расширение доверия** (&H00000100)</span><span class="sxs-lookup"><span data-stu-id="56d2e-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM\_TRUST\_INVALID\_EXTENSION** (&H00000100)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-130">Один из сертификатов имеет недопустимое расширение.</span><span class="sxs-lookup"><span data-stu-id="56d2e-130">One of the certificates has an extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span data-ttu-id="56d2e-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ ДОВЕРЯТЬ \_ недопустимым \_ \_ ограничениям политики** (&H00000200)</span><span class="sxs-lookup"><span data-stu-id="56d2e-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM\_TRUST\_INVALID\_POLICY\_CONSTRAINTS** (&H00000200)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-132">Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений политики, а один из выданных сертификатов имеет неразрешенное расширение сопоставления политик или не имеет необходимого расширения политик выдачи.</span><span class="sxs-lookup"><span data-stu-id="56d2e-132">The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span data-ttu-id="56d2e-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ ДОВЕРЯТЬ \_ недопустимым \_ базовым \_ ограничениям** (&H00000400)</span><span class="sxs-lookup"><span data-stu-id="56d2e-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM\_TRUST\_INVALID\_BASIC\_CONSTRAINTS** (&H00000400)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-134">Сертификат или один из сертификатов в цепочке сертификатов имеет расширение базовых ограничений, а либо сертификат не может использоваться для выдаче других сертификатов, либо превышена длина пути цепочки.</span><span class="sxs-lookup"><span data-stu-id="56d2e-134">The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span data-ttu-id="56d2e-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ ДОВЕРЯТЬ \_ недопустимым \_ \_ ограничениям имен** (&H00000800)</span><span class="sxs-lookup"><span data-stu-id="56d2e-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM\_TRUST\_INVALID\_NAME\_CONSTRAINTS** (&H00000800)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-136">Сертификат или один из сертификатов в цепочке сертификатов имеет недопустимое расширение ограничений имен.</span><span class="sxs-lookup"><span data-stu-id="56d2e-136">The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span data-ttu-id="56d2e-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ Отношение \_ доверия \_ не \_ поддерживает \_ \_ ограничение имен** (&H00001000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_SUPPORTED\_NAME\_CONSTRAINT** (&H00001000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-138">Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, которое содержит неподдерживаемые поля.</span><span class="sxs-lookup"><span data-stu-id="56d2e-138">The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields.</span></span> <span data-ttu-id="56d2e-139">Поля минимум и максимум не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="56d2e-139">The minimum and maximum fields are not supported.</span></span> <span data-ttu-id="56d2e-140">Таким, минимальное значение всегда должно быть нулевым, а максимальное — нет.</span><span class="sxs-lookup"><span data-stu-id="56d2e-140">Thus minimum must always be zero and maximum must always be absent.</span></span> <span data-ttu-id="56d2e-141">Для другого имени поддерживается только имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="56d2e-141">Only UPN is supported for an Other Name.</span></span> <span data-ttu-id="56d2e-142">Следующие варианты альтернативного имени не поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="56d2e-142">The following alternative name choices are not supported:</span></span>

-   <span data-ttu-id="56d2e-143">X400 адрес</span><span class="sxs-lookup"><span data-stu-id="56d2e-143">X400 Address</span></span>
-   <span data-ttu-id="56d2e-144">Имя субъекта EDI</span><span class="sxs-lookup"><span data-stu-id="56d2e-144">EDI Party Name</span></span>
-   <span data-ttu-id="56d2e-145">Зарегистрированный идентификатор</span><span class="sxs-lookup"><span data-stu-id="56d2e-145">Registered Id</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span data-ttu-id="56d2e-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ Отношение \_ доверия \_ не \_ определило \_ \_ ограничение имени** (&H00002000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_DEFINED\_NAME\_CONSTRAINT** (&H00002000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-147">Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, а для одного из вариантов имени в конечном сертификате отсутствует ограничение имени.</span><span class="sxs-lookup"><span data-stu-id="56d2e-147">The certificate or one of the certificates in the certificate chain has a name constraints extension, and a name constraint is missing for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span data-ttu-id="56d2e-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ \_ не имеет \_ разрешенного \_ \_ ограничения имен** (&H00004000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_PERMITTED\_NAME\_CONSTRAINT** (&H00004000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-149">Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, и для одного из вариантов имени в конечном сертификате не предусмотрено допустимое ограничение имени.</span><span class="sxs-lookup"><span data-stu-id="56d2e-149">The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span data-ttu-id="56d2e-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ Отношение доверия \_ имеет \_ исключенное \_ \_ ограничение имени** (&H00008000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_EXCLUDED\_NAME\_CONSTRAINT** (&H00008000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-151">Сертификат или один из сертификатов в цепочке сертификатов имеет расширение ограничений имен, и один из вариантов имени в конечном сертификате явно исключается.</span><span class="sxs-lookup"><span data-stu-id="56d2e-151">The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span data-ttu-id="56d2e-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ ДОВЕРИЕ \_ является \_ АВТОНОМным \_ отзывом** (&H01000000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM\_TRUST\_IS\_OFFLINE\_REVOCATION** (&H01000000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-153">Состояние отзыва сертификата или одного из сертификатов в цепочке сертификатов — «вне сети» или «устарело».</span><span class="sxs-lookup"><span data-stu-id="56d2e-153">The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span data-ttu-id="56d2e-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ \_Политика доверия \_ без \_ \_ политики цепочки выдачи** (&H02000000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM\_TRUST\_NO\_ISSUANCE\_CHAIN\_POLICY** (&H02000000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-155">У конечного сертификата нет результирующих политик выдачи, и у одного из выдающих сертификатов ЦС есть расширение ограничений политики, которое ему требуется.</span><span class="sxs-lookup"><span data-stu-id="56d2e-155">The end certificate does not have any resultant issuance policies, and one of the issuing CA certificates has a policy constraints extension requiring it.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span data-ttu-id="56d2e-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ ДОВЕРИЕ \_ является \_ частичной \_ цепочкой** (&H00010000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM\_TRUST\_IS\_PARTIAL\_CHAIN** (&H00010000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-157">Цепочка сертификатов не конкурирует.</span><span class="sxs-lookup"><span data-stu-id="56d2e-157">The certificate chain is not compete.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span data-ttu-id="56d2e-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ ДОВЕРЕНный \_ CTL доверия \_ \_ не является \_ \_ допустимым временем** (&H00020000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_TIME\_VALID** (&H00020000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-159">Список доверия сертификатов, используемый для создания этой цепочки, не является допустимым временем.</span><span class="sxs-lookup"><span data-stu-id="56d2e-159">A CTL used to create this chain was not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span data-ttu-id="56d2e-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ \_CTL доверия \_ \_ не является \_ \_ допустимым сигнатурой** (&H00040000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_SIGNATURE\_VALID** (&H00040000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-161">Список доверия сертификатов, используемый для создания этой цепочки, не имеет действительной подписи.</span><span class="sxs-lookup"><span data-stu-id="56d2e-161">A CTL used to create this chain did not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span data-ttu-id="56d2e-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ \_CTL доверия \_ \_ не \_ подходит \_ для \_ использования** (&H00080000)</span><span class="sxs-lookup"><span data-stu-id="56d2e-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00080000)</span></span>


</dt> <dd>

<span data-ttu-id="56d2e-163">Список доверия сертификатов, используемый для создания этой цепочки, недопустим для этого использования.</span><span class="sxs-lookup"><span data-stu-id="56d2e-163">A CTL used to create this chain is not valid for this usage.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56d2e-164">Требования</span><span class="sxs-lookup"><span data-stu-id="56d2e-164">Requirements</span></span>



| <span data-ttu-id="56d2e-165">Требование</span><span class="sxs-lookup"><span data-stu-id="56d2e-165">Requirement</span></span> | <span data-ttu-id="56d2e-166">Значение</span><span class="sxs-lookup"><span data-stu-id="56d2e-166">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56d2e-167">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="56d2e-167">End of client support</span></span><br/> | <span data-ttu-id="56d2e-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56d2e-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="56d2e-169">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="56d2e-169">End of server support</span></span><br/> | <span data-ttu-id="56d2e-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56d2e-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="56d2e-171">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="56d2e-171">Redistributable</span></span><br/>       | <span data-ttu-id="56d2e-172">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="56d2e-172">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="56d2e-173">DLL</span><span class="sxs-lookup"><span data-stu-id="56d2e-173">DLL</span></span><br/>                   | <dl> <span data-ttu-id="56d2e-174"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d2e-174"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
