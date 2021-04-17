---
description: Предоставляет доступ только для чтения к свойствам использования ключа сертификата.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Объект Кэйусаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685026"
---
# <a name="keyusage-object"></a><span data-ttu-id="c7338-103">Объект Кэйусаже</span><span class="sxs-lookup"><span data-stu-id="c7338-103">KeyUsage object</span></span>

<span data-ttu-id="c7338-104">\[Объект **кэйусаже** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c7338-104">\[The **KeyUsage** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7338-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c7338-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c7338-106">Объект **кэйусаже** предоставляет доступ только для чтения к свойствам использования ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="c7338-106">The **KeyUsage** object provides read-only access to key usage properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="c7338-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="c7338-107">Members</span></span>

<span data-ttu-id="c7338-108">Объект **кэйусаже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c7338-108">The **KeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="c7338-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7338-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7338-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7338-110">Properties</span></span>

<span data-ttu-id="c7338-111">Объект **кэйусаже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c7338-111">The **KeyUsage** object has these properties.</span></span>



| <span data-ttu-id="c7338-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="c7338-112">Property</span></span>                                                                           | <span data-ttu-id="c7338-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="c7338-113">Access type</span></span>          | <span data-ttu-id="c7338-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c7338-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7338-115">**Критическое**</span><span class="sxs-lookup"><span data-stu-id="c7338-115">**IsCritical**</span></span>](keyusage-iscritical.md)<br/>                               | <span data-ttu-id="c7338-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-116">Read-only</span></span><br/> | <span data-ttu-id="c7338-117">Получает логическое значение, указывающее, помечено ли расширение **кэйусаже** как критическое.</span><span class="sxs-lookup"><span data-stu-id="c7338-117">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is marked critical.</span></span><br/>                                  |
| [<span data-ttu-id="c7338-118">**искрлсигненаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-118">**IsCRLSignEnabled**</span></span>](keyusage-iscrlsignenabled.md)<br/>                   | <span data-ttu-id="c7338-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-119">Read-only</span></span><br/> | <span data-ttu-id="c7338-120">Получает логическое значение, указывающее, задан ли бит Крлсигн.</span><span class="sxs-lookup"><span data-stu-id="c7338-120">Retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span><br/>                                                         |
| [<span data-ttu-id="c7338-121">**исдатаенЦиферментенаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-121">**IsDataEnciphermentEnabled**</span></span>](keyusage-isdataenciphermentenabled.md)<br/> | <span data-ttu-id="c7338-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-122">Read-only</span></span><br/> | <span data-ttu-id="c7338-123">Получает логическое значение, указывающее, задан ли бит ДатаенЦифермент.</span><span class="sxs-lookup"><span data-stu-id="c7338-123">Retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="c7338-124">**исдеЦиферонленаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-124">**IsDecipherOnlyEnabled**</span></span>](keyusage-isdecipheronlyenabled.md)<br/>         | <span data-ttu-id="c7338-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-125">Read-only</span></span><br/> | <span data-ttu-id="c7338-126">Получает логическое значение, указывающее, задан ли бит ДеЦиферонли.</span><span class="sxs-lookup"><span data-stu-id="c7338-126">Retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="c7338-127">**исдигиталсигнатуринаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-127">**IsDigitalSignatureEnabled**</span></span>](keyusage-isdigitalsignatureenabled.md)<br/> | <span data-ttu-id="c7338-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-128">Read-only</span></span><br/> | <span data-ttu-id="c7338-129">Получает логическое значение, указывающее, задан ли бит Дигиталсигнатуре.</span><span class="sxs-lookup"><span data-stu-id="c7338-129">Retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="c7338-130">**исенЦиферонленаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-130">**IsEncipherOnlyEnabled**</span></span>](keyusage-isencipheronlyenabled.md)<br/>         | <span data-ttu-id="c7338-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-131">Read-only</span></span><br/> | <span data-ttu-id="c7338-132">Получает логическое значение, указывающее, задан ли бит ЕнЦиферонли.</span><span class="sxs-lookup"><span data-stu-id="c7338-132">Retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="c7338-133">**искэйагриментенаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-133">**IsKeyAgreementEnabled**</span></span>](keyusage-iskeyagreementenabled.md)<br/>         | <span data-ttu-id="c7338-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-134">Read-only</span></span><br/> | <span data-ttu-id="c7338-135">Получает логическое значение, указывающее, задан ли бит Кэйагримент.</span><span class="sxs-lookup"><span data-stu-id="c7338-135">Retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="c7338-136">**искэйцертсигненаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-136">**IsKeyCertSignEnabled**</span></span>](keyusage-iskeycertsignenabled.md)<br/>           | <span data-ttu-id="c7338-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-137">Read-only</span></span><br/> | <span data-ttu-id="c7338-138">Получает логическое значение, указывающее, задан ли бит Кэйцертсигн.</span><span class="sxs-lookup"><span data-stu-id="c7338-138">Retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span><br/>                                                     |
| [<span data-ttu-id="c7338-139">**искэйенЦиферментенаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-139">**IsKeyEnciphermentEnabled**</span></span>](keyusage-iskeyenciphermentenabled.md)<br/>   | <span data-ttu-id="c7338-140">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-140">Read-only</span></span><br/> | <span data-ttu-id="c7338-141">Получает логическое значение, указывающее, задан ли бит keyEncipherment.</span><span class="sxs-lookup"><span data-stu-id="c7338-141">Retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span><br/>                                                 |
| [<span data-ttu-id="c7338-142">**иснонрепудиатионенаблед**</span><span class="sxs-lookup"><span data-stu-id="c7338-142">**IsNonRepudiationEnabled**</span></span>](keyusage-isnonrepudiationenabled.md)<br/>     | <span data-ttu-id="c7338-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-143">Read-only</span></span><br/> | <span data-ttu-id="c7338-144">Получает логическое значение, указывающее, задан ли бит Нонрепудиатионенаблед.</span><span class="sxs-lookup"><span data-stu-id="c7338-144">Retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span><br/>                                           |
| [<span data-ttu-id="c7338-145">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="c7338-145">**IsPresent**</span></span>](keyusage-ispresent.md)<br/>                                 | <span data-ttu-id="c7338-146">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7338-146">Read-only</span></span><br/> | <span data-ttu-id="c7338-147">Получает логическое значение, указывающее, имеется ли расширение **кэйусаже** .</span><span class="sxs-lookup"><span data-stu-id="c7338-147">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is present.</span></span><br/> <span data-ttu-id="c7338-148">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7338-148">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7338-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7338-149">Remarks</span></span>

<span data-ttu-id="c7338-150">Не удается создать объект **кэйусаже** .</span><span class="sxs-lookup"><span data-stu-id="c7338-150">The **KeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7338-151">Требования</span><span class="sxs-lookup"><span data-stu-id="c7338-151">Requirements</span></span>



| <span data-ttu-id="c7338-152">Требование</span><span class="sxs-lookup"><span data-stu-id="c7338-152">Requirement</span></span> | <span data-ttu-id="c7338-153">Значение</span><span class="sxs-lookup"><span data-stu-id="c7338-153">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7338-154">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c7338-154">Redistributable</span></span><br/> | <span data-ttu-id="c7338-155">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7338-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c7338-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c7338-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="c7338-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7338-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7338-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7338-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7338-159">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="c7338-159">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
