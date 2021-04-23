---
description: 'В отличие от криптографических API (CryptoAPI), API шифрования: следующее поколение (CNG) отделяет поставщиков служб шифрования от поставщиков хранилища ключей.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Поставщики алгоритмов шифрования CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647504"
---
# <a name="cng-cryptographic-algorithm-providers"></a><span data-ttu-id="f01ff-103">Поставщики алгоритмов шифрования CNG</span><span class="sxs-lookup"><span data-stu-id="f01ff-103">CNG Cryptographic Algorithm Providers</span></span>

<span data-ttu-id="f01ff-104">В отличие от криптографических API (CryptoAPI), API шифрования: следующее поколение (CNG) отделяет поставщиков служб шифрования от поставщиков хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f01ff-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers.</span></span> <span data-ttu-id="f01ff-105">Основные операции криптографических алгоритмов, такие как хеширование и подписывание, называются простыми операциями или просто примитивами.</span><span class="sxs-lookup"><span data-stu-id="f01ff-105">Basic cryptographic algorithm operations such as hashing and signing are called primitive operations or simply primitives.</span></span> <span data-ttu-id="f01ff-106">CNG включает в себя поставщик, реализующий следующие алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="f01ff-106">CNG includes a provider that implements the following algorithms.</span></span>

