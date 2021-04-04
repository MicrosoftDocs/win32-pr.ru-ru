---
description: Службы сертификатов поддерживают использование сертификатов, как определено в рекомендации ITU-T X. 509 (также ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Свойства сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908980"
---
# <a name="certificate-properties"></a><span data-ttu-id="1c4f3-103">Свойства сертификата</span><span class="sxs-lookup"><span data-stu-id="1c4f3-103">Certificate Properties</span></span>

<span data-ttu-id="1c4f3-104">Службы сертификатов поддерживают использование сертификатов, как определено в рекомендации ITU-T [*X. 509*](../secgloss/x-gly.md) (также ISO/IEC 9594-8).</span><span class="sxs-lookup"><span data-stu-id="1c4f3-104">Certificate Services supports the use of certificates as defined in the ITU-T recommendation [*X.509*](../secgloss/x-gly.md) (also, ISO/IEC 9594-8).</span></span> <span data-ttu-id="1c4f3-105">Ниже перечислены свойства, которые содержатся в стандартном сертификате X. 509.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-105">The following are properties that are contained in a standard X.509 certificate.</span></span>



| <span data-ttu-id="1c4f3-106">Поле</span><span class="sxs-lookup"><span data-stu-id="1c4f3-106">Field</span></span>                                       | <span data-ttu-id="1c4f3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1c4f3-107">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4f3-108">Версия</span><span class="sxs-lookup"><span data-stu-id="1c4f3-108">Version</span></span>                                     | <span data-ttu-id="1c4f3-109">Номер версии формата сертификата.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-109">Version number of the certificate format.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="1c4f3-110">Серийный номер</span><span class="sxs-lookup"><span data-stu-id="1c4f3-110">Serial Number</span></span>                               | <span data-ttu-id="1c4f3-111">Серийный номер сертификата.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-111">Serial number of the certificate.</span></span> <span data-ttu-id="1c4f3-112">Этот номер назначается издателем и уникален в списке выданных сертификатов поставщика.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-112">This number is assigned by the issuer and is unique within the issuer's list of issued certificates.</span></span>                                                                          |
| <span data-ttu-id="1c4f3-113">Идентификатор и параметры алгоритма</span><span class="sxs-lookup"><span data-stu-id="1c4f3-113">Algorithm Identifier and Parameters</span></span>         | <span data-ttu-id="1c4f3-114">Алгоритм подписи и все параметры, используемые издателем.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-114">Signature algorithm and any parameters used by the issuer.</span></span>                                                                                                                                                      |
| <span data-ttu-id="1c4f3-115">Издатель</span><span class="sxs-lookup"><span data-stu-id="1c4f3-115">Issuer</span></span>                                      | <span data-ttu-id="1c4f3-116">Имя [*центра сертификации*](../secgloss/c-gly.md) , который выдал сертификат.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-116">Name of the [*certification authority*](../secgloss/c-gly.md) which issued the certificate.</span></span>                                               |
| <span data-ttu-id="1c4f3-117">Не ранее (дата)</span><span class="sxs-lookup"><span data-stu-id="1c4f3-117">Not Before (Date)</span></span>                           | <span data-ttu-id="1c4f3-118">Сертификат не действителен до этой даты.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-118">Certificate not valid before this date.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="1c4f3-119">Не после (дата)</span><span class="sxs-lookup"><span data-stu-id="1c4f3-119">Not After (Date)</span></span>                            | <span data-ttu-id="1c4f3-120">Сертификат не действителен после этой даты.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-120">Certificate not valid after this date.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="1c4f3-121">Имя субъекта</span><span class="sxs-lookup"><span data-stu-id="1c4f3-121">Subject Name</span></span>                                | <span data-ttu-id="1c4f3-122">Имя пользователя или сущности, которым выдан сертификат.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-122">Name of the person or entity to whom the certificate is being issued.</span></span> <span data-ttu-id="1c4f3-123">Это поле может также включать в себя организацию получателя сертификата, организационную единицу, страну, штат или провинцию, страна или регион.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-123">This field can also include the certificate recipient's organization, organization unit, locality, state or province, and country/region.</span></span> |
| <span data-ttu-id="1c4f3-124">Алгоритм и параметры открытого ключа субъекта</span><span class="sxs-lookup"><span data-stu-id="1c4f3-124">Subject Public Key Algorithm and Parameters</span></span> | <span data-ttu-id="1c4f3-125">Алгоритм и все параметры, используемые для [*открытого ключа*](../secgloss/p-gly.md)субъекта.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-125">The algorithm and any parameters used for the subject's [*public key*](../secgloss/p-gly.md).</span></span>                                                                       |
| <span data-ttu-id="1c4f3-126">Открытый ключ субъекта</span><span class="sxs-lookup"><span data-stu-id="1c4f3-126">Subject Public Key</span></span>                          | <span data-ttu-id="1c4f3-127">Фактический открытый ключ (битовая строка).</span><span class="sxs-lookup"><span data-stu-id="1c4f3-127">The actual public key (a bit string).</span></span>                                                                                                                                                                           |
| <span data-ttu-id="1c4f3-128">Подпись</span><span class="sxs-lookup"><span data-stu-id="1c4f3-128">Signature</span></span>                                   | <span data-ttu-id="1c4f3-129">Сигнатура, предоставленная издателем.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-129">Signature as provided by the issuer.</span></span>                                                                                                                                                                            |



 

<span data-ttu-id="1c4f3-130">Сертификат может содержать следующие элементы в зависимости от версии сертификата [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1c4f3-130">A certificate can contain the following items, depending on the [*X.509*](../secgloss/x-gly.md) version of the certificate.</span></span>



| <span data-ttu-id="1c4f3-131">Необязательное поле</span><span class="sxs-lookup"><span data-stu-id="1c4f3-131">Optional field</span></span>    | <span data-ttu-id="1c4f3-132">Описание</span><span class="sxs-lookup"><span data-stu-id="1c4f3-132">Description</span></span>                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4f3-133">Уникальный идентификатор издателя</span><span class="sxs-lookup"><span data-stu-id="1c4f3-133">Issuer Unique ID</span></span>  | <span data-ttu-id="1c4f3-134">Используется для однозначного создания имени издателя, если оно использовалось более чем в одной сущности.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-134">Used to make the issuer name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="1c4f3-135">Имеется только в версиях [*X. 509*](../secgloss/x-gly.md) 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-135">Present only in versions [*X.509*](../secgloss/x-gly.md) 2.0 or later.</span></span><br/> |
| <span data-ttu-id="1c4f3-136">Уникальный идентификатор субъекта</span><span class="sxs-lookup"><span data-stu-id="1c4f3-136">Subject unique ID</span></span> | <span data-ttu-id="1c4f3-137">Используется, чтобы сделать имя субъекта неоднозначным, если оно использовалось более чем в одной сущности.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-137">Used to make the subject name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="1c4f3-138">Имеется только в X. 509 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-138">Present only in X.509 2.0 or later.</span></span><br/>                                                                     |
| <span data-ttu-id="1c4f3-139">Модули</span><span class="sxs-lookup"><span data-stu-id="1c4f3-139">Extensions</span></span>        | <span data-ttu-id="1c4f3-140">Для указания требуемых пользовательских свойств.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-140">For specifying any desired custom properties.</span></span> <span data-ttu-id="1c4f3-141">В сертификат можно включать любое количество полей расширения.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-141">Any number of extension fields can be included in the certificate.</span></span> <span data-ttu-id="1c4f3-142">Имеется только в версии X. 509 3,0.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-142">Present only in version X.509 3.0.</span></span><br/>                                            |



 

> [!Note]  
> <span data-ttu-id="1c4f3-143">Службы сертификации Майкрософт выпускают сертификаты X. 509 версии 3.</span><span class="sxs-lookup"><span data-stu-id="1c4f3-143">Microsoft Certificate Services issues X.509 version 3 certificates.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1c4f3-144">См. также</span><span class="sxs-lookup"><span data-stu-id="1c4f3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c4f3-145">Свойства имени</span><span class="sxs-lookup"><span data-stu-id="1c4f3-145">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
