---
description: Поддерживает цифровые подписи и шифрование данных. Он считается поставщиком служб шифрования общего назначения (CSP).
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081218"
---
# <a name="prov_rsa_aes"></a><span data-ttu-id="38755-104">PROV \_ RSA \_ AES</span><span class="sxs-lookup"><span data-stu-id="38755-104">PROV\_RSA\_AES</span></span>

<span data-ttu-id="38755-105">\_ \_ Тип поставщика RSA AES Prov поддерживает [цифровые подписи](digital-signatures.md) и шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="38755-105">The PROV\_RSA\_AES provider type supports both [digital signatures](digital-signatures.md) and data encryption.</span></span> <span data-ttu-id="38755-106">Он считается [*поставщиком служб шифрования*](../secgloss/c-gly.md) общего назначения (CSP).</span><span class="sxs-lookup"><span data-stu-id="38755-106">It is considered a general purpose [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="38755-107">[*Алгоритм открытого ключа*](../secgloss/p-gly.md) RSA используется для всех операций [*открытого ключа*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="38755-107">The RSA [*public key algorithm*](../secgloss/p-gly.md) is used for all [*public key*](../secgloss/p-gly.md) operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="38755-108">Поддерживаемые алгоритмы</span><span class="sxs-lookup"><span data-stu-id="38755-108">Algorithms Supported</span></span>

<span data-ttu-id="38755-109">Описание каждого из этих алгоритмов см. в глоссарии.</span><span class="sxs-lookup"><span data-stu-id="38755-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="38755-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="38755-110">Purpose</span></span>      | <span data-ttu-id="38755-111">Поддерживаемые алгоритмы</span><span class="sxs-lookup"><span data-stu-id="38755-111">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38755-112">Обмен ключами</span><span class="sxs-lookup"><span data-stu-id="38755-112">Key Exchange</span></span> | [<span data-ttu-id="38755-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="38755-113">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="38755-114">Подпись</span><span class="sxs-lookup"><span data-stu-id="38755-114">Signature</span></span>    | [<span data-ttu-id="38755-115">*RSA*</span><span class="sxs-lookup"><span data-stu-id="38755-115">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="38755-116">Шифрование</span><span class="sxs-lookup"><span data-stu-id="38755-116">Encryption</span></span>   | [<span data-ttu-id="38755-117">*RC2*</span><span class="sxs-lookup"><span data-stu-id="38755-117">*RC2*</span></span>](../secgloss/r-gly.md)<br/> [<span data-ttu-id="38755-118">*RC4;*</span><span class="sxs-lookup"><span data-stu-id="38755-118">*RC4*</span></span>](../secgloss/r-gly.md)<br/> <span data-ttu-id="38755-119">[*AES*](../secgloss/a-gly.md) (AES)</span><span class="sxs-lookup"><span data-stu-id="38755-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span></span> <br/>                                                       |
| <span data-ttu-id="38755-120">Хэширование</span><span class="sxs-lookup"><span data-stu-id="38755-120">Hashing</span></span>      | [<span data-ttu-id="38755-121">*MD2*</span><span class="sxs-lookup"><span data-stu-id="38755-121">*MD2*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="38755-122">*MD4*</span><span class="sxs-lookup"><span data-stu-id="38755-122">*MD4*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="38755-123">*MD5*</span><span class="sxs-lookup"><span data-stu-id="38755-123">*MD5*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="38755-124">*SHA-1*</span><span class="sxs-lookup"><span data-stu-id="38755-124">*SHA-1*</span></span>](../secgloss/s-gly.md)<br/> <span data-ttu-id="38755-125">SHA-2 (SHA-256, SHA-384 и SHA-512);</span><span class="sxs-lookup"><span data-stu-id="38755-125">SHA-2 (SHA-256, SHA-384, and SHA-512)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="38755-126">Сопутствующая документация</span><span class="sxs-lookup"><span data-stu-id="38755-126">Related Documentation</span></span>

<span data-ttu-id="38755-127">Этот тип поставщика определяется корпорацией Майкрософт и RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="38755-127">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="38755-128">Он описан в следующих документах:</span><span class="sxs-lookup"><span data-stu-id="38755-128">It is described in the following documents:</span></span>

-   <span data-ttu-id="38755-129">*Руководства программиста поставщика служб шифрования Майкрософт*, microsoft, 1996.</span><span class="sxs-lookup"><span data-stu-id="38755-129">*Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.</span></span>
-   <span data-ttu-id="38755-130">Лабораториях RSA, стандартов шифрования с открытым ключом, RSA Data Security, 1993 ноября.</span><span class="sxs-lookup"><span data-stu-id="38755-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

> [!Note]  
> <span data-ttu-id="38755-131">Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="38755-131">These resources may not be available in some languages and countries or regions.</span></span>

 

 

 
