---
description: Содержит сведения о создании цепочки доверия сертификатов.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Объект Цертификатестатус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665421"
---
# <a name="certificatestatus-object"></a><span data-ttu-id="20bb5-103">Объект Цертификатестатус</span><span class="sxs-lookup"><span data-stu-id="20bb5-103">CertificateStatus object</span></span>

<span data-ttu-id="20bb5-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="20bb5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="20bb5-105">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="20bb5-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="20bb5-106">Объект **цертификатестатус** содержит сведения о создании цепочки доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="20bb5-106">The **CertificateStatus** object contains information about how to construct a certificate trust chain.</span></span>

## <a name="members"></a><span data-ttu-id="20bb5-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="20bb5-107">Members</span></span>

<span data-ttu-id="20bb5-108">Объект **цертификатестатус** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="20bb5-108">The **CertificateStatus** object has these types of members:</span></span>

-   [<span data-ttu-id="20bb5-109">Методы</span><span class="sxs-lookup"><span data-stu-id="20bb5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="20bb5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="20bb5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20bb5-111">Методы</span><span class="sxs-lookup"><span data-stu-id="20bb5-111">Methods</span></span>

<span data-ttu-id="20bb5-112">Объект **цертификатестатус** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="20bb5-112">The **CertificateStatus** object has these methods.</span></span>



| <span data-ttu-id="20bb5-113">Метод</span><span class="sxs-lookup"><span data-stu-id="20bb5-113">Method</span></span>                                                               | <span data-ttu-id="20bb5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="20bb5-114">Description</span></span>                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20bb5-115">**аппликатионполиЦиес**</span><span class="sxs-lookup"><span data-stu-id="20bb5-115">**ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md) | <span data-ttu-id="20bb5-116">Возвращает коллекцию [**OID**](oids.md) , представляющую идентификатор объекта (OID) политики приложения.</span><span class="sxs-lookup"><span data-stu-id="20bb5-116">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs.</span></span><br/>                                           |
| [<span data-ttu-id="20bb5-117">**цертификатеполиЦиес**</span><span class="sxs-lookup"><span data-stu-id="20bb5-117">**CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md) | <span data-ttu-id="20bb5-118">Возвращает коллекцию [**OID**](oids.md) , представляющую идентификатор объекта (OID) политики сертификата, используемый во время построения цепочки.</span><span class="sxs-lookup"><span data-stu-id="20bb5-118">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs used during chain building.</span></span><br/>                |
| [<span data-ttu-id="20bb5-119">**EKU**</span><span class="sxs-lookup"><span data-stu-id="20bb5-119">**EKU**</span></span>](certificatestatus-eku.md)                                 | <span data-ttu-id="20bb5-120">Возвращает объект [**EKU**](eku.md) , используемый для задания элементов EKU, которые должны быть возвращены при установке состояния срока действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="20bb5-120">Returns the [**EKU**](eku.md) object used to set the EKU elements to be checked in establishing a certificate's validity status.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="20bb5-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="20bb5-121">Properties</span></span>

<span data-ttu-id="20bb5-122">Объект **цертификатестатус** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="20bb5-122">The **CertificateStatus** object has these properties.</span></span>



