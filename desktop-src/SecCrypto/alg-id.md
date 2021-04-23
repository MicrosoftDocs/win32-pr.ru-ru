---
description: Задает идентификатор алгоритма.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664639"
---
# <a name="alg_id"></a><span data-ttu-id="26abd-103">ALG_ID</span><span class="sxs-lookup"><span data-stu-id="26abd-103">ALG_ID</span></span>

<span data-ttu-id="26abd-104">Тип данных **ALG_ID** задает идентификатор алгоритма.</span><span class="sxs-lookup"><span data-stu-id="26abd-104">The **ALG_ID** data type specifies an algorithm identifier.</span></span> <span data-ttu-id="26abd-105">Параметры этого типа данных передаются большинству функций в CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="26abd-105">Parameters of this data type are passed to most of the functions in CryptoAPI.</span></span>


```C++
typedef unsigned int ALG_ID;
```



<span data-ttu-id="26abd-106">В следующей таблице перечислены идентификаторы алгоритмов, которые в настоящее время определены.</span><span class="sxs-lookup"><span data-stu-id="26abd-106">The following table lists the algorithm identifiers that are currently defined.</span></span> <span data-ttu-id="26abd-107">Авторы пользовательских [*поставщиков служб шифрования*](../secgloss/c-gly.md) (CSP) могут определять новые значения.</span><span class="sxs-lookup"><span data-stu-id="26abd-107">Authors of custom [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs) can define new values.</span></span> <span data-ttu-id="26abd-108">Кроме того, **ALG_ID** , используемые пользовательскими CSP для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , являются зависимыми от поставщика.</span><span class="sxs-lookup"><span data-stu-id="26abd-108">Also, the **ALG_ID** used by custom CSPs for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are provider dependent.</span></span> <span data-ttu-id="26abd-109">Текущие сопоставления следуют таблице.</span><span class="sxs-lookup"><span data-stu-id="26abd-109">Current mappings follow the table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26abd-110">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="26abd-110">Identifier</span></span></th>
<th><span data-ttu-id="26abd-111">Значение</span><span class="sxs-lookup"><span data-stu-id="26abd-111">Value</span></span></th>
<th><span data-ttu-id="26abd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="26abd-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26abd-113">CALG_3DES</span><span class="sxs-lookup"><span data-stu-id="26abd-113">CALG_3DES</span></span></td>
<td><span data-ttu-id="26abd-114">0x00006603</span><span class="sxs-lookup"><span data-stu-id="26abd-114">0x00006603</span></span></td>
<td><span data-ttu-id="26abd-115">Алгоритм шифрования <a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> .</span><span class="sxs-lookup"><span data-stu-id="26abd-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-116">CALG_3DES_112</span><span class="sxs-lookup"><span data-stu-id="26abd-116">CALG_3DES_112</span></span></td>
<td><span data-ttu-id="26abd-117">0x00006609</span><span class="sxs-lookup"><span data-stu-id="26abd-117">0x00006609</span></span></td>
<td><span data-ttu-id="26abd-118"><a href="/windows/desktop/SecGloss/t-gly"><em>Тройное шифрование Triple DES</em></a> с действующей длиной ключа, равной 112 битам.</span><span class="sxs-lookup"><span data-stu-id="26abd-118">Two-key <a href="/windows/desktop/SecGloss/t-gly"><em>triple DES</em></a> encryption with effective key length equal to 112 bits.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-119">CALG_AES</span><span class="sxs-lookup"><span data-stu-id="26abd-119">CALG_AES</span></span></td>
<td><span data-ttu-id="26abd-120">0x00006611</span><span class="sxs-lookup"><span data-stu-id="26abd-120">0x00006611</span></span></td>
<td><span data-ttu-id="26abd-121">AES (AES).</span><span class="sxs-lookup"><span data-stu-id="26abd-121">Advanced Encryption Standard (AES).</span></span> <span data-ttu-id="26abd-122">Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-122">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-123">CALG_AES_128</span><span class="sxs-lookup"><span data-stu-id="26abd-123">CALG_AES_128</span></span></td>
<td><span data-ttu-id="26abd-124">0x0000660e</span><span class="sxs-lookup"><span data-stu-id="26abd-124">0x0000660e</span></span></td>
<td><span data-ttu-id="26abd-125">128 разрядов AES.</span><span class="sxs-lookup"><span data-stu-id="26abd-125">128 bit AES.</span></span> <span data-ttu-id="26abd-126">Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-126">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-127">CALG_AES_192</span><span class="sxs-lookup"><span data-stu-id="26abd-127">CALG_AES_192</span></span></td>
<td><span data-ttu-id="26abd-128">0x0000660f</span><span class="sxs-lookup"><span data-stu-id="26abd-128">0x0000660f</span></span></td>
<td><span data-ttu-id="26abd-129">192 разрядов AES.</span><span class="sxs-lookup"><span data-stu-id="26abd-129">192 bit AES.</span></span> <span data-ttu-id="26abd-130">Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-130">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-131">CALG_AES_256</span><span class="sxs-lookup"><span data-stu-id="26abd-131">CALG_AES_256</span></span></td>
<td><span data-ttu-id="26abd-132">0x00006610</span><span class="sxs-lookup"><span data-stu-id="26abd-132">0x00006610</span></span></td>
<td><span data-ttu-id="26abd-133">256 разрядов AES.</span><span class="sxs-lookup"><span data-stu-id="26abd-133">256 bit AES.</span></span> <span data-ttu-id="26abd-134">Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-134">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-135">CALG_AGREEDKEY_ANY</span><span class="sxs-lookup"><span data-stu-id="26abd-135">CALG_AGREEDKEY_ANY</span></span></td>
<td><span data-ttu-id="26abd-136">0x0000aa03</span><span class="sxs-lookup"><span data-stu-id="26abd-136">0x0000aa03</span></span></td>
<td><span data-ttu-id="26abd-137">Временный идентификатор алгоритма для дескрипторов согласованных ключей Диффи-Хелмана.</span><span class="sxs-lookup"><span data-stu-id="26abd-137">Temporary algorithm identifier for handles of Diffie-Hellman–agreed keys.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-138">CALG_CYLINK_MEK</span><span class="sxs-lookup"><span data-stu-id="26abd-138">CALG_CYLINK_MEK</span></span></td>
<td><span data-ttu-id="26abd-139">0x0000660c</span><span class="sxs-lookup"><span data-stu-id="26abd-139">0x0000660c</span></span></td>
<td><span data-ttu-id="26abd-140">Алгоритм для создания 40-разрядного ключа DES с битами четности и нулевыми битами ключа для обеспечения длины ключа 64 бит.</span><span class="sxs-lookup"><span data-stu-id="26abd-140">An algorithm to create a 40-bit DES key that has parity bits and zeroed key bits to make its key length 64 bits.</span></span> <span data-ttu-id="26abd-141">Этот алгоритм поддерживается в <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-141">This algorithm is supported by the <a href=""></a><a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-142">CALG_DES</span><span class="sxs-lookup"><span data-stu-id="26abd-142">CALG_DES</span></span></td>
<td><span data-ttu-id="26abd-143">0x00006601</span><span class="sxs-lookup"><span data-stu-id="26abd-143">0x00006601</span></span></td>
<td><span data-ttu-id="26abd-144">Алгоритм шифрования DES.</span><span class="sxs-lookup"><span data-stu-id="26abd-144">DES encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-145">CALG_DESX</span><span class="sxs-lookup"><span data-stu-id="26abd-145">CALG_DESX</span></span></td>
<td><span data-ttu-id="26abd-146">0x00006604</span><span class="sxs-lookup"><span data-stu-id="26abd-146">0x00006604</span></span></td>
<td><span data-ttu-id="26abd-147">Алгоритм шифрования DESX.</span><span class="sxs-lookup"><span data-stu-id="26abd-147">DESX encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-148">CALG_DH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="26abd-148">CALG_DH_EPHEM</span></span></td>
<td><span data-ttu-id="26abd-149">0x0000aa02</span><span class="sxs-lookup"><span data-stu-id="26abd-149">0x0000aa02</span></span></td>
<td><span data-ttu-id="26abd-150">Алгоритм обмена ключами с временным ключом Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="26abd-150">Diffie-Hellman ephemeral key exchange algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-151">CALG_DH_SF</span><span class="sxs-lookup"><span data-stu-id="26abd-151">CALG_DH_SF</span></span></td>
<td><span data-ttu-id="26abd-152">0x0000aa01</span><span class="sxs-lookup"><span data-stu-id="26abd-152">0x0000aa01</span></span></td>
<td><span data-ttu-id="26abd-153">Алгоритм обмена ключами с Diffie-Hellman Store и forward.</span><span class="sxs-lookup"><span data-stu-id="26abd-153">Diffie-Hellman store and forward key exchange algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-154">CALG_DSS_SIGN</span><span class="sxs-lookup"><span data-stu-id="26abd-154">CALG_DSS_SIGN</span></span></td>
<td><span data-ttu-id="26abd-155">0x00002200</span><span class="sxs-lookup"><span data-stu-id="26abd-155">0x00002200</span></span></td>
<td><span data-ttu-id="26abd-156">Алгоритм подписи <a href="/windows/desktop/SecGloss/p-gly"><em>открытого ключа</em></a> DSA.</span><span class="sxs-lookup"><span data-stu-id="26abd-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>public key</em></a> signature algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-157">CALG_ECDH</span><span class="sxs-lookup"><span data-stu-id="26abd-157">CALG_ECDH</span></span></td>
<td><span data-ttu-id="26abd-158">0x0000aa05</span><span class="sxs-lookup"><span data-stu-id="26abd-158">0x0000aa05</span></span></td>
<td><span data-ttu-id="26abd-159">Алгоритм обмена ключами на эллиптической кривой Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="26abd-159">Elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="26abd-160">Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-160">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="26abd-161"><strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-161"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-162">CALG_ECDH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="26abd-162">CALG_ECDH_EPHEM</span></span></td>
<td><span data-ttu-id="26abd-163">0x0000ae06</span><span class="sxs-lookup"><span data-stu-id="26abd-163">0x0000ae06</span></span></td>
<td><span data-ttu-id="26abd-164">Многовременная эллиптическая кривая Diffie-Hellman алгоритм обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="26abd-164">Ephemeral elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="26abd-165">Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-165">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="26abd-166"><strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-166"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-167">CALG_ECDSA</span><span class="sxs-lookup"><span data-stu-id="26abd-167">CALG_ECDSA</span></span></td>
<td><span data-ttu-id="26abd-168">0x00002203</span><span class="sxs-lookup"><span data-stu-id="26abd-168">0x00002203</span></span></td>
<td><span data-ttu-id="26abd-169">Алгоритм цифровых подписей на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="26abd-169">Elliptic curve digital signature algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="26abd-170">Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-170">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="26abd-171"><strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-171"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-172">CALG_ECMQV</span><span class="sxs-lookup"><span data-stu-id="26abd-172">CALG_ECMQV</span></span></td>
<td><span data-ttu-id="26abd-173">0x0000a001</span><span class="sxs-lookup"><span data-stu-id="26abd-173">0x0000a001</span></span></td>
<td><span data-ttu-id="26abd-174">Алгоритм обмена ключами на эллиптических кривых Менезес, qu и Ванстоне (МКВ).</span><span class="sxs-lookup"><span data-stu-id="26abd-174">Elliptic curve Menezes, Qu, and Vanstone (MQV) key exchange algorithm.</span></span> <span data-ttu-id="26abd-175">Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-175">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-176">CALG_HASH_REPLACE_OWF</span><span class="sxs-lookup"><span data-stu-id="26abd-176">CALG_HASH_REPLACE_OWF</span></span></td>
<td><span data-ttu-id="26abd-177">0x0000800b</span><span class="sxs-lookup"><span data-stu-id="26abd-177">0x0000800b</span></span></td>
<td><span data-ttu-id="26abd-178">Один из способов хэширования функций.</span><span class="sxs-lookup"><span data-stu-id="26abd-178">One way function hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-179">CALG_HUGHES_MD5</span><span class="sxs-lookup"><span data-stu-id="26abd-179">CALG_HUGHES_MD5</span></span></td>
<td><span data-ttu-id="26abd-180">0x0000a003</span><span class="sxs-lookup"><span data-stu-id="26abd-180">0x0000a003</span></span></td>
<td><span data-ttu-id="26abd-181">Алгоритм хэширования MD5 Хьюз.</span><span class="sxs-lookup"><span data-stu-id="26abd-181">Hughes MD5 hashing algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-182">CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="26abd-182">CALG_HMAC</span></span></td>
<td><span data-ttu-id="26abd-183">0x00008009</span><span class="sxs-lookup"><span data-stu-id="26abd-183">0x00008009</span></span></td>
<td><span data-ttu-id="26abd-184">Хэш-алгоритм с ключом HMAC.</span><span class="sxs-lookup"><span data-stu-id="26abd-184">HMAC keyed hash algorithm.</span></span> <span data-ttu-id="26abd-185">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-185">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-186">CALG_KEA_KEYX</span><span class="sxs-lookup"><span data-stu-id="26abd-186">CALG_KEA_KEYX</span></span></td>
<td><span data-ttu-id="26abd-187">0x0000aa04</span><span class="sxs-lookup"><span data-stu-id="26abd-187">0x0000aa04</span></span></td>
<td><span data-ttu-id="26abd-188">Алгоритм обмена ключами Кеа (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="26abd-188">KEA key exchange algorithm (FORTEZZA).</span></span> <span data-ttu-id="26abd-189">Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-189">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-190">CALG_MAC</span><span class="sxs-lookup"><span data-stu-id="26abd-190">CALG_MAC</span></span></td>
<td><span data-ttu-id="26abd-191">0x00008005</span><span class="sxs-lookup"><span data-stu-id="26abd-191">0x00008005</span></span></td>
<td><span data-ttu-id="26abd-192">Хэш-алгоритм с ключом <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> .</span><span class="sxs-lookup"><span data-stu-id="26abd-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> keyed hash algorithm.</span></span> <span data-ttu-id="26abd-193">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-193">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-194">CALG_MD2</span><span class="sxs-lookup"><span data-stu-id="26abd-194">CALG_MD2</span></span></td>
<td><span data-ttu-id="26abd-195">0x00008001</span><span class="sxs-lookup"><span data-stu-id="26abd-195">0x00008001</span></span></td>
<td><span data-ttu-id="26abd-196">Алгоритм хэширования MD2.</span><span class="sxs-lookup"><span data-stu-id="26abd-196">MD2 hashing algorithm.</span></span> <span data-ttu-id="26abd-197">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-197">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-198">CALG_MD4</span><span class="sxs-lookup"><span data-stu-id="26abd-198">CALG_MD4</span></span></td>
<td><span data-ttu-id="26abd-199">0x00008002</span><span class="sxs-lookup"><span data-stu-id="26abd-199">0x00008002</span></span></td>
<td><span data-ttu-id="26abd-200">Алгоритм хэширования MD4.</span><span class="sxs-lookup"><span data-stu-id="26abd-200">MD4 hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-201">CALG_MD5</span><span class="sxs-lookup"><span data-stu-id="26abd-201">CALG_MD5</span></span></td>
<td><span data-ttu-id="26abd-202">0x00008003</span><span class="sxs-lookup"><span data-stu-id="26abd-202">0x00008003</span></span></td>
<td><span data-ttu-id="26abd-203">Алгоритм хэширования MD5.</span><span class="sxs-lookup"><span data-stu-id="26abd-203">MD5 hashing algorithm.</span></span> <span data-ttu-id="26abd-204">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-204">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-205">CALG_NO_SIGN</span><span class="sxs-lookup"><span data-stu-id="26abd-205">CALG_NO_SIGN</span></span></td>
<td><span data-ttu-id="26abd-206">0x00002000</span><span class="sxs-lookup"><span data-stu-id="26abd-206">0x00002000</span></span></td>
<td><span data-ttu-id="26abd-207">Нет алгоритма подписи.</span><span class="sxs-lookup"><span data-stu-id="26abd-207">No signature algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-208">CALG_OID_INFO_CNG_ONLY</span><span class="sxs-lookup"><span data-stu-id="26abd-208">CALG_OID_INFO_CNG_ONLY</span></span></td>
<td><span data-ttu-id="26abd-209">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="26abd-209">0xffffffff</span></span></td>
<td><span data-ttu-id="26abd-210">Алгоритм реализуется только в CNG.</span><span class="sxs-lookup"><span data-stu-id="26abd-210">The algorithm is only implemented in CNG.</span></span> <span data-ttu-id="26abd-211">Макрос IS_SPECIAL_OID_INFO_ALGID можно использовать, чтобы определить, поддерживается ли алгоритм шифрования только с помощью функций CNG.</span><span class="sxs-lookup"><span data-stu-id="26abd-211">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-212">CALG_OID_INFO_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26abd-212">CALG_OID_INFO_PARAMETERS</span></span></td>
<td><span data-ttu-id="26abd-213">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="26abd-213">0xfffffffe</span></span></td>
<td><span data-ttu-id="26abd-214">Алгоритм определяется в закодированных параметрах.</span><span class="sxs-lookup"><span data-stu-id="26abd-214">The algorithm is defined in the encoded parameters.</span></span> <span data-ttu-id="26abd-215">Алгоритм поддерживается только с помощью CNG.</span><span class="sxs-lookup"><span data-stu-id="26abd-215">The algorithm is only supported by using CNG.</span></span> <span data-ttu-id="26abd-216">Макрос IS_SPECIAL_OID_INFO_ALGID можно использовать, чтобы определить, поддерживается ли алгоритм шифрования только с помощью функций CNG.</span><span class="sxs-lookup"><span data-stu-id="26abd-216">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-217">CALG_PCT1_MASTER</span><span class="sxs-lookup"><span data-stu-id="26abd-217">CALG_PCT1_MASTER</span></span></td>
<td><span data-ttu-id="26abd-218">0x00004c04</span><span class="sxs-lookup"><span data-stu-id="26abd-218">0x00004c04</span></span></td>
<td><span data-ttu-id="26abd-219">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-219">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-220">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-220">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-221">CALG_RC2</span><span class="sxs-lookup"><span data-stu-id="26abd-221">CALG_RC2</span></span></td>
<td><span data-ttu-id="26abd-222">0x00006602</span><span class="sxs-lookup"><span data-stu-id="26abd-222">0x00006602</span></span></td>
<td><span data-ttu-id="26abd-223">Алгоритм шифрования блока RC2.</span><span class="sxs-lookup"><span data-stu-id="26abd-223">RC2 block encryption algorithm.</span></span> <span data-ttu-id="26abd-224">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-224">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-225">CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="26abd-225">CALG_RC4</span></span></td>
<td><span data-ttu-id="26abd-226">0x00006801</span><span class="sxs-lookup"><span data-stu-id="26abd-226">0x00006801</span></span></td>
<td><span data-ttu-id="26abd-227">Алгоритм шифрования потока RC4.</span><span class="sxs-lookup"><span data-stu-id="26abd-227">RC4 stream encryption algorithm.</span></span> <span data-ttu-id="26abd-228">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-228">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-229">CALG_RC5</span><span class="sxs-lookup"><span data-stu-id="26abd-229">CALG_RC5</span></span></td>
<td><span data-ttu-id="26abd-230">0x0000660d</span><span class="sxs-lookup"><span data-stu-id="26abd-230">0x0000660d</span></span></td>
<td><span data-ttu-id="26abd-231">Алгоритм шифрования блока RC5.</span><span class="sxs-lookup"><span data-stu-id="26abd-231">RC5 block encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-232">CALG_RSA_KEYX</span><span class="sxs-lookup"><span data-stu-id="26abd-232">CALG_RSA_KEYX</span></span></td>
<td><span data-ttu-id="26abd-233">0x0000a400</span><span class="sxs-lookup"><span data-stu-id="26abd-233">0x0000a400</span></span></td>
<td><span data-ttu-id="26abd-234">Алгоритм обмена открытыми ключами RSA.</span><span class="sxs-lookup"><span data-stu-id="26abd-234">RSA public key exchange algorithm.</span></span> <span data-ttu-id="26abd-235">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-235">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-236">CALG_RSA_SIGN</span><span class="sxs-lookup"><span data-stu-id="26abd-236">CALG_RSA_SIGN</span></span></td>
<td><span data-ttu-id="26abd-237">0x00002400</span><span class="sxs-lookup"><span data-stu-id="26abd-237">0x00002400</span></span></td>
<td><span data-ttu-id="26abd-238">Алгоритм подписи открытого ключа RSA.</span><span class="sxs-lookup"><span data-stu-id="26abd-238">RSA public key signature algorithm.</span></span> <span data-ttu-id="26abd-239">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-239">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-240">CALG_SCHANNEL_ENC_KEY</span><span class="sxs-lookup"><span data-stu-id="26abd-240">CALG_SCHANNEL_ENC_KEY</span></span></td>
<td><span data-ttu-id="26abd-241">0x00004c07</span><span class="sxs-lookup"><span data-stu-id="26abd-241">0x00004c07</span></span></td>
<td><span data-ttu-id="26abd-242">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-242">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-243">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-243">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-244">CALG_SCHANNEL_MAC_KEY</span><span class="sxs-lookup"><span data-stu-id="26abd-244">CALG_SCHANNEL_MAC_KEY</span></span></td>
<td><span data-ttu-id="26abd-245">0x00004c03</span><span class="sxs-lookup"><span data-stu-id="26abd-245">0x00004c03</span></span></td>
<td><span data-ttu-id="26abd-246">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-246">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-247">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-247">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-248">CALG_SCHANNEL_MASTER_HASH</span><span class="sxs-lookup"><span data-stu-id="26abd-248">CALG_SCHANNEL_MASTER_HASH</span></span></td>
<td><span data-ttu-id="26abd-249">0x00004c02</span><span class="sxs-lookup"><span data-stu-id="26abd-249">0x00004c02</span></span></td>
<td><span data-ttu-id="26abd-250">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-250">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-251">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-251">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-252">CALG_SEAL</span><span class="sxs-lookup"><span data-stu-id="26abd-252">CALG_SEAL</span></span></td>
<td><span data-ttu-id="26abd-253">0x00006802</span><span class="sxs-lookup"><span data-stu-id="26abd-253">0x00006802</span></span></td>
<td><span data-ttu-id="26abd-254">Запечатайте алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="26abd-254">SEAL encryption algorithm.</span></span> <span data-ttu-id="26abd-255">Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-255">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-256">CALG_SHA</span><span class="sxs-lookup"><span data-stu-id="26abd-256">CALG_SHA</span></span></td>
<td><span data-ttu-id="26abd-257">0x00008004</span><span class="sxs-lookup"><span data-stu-id="26abd-257">0x00008004</span></span></td>
<td><span data-ttu-id="26abd-258">Алгоритм хэширования SHA.</span><span class="sxs-lookup"><span data-stu-id="26abd-258">SHA hashing algorithm.</span></span> <span data-ttu-id="26abd-259">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-259">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-260">CALG_SHA1</span><span class="sxs-lookup"><span data-stu-id="26abd-260">CALG_SHA1</span></span></td>
<td><span data-ttu-id="26abd-261">0x00008004</span><span class="sxs-lookup"><span data-stu-id="26abd-261">0x00008004</span></span></td>
<td><span data-ttu-id="26abd-262">То же, что и <strong>CALG_SHA</strong>.</span><span class="sxs-lookup"><span data-stu-id="26abd-262">Same as <strong>CALG_SHA</strong>.</span></span> <span data-ttu-id="26abd-263">Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</span><span class="sxs-lookup"><span data-stu-id="26abd-263">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-264">CALG_SHA_256</span><span class="sxs-lookup"><span data-stu-id="26abd-264">CALG_SHA_256</span></span></td>
<td><span data-ttu-id="26abd-265">0x0000800c</span><span class="sxs-lookup"><span data-stu-id="26abd-265">0x0000800c</span></span></td>
<td><span data-ttu-id="26abd-266">256-разрядный алгоритм хэширования SHA.</span><span class="sxs-lookup"><span data-stu-id="26abd-266">256 bit SHA hashing algorithm.</span></span> <span data-ttu-id="26abd-267">Этот алгоритм поддерживается в поставщике служб шифрования Microsoft Enhanced RSA и AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="26abd-267">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider..<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="26abd-268"><strong>Windows XP с пакетом обновления 2 (SP2), Windows XP с пакетом обновления SP1 и Windows XP:</strong> Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-268"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-269">CALG_SHA_384</span><span class="sxs-lookup"><span data-stu-id="26abd-269">CALG_SHA_384</span></span></td>
<td><span data-ttu-id="26abd-270">0x0000800d</span><span class="sxs-lookup"><span data-stu-id="26abd-270">0x0000800d</span></span></td>
<td><span data-ttu-id="26abd-271">384-разрядный алгоритм хэширования SHA.</span><span class="sxs-lookup"><span data-stu-id="26abd-271">384 bit SHA hashing algorithm.</span></span> <span data-ttu-id="26abd-272">Этот алгоритм поддерживается поставщиком служб Microsoft Enhanced RSA and AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="26abd-272">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="26abd-273"><strong>Windows XP с пакетом обновления 2 (SP2), Windows XP с пакетом обновления SP1 и Windows XP:</strong> Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-273"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-274">CALG_SHA_512</span><span class="sxs-lookup"><span data-stu-id="26abd-274">CALG_SHA_512</span></span></td>
<td><span data-ttu-id="26abd-275">0x0000800e</span><span class="sxs-lookup"><span data-stu-id="26abd-275">0x0000800e</span></span></td>
<td><span data-ttu-id="26abd-276">512-разрядный алгоритм хэширования SHA.</span><span class="sxs-lookup"><span data-stu-id="26abd-276">512 bit SHA hashing algorithm.</span></span> <span data-ttu-id="26abd-277">Этот алгоритм поддерживается поставщиком служб Microsoft Enhanced RSA and AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="26abd-277">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="26abd-278"><strong>Windows XP с пакетом обновления 2 (SP2), Windows XP с пакетом обновления SP1 и Windows XP:</strong> Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-278"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-279">CALG_SKIPJACK</span><span class="sxs-lookup"><span data-stu-id="26abd-279">CALG_SKIPJACK</span></span></td>
<td><span data-ttu-id="26abd-280">0x0000660a</span><span class="sxs-lookup"><span data-stu-id="26abd-280">0x0000660a</span></span></td>
<td><span data-ttu-id="26abd-281">Алгоритм шифрования блоков Skipjack (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="26abd-281">Skipjack block encryption algorithm (FORTEZZA).</span></span> <span data-ttu-id="26abd-282">Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-282">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-283">CALG_SSL2_MASTER</span><span class="sxs-lookup"><span data-stu-id="26abd-283">CALG_SSL2_MASTER</span></span></td>
<td><span data-ttu-id="26abd-284">0x00004c05</span><span class="sxs-lookup"><span data-stu-id="26abd-284">0x00004c05</span></span></td>
<td><span data-ttu-id="26abd-285">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-285">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-286">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-286">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-287">CALG_SSL3_MASTER</span><span class="sxs-lookup"><span data-stu-id="26abd-287">CALG_SSL3_MASTER</span></span></td>
<td><span data-ttu-id="26abd-288">0x00004c01</span><span class="sxs-lookup"><span data-stu-id="26abd-288">0x00004c01</span></span></td>
<td><span data-ttu-id="26abd-289">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-289">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-290">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-290">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-291">CALG_SSL3_SHAMD5</span><span class="sxs-lookup"><span data-stu-id="26abd-291">CALG_SSL3_SHAMD5</span></span></td>
<td><span data-ttu-id="26abd-292">0x00008008</span><span class="sxs-lookup"><span data-stu-id="26abd-292">0x00008008</span></span></td>
<td><span data-ttu-id="26abd-293">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-293">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-294">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-294">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-295">CALG_TEK</span><span class="sxs-lookup"><span data-stu-id="26abd-295">CALG_TEK</span></span></td>
<td><span data-ttu-id="26abd-296">0x0000660b</span><span class="sxs-lookup"><span data-stu-id="26abd-296">0x0000660b</span></span></td>
<td><span data-ttu-id="26abd-297">ТЕК (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="26abd-297">TEK (FORTEZZA).</span></span> <span data-ttu-id="26abd-298">Этот алгоритм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26abd-298">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26abd-299">CALG_TLS1_MASTER</span><span class="sxs-lookup"><span data-stu-id="26abd-299">CALG_TLS1_MASTER</span></span></td>
<td><span data-ttu-id="26abd-300">0x00004c06</span><span class="sxs-lookup"><span data-stu-id="26abd-300">0x00004c06</span></span></td>
<td><span data-ttu-id="26abd-301">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-301">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-302">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-302">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26abd-303">CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="26abd-303">CALG_TLS1PRF</span></span></td>
<td><span data-ttu-id="26abd-304">0x0000800a</span><span class="sxs-lookup"><span data-stu-id="26abd-304">0x0000800a</span></span></td>
<td><span data-ttu-id="26abd-305">Используется системой Schannel.dllных операций.</span><span class="sxs-lookup"><span data-stu-id="26abd-305">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="26abd-306">Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="26abd-306">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="26abd-307">Для [базового поставщика служб шифрования Майкрософт](microsoft-base-cryptographic-provider.md), [поставщика строгой криптографии](microsoft-strong-cryptographic-provider.md)(Майкрософт) и [расширенного поставщика служб шифрования Майкрософт](microsoft-enhanced-cryptographic-provider.md) **ALG_IDs** , используемые для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="26abd-307">For the [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), the [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md), and the [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="26abd-308">**CALG_RSA_KEYX** используется для **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="26abd-308">**CALG_RSA_KEYX** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="26abd-309">**CALG_RSA_SIGN** используется для **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="26abd-309">**CALG_RSA_SIGN** is used for **AT_SIGNATURE**.</span></span>

<span data-ttu-id="26abd-310">Для [поставщика служб шифрования Microsoft Base DSS и Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md) **ALG_IDs** , используемый для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="26abd-310">For the [Microsoft Base DSS and Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="26abd-311">**CALG_DH_SF** используется для **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="26abd-311">**CALG_DH_SF** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="26abd-312">**CALG_DSS_SIGN** используется для **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="26abd-312">**CALG_DSS_SIGN** is used for **AT_SIGNATURE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="26abd-313">Требования</span><span class="sxs-lookup"><span data-stu-id="26abd-313">Requirements</span></span>



| <span data-ttu-id="26abd-314">Требование</span><span class="sxs-lookup"><span data-stu-id="26abd-314">Requirement</span></span> | <span data-ttu-id="26abd-315">Значение</span><span class="sxs-lookup"><span data-stu-id="26abd-315">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26abd-316">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26abd-316">Minimum supported client</span></span><br/> | <span data-ttu-id="26abd-317">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="26abd-317">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="26abd-318">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26abd-318">Minimum supported server</span></span><br/> | <span data-ttu-id="26abd-319">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26abd-319">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26abd-320">Header</span><span class="sxs-lookup"><span data-stu-id="26abd-320">Header</span></span><br/>                   | <dl> <span data-ttu-id="26abd-321"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="26abd-321"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26abd-322">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26abd-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26abd-323">Криптографические функции</span><span class="sxs-lookup"><span data-stu-id="26abd-323">Cryptography Functions</span></span>](cryptography-functions.md)
</dt> <dt>

[<span data-ttu-id="26abd-324">**CRYPT_ALGORITHM_IDENTIFIER**</span><span class="sxs-lookup"><span data-stu-id="26abd-324">**CRYPT_ALGORITHM_IDENTIFIER**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[<span data-ttu-id="26abd-325">**криптфиндоидинфо**</span><span class="sxs-lookup"><span data-stu-id="26abd-325">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
