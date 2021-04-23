---
description: Используется с функциями BCryptGetProperty и Бкриптсетпроперти для обнаружения свойства.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Идентификаторы свойств примитивов шифрования (BCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896738"
---
# <a name="cryptography-primitive-property-identifiers"></a><span data-ttu-id="886cc-103">Идентификаторы свойств примитивов шифрования</span><span class="sxs-lookup"><span data-stu-id="886cc-103">Cryptography Primitive Property Identifiers</span></span>

<span data-ttu-id="886cc-104">Для обнаружения свойства используются следующие значения с функциями [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) и [**бкриптсетпроперти**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .</span><span class="sxs-lookup"><span data-stu-id="886cc-104">The following values are used with the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) and [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) functions to identify a property.</span></span>

<dl> <dt>

<span data-ttu-id="886cc-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_имя алгоритма BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT\_ALGORITHM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-106">L "AlgorithmName"</span><span class="sxs-lookup"><span data-stu-id="886cc-106">L"AlgorithmName"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-107">Строка в Юникоде, заканчивающаяся нулем и содержащая имя алгоритма.</span><span class="sxs-lookup"><span data-stu-id="886cc-107">A null-terminated Unicode string that contains the name of the algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_длина тега проверки подлинности BCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT\_AUTH\_TAG\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-109">L "Аустагленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-109">L"AuthTagLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-110">Длина тега проверки подлинности, поддерживаемая алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="886cc-110">The authentication tag lengths that are supported by the algorithm.</span></span> <span data-ttu-id="886cc-111">Это свойство представляет структуру [**структуры \_ проверки подлинности \_ тегов \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="886cc-111">This property is a [**BCRYPT\_AUTH\_TAG\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="886cc-112">Это свойство применяется только к алгоритмам.</span><span class="sxs-lookup"><span data-stu-id="886cc-112">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_Длина блока \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-114">L "Блоккленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-114">L"BlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-115">Размер блока шифра в байтах для алгоритма.</span><span class="sxs-lookup"><span data-stu-id="886cc-115">The size, in bytes, of a cipher block for the algorithm.</span></span> <span data-ttu-id="886cc-116">Это свойство применимо только к алгоритмам блочного шифрования.</span><span class="sxs-lookup"><span data-stu-id="886cc-116">This property only applies to block cipher algorithms.</span></span> <span data-ttu-id="886cc-117">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-117">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_ \_ список размеров блоков \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT\_BLOCK\_SIZE\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-119">L "Блокксизелист"</span><span class="sxs-lookup"><span data-stu-id="886cc-119">L"BlockSizeList"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-120">Список длин блоков, поддерживаемых алгоритмом шифрования.</span><span class="sxs-lookup"><span data-stu-id="886cc-120">A list of the block lengths supported by an encryption algorithm.</span></span> <span data-ttu-id="886cc-121">Этот тип данных является массивом типов **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-121">This data type is an array of **DWORDs**.</span></span> <span data-ttu-id="886cc-122">Количество элементов в массиве можно определить, разделив число байтов, полученных размером одного **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-122">The number of elements in the array can be determined by dividing the number of bytes retrieved by the size of a single **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_режим цепочки \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT\_CHAINING\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-124">L "Чаинингмоде"</span><span class="sxs-lookup"><span data-stu-id="886cc-124">L"ChainingMode"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-125">Указатель на строку в Юникоде, завершающуюся нулем, которая представляет режим цепочки алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="886cc-125">A pointer to a null-terminated Unicode string that represents the chaining mode of the encryption algorithm.</span></span> <span data-ttu-id="886cc-126">Это свойство может быть задано для обработчика алгоритма или для одного из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="886cc-126">This property can be set on an algorithm handle or a key handle to one of the following values.</span></span>



| <span data-ttu-id="886cc-127">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="886cc-127">Identifier</span></span>                   | <span data-ttu-id="886cc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="886cc-128">Value</span></span>                         | <span data-ttu-id="886cc-129">Описание</span><span class="sxs-lookup"><span data-stu-id="886cc-129">Description</span></span>                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="886cc-130">**\_режим цепочки BCRYPT \_ \_ CBC**</span><span class="sxs-lookup"><span data-stu-id="886cc-130">**BCRYPT\_CHAIN\_MODE\_CBC**</span></span> | <span data-ttu-id="886cc-131">L "Чаинингмодекбк"</span><span class="sxs-lookup"><span data-stu-id="886cc-131">L"ChainingModeCBC"</span></span><br/> | <span data-ttu-id="886cc-132">Устанавливает режим цепочки алгоритма для [*шифрования цепочек блоков*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="886cc-132">Sets the algorithm's chaining mode to [*cipher block chaining*](/windows/desktop/SecGloss/c-gly).</span></span><br/>            |
| <span data-ttu-id="886cc-133">**\_CCM в \_ режиме ЦЕПОЧКи BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-133">**BCRYPT\_CHAIN\_MODE\_CCM**</span></span> | <span data-ttu-id="886cc-134">L "Чаинингмодеккм"</span><span class="sxs-lookup"><span data-stu-id="886cc-134">L"ChainingModeCCM"</span></span><br/> | <span data-ttu-id="886cc-135">Задает для алгоритма режим цепочки "Счетчик" с помощью CBC-MAC Mode (CCM). **Windows Vista:** Это значение поддерживается начиная с Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="886cc-135">Sets the algorithm's chaining mode to counter with CBC-MAC mode (CCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/> |
| <span data-ttu-id="886cc-136">**\_CFB режим цепочки BCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-136">**BCRYPT\_CHAIN\_MODE\_CFB**</span></span> | <span data-ttu-id="886cc-137">L "Чаинингмодекфб"</span><span class="sxs-lookup"><span data-stu-id="886cc-137">L"ChainingModeCFB"</span></span><br/> | <span data-ttu-id="886cc-138">Задает режим цепочки алгоритма для [*шифрования отзывов*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="886cc-138">Sets the algorithm's chaining mode to [*cipher feedback*](/windows/desktop/SecGloss/c-gly).</span></span><br/>                              |
| <span data-ttu-id="886cc-139">**\_режим цепочки BCRYPT \_ \_ ECB**</span><span class="sxs-lookup"><span data-stu-id="886cc-139">**BCRYPT\_CHAIN\_MODE\_ECB**</span></span> | <span data-ttu-id="886cc-140">L "Чаинингмодикб"</span><span class="sxs-lookup"><span data-stu-id="886cc-140">L"ChainingModeECB"</span></span><br/> | <span data-ttu-id="886cc-141">Задает для алгоритма режим цепочки " [*электронный режимом*](/windows/desktop/SecGloss/e-gly)".</span><span class="sxs-lookup"><span data-stu-id="886cc-141">Sets the algorithm's chaining mode to [*electronic codebook*](/windows/desktop/SecGloss/e-gly).</span></span><br/>                  |
| <span data-ttu-id="886cc-142">**\_gcm в \_ режиме ЦЕПОЧКи BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-142">**BCRYPT\_CHAIN\_MODE\_GCM**</span></span> | <span data-ttu-id="886cc-143">L "Чаинингмодегкм"</span><span class="sxs-lookup"><span data-stu-id="886cc-143">L"ChainingModeGCM"</span></span><br/> | <span data-ttu-id="886cc-144">Устанавливает режим цепочки алгоритма в режим Галоис/Counter (GCM). **Windows Vista:** Это значение поддерживается начиная с Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="886cc-144">Sets the algorithm's chaining mode to Galois/counter mode (GCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/>       |
| <span data-ttu-id="886cc-145">**\_режим цепочки BCRYPT в \_ \_ НД**</span><span class="sxs-lookup"><span data-stu-id="886cc-145">**BCRYPT\_CHAIN\_MODE\_NA**</span></span>  | <span data-ttu-id="886cc-146">L "Чаинингмоден/A"</span><span class="sxs-lookup"><span data-stu-id="886cc-146">L"ChainingModeN/A"</span></span><br/> | <span data-ttu-id="886cc-147">Алгоритм не поддерживает создание цепочек.</span><span class="sxs-lookup"><span data-stu-id="886cc-147">The algorithm does not support chaining.</span></span><br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_Параметры BCRYPT DH \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT\_DH\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-149">L "Дхпараметерс"</span><span class="sxs-lookup"><span data-stu-id="886cc-149">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-150">Указывает параметры для использования с ключом Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="886cc-150">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="886cc-151">Этот тип данных является указателем на структуру [**\_ \_ \_ заголовков параметра BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="886cc-151">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="886cc-152">Это свойство может быть задано только и должно быть установлено для ключа до завершения выполнения ключа.</span><span class="sxs-lookup"><span data-stu-id="886cc-152">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**Параметры "BCRYPT \_ DSA" \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT\_DSA\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-154">L "Дсапараметерс"</span><span class="sxs-lookup"><span data-stu-id="886cc-154">L"DSAParameters"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-155">Указывает параметры для использования с ключом DSA.</span><span class="sxs-lookup"><span data-stu-id="886cc-155">Specifies parameters to use with a DSA key.</span></span> <span data-ttu-id="886cc-156">Это свойство является [**\_ \_ \_ заголовком параметра BCrypt DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) или структурой [**\_ \_ \_ заголовка \_ 2 параметра BCrypt DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="886cc-156">This property is a [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) or a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="886cc-157">Это свойство может быть задано только и должно быть установлено для ключа до завершения выполнения ключа.</span><span class="sxs-lookup"><span data-stu-id="886cc-157">This property can only be set and must be set for the key before the key is completed.</span></span>

<span data-ttu-id="886cc-158">**Windows 8:** Начиная с Windows 8, это свойство может иметь структуру [**\_ \_ \_ заголовка \_ версии 2 параметра DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="886cc-158">**Windows 8:** Beginning with Windows 8, this property can be a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="886cc-159">Используйте эту структуру, если размер ключа превышает 1024 бит и меньше или равен 3072 бит.</span><span class="sxs-lookup"><span data-stu-id="886cc-159">Use this structure if the key size exceeds 1024 bits and is less than or equal to 3072 bits.</span></span> <span data-ttu-id="886cc-160">Если размер ключа больше или равен 512, но меньше или равен 1024 бит, используйте структуру [**\_ \_ \_ заголовка параметра BCRYPT DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="886cc-160">If the key size is greater than or equal to 512 but less than or equal to 1024 bits, use the [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_Длина действующего \_ ключа BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT\_EFFECTIVE\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-162">L "Еффективекэйленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-162">L"EffectiveKeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-163">Размер (в битах) эффективной длины ключа RC2.</span><span class="sxs-lookup"><span data-stu-id="886cc-163">The size, in bits, of the effective length of an RC2 key.</span></span> <span data-ttu-id="886cc-164">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-164">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_ \_ Длина блока хэша \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT\_HASH\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-166">L "Хашблоккленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-166">L"HashBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-167">Размер (в байтах) блока для хэша.</span><span class="sxs-lookup"><span data-stu-id="886cc-167">The size, in bytes, of the block for a hash.</span></span> <span data-ttu-id="886cc-168">Это свойство применяется только к алгоритмам хэширования.</span><span class="sxs-lookup"><span data-stu-id="886cc-168">This property only applies to hash algorithms.</span></span> <span data-ttu-id="886cc-169">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-169">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_Длина ХЭША \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-171">L "Хашдижестленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-171">L"HashDigestLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-172">Размер (в байтах) хэш-значения поставщика хэша.</span><span class="sxs-lookup"><span data-stu-id="886cc-172">The size, in bytes, of the hash value of a hash provider.</span></span> <span data-ttu-id="886cc-173">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-173">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_список хэш-кодов \_ объекта BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT\_HASH\_OID\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-175">L "Хашоидлист"</span><span class="sxs-lookup"><span data-stu-id="886cc-175">L"HashOIDList"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-176">Список [*идентификаторов объектов*](/windows/desktop/SecGloss/o-gly) хэширования, закодированных в [*der*](/windows/desktop/SecGloss/d-gly).</span><span class="sxs-lookup"><span data-stu-id="886cc-176">The list of [*DER*](/windows/desktop/SecGloss/d-gly)-encoded hashing [*object identifiers*](/windows/desktop/SecGloss/o-gly) (OIDs).</span></span> <span data-ttu-id="886cc-177">Это свойство представляет собой [**структуру \_ \_ списка объекта BCRYPT OID**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) .</span><span class="sxs-lookup"><span data-stu-id="886cc-177">This property is a [**BCRYPT\_OID\_LIST**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) structure.</span></span> <span data-ttu-id="886cc-178">Это свойство может быть доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="886cc-178">This property can only be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_вектор инициализации \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT\_INITIALIZATION\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-180">L "IV"</span><span class="sxs-lookup"><span data-stu-id="886cc-180">L"IV"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-181">Содержит [*вектор инициализации*](/windows/desktop/SecGloss/i-gly) (IV) для ключа.</span><span class="sxs-lookup"><span data-stu-id="886cc-181">Contains the [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) for a key.</span></span> <span data-ttu-id="886cc-182">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="886cc-182">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_Длина ключа \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-184">L "KeyLength"</span><span class="sxs-lookup"><span data-stu-id="886cc-184">L"KeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-185">Размер значения ключа поставщика симметричного ключа (в битах).</span><span class="sxs-lookup"><span data-stu-id="886cc-185">The size, in bits, of the key value of a symmetric key provider.</span></span> <span data-ttu-id="886cc-186">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-186">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_Длина ключей \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT\_KEY\_LENGTHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-188">L "Кэйленгсс"</span><span class="sxs-lookup"><span data-stu-id="886cc-188">L"KeyLengths"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-189">Длина ключа, поддерживаемая алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="886cc-189">The key lengths that are supported by the algorithm.</span></span> <span data-ttu-id="886cc-190">Это свойство представляет структуру [**структуры \_ ключей \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="886cc-190">This property is a [**BCRYPT\_KEY\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="886cc-191">Это свойство применяется только к алгоритмам.</span><span class="sxs-lookup"><span data-stu-id="886cc-191">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_ \_ длина объекта ключа \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT\_KEY\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-193">L "Кэйобжектленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-193">L"KeyObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-194">Это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="886cc-194">This property is not used.</span></span> <span data-ttu-id="886cc-195">Для получения этих сведений используется свойство **\_ \_ Length объекта BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="886cc-195">The **BCRYPT\_OBJECT\_LENGTH** property is used to obtain this information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_сила ключа \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT\_KEY\_STRENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-197">L "Кэйстренгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-197">L"KeyStrength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-198">Число битов в ключе.</span><span class="sxs-lookup"><span data-stu-id="886cc-198">The number of bits in the key.</span></span> <span data-ttu-id="886cc-199">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-199">This data type is a **DWORD**.</span></span> <span data-ttu-id="886cc-200">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="886cc-200">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_ \_ Длина блока сообщений \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT\_MESSAGE\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-202">L "Мессажеблоккленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-202">L"MessageBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-203">Это можно задать для любого маркера ключа, в котором установлен режим цепочки CFB.</span><span class="sxs-lookup"><span data-stu-id="886cc-203">This can be set on any key handle that has the CFB chaining mode set.</span></span> <span data-ttu-id="886cc-204">По умолчанию для этого свойства задано значение 1 для 8-битного CFB.</span><span class="sxs-lookup"><span data-stu-id="886cc-204">By default, this property is set to 1 for 8-bit CFB.</span></span> <span data-ttu-id="886cc-205">Если задать для него размер блока в байтах, то CFB будет использоваться полностью.</span><span class="sxs-lookup"><span data-stu-id="886cc-205">Setting it to the block size in bytes causes full-block CFB to be used.</span></span> <span data-ttu-id="886cc-206">Для ключей XTS он используется для задания размера (в байтах) единицы данных XTS (обычно 512 или 4096).</span><span class="sxs-lookup"><span data-stu-id="886cc-206">For XTS keys it is used to set the size, in bytes, of the XTS Data Unit (commonly 512 or 4096).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT \_ Длина множественных \_ объектов \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT\_MULTI\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-208">L "Мултиобжектленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-208">L"MultiObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-209">Это свойство возвращает [**\_ \_ \_ \_ структуру объекта BCRYPT с несколькими объектами**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), которая содержит сведения, необходимые для вычисления размера буфера объекта.</span><span class="sxs-lookup"><span data-stu-id="886cc-209">This property returns a [**BCRYPT\_MULTI\_OBJECT\_LENGTH\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), which contains information necessary to calculate the size of an object buffer.</span></span> <span data-ttu-id="886cc-210">Это свойство поддерживается только в версиях операционной системы, поддерживающих функцию [**бкрипткреатемултихаш**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .</span><span class="sxs-lookup"><span data-stu-id="886cc-210">This property is only supported on operating system versions that support the [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_длина объекта \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-212">L "Обжектленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-212">L"ObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-213">Размер (в байтах) подобъекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="886cc-213">The size, in bytes, of the subobject of a provider.</span></span> <span data-ttu-id="886cc-214">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-214">This data type is a **DWORD**.</span></span> <span data-ttu-id="886cc-215">В настоящее время поставщики алгоритмов хэширования и симметричного шифра используют выделенные вызывающими буферами буферы для хранения своих подобъектов.</span><span class="sxs-lookup"><span data-stu-id="886cc-215">Currently, the hash and symmetric cipher algorithm providers use caller-allocated buffers to store their subobjects.</span></span> <span data-ttu-id="886cc-216">Например, поставщик хэша требует выделения памяти для хэш-объекта, полученного с помощью функции [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="886cc-216">For example, the hash provider requires you to allocate memory for the hash object obtained with the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="886cc-217">Это свойство предоставляет размер буфера для объекта поставщика, чтобы можно было выделить память для объекта, созданного поставщиком.</span><span class="sxs-lookup"><span data-stu-id="886cc-217">This property provides the buffer size for a provider's object so you can allocate memory for the object created by the provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_схемы заполнения BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT\_PADDING\_SCHEMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-219">L "Паддингсчемес"</span><span class="sxs-lookup"><span data-stu-id="886cc-219">L"PaddingSchemes"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-220">Представляет схему заполнения поставщика алгоритма RSA.</span><span class="sxs-lookup"><span data-stu-id="886cc-220">Represents the padding scheme of the RSA algorithm provider.</span></span> <span data-ttu-id="886cc-221">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-221">This data type is a **DWORD**.</span></span> <span data-ttu-id="886cc-222">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="886cc-222">This can be one of the following values.</span></span>



| <span data-ttu-id="886cc-223">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="886cc-223">Identifier</span></span>                             | <span data-ttu-id="886cc-224">Значение</span><span class="sxs-lookup"><span data-stu-id="886cc-224">Value</span></span>      | <span data-ttu-id="886cc-225">Описание</span><span class="sxs-lookup"><span data-stu-id="886cc-225">Description</span></span>                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| <span data-ttu-id="886cc-226">**\_поддерживаемый \_ маршрутизатор Pad (BCRYPT) \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-226">**BCRYPT\_SUPPORTED\_PAD\_ROUTER**</span></span>     | <span data-ttu-id="886cc-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="886cc-227">0x00000001</span></span> | <span data-ttu-id="886cc-228">Поставщик поддерживает дополнение, добавленное маршрутизатором.</span><span class="sxs-lookup"><span data-stu-id="886cc-228">The provider supports padding added by the router.</span></span>         |
| <span data-ttu-id="886cc-229">**\_Поддерживаемая \_ панель \_ PKCS1 (BCRYPT) \_**</span><span class="sxs-lookup"><span data-stu-id="886cc-229">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_ENC**</span></span> | <span data-ttu-id="886cc-230">0x00000002</span><span class="sxs-lookup"><span data-stu-id="886cc-230">0x00000002</span></span> | <span data-ttu-id="886cc-231">Поставщик поддерживает схему заполнения шифрования PKCS1.</span><span class="sxs-lookup"><span data-stu-id="886cc-231">The provider supports the PKCS1 encryption padding scheme.</span></span> |
| <span data-ttu-id="886cc-232">**\_Поддержка BCRYPT \_ Pad \_ PKCS1 \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="886cc-232">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_SIG**</span></span> | <span data-ttu-id="886cc-233">0x00000004</span><span class="sxs-lookup"><span data-stu-id="886cc-233">0x00000004</span></span> | <span data-ttu-id="886cc-234">Поставщик поддерживает схему заполнения подписи PKCS1.</span><span class="sxs-lookup"><span data-stu-id="886cc-234">The provider supports the PKCS1 signature padding scheme.</span></span>  |
| <span data-ttu-id="886cc-235">**поддерживаемый для заполнения заполненный заполненный \_ \_ \_ OAEP**</span><span class="sxs-lookup"><span data-stu-id="886cc-235">**BCRYPT\_SUPPORTED\_PAD\_OAEP**</span></span>       | <span data-ttu-id="886cc-236">0x00000008</span><span class="sxs-lookup"><span data-stu-id="886cc-236">0x00000008</span></span> | <span data-ttu-id="886cc-237">Поставщик поддерживает схему заполнения OAEP.</span><span class="sxs-lookup"><span data-stu-id="886cc-237">The provider supports the OAEP padding scheme.</span></span>             |
| <span data-ttu-id="886cc-238">**\_поддерживаемая \_ панелью \_ поддержки BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-238">**BCRYPT\_SUPPORTED\_PAD\_PSS**</span></span>        | <span data-ttu-id="886cc-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="886cc-239">0x00000010</span></span> | <span data-ttu-id="886cc-240">Поставщик поддерживает схему заполнения PSS.</span><span class="sxs-lookup"><span data-stu-id="886cc-240">The provider supports the PSS padding scheme.</span></span>              |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_маркер поставщика \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT\_PROVIDER\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-242">L "Провидерхандле"</span><span class="sxs-lookup"><span data-stu-id="886cc-242">L"ProviderHandle"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-243">Маркер поставщика CNG, который создал объект, переданный в параметре *хобжект* .</span><span class="sxs-lookup"><span data-stu-id="886cc-243">The handle of the CNG provider that created the object passed in the *hObject* parameter.</span></span> <span data-ttu-id="886cc-244">Этот тип данных является **\_ \_ обработчиком алгоритма BCRYPT**.</span><span class="sxs-lookup"><span data-stu-id="886cc-244">This data type is a **BCRYPT\_ALG\_HANDLE**.</span></span> <span data-ttu-id="886cc-245">Это свойство может быть извлечено только. его нельзя задать.</span><span class="sxs-lookup"><span data-stu-id="886cc-245">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="886cc-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**\_Длина подписи \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="886cc-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT\_SIGNATURE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="886cc-247">L "Сигнатуреленгс"</span><span class="sxs-lookup"><span data-stu-id="886cc-247">L"SignatureLength"</span></span>
</dt> <dt>



<span data-ttu-id="886cc-248">Размер (в байтах) длины подписи для ключа.</span><span class="sxs-lookup"><span data-stu-id="886cc-248">The size, in bytes, of the length of a signature for a key.</span></span> <span data-ttu-id="886cc-249">Этот тип данных — **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="886cc-249">This data type is a **DWORD**.</span></span> <span data-ttu-id="886cc-250">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="886cc-250">This property only applies to keys.</span></span> <span data-ttu-id="886cc-251">Это свойство может быть извлечено только. его нельзя задать.</span><span class="sxs-lookup"><span data-stu-id="886cc-251">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="886cc-252">Требования</span><span class="sxs-lookup"><span data-stu-id="886cc-252">Requirements</span></span>



| <span data-ttu-id="886cc-253">Требование</span><span class="sxs-lookup"><span data-stu-id="886cc-253">Requirement</span></span> | <span data-ttu-id="886cc-254">Значение</span><span class="sxs-lookup"><span data-stu-id="886cc-254">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="886cc-255">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="886cc-255">Minimum supported client</span></span><br/> | <span data-ttu-id="886cc-256">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="886cc-256">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="886cc-257">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="886cc-257">Minimum supported server</span></span><br/> | <span data-ttu-id="886cc-258">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="886cc-258">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="886cc-259">Header</span><span class="sxs-lookup"><span data-stu-id="886cc-259">Header</span></span><br/>                   | <dl> <span data-ttu-id="886cc-260"><dt>BCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="886cc-260"><dt>Bcrypt.h</dt></span></span> </dl> |



 