| <span data-ttu-id="20bb5-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="20bb5-123">Property</span></span>                                                                        | <span data-ttu-id="20bb5-124">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="20bb5-124">Access type</span></span>           | <span data-ttu-id="20bb5-125">Описание</span><span class="sxs-lookup"><span data-stu-id="20bb5-125">Description</span></span>                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20bb5-126">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="20bb5-126">**Certificates**</span></span>](certificatestatus-certificates.md)<br/>               | <span data-ttu-id="20bb5-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="20bb5-127">Read/write</span></span><br/> | <span data-ttu-id="20bb5-128">Задает или получает коллекцию сертификатов, которые можно использовать для построения цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="20bb5-128">Sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span><br/> <span data-ttu-id="20bb5-129">**CAPICOM 2.0.0.3 и более ранние версии:** Свойство [**Certificates**](certificatestatus-certificates.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="20bb5-129">**CAPICOM 2.0.0.3 and earlier:** The [**Certificates**](certificatestatus-certificates.md) property is not supported.</span></span><br/>                    |
| [<span data-ttu-id="20bb5-130">**чеккфлаг**</span><span class="sxs-lookup"><span data-stu-id="20bb5-130">**CheckFlag**</span></span>](certificatestatus-checkflag.md)<br/>                     | <span data-ttu-id="20bb5-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="20bb5-131">Read/write</span></span><br/> | <span data-ttu-id="20bb5-132">Флаг проверки достоверности.</span><span class="sxs-lookup"><span data-stu-id="20bb5-132">Validity check flag.</span></span> <span data-ttu-id="20bb5-133">Значения можно объединить с помощью логического оператора **или** .</span><span class="sxs-lookup"><span data-stu-id="20bb5-133">Values can be joined by using a logical **OR** operator.</span></span> <span data-ttu-id="20bb5-134">Флаг проверки по умолчанию — [**CAPICOM \_ Check on \_ Online \_**](capicom-check-flag.md).</span><span class="sxs-lookup"><span data-stu-id="20bb5-134">The default check flag is [**CAPICOM\_CHECK\_ONLINE\_ALL**](capicom-check-flag.md).</span></span><br/>                                                                                     |
| [<span data-ttu-id="20bb5-135">**Результат**</span><span class="sxs-lookup"><span data-stu-id="20bb5-135">**Result**</span></span>](certificatestatus-result.md)<br/>                           | <span data-ttu-id="20bb5-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="20bb5-136">Read-only</span></span><br/>  | <span data-ttu-id="20bb5-137">Указывает, действителен ли сертификат.</span><span class="sxs-lookup"><span data-stu-id="20bb5-137">Indicates whether the certificate is valid.</span></span> <span data-ttu-id="20bb5-138">Срок действия сертификата проверяется с использованием текущего значения свойства [**чеккфлаг**](certificatestatus-checkflag.md) и параметров политики сертификата.</span><span class="sxs-lookup"><span data-stu-id="20bb5-138">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the policy settings of the certificate.</span></span> <span data-ttu-id="20bb5-139">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20bb5-139">This is the default property.</span></span><br/> |
| [<span data-ttu-id="20bb5-140">**урлретриевалтимеаут**</span><span class="sxs-lookup"><span data-stu-id="20bb5-140">**UrlRetrievalTimeout**</span></span>](certificatestatus-urlretrievaltimeout.md)<br/> | <span data-ttu-id="20bb5-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="20bb5-141">Read/write</span></span><br/> | <span data-ttu-id="20bb5-142">Задает или получает продолжительность времени до того, как URL-адрес будет определен как недоступный.</span><span class="sxs-lookup"><span data-stu-id="20bb5-142">Sets or retrieves the length of time before a URL is determined to be unreachable.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="20bb5-143">**верификатионтиме**</span><span class="sxs-lookup"><span data-stu-id="20bb5-143">**VerificationTime**</span></span>](certificatestatus-verificationtime.md)<br/>       | <span data-ttu-id="20bb5-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="20bb5-144">Read/write</span></span><br/> | <span data-ttu-id="20bb5-145">Задает или получает время проверки сертификата.</span><span class="sxs-lookup"><span data-stu-id="20bb5-145">Sets or retrieves the time that the certificate was verified.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="20bb5-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20bb5-146">Remarks</span></span>

<span data-ttu-id="20bb5-147">Не удается создать объект **цертификатестатус** .</span><span class="sxs-lookup"><span data-stu-id="20bb5-147">The **CertificateStatus** object cannot be created.</span></span>

<span data-ttu-id="20bb5-148">Объект **цертификатестатус** возвращается методом [**Certificate. IsValid**](certificate-isvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="20bb5-148">The **CertificateStatus** object is returned by the [**Certificate.IsValid**](certificate-isvalid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bb5-149">Требования</span><span class="sxs-lookup"><span data-stu-id="20bb5-149">Requirements</span></span>



| <span data-ttu-id="20bb5-150">Требование</span><span class="sxs-lookup"><span data-stu-id="20bb5-150">Requirement</span></span> | <span data-ttu-id="20bb5-151">Значение</span><span class="sxs-lookup"><span data-stu-id="20bb5-151">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20bb5-152">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="20bb5-152">End of client support</span></span><br/> | <span data-ttu-id="20bb5-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20bb5-153">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="20bb5-154">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="20bb5-154">End of server support</span></span><br/> | <span data-ttu-id="20bb5-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20bb5-155">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="20bb5-156">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="20bb5-156">Redistributable</span></span><br/>       | <span data-ttu-id="20bb5-157">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="20bb5-157">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="20bb5-158">DLL</span><span class="sxs-lookup"><span data-stu-id="20bb5-158">DLL</span></span><br/>                   | <dl> <span data-ttu-id="20bb5-159"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20bb5-159"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bb5-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20bb5-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bb5-161">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="20bb5-161">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="20bb5-162">**Цепочк**</span><span class="sxs-lookup"><span data-stu-id="20bb5-162">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
