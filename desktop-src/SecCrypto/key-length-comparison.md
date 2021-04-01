---
description: Расширенный поставщик служб шифрования Майкрософт предоставляет приложение с более высокой безопасностью, чем в настоящее время доступно в базовом поставщике служб шифрования Майкрософт. Большая длина ключа позволяет пользователям более защищать конфиденциальные данные.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Сравнение длины ключа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913631"
---
# <a name="key-length-comparison"></a><span data-ttu-id="7c412-104">Сравнение длины ключа</span><span class="sxs-lookup"><span data-stu-id="7c412-104">Key Length Comparison</span></span>

<span data-ttu-id="7c412-105">Расширенный поставщик служб шифрования Майкрософт предоставляет приложение с более высокой безопасностью, чем в настоящее время доступно в базовом поставщике служб шифрования Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7c412-105">The Microsoft Enhanced Cryptographic Provider provides an application with stronger security than currently available with the Microsoft Base Cryptographic Provider.</span></span> <span data-ttu-id="7c412-106">Большая длина ключа позволяет пользователям более защищать конфиденциальные данные.</span><span class="sxs-lookup"><span data-stu-id="7c412-106">Greater key length gives users more protection for sensitive data.</span></span>

<span data-ttu-id="7c412-107">В следующей таблице перечислены [*длины ключей*](../secgloss/k-gly.md) по умолчанию, поддерживаемые базовым поставщиком, и Улучшенный поставщик для стандартных алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="7c412-107">The following table lists the default [*key lengths*](../secgloss/k-gly.md) supported by the Base Provider and the Enhanced Provider for standard algorithms.</span></span>



| <span data-ttu-id="7c412-108">Алгоритм</span><span class="sxs-lookup"><span data-stu-id="7c412-108">Algorithm</span></span>                                                                                | <span data-ttu-id="7c412-109">Базовый поставщик</span><span class="sxs-lookup"><span data-stu-id="7c412-109">Base Provider</span></span> | <span data-ttu-id="7c412-110">Надежные и расширенные поставщики</span><span class="sxs-lookup"><span data-stu-id="7c412-110">Strong and Enhanced Providers</span></span> |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| <span data-ttu-id="7c412-111">Обмен ключами RSA</span><span class="sxs-lookup"><span data-stu-id="7c412-111">RSA Key Exchange</span></span>                                                                         | <span data-ttu-id="7c412-112">512-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-112">512-bit</span></span>       | <span data-ttu-id="7c412-113">1 024-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-113">1,024-bit</span></span>                     |
| <span data-ttu-id="7c412-114">Подпись RSA</span><span class="sxs-lookup"><span data-stu-id="7c412-114">RSA Signature</span></span>                                                                            | <span data-ttu-id="7c412-115">512-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-115">512-bit</span></span>       | <span data-ttu-id="7c412-116">1 024-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-116">1,024-bit</span></span>                     |
| <span data-ttu-id="7c412-117">RC2</span><span class="sxs-lookup"><span data-stu-id="7c412-117">RC2</span></span>                                                                                      | <span data-ttu-id="7c412-118">40-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-118">40-bit</span></span>        | <span data-ttu-id="7c412-119">128-разрядное</span><span class="sxs-lookup"><span data-stu-id="7c412-119">128-bit</span></span>                       |
| <span data-ttu-id="7c412-120">RC4;</span><span class="sxs-lookup"><span data-stu-id="7c412-120">RC4</span></span>                                                                                      | <span data-ttu-id="7c412-121">40-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-121">40-bit</span></span>        | <span data-ttu-id="7c412-122">128-разрядное</span><span class="sxs-lookup"><span data-stu-id="7c412-122">128-bit</span></span>                       |
| <span data-ttu-id="7c412-123">DES</span><span class="sxs-lookup"><span data-stu-id="7c412-123">DES</span></span>                                                                                      | <span data-ttu-id="7c412-124">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7c412-124">Not supported</span></span> | <span data-ttu-id="7c412-125">56-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-125">56-bit</span></span>                        |
| <span data-ttu-id="7c412-126">[*Тройной алгоритм DES*](../secgloss/t-gly.md) (2 ключа)</span><span class="sxs-lookup"><span data-stu-id="7c412-126">[*Triple DES*](../secgloss/t-gly.md) (2-key)</span></span> | <span data-ttu-id="7c412-127">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7c412-127">Not supported</span></span> | <span data-ttu-id="7c412-128">112-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-128">112-bit</span></span>                       |
| <span data-ttu-id="7c412-129">Тройной алгоритм DES (3 ключа)</span><span class="sxs-lookup"><span data-stu-id="7c412-129">Triple DES (3-key)</span></span>                                                                       | <span data-ttu-id="7c412-130">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7c412-130">Not supported</span></span> | <span data-ttu-id="7c412-131">168-разрядный</span><span class="sxs-lookup"><span data-stu-id="7c412-131">168-bit</span></span>                       |



 

<span data-ttu-id="7c412-132">В расширенном поставщике поддерживаются алгоритмы [*des*](../secgloss/d-gly.md) и [*Triple DES*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7c412-132">[*DES*](../secgloss/d-gly.md) and [*Triple DES*](../secgloss/t-gly.md) algorithms are supported in the Enhanced Provider.</span></span>

<span data-ttu-id="7c412-133">Улучшенный поставщик обратно совместим с базовым поставщиком, распространяемым с более ранними версиями CryptoAPI, со следующим исключением.</span><span class="sxs-lookup"><span data-stu-id="7c412-133">The Enhanced Provider is backward-compatible with the Base Provider distributed with earlier versions of CryptoAPI with the following exception.</span></span> <span data-ttu-id="7c412-134">Как базовый, так и расширенный поставщик могут формировать только ключи сеанса длиной ключа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c412-134">Both the base provider and the Enhanced Provider can only generate session keys of default key length.</span></span> <span data-ttu-id="7c412-135">Длина ключей сеанса по умолчанию для базового поставщика составляет 40 бит.</span><span class="sxs-lookup"><span data-stu-id="7c412-135">The default length of session keys for the Base Provider is 40 bits.</span></span> <span data-ttu-id="7c412-136">Длина ключа по умолчанию для расширенного поставщика составляет 128 бит.</span><span class="sxs-lookup"><span data-stu-id="7c412-136">The default key length for the Enhanced Provider is 128 bits.</span></span> <span data-ttu-id="7c412-137">Улучшенный поставщик не может создавать ключи с длиной ключа, совместимой с базовым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="7c412-137">The Enhanced Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="7c412-138">Однако Улучшенный поставщик может импортировать длину ключей любого размера, до 128 бит.</span><span class="sxs-lookup"><span data-stu-id="7c412-138">However, the Enhanced Provider can import key lengths of any size, up to 128 bits.</span></span>

 

 
