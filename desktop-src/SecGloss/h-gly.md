---
description: Содержит определения терминов безопасности, начинающихся с буквы H.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4165b820-30fc-477e-a690-81109f161323
title: H (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665cd90cfc8a849030b6a1cfd1cb4e6d6f687557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683811"
---
# <a name="h-security-glossary"></a><span data-ttu-id="c2194-103">H (глоссарий по безопасности)</span><span class="sxs-lookup"><span data-stu-id="c2194-103">H (Security Glossary)</span></span>

<span data-ttu-id="c2194-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) р [.](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="c2194-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) H [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c2194-105"><span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**справиться**</span><span class="sxs-lookup"><span data-stu-id="c2194-105"><span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**handle**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-106">Маркер, используемый для обнаружения или доступа к объекту, например к поставщику служб шифрования, хранилищу сертификатов, сообщениям или паре ключей.</span><span class="sxs-lookup"><span data-stu-id="c2194-106">A token used to identify or access an object, such as the handle to a cryptographic provider, certificate store, message, or key pair.</span></span>

</dd> <dt>

<span data-ttu-id="c2194-107"><span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**функции**</span><span class="sxs-lookup"><span data-stu-id="c2194-107"><span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**hash**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-108">Результат фиксированного размера, полученный путем применения математической функции ( *алгоритма хэширования*) к произвольному объему данных.</span><span class="sxs-lookup"><span data-stu-id="c2194-108">A fixed-size result obtained by applying a mathematical function (the *hashing algorithm*) to an arbitrary amount of data.</span></span> <span data-ttu-id="c2194-109">(Также называется "дайджестом сообщений".)</span><span class="sxs-lookup"><span data-stu-id="c2194-109">(Also known as "message digest.")</span></span>

<span data-ttu-id="c2194-110">См. также *функции хэширования*.</span><span class="sxs-lookup"><span data-stu-id="c2194-110">See also *hashing functions*.</span></span>

</dd> <dt>

<span data-ttu-id="c2194-111"><span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**хэш-объект**</span><span class="sxs-lookup"><span data-stu-id="c2194-111"><span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**hash object**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-112">Объект, используемый для хэширования сообщений или ключей сеанса.</span><span class="sxs-lookup"><span data-stu-id="c2194-112">An object used to hash messages or session keys.</span></span> <span data-ttu-id="c2194-113">Хэш-объект создается путем вызова **CryptCreateHash**.</span><span class="sxs-lookup"><span data-stu-id="c2194-113">The hash object is created by a call to **CryptCreateHash**.</span></span> <span data-ttu-id="c2194-114">Определение объекта определяется CSP, указанным в вызове.</span><span class="sxs-lookup"><span data-stu-id="c2194-114">The definition of the object is defined by the CSP specified in the call.</span></span>

</dd> <dt>

<span data-ttu-id="c2194-115"><span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**алгоритм хэширования**</span><span class="sxs-lookup"><span data-stu-id="c2194-115"><span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**hashing algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-116">Алгоритм, используемый для получения хэш-значения некоторого блока данных, например сообщения или сеансового ключа.</span><span class="sxs-lookup"><span data-stu-id="c2194-116">An algorithm used to produce a hash value of some piece of data, such as a message or session key.</span></span> <span data-ttu-id="c2194-117">К типичным хэш-алгоритмам относятся MD2, MD4, MD5 и SHA-1.</span><span class="sxs-lookup"><span data-stu-id="c2194-117">Typical hashing algorithms include MD2, MD4, MD5, and SHA-1.</span></span>

</dd> <dt>

<span data-ttu-id="c2194-118"><span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**функции хэширования**</span><span class="sxs-lookup"><span data-stu-id="c2194-118"><span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**hashing functions**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-119">Набор функций, используемых для создания и уничтожения хэш-объектов, получения или задания параметров хэш-объекта, а также хэш-данных и ключей сеанса.</span><span class="sxs-lookup"><span data-stu-id="c2194-119">A set of functions used to create and destroy hash objects, get or set the parameters of a hash object, and hash data and session keys.</span></span>

</dd> <dt>

<span data-ttu-id="c2194-120"><span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**код проверки подлинности сообщения на основе хэша**</span><span class="sxs-lookup"><span data-stu-id="c2194-120"><span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Hash-Based Message Authentication Code**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-121">HMAC Алгоритм хэширования с симметричным ключом, реализованный поставщиками служб шифрования (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="c2194-121">(HMAC) A symmetric keyed hashing algorithm implemented by Microsoft cryptographic service providers.</span></span> <span data-ttu-id="c2194-122">HMAC используется для проверки целостности данных, чтобы гарантировать, что они не изменялись во время хранения или передачи.</span><span class="sxs-lookup"><span data-stu-id="c2194-122">An HMAC is used to verify the integrity of data to help ensure it has not been modified while in storage or transit.</span></span> <span data-ttu-id="c2194-123">Его можно использовать с любым циклическим хэш-алгоритмом шифрования, например MD5 или SHA-1.</span><span class="sxs-lookup"><span data-stu-id="c2194-123">It can be used with any iterated cryptographic hash algorithm, such as MD5 or SHA-1.</span></span> <span data-ttu-id="c2194-124">CryptoAPI ссылается на этот алгоритм по идентификатору алгоритма (КАЛГ \_ HMAC) и классу ( \_ хэш класса алгоритма \_ ).</span><span class="sxs-lookup"><span data-stu-id="c2194-124">CryptoAPI references this algorithm by its algorithm identifier (CALG\_HMAC) and class (ALG\_CLASS\_HASH).</span></span>

<span data-ttu-id="c2194-125">См. также [*код проверки подлинности сообщения*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c2194-125">See also [*Message Authentication Code*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2194-126"><span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**хксбк**</span><span class="sxs-lookup"><span data-stu-id="c2194-126"><span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**HCSBC**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-127">Тип данных, который служит в качестве маркера для контекста резервного копирования служб сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c2194-127">Data type which serves as a handle to a Certificate Services backup context.</span></span> <span data-ttu-id="c2194-128">Его роль заключается в поддержке состояния контекста между сервером и API-интерфейсами резервного копирования при выполнении резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="c2194-128">Its role is to maintain context state between the server and the backup APIs when a backup is being performed.</span></span>

</dd> <dt>

<span data-ttu-id="c2194-129"><span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**HMAC**</span><span class="sxs-lookup"><span data-stu-id="c2194-129"><span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**HMAC**</span></span>
</dt> <dd>

<span data-ttu-id="c2194-130">См. раздел *код проверки подлинности сообщения на основе хэша*.</span><span class="sxs-lookup"><span data-stu-id="c2194-130">See *Hash-Based Message Authentication Code*.</span></span>

</dd> </dl>

 

 



