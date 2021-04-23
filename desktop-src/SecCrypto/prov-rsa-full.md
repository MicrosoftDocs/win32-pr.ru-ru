---
description: Поддерживает цифровые подписи и шифрование данных. Он считается CSP общего назначения.
ms.assetid: 44b13a96-aba2-4b77-8e66-416aa0bcb8ad
title: PROV_RSA_FULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f473d49e2d27bfc26df7e655c50e039dffd550a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683944"
---
# <a name="prov_rsa_full"></a><span data-ttu-id="0cb25-104">PROV \_ RSA \_ Full</span><span class="sxs-lookup"><span data-stu-id="0cb25-104">PROV\_RSA\_FULL</span></span>

<span data-ttu-id="0cb25-105">\_ \_ Тип поставщика Prov RSA Full поддерживает [*цифровые подписи*](../secgloss/d-gly.md) и шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="0cb25-105">The PROV\_RSA\_FULL provider type supports both [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span> <span data-ttu-id="0cb25-106">Он считается CSP общего назначения.</span><span class="sxs-lookup"><span data-stu-id="0cb25-106">It is considered a general purpose CSP.</span></span> <span data-ttu-id="0cb25-107">Алгоритм открытого ключа RSA используется для всех операций открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="0cb25-107">The RSA public key algorithm is used for all public key operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="0cb25-108">Поддерживаемые алгоритмы</span><span class="sxs-lookup"><span data-stu-id="0cb25-108">Algorithms Supported</span></span>

<span data-ttu-id="0cb25-109">Описание каждого из этих алгоритмов см. в глоссарии.</span><span class="sxs-lookup"><span data-stu-id="0cb25-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="0cb25-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="0cb25-110">Purpose</span></span>      | <span data-ttu-id="0cb25-111">Поддерживаемые алгоритмы</span><span class="sxs-lookup"><span data-stu-id="0cb25-111">Supported algorithms</span></span>                                                                                                              |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb25-112">Обмен ключами</span><span class="sxs-lookup"><span data-stu-id="0cb25-112">Key Exchange</span></span> | [<span data-ttu-id="0cb25-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="0cb25-113">*RSA*</span></span>](../secgloss/r-gly.md)                                                                       |
| <span data-ttu-id="0cb25-114">Подпись</span><span class="sxs-lookup"><span data-stu-id="0cb25-114">Signature</span></span>    | <span data-ttu-id="0cb25-115">RSA</span><span class="sxs-lookup"><span data-stu-id="0cb25-115">RSA</span></span>                                                                                                                               |
| <span data-ttu-id="0cb25-116">Шифрование</span><span class="sxs-lookup"><span data-stu-id="0cb25-116">Encryption</span></span>   | <span data-ttu-id="0cb25-117">[*RC2*](../secgloss/r-gly.md)-[*RC4*](../secgloss/r-gly.md)</span><span class="sxs-lookup"><span data-stu-id="0cb25-117">[*RC2*](../secgloss/r-gly.md)[*RC4*](../secgloss/r-gly.md)</span></span><br/> |
| <span data-ttu-id="0cb25-118">Хэширование</span><span class="sxs-lookup"><span data-stu-id="0cb25-118">Hashing</span></span>      | <span data-ttu-id="0cb25-119">[*MD5*](../secgloss/m-gly.md)[*SHA*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="0cb25-119">[*MD5*](../secgloss/m-gly.md)[*SHA*](../secgloss/s-gly.md)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="0cb25-120">Сопутствующая документация</span><span class="sxs-lookup"><span data-stu-id="0cb25-120">Related Documentation</span></span>

<span data-ttu-id="0cb25-121">Этот тип поставщика определяется корпорацией Майкрософт и RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="0cb25-121">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="0cb25-122">Он описан в следующих документах:</span><span class="sxs-lookup"><span data-stu-id="0cb25-122">It is described in the following documents:</span></span>

-   <span data-ttu-id="0cb25-123">Лабораториях RSA, стандартов шифрования с открытым ключом, RSA Data Security, 1993 ноября.</span><span class="sxs-lookup"><span data-stu-id="0cb25-123">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

 

 
