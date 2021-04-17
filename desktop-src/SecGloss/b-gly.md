---
description: Содержит определения терминов безопасности, начинающихся с буквы B.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: B (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684080"
---
# <a name="b-security-glossary"></a><span data-ttu-id="7ad67-103">B (глоссарий по безопасности)</span><span class="sxs-lookup"><span data-stu-id="7ad67-103">B (Security Glossary)</span></span>

<span data-ttu-id="7ad67-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [р](h-gly.md) [.](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="7ad67-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7ad67-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**Центр архивации**</span><span class="sxs-lookup"><span data-stu-id="7ad67-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**backup authority**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-106">Доверенное приложение, работающее на защищенном компьютере, предоставляющем вторичное хранилище для ключей сеансов своих клиентов.</span><span class="sxs-lookup"><span data-stu-id="7ad67-106">A trusted application running on a secure computer that provides secondary storage for the session keys of its clients.</span></span> <span data-ttu-id="7ad67-107">Центр архивации сохраняет ключи сеанса в виде ключевых BLOB-объектов, которые шифруются с помощью открытого ключа резервного центра.</span><span class="sxs-lookup"><span data-stu-id="7ad67-107">The backup authority stores session keys as key BLOBs that are encrypted with the backup authority's public key.</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**базовый тип содержимого**</span><span class="sxs-lookup"><span data-stu-id="7ad67-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**base content type**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-109">Тип данных, содержащихся в сообщении PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="7ad67-109">A type of data contained in a PKCS \#7 message.</span></span> <span data-ttu-id="7ad67-110">Базовые типы содержимого содержат только данные без криптографических расширений, таких как хэши или подписи.</span><span class="sxs-lookup"><span data-stu-id="7ad67-110">Base content types only contain data, no cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="7ad67-111">В настоящее время единственным базовым типом содержимого является тип содержимого данных.</span><span class="sxs-lookup"><span data-stu-id="7ad67-111">Currently, the only base content type is the Data content type.</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**базовые криптографические функции**</span><span class="sxs-lookup"><span data-stu-id="7ad67-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**base cryptographic functions**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-113">Самый низкий уровень функций в архитектуре CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="7ad67-113">The lowest level of functions in the CryptoAPI architecture.</span></span> <span data-ttu-id="7ad67-114">Они используются приложениями и другими высокоуровневые функции CryptoAPI для предоставления доступа к алгоритмам шифрования, предоставляемым CSP, созданию безопасного ключа и защищенному хранению секретов.</span><span class="sxs-lookup"><span data-stu-id="7ad67-114">They are used by applications and other high-level CryptoAPI functions to provide access to CSP-provided cryptographic algorithms, secure key generation, and secure storage of secrets.</span></span>

<span data-ttu-id="7ad67-115">См. также [*поставщики служб шифрования*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7ad67-115">See also [*cryptographic service providers*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Базовые правила кодирования**</span><span class="sxs-lookup"><span data-stu-id="7ad67-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Basic Encoding Rules**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-117">ЛИЧЕСТВО Набор правил, используемый для кодирования ASN. 1 определенных данных в поток битов (нулей или единиц) для внешнего хранилища или передачи.</span><span class="sxs-lookup"><span data-stu-id="7ad67-117">(BER) The set of rules used to encode ASN.1 defined data into a stream of bits (zeros or ones) for external storage or transmission.</span></span> <span data-ttu-id="7ad67-118">Один объект ASN. 1 может иметь несколько эквивалентных закодированных ЛИЧЕСТВО.</span><span class="sxs-lookup"><span data-stu-id="7ad67-118">A single ASN.1 object may have several equivalent BER encodes.</span></span> <span data-ttu-id="7ad67-119">ЛИЧЕСТВО определяется в рекомендации CCITT X. 209.</span><span class="sxs-lookup"><span data-stu-id="7ad67-119">BER is defined in CCITT Recommendation X.209.</span></span> <span data-ttu-id="7ad67-120">Это один из двух методов кодирования, используемых в настоящее время интерфейсом CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="7ad67-120">This is one of the two encoding methods currently used by CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**ЛИЧЕСТВО**</span><span class="sxs-lookup"><span data-stu-id="7ad67-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-122">См. раздел *основные правила кодирования*.</span><span class="sxs-lookup"><span data-stu-id="7ad67-122">See *Basic Encoding Rules*.</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**с обратным порядком байтов**</span><span class="sxs-lookup"><span data-stu-id="7ad67-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big-endian**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-124">Формат памяти или данных, в котором наиболее значимый байт хранится по нижнему адресу или сначала прибывается.</span><span class="sxs-lookup"><span data-stu-id="7ad67-124">A memory or data format in which the most significant byte is stored at the lower address or arrives first.</span></span>

<span data-ttu-id="7ad67-125">См. также [*прямой порядок байтов*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7ad67-125">See also [*little-endian*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**ОБЪЕКТЕ**</span><span class="sxs-lookup"><span data-stu-id="7ad67-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-127">Универсальная последовательность битов, содержащая одну или несколько структур заголовков фиксированной длины и конкретных данных контекста.</span><span class="sxs-lookup"><span data-stu-id="7ad67-127">A generic sequence of bits that contain one or more fixed-length header structures plus context specific data.</span></span>

<span data-ttu-id="7ad67-128">См. также [*Ключевые BLOB*](k-gly.md)-объекты, [*Сертификаты BLOB*](c-gly.md)-объектов, [*имена сертификатов*](c-gly.md)и [*BLOB-объекты атрибутов*](a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7ad67-128">See also [*key BLOBs*](k-gly.md), [*certificate BLOBs*](c-gly.md), [*certificate name BLOBs*](c-gly.md), and [*attribute BLOBs*](a-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**блочный шифр**</span><span class="sxs-lookup"><span data-stu-id="7ad67-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**block cipher**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-130">Алгоритм шифрования, который шифрует данные в дискретных единицах (называемых блоками), а не в виде непрерывного потока битов.</span><span class="sxs-lookup"><span data-stu-id="7ad67-130">A cipher algorithm that encrypts data in discrete units (called blocks), rather than as a continuous stream of bits.</span></span> <span data-ttu-id="7ad67-131">Наиболее распространенный размер блока — 64 бит.</span><span class="sxs-lookup"><span data-stu-id="7ad67-131">The most common block size is 64 bits.</span></span> <span data-ttu-id="7ad67-132">Например, DES является блочным шифром.</span><span class="sxs-lookup"><span data-stu-id="7ad67-132">For example, DES is a block cipher.</span></span>

<span data-ttu-id="7ad67-133">См. также [*Stream Cipher*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7ad67-133">See also [*stream cipher*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ad67-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**ключ для групповой шифрования**</span><span class="sxs-lookup"><span data-stu-id="7ad67-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**bulk encryption key**</span></span>
</dt> <dd>

<span data-ttu-id="7ad67-135">Ключ сеанса, полученный из главного ключа.</span><span class="sxs-lookup"><span data-stu-id="7ad67-135">A session key derived from a master key.</span></span> <span data-ttu-id="7ad67-136">В шифровании [*SChannel*](s-gly.md) используются ключи с массовым шифрованием.</span><span class="sxs-lookup"><span data-stu-id="7ad67-136">Bulk encryption keys are used in [*Schannel*](s-gly.md) encryption.</span></span>

</dd> </dl>

 

 