-   [<span data-ttu-id="f01ff-107">Симметричные алгоритмы</span><span class="sxs-lookup"><span data-stu-id="f01ff-107">Symmetric Algorithms</span></span>](#symmetric-algorithms)
-   [<span data-ttu-id="f01ff-108">Асимметричные алгоритмы</span><span class="sxs-lookup"><span data-stu-id="f01ff-108">Asymmetric Algorithms</span></span>](#asymmetric-algorithms)
-   [<span data-ttu-id="f01ff-109">Алгоритмы хеширования</span><span class="sxs-lookup"><span data-stu-id="f01ff-109">Hashing Algorithms</span></span>](#hashing-algorithms)
-   [<span data-ttu-id="f01ff-110">Алгоритмы обмена ключами</span><span class="sxs-lookup"><span data-stu-id="f01ff-110">Key Exchange Algorithms</span></span>](#key-exchange-algorithms)
-   [<span data-ttu-id="f01ff-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f01ff-111">Related topics</span></span>](#related-topics)

## <a name="symmetric-algorithms"></a><span data-ttu-id="f01ff-112">Симметричные алгоритмы</span><span class="sxs-lookup"><span data-stu-id="f01ff-112">Symmetric Algorithms</span></span>



| <span data-ttu-id="f01ff-113">Имя</span><span class="sxs-lookup"><span data-stu-id="f01ff-113">Name</span></span>                                   | <span data-ttu-id="f01ff-114">Поддерживаемые режимы</span><span class="sxs-lookup"><span data-stu-id="f01ff-114">Supported modes</span></span>                                                                                                                                                                                                 | <span data-ttu-id="f01ff-115">Размер ключа в битах (по умолчанию/мин/макс)</span><span class="sxs-lookup"><span data-stu-id="f01ff-115">Key size in bits (Default/Min/Max)</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="f01ff-116">Стандарт AES (Advanced Encryption Standard)</span><span class="sxs-lookup"><span data-stu-id="f01ff-116">Advanced Encryption Standard (AES)</span></span>     | <span data-ttu-id="f01ff-117">ECB, CBC, CFB8, CFB128, GCM, CCM, ГМАК, КМАК, перенос ключа AES, XTS</span><span class="sxs-lookup"><span data-stu-id="f01ff-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span></span><br/> <span data-ttu-id="f01ff-118">**Windows 8:** Начинается поддержка режимов CFB128 и КМАК.</span><span class="sxs-lookup"><span data-stu-id="f01ff-118">**Windows 8:** Support for the CFB128 and CMAC modes begins.</span></span><br/> <span data-ttu-id="f01ff-119">**Windows 10:** Начинается поддержка режима XTS-AES.</span><span class="sxs-lookup"><span data-stu-id="f01ff-119">**Windows 10:** Support for XTS-AES mode begins.</span></span><br/> | <span data-ttu-id="f01ff-120">128/192/256</span><span class="sxs-lookup"><span data-stu-id="f01ff-120">128/192/256</span></span>                        |
| <span data-ttu-id="f01ff-121">Стандарт шифрования данных (DES)</span><span class="sxs-lookup"><span data-stu-id="f01ff-121">Data Encryption Standard (DES)</span></span>         | <span data-ttu-id="f01ff-122">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="f01ff-122">ECB, CBC, CFB8, CFB64</span></span><br/> <span data-ttu-id="f01ff-123">**Windows 8:** Начинается поддержка режима CFB64.</span><span class="sxs-lookup"><span data-stu-id="f01ff-123">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                   | <span data-ttu-id="f01ff-124">56/56/56</span><span class="sxs-lookup"><span data-stu-id="f01ff-124">56/56/56</span></span>                           |
| <span data-ttu-id="f01ff-125">Стандарт шифрования данных Ксоред (DESX)</span><span class="sxs-lookup"><span data-stu-id="f01ff-125">Data Encryption Standard XORed(DESX)</span></span>   | <span data-ttu-id="f01ff-126">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="f01ff-126">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="f01ff-127">**Windows 8:** Начинается поддержка режима CFB64.</span><span class="sxs-lookup"><span data-stu-id="f01ff-127">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="f01ff-128">192/192/192</span><span class="sxs-lookup"><span data-stu-id="f01ff-128">192/192/192</span></span>                        |
| <span data-ttu-id="f01ff-129">Тройной стандарт шифрования данных (3DES)</span><span class="sxs-lookup"><span data-stu-id="f01ff-129">Triple Data Encryption Standard (3DES)</span></span> | <span data-ttu-id="f01ff-130">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="f01ff-130">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="f01ff-131">**Windows 8:** Начинается поддержка режима CFB64.</span><span class="sxs-lookup"><span data-stu-id="f01ff-131">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="f01ff-132">112/168</span><span class="sxs-lookup"><span data-stu-id="f01ff-132">112/168</span></span>                            |
| <span data-ttu-id="f01ff-133">RSA Data Security 2 (RC2)</span><span class="sxs-lookup"><span data-stu-id="f01ff-133">RSA Data Security 2 (RC2)</span></span>              | <span data-ttu-id="f01ff-134">Поддерживаются режимы ECB, CBC, CFB8, CFB64.</span><span class="sxs-lookup"><span data-stu-id="f01ff-134">ECB, CBC, CFB8, CFB64 modes are supported.</span></span><br/> <span data-ttu-id="f01ff-135">**Windows 8:** Начинается поддержка режима CFB64.</span><span class="sxs-lookup"><span data-stu-id="f01ff-135">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                              | <span data-ttu-id="f01ff-136">от 16 до 128 с шагом 8 бит</span><span class="sxs-lookup"><span data-stu-id="f01ff-136">16 to 128 in 8 bit increments</span></span>      |
| <span data-ttu-id="f01ff-137">RSA Data Security 4 (RC4)</span><span class="sxs-lookup"><span data-stu-id="f01ff-137">RSA Data Security 4 (RC4)</span></span>              |                                                                                                                                                                                                                 | <span data-ttu-id="f01ff-138">от 8 до 512 с шагом в 8 бит</span><span class="sxs-lookup"><span data-stu-id="f01ff-138">8 to 512, in 8-bit increments</span></span>      |



 

## <a name="asymmetric-algorithms"></a><span data-ttu-id="f01ff-139">Асимметричные алгоритмы</span><span class="sxs-lookup"><span data-stu-id="f01ff-139">Asymmetric Algorithms</span></span>



| <span data-ttu-id="f01ff-140">Имя</span><span class="sxs-lookup"><span data-stu-id="f01ff-140">Name</span></span>                              | <span data-ttu-id="f01ff-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="f01ff-141">Notes</span></span>                                                                                                                                                                             | <span data-ttu-id="f01ff-142">Размер ключа в битах (по умолчанию/мин/макс)</span><span class="sxs-lookup"><span data-stu-id="f01ff-142">Key size in bits (Default/Min/Max)</span></span>                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f01ff-143">Алгоритм цифровых подписей (DSA)</span><span class="sxs-lookup"><span data-stu-id="f01ff-143">Digital Signature Algorithm (DSA)</span></span> | <span data-ttu-id="f01ff-144">Реализация соответствует стандарту FIPS 186-3 для размеров ключей в диапазоне от 1024 до 3072 бит.</span><span class="sxs-lookup"><span data-stu-id="f01ff-144">Implementation conforms to FIPS 186-3 for key sizes between 1024 and 3072 bits.</span></span> <br/> <span data-ttu-id="f01ff-145">Реализация соответствует стандарту FIPS 186-2 для размеров ключей с 512 до 1024 бит.</span><span class="sxs-lookup"><span data-stu-id="f01ff-145">Implementation conforms to FIPS 186-2 for key sizes from 512 to 1024 bits.</span></span><br/> | <span data-ttu-id="f01ff-146">от 512 до 3072, с шагом 64-bit</span><span class="sxs-lookup"><span data-stu-id="f01ff-146">512 to 3072, in 64-bit increments</span></span><br/> <span data-ttu-id="f01ff-147">**Windows 8:** Начинается поддержка 3072-разрядного ключа.</span><span class="sxs-lookup"><span data-stu-id="f01ff-147">**Windows 8:** Support for the a 3072 bit key begins.</span></span><br/> |
| <span data-ttu-id="f01ff-148">RSA</span><span class="sxs-lookup"><span data-stu-id="f01ff-148">RSA</span></span>                               | <span data-ttu-id="f01ff-149">Включает алгоритмы RSA, в которых используется PKCS1, оптимальное кодирование и заполнение OAEP, а также заполнение в виде обычного текста для схемы подписи вероятностная (PSS).</span><span class="sxs-lookup"><span data-stu-id="f01ff-149">Includes RSA algorithms that use PKCS1, Optimal Asymmetric Encryption Padding (OAEP) encoding or padding, or Probabilistic Signature Scheme (PSS) plaintext padding</span></span>               | <span data-ttu-id="f01ff-150">от 512 до 16384, с шагом 64-bit</span><span class="sxs-lookup"><span data-stu-id="f01ff-150">512 to 16384, in 64-bit increments</span></span>                                                                            |



 

## <a name="hashing-algorithms"></a><span data-ttu-id="f01ff-151">Алгоритмы хеширования</span><span class="sxs-lookup"><span data-stu-id="f01ff-151">Hashing Algorithms</span></span>



| <span data-ttu-id="f01ff-152">Имя</span><span class="sxs-lookup"><span data-stu-id="f01ff-152">Name</span></span>                               | <span data-ttu-id="f01ff-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="f01ff-153">Notes</span></span>               | <span data-ttu-id="f01ff-154">Размер ключа в битах (по умолчанию/мин/макс)</span><span class="sxs-lookup"><span data-stu-id="f01ff-154">Key size in bits (Default/Min/Max)</span></span> |
|------------------------------------|---------------------|------------------------------------|
| <span data-ttu-id="f01ff-155">Алгоритм SHA-1 (SHA1)</span><span class="sxs-lookup"><span data-stu-id="f01ff-155">Secure Hash Algorithm 1 (SHA1)</span></span>     | <span data-ttu-id="f01ff-156">Включает HmacSha1</span><span class="sxs-lookup"><span data-stu-id="f01ff-156">Includes HmacSha1</span></span>   | <span data-ttu-id="f01ff-157">160/160/160</span><span class="sxs-lookup"><span data-stu-id="f01ff-157">160/160/160</span></span>                        |
| <span data-ttu-id="f01ff-158">Безопасный хэш-алгоритм 256 (SHA256)</span><span class="sxs-lookup"><span data-stu-id="f01ff-158">Secure Hash Algorithm 256 (SHA256)</span></span> | <span data-ttu-id="f01ff-159">Включает HmacSha256</span><span class="sxs-lookup"><span data-stu-id="f01ff-159">Includes HmacSha256</span></span> | <span data-ttu-id="f01ff-160">256/256/256</span><span class="sxs-lookup"><span data-stu-id="f01ff-160">256/256/256</span></span>                        |
| <span data-ttu-id="f01ff-161">Безопасный хэш-алгоритм 384 (SHA384)</span><span class="sxs-lookup"><span data-stu-id="f01ff-161">Secure Hash Algorithm 384 (SHA384)</span></span> | <span data-ttu-id="f01ff-162">Включает HmacSha384</span><span class="sxs-lookup"><span data-stu-id="f01ff-162">Includes HmacSha384</span></span> | <span data-ttu-id="f01ff-163">384/384/384</span><span class="sxs-lookup"><span data-stu-id="f01ff-163">384/384/384</span></span>                        |
| <span data-ttu-id="f01ff-164">Безопасный хэш-алгоритм 512 (SHA512)</span><span class="sxs-lookup"><span data-stu-id="f01ff-164">Secure Hash Algorithm 512 (SHA512)</span></span> | <span data-ttu-id="f01ff-165">Включает HmacSha512</span><span class="sxs-lookup"><span data-stu-id="f01ff-165">Includes HmacSha512</span></span> | <span data-ttu-id="f01ff-166">512/512/512</span><span class="sxs-lookup"><span data-stu-id="f01ff-166">512/512/512</span></span>                        |
| <span data-ttu-id="f01ff-167">Дайджест сообщения 2 (MD2)</span><span class="sxs-lookup"><span data-stu-id="f01ff-167">Message Digest 2 (MD2)</span></span>             | <span data-ttu-id="f01ff-168">Включает HmacMd2</span><span class="sxs-lookup"><span data-stu-id="f01ff-168">Includes HmacMd2</span></span>    | <span data-ttu-id="f01ff-169">128/128/128</span><span class="sxs-lookup"><span data-stu-id="f01ff-169">128/128/128</span></span>                        |
| <span data-ttu-id="f01ff-170">Дайджест сообщения 4 (MD4)</span><span class="sxs-lookup"><span data-stu-id="f01ff-170">Message Digest 4 (MD4)</span></span>             | <span data-ttu-id="f01ff-171">Включает HmacMd4</span><span class="sxs-lookup"><span data-stu-id="f01ff-171">Includes HmacMd4</span></span>    | <span data-ttu-id="f01ff-172">128/128/128</span><span class="sxs-lookup"><span data-stu-id="f01ff-172">128/128/128</span></span>                        |
| <span data-ttu-id="f01ff-173">Дайджест сообщения 5 (MD5)</span><span class="sxs-lookup"><span data-stu-id="f01ff-173">Message Digest 5 (MD5)</span></span>             | <span data-ttu-id="f01ff-174">Включает HmacMd5</span><span class="sxs-lookup"><span data-stu-id="f01ff-174">Includes HmacMd5</span></span>    | <span data-ttu-id="f01ff-175">128/128/128</span><span class="sxs-lookup"><span data-stu-id="f01ff-175">128/128/128</span></span>                        |



 

## <a name="key-exchange-algorithms"></a><span data-ttu-id="f01ff-176">Алгоритмы обмена ключами</span><span class="sxs-lookup"><span data-stu-id="f01ff-176">Key Exchange Algorithms</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f01ff-177">Имя алгоритма</span><span class="sxs-lookup"><span data-stu-id="f01ff-177">Algorithm name</span></span></th>
<th><span data-ttu-id="f01ff-178">Примечания</span><span class="sxs-lookup"><span data-stu-id="f01ff-178">Notes</span></span></th>
<th><span data-ttu-id="f01ff-179">Размер ключа в битах (по умолчанию/мин/макс)</span><span class="sxs-lookup"><span data-stu-id="f01ff-179">Key size in bits (Default/Min/Max)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f01ff-180">Алгоритм обмена ключами Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="f01ff-180">Diffie-Hellman Key Exchange Algorithm</span></span></td>

<td><span data-ttu-id="f01ff-181">от 512 до 4096, с шагом 64-bit</span><span class="sxs-lookup"><span data-stu-id="f01ff-181">512 to 4096, in 64-bit increments</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f01ff-182">Diffie-Hellman на эллиптических кривых (ECDH)</span><span class="sxs-lookup"><span data-stu-id="f01ff-182">Elliptic Curve Diffie-Hellman (ECDH)</span></span></td>
<td><span data-ttu-id="f01ff-183">Содержит кривые, использующие битовые открытые ключи 256, 384 и 521, как указано в SP800-56A.</span><span class="sxs-lookup"><span data-stu-id="f01ff-183">Includes curves that use 256, 384 and 521 bit public keys as specified in SP800-56A.</span></span></td>
<td><span data-ttu-id="f01ff-184">256/384/521</span><span class="sxs-lookup"><span data-stu-id="f01ff-184">256/384/521</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f01ff-185">Алгоритм цифровых подписей на основе эллиптических кривых (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="f01ff-185">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span></td>
<td><span data-ttu-id="f01ff-186">Включает кривые, использующие битовые открытые ключи 256, 384 и 521, как указано в FIPS 186-3.</span><span class="sxs-lookup"><span data-stu-id="f01ff-186">Includes curves that use 256, 384 and 521 bit public keys as specified in FIPS 186-3.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f01ff-187">Чтобы отобразить все именованные эллиптические кривые, используйте <strong>certutil дисплайекккурве</strong>.</span><span class="sxs-lookup"><span data-stu-id="f01ff-187">To display all named elliptic curves, use <strong>certutil  displayEccCurve</strong>.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="f01ff-188">256/384/521</span><span class="sxs-lookup"><span data-stu-id="f01ff-188">256/384/521</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f01ff-189">См. также</span><span class="sxs-lookup"><span data-stu-id="f01ff-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f01ff-190">**Идентификаторы алгоритма CNG**</span><span class="sxs-lookup"><span data-stu-id="f01ff-190">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="f01ff-191">Примитивные функции шифрования CNG</span><span class="sxs-lookup"><span data-stu-id="f01ff-191">CNG Cryptographic Primitive Functions</span></span>](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[<span data-ttu-id="f01ff-192">Общие сведения о поставщиках служб шифрования</span><span class="sxs-lookup"><span data-stu-id="f01ff-192">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

