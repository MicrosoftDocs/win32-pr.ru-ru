---
description: '\_ \_ Перечисление использования CAPICOM определяет способы использования ключа. Представлено в CAPICOM 2,0.'
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Перечисление CAPICOM_KEY_USAGE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648693"
---
# <a name="capicom_key_usage-enumeration"></a><span data-ttu-id="0594b-104">\_ \_ Перечисление использования CAPICOM Key</span><span class="sxs-lookup"><span data-stu-id="0594b-104">CAPICOM\_KEY\_USAGE enumeration</span></span>

<span data-ttu-id="0594b-105">Перечисление **\_ \_ использования CAPICOM** определяет способы использования ключа.</span><span class="sxs-lookup"><span data-stu-id="0594b-105">The **CAPICOM\_KEY\_USAGE** enumeration defines the ways in which a key can be used.</span></span> <span data-ttu-id="0594b-106">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="0594b-106">Introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="0594b-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="0594b-107">Members</span></span>



| <span data-ttu-id="0594b-108">Член</span><span class="sxs-lookup"><span data-stu-id="0594b-108">Member</span></span>                                      | <span data-ttu-id="0594b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0594b-109">Description</span></span>                                                                                                                      | <span data-ttu-id="0594b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0594b-110">Value</span></span>      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="0594b-111">**\_ \_ \_ Использование ключа цифровой подписи \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="0594b-111">**CAPICOM\_DIGITAL\_SIGNATURE\_KEY\_USAGE**</span></span> | <span data-ttu-id="0594b-112">Ключ можно использовать для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="0594b-112">The key can be used to create a digital signature.</span></span><br/>                                                                    | <span data-ttu-id="0594b-113">0x00000080</span><span class="sxs-lookup"><span data-stu-id="0594b-113">0x00000080</span></span> |
| <span data-ttu-id="0594b-114">**\_Использование ключа "CAPICOM не \_ отрицание" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0594b-114">**CAPICOM\_NON\_REPUDIATION\_KEY\_USAGE**</span></span>   | <span data-ttu-id="0594b-115">Ключ можно использовать для [*неподдельности*](../secgloss/n-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0594b-115">The key can be used for [*nonrepudiation*](../secgloss/n-gly.md).</span></span><br/> | <span data-ttu-id="0594b-116">0x00000040</span><span class="sxs-lookup"><span data-stu-id="0594b-116">0x00000040</span></span> |
| <span data-ttu-id="0594b-117">**\_ \_ \_ Использование ключа шифрования для ключа CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="0594b-117">**CAPICOM\_KEY\_ENCIPHERMENT\_KEY\_USAGE**</span></span>  | <span data-ttu-id="0594b-118">Ключ можно использовать для шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="0594b-118">The key can be used to encrypt a key.</span></span><br/>                                                                                 | <span data-ttu-id="0594b-119">0x00000020</span><span class="sxs-lookup"><span data-stu-id="0594b-119">0x00000020</span></span> |
| <span data-ttu-id="0594b-120">**\_ \_ Использование ключа для шифрования данных \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="0594b-120">**CAPICOM\_DATA\_ENCIPHERMENT\_KEY\_USAGE**</span></span> | <span data-ttu-id="0594b-121">Ключ можно использовать для шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="0594b-121">The key can be used to encrypt data.</span></span><br/>                                                                                  | <span data-ttu-id="0594b-122">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0594b-122">0x00000010</span></span> |
| <span data-ttu-id="0594b-123">**\_ \_ \_ Использование ключа соглашения "CAPICOM Key" \_**</span><span class="sxs-lookup"><span data-stu-id="0594b-123">**CAPICOM\_KEY\_AGREEMENT\_KEY\_USAGE**</span></span>     | <span data-ttu-id="0594b-124">Ключ можно использовать для соглашения Key.</span><span class="sxs-lookup"><span data-stu-id="0594b-124">The key can be used for key agreement.</span></span><br/>                                                                                | <span data-ttu-id="0594b-125">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0594b-125">0x00000008</span></span> |
| <span data-ttu-id="0594b-126">**\_ \_ \_ Использование ключа ПОДписывания \_ сертификата \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="0594b-126">**CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE**</span></span>    | <span data-ttu-id="0594b-127">Ключ можно использовать для подписи сертификата ключа.</span><span class="sxs-lookup"><span data-stu-id="0594b-127">The key can be used for key certificate signing.</span></span> <span data-ttu-id="0594b-128">Это значение эквивалентно \_ \_ \_ использованию ключа подписывания списка отзыва сертификатов CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0594b-128">This value is equivalent to CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE.</span></span><br/> | <span data-ttu-id="0594b-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0594b-129">0x00000004</span></span> |
| <span data-ttu-id="0594b-130">**сведения \_ \_ \_ \_ об использовании ключа для знака CAPICOM offline CRL \_**</span><span class="sxs-lookup"><span data-stu-id="0594b-130">**CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE**</span></span> | <span data-ttu-id="0594b-131">Ключ можно использовать для подписи сертификата ключа.</span><span class="sxs-lookup"><span data-stu-id="0594b-131">The key can be used for key certificate signing.</span></span> <span data-ttu-id="0594b-132">Это значение эквивалентно \_ \_ \_ использованию ключа подписи сертификата CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0594b-132">This value is equivalent to CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE.</span></span><br/>    | <span data-ttu-id="0594b-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0594b-133">0x00000002</span></span> |
| <span data-ttu-id="0594b-134">**\_ \_ \_ Использование ключа знака CAPICOM \_ CRL**</span><span class="sxs-lookup"><span data-stu-id="0594b-134">**CAPICOM\_CRL\_SIGN\_KEY\_USAGE**</span></span>          | <span data-ttu-id="0594b-135">Ключ можно использовать для подписывания.</span><span class="sxs-lookup"><span data-stu-id="0594b-135">The key can be used for signing.</span></span><br/>                                                                                      | <span data-ttu-id="0594b-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0594b-136">0x00000002</span></span> |
| <span data-ttu-id="0594b-137">**Использование элемента CAPICOM \_ шифрования паролей \_ только для \_ ключа \_**</span><span class="sxs-lookup"><span data-stu-id="0594b-137">**CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="0594b-138">Ключ можно использовать только для шифрования.</span><span class="sxs-lookup"><span data-stu-id="0594b-138">The key can only be used to encrypt.</span></span><br/>                                                                                  | <span data-ttu-id="0594b-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0594b-139">0x00000001</span></span> |
| <span data-ttu-id="0594b-140">**\_использование только CAPICOM для расшифровки \_ \_ ключа \_**</span><span class="sxs-lookup"><span data-stu-id="0594b-140">**CAPICOM\_DECIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="0594b-141">Ключ можно использовать только для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="0594b-141">The key can only be used to decrypt.</span></span><br/>                                                                                  | <span data-ttu-id="0594b-142">0x00008000</span><span class="sxs-lookup"><span data-stu-id="0594b-142">0x00008000</span></span> |



## <a name="requirements"></a><span data-ttu-id="0594b-143">Требования</span><span class="sxs-lookup"><span data-stu-id="0594b-143">Requirements</span></span>



| <span data-ttu-id="0594b-144">Требование</span><span class="sxs-lookup"><span data-stu-id="0594b-144">Requirement</span></span> | <span data-ttu-id="0594b-145">Значение</span><span class="sxs-lookup"><span data-stu-id="0594b-145">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0594b-146">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0594b-146">Redistributable</span></span><br/> | <span data-ttu-id="0594b-147">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0594b-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0594b-148">Header</span><span class="sxs-lookup"><span data-stu-id="0594b-148">Header</span></span><br/>          | <dl> <span data-ttu-id="0594b-149"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0594b-149"><dt>Capicom.h</dt></span></span> </dl> |



 

 
