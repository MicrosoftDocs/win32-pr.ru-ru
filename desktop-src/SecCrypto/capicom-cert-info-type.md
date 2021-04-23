---
description: Определяет, какие сведения должны быть запрошены из сертификата.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Перечисление CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665524"
---
# <a name="capicom_cert_info_type-enumeration"></a><span data-ttu-id="9c8f5-103">\_ \_ Перечисление типа сведений CAPICOM CERT \_</span><span class="sxs-lookup"><span data-stu-id="9c8f5-103">CAPICOM\_CERT\_INFO\_TYPE enumeration</span></span>

<span data-ttu-id="9c8f5-104">Тип **перечисления \_ CAPICOM \_ CERT \_ info** определяет, какие сведения должны быть запрошены из сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-104">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type defines what information is to be queried from a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="9c8f5-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="9c8f5-105">Members</span></span>



| <span data-ttu-id="9c8f5-106">Член</span><span class="sxs-lookup"><span data-stu-id="9c8f5-106">Member</span></span>                                         | <span data-ttu-id="9c8f5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9c8f5-107">Description</span></span>                                                                                  | <span data-ttu-id="9c8f5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9c8f5-108">Value</span></span> |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="9c8f5-109">**\_ \_ \_ имя субъекта сведений об CAPICOM \_ CERT \_**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-109">**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</span></span> | <span data-ttu-id="9c8f5-110">Возвращает отображаемое имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-110">Returns the display name of the certificate subject.</span></span><br/>                              | <span data-ttu-id="9c8f5-111">0</span><span class="sxs-lookup"><span data-stu-id="9c8f5-111">0</span></span>     |
| <span data-ttu-id="9c8f5-112">**\_ \_ \_ \_ необычное имя поставщика сведений CAPICOM CERT \_**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-112">**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</span></span>  | <span data-ttu-id="9c8f5-113">Возвращает отображаемое имя издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-113">Returns the display name of the issuer of the certificate.</span></span><br/>                        | <span data-ttu-id="9c8f5-114">1</span><span class="sxs-lookup"><span data-stu-id="9c8f5-114">1</span></span>     |
| <span data-ttu-id="9c8f5-115">**\_ \_ \_ \_ имя электронной почты субъекта сведений об CAPICOM CERT \_**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-115">**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</span></span>  | <span data-ttu-id="9c8f5-116">Возвращает адрес электронной почты субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-116">Returns the email address of the certificate subject.</span></span><br/>                             | <span data-ttu-id="9c8f5-117">2</span><span class="sxs-lookup"><span data-stu-id="9c8f5-117">2</span></span>     |
| <span data-ttu-id="9c8f5-118">**CAPICOM \_ CERT \_ info \_ \_ имя электронной почты поставщика \_**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-118">**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</span></span>   | <span data-ttu-id="9c8f5-119">Возвращает адрес электронной почты издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-119">Returns the email address of the issuer of the certificate.</span></span><br/>                       | <span data-ttu-id="9c8f5-120">3</span><span class="sxs-lookup"><span data-stu-id="9c8f5-120">3</span></span>     |
| <span data-ttu-id="9c8f5-121">**CAPICOM \_ \_ сведения о сертификате \_ субъект \_ имени участника-пользователя**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-121">**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</span></span>          | <span data-ttu-id="9c8f5-122">Возвращает имя участника-пользователя для субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-122">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="9c8f5-123">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-123">Introduced in CAPICOM 2.0.</span></span><br/>            | <span data-ttu-id="9c8f5-124">4</span><span class="sxs-lookup"><span data-stu-id="9c8f5-124">4</span></span>     |
| <span data-ttu-id="9c8f5-125">**\_ \_ \_ имя участника-пользователя для заверителя сертификата \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-125">**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</span></span>           | <span data-ttu-id="9c8f5-126">Возвращает имя участника-пользователя (UPN) издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="9c8f5-127">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-127">Introduced in CAPICOM 2.0.</span></span><br/>      | <span data-ttu-id="9c8f5-128">5</span><span class="sxs-lookup"><span data-stu-id="9c8f5-128">5</span></span>     |
| <span data-ttu-id="9c8f5-129">**\_ \_ \_ имя DNS субъекта сведений об \_ CAPICOM CERT \_**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-129">**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</span></span>    | <span data-ttu-id="9c8f5-130">Возвращает DNS-имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-130">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="9c8f5-131">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-131">Introduced in CAPICOM 2.0.</span></span><br/>       | <span data-ttu-id="9c8f5-132">6</span><span class="sxs-lookup"><span data-stu-id="9c8f5-132">6</span></span>     |
| <span data-ttu-id="9c8f5-133">**\_ \_ \_ \_ имя DNS-сервера поставщика сведений CAPICOM CERT \_**</span><span class="sxs-lookup"><span data-stu-id="9c8f5-133">**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</span></span>     | <span data-ttu-id="9c8f5-134">Возвращает DNS-имя издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-134">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="9c8f5-135">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9c8f5-135">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="9c8f5-136">7</span><span class="sxs-lookup"><span data-stu-id="9c8f5-136">7</span></span>     |



## <a name="remarks"></a><span data-ttu-id="9c8f5-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c8f5-137">Remarks</span></span>

<span data-ttu-id="9c8f5-138">Тип перечисления " **CAPICOM \_ CERT \_ info \_** " используется методом [**Certificate.-info**](certificate-getinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9c8f5-138">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type is used by the [**Certificate.GetInfo**](certificate-getinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8f5-139">Требования</span><span class="sxs-lookup"><span data-stu-id="9c8f5-139">Requirements</span></span>



| <span data-ttu-id="9c8f5-140">Требование</span><span class="sxs-lookup"><span data-stu-id="9c8f5-140">Requirement</span></span> | <span data-ttu-id="9c8f5-141">Значение</span><span class="sxs-lookup"><span data-stu-id="9c8f5-141">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8f5-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9c8f5-142">Redistributable</span></span><br/> | <span data-ttu-id="9c8f5-143">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c8f5-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="9c8f5-144">Header</span><span class="sxs-lookup"><span data-stu-id="9c8f5-144">Header</span></span><br/>          | <dl> <span data-ttu-id="9c8f5-145"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c8f5-145"><dt>Capicom.h</dt></span></span> </dl> |



 

 




