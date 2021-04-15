---
description: Содержит определения терминов безопасности, начинающихся с буквы E.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f1caccd2-3453-448e-b194-bf899eff8091
title: E (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed30465ef5764d4553ceb03e1094b73d940f85f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546114"
---
# <a name="e-security-glossary"></a><span data-ttu-id="b629e-103">E (глоссарий по безопасности)</span><span class="sxs-lookup"><span data-stu-id="b629e-103">E (Security Glossary)</span></span>

<span data-ttu-id="b629e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E F [G](g-gly.md) [р](h-gly.md) [.](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="b629e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b629e-105"><span id="_security_ecb_gly"></span><span id="_SECURITY_ECB_GLY"></span>**ECB**</span><span class="sxs-lookup"><span data-stu-id="b629e-105"><span id="_security_ecb_gly"></span><span id="_SECURITY_ECB_GLY"></span>**ECB**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-106">См. раздел *Electronic режимом*.</span><span class="sxs-lookup"><span data-stu-id="b629e-106">See *electronic codebook*.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-107"><span id="_security_ecc_gly"></span><span id="_SECURITY_ECC_GLY"></span>**РАЗРЯД**</span><span class="sxs-lookup"><span data-stu-id="b629e-107"><span id="_security_ecc_gly"></span><span id="_SECURITY_ECC_GLY"></span>**ECC**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-108">См. раздел *Криптография на основе эллиптических кривых*.</span><span class="sxs-lookup"><span data-stu-id="b629e-108">See *elliptic curve cryptography*.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-109"><span id="_security_efs_gly"></span><span id="_SECURITY_EFS_GLY"></span>**КОМПОНЕНТА**</span><span class="sxs-lookup"><span data-stu-id="b629e-109"><span id="_security_efs_gly"></span><span id="_SECURITY_EFS_GLY"></span>**EFS**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-110">См. *Шифрованная файловая система (EFS)*.</span><span class="sxs-lookup"><span data-stu-id="b629e-110">See *Encrypting File System*.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-111"><span id="_security_eku_gly"></span><span id="_SECURITY_EKU_GLY"></span>**EKU**</span><span class="sxs-lookup"><span data-stu-id="b629e-111"><span id="_security_eku_gly"></span><span id="_SECURITY_EKU_GLY"></span>**EKU**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-112">См. раздел *Расширенное использование ключа*.</span><span class="sxs-lookup"><span data-stu-id="b629e-112">See *enhanced key usage*.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-113"><span id="_security_electronic_codebook_gly"></span><span id="_SECURITY_ELECTRONIC_CODEBOOK_GLY"></span>**электронный режимом**</span><span class="sxs-lookup"><span data-stu-id="b629e-113"><span id="_security_electronic_codebook_gly"></span><span id="_SECURITY_ELECTRONIC_CODEBOOK_GLY"></span>**electronic codebook**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-114">ECB Режим блочного шифрования (каждый блок шифруется по отдельности), который не использует никаких отзывов.</span><span class="sxs-lookup"><span data-stu-id="b629e-114">(ECB) A block cipher mode (each block is encrypted individually) that uses no feedback.</span></span> <span data-ttu-id="b629e-115">Это означает, что все блоки открытого текста, которые идентичны (в одном сообщении или в другом сообщении, зашифрованном с помощью одного и того же ключа), преобразуются в идентичные блоки зашифрованного текста.</span><span class="sxs-lookup"><span data-stu-id="b629e-115">This means any blocks of plaintext that are identical (either in the same message or in a different message that is encrypted with the same key) is transformed into identical ciphertext blocks.</span></span> <span data-ttu-id="b629e-116">Векторы инициализации нельзя использовать с этим режимом шифрования.</span><span class="sxs-lookup"><span data-stu-id="b629e-116">Initialization vectors cannot be used with this cipher mode.</span></span> <span data-ttu-id="b629e-117">Если один бит блока зашифрованного текста искажен, то весь соответствующий блок текста также будет искажен.</span><span class="sxs-lookup"><span data-stu-id="b629e-117">If a single bit of the ciphertext block is garbled, then the entire corresponding plaintext block is also garbled.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-118"><span id="_security_elliptic_curve_cryptography_gly"></span><span id="_SECURITY_ELLIPTIC_CURVE_CRYPTOGRAPHY_GLY"></span>**шифрование на основе эллиптических кривых**</span><span class="sxs-lookup"><span data-stu-id="b629e-118"><span id="_security_elliptic_curve_cryptography_gly"></span><span id="_SECURITY_ELLIPTIC_CURVE_CRYPTOGRAPHY_GLY"></span>**elliptic curve cryptography**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-119">РАЗРЯД Подход к шифрованию с открытым ключом, основанный на свойствах эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="b629e-119">(ECC) An approach to public key cryptography based on properties of elliptic curves.</span></span> <span data-ttu-id="b629e-120">Основным преимуществом ECC является эффективность, что становится важным, так как устройства, применяющие меньшие размеры, и требования к безопасности становятся более ресурсоемкими.</span><span class="sxs-lookup"><span data-stu-id="b629e-120">The primary advantage of ECC is efficiency, which becomes important as devices get smaller and security requirements get more demanding.</span></span> <span data-ttu-id="b629e-121">Например, ключи ECC с 163 бит/с 512 бит — один шестой к одному-сиртиес размер эквивалентных ключей RSA уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="b629e-121">For example, ECC keys between 163 bits and 512 bits are one-sixth to one-thirtieth the size of equivalent security-level RSA keys.</span></span> <span data-ttu-id="b629e-122">По мере увеличения размера ключа относительная эффективность роста ECC.</span><span class="sxs-lookup"><span data-stu-id="b629e-122">As key size increases the relative efficiency of ECC increases.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-123"><span id="_security_encoding_gly"></span><span id="_SECURITY_ENCODING_GLY"></span>**шифрования**</span><span class="sxs-lookup"><span data-stu-id="b629e-123"><span id="_security_encoding_gly"></span><span id="_SECURITY_ENCODING_GLY"></span>**encoding**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-124">Процесс преобразования данных в поток битов.</span><span class="sxs-lookup"><span data-stu-id="b629e-124">The process of turning data into a stream of bits.</span></span> <span data-ttu-id="b629e-125">Кодирование является частью процесса сериализации, преобразующего данные в поток единиц и нулей.</span><span class="sxs-lookup"><span data-stu-id="b629e-125">Encoding is part of the serialization process that converts data into a stream of ones and zeros.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-126"><span id="_security_encoding_type_gly"></span><span id="_SECURITY_ENCODING_TYPE_GLY"></span>**тип кодировки**</span><span class="sxs-lookup"><span data-stu-id="b629e-126"><span id="_security_encoding_type_gly"></span><span id="_SECURITY_ENCODING_TYPE_GLY"></span>**encoding type**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-127">Указывает тип кодирования, используемый для шифрования сертификатов и сообщений.</span><span class="sxs-lookup"><span data-stu-id="b629e-127">Refers to which type of encoding is used for certificate and message encoding.</span></span> <span data-ttu-id="b629e-128">Типы кодировки задаются в виде **DWORD** с типом кодирования сертификата, хранящимся в слове низкого порядка, и типом кодировки сообщений, хранящейся в слове в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="b629e-128">The encoding types are specified as a **DWORD**, with the type of certificate encoding stored in the low-order word and the type of message encoding stored in the high-order word.</span></span> <span data-ttu-id="b629e-129">Хотя некоторым функциям или полям структуры требуется только один из типов кодирования, всегда допустимо указывать и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="b629e-129">Although some functions or structure fields require only one of the encoding types, it is always acceptable to specify both.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-130"><span id="_security_encryption_gly"></span><span id="_SECURITY_ENCRYPTION_GLY"></span>**ключ**</span><span class="sxs-lookup"><span data-stu-id="b629e-130"><span id="_security_encryption_gly"></span><span id="_SECURITY_ENCRYPTION_GLY"></span>**encryption**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-131">Процесс преобразования открытого текста в зашифрованный текст, чтобы предотвратить его чтение и понимание неавторизованной стороной.</span><span class="sxs-lookup"><span data-stu-id="b629e-131">The process of converting plaintext to ciphertext to help prevent it from being read and understood by an unauthorized party.</span></span> <span data-ttu-id="b629e-132">Шифрование является противоположностью расшифровки.</span><span class="sxs-lookup"><span data-stu-id="b629e-132">Encryption is the opposite of decryption.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-133"><span id="_security_encrypted_data_gly"></span><span id="_SECURITY_ENCRYPTED_DATA_GLY"></span>**зашифрованные данные**</span><span class="sxs-lookup"><span data-stu-id="b629e-133"><span id="_security_encrypted_data_gly"></span><span id="_SECURITY_ENCRYPTED_DATA_GLY"></span>**encrypted data**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-134">Данные, преобразованные из открытого текста в зашифрованный текст.</span><span class="sxs-lookup"><span data-stu-id="b629e-134">Data that has been converted from plaintext into ciphertext.</span></span> <span data-ttu-id="b629e-135">Зашифрованные сообщения используются для маскировки содержимого сообщения при его отправке или хранении.</span><span class="sxs-lookup"><span data-stu-id="b629e-135">Encrypted messages are used to disguise the content of a message when it is sent or stored.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-136"><span id="_security_encrypting_file_system_gly"></span><span id="_SECURITY_ENCRYPTING_FILE_SYSTEM_GLY"></span>**шифрованная файловая система (EFS)**</span><span class="sxs-lookup"><span data-stu-id="b629e-136"><span id="_security_encrypting_file_system_gly"></span><span id="_SECURITY_ENCRYPTING_FILE_SYSTEM_GLY"></span>**Encrypting File System**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-137">КОМПОНЕНТА Функция операционной системы Windows, которая позволяет пользователям шифровать файлы и папки на диске NTFS, чтобы защитить их от несанкционированного доступа.</span><span class="sxs-lookup"><span data-stu-id="b629e-137">(EFS) A feature in the Windows operating system that enables users to encrypt files and folders on an NTFS volume disk to keep them safe from access by intruders.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-138"><span id="_security_encryption_and_decryption_functions_gly"></span><span id="_SECURITY_ENCRYPTION_AND_DECRYPTION_FUNCTIONS_GLY"></span>**функции шифрования и расшифровки**</span><span class="sxs-lookup"><span data-stu-id="b629e-138"><span id="_security_encryption_and_decryption_functions_gly"></span><span id="_SECURITY_ENCRYPTION_AND_DECRYPTION_FUNCTIONS_GLY"></span>**encryption and decryption functions**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-139">Упрощенные функции сообщений, используемые для кодирования и шифрования (расшифровки и расшифровки) данных.</span><span class="sxs-lookup"><span data-stu-id="b629e-139">Simplified message functions used to encode and encrypt (or decode and decrypt) data.</span></span> <span data-ttu-id="b629e-140">В качестве набора эти функции включают поддержку одновременного шифрования и расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="b629e-140">As a set, these functions include support for simultaneously encrypting and decrypting data.</span></span>

<span data-ttu-id="b629e-141">См. также [*упрощенные функции сообщений*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b629e-141">See also [*simplified message functions*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b629e-142"><span id="_security_enhanced_content_type_gly"></span><span id="_SECURITY_ENHANCED_CONTENT_TYPE_GLY"></span>**Расширенный тип содержимого**</span><span class="sxs-lookup"><span data-stu-id="b629e-142"><span id="_security_enhanced_content_type_gly"></span><span id="_SECURITY_ENHANCED_CONTENT_TYPE_GLY"></span>**enhanced content type**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-143">Класс данных, содержащихся в сообщении PKCS \# 7, содержащем данные (возможно, зашифрованные), а также расширения криптографии, такие как хэши или подписи.</span><span class="sxs-lookup"><span data-stu-id="b629e-143">A class of data contained in a PKCS \#7 message that contains data (possibly encrypted), plus cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="b629e-144">Типы расширенных данных, определенных в PKCS \# 7, включают подписанные данные, запечатанные данные, подписанные и запечатанные данные, а затем данные (хэшированные).</span><span class="sxs-lookup"><span data-stu-id="b629e-144">Types of enhanced data defined by PKCS \#7 include signed data, enveloped data, signed-and-enveloped data, and digested (hashed) data.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-145"><span id="_security_enhanced_key_usage_gly"></span><span id="_SECURITY_ENHANCED_KEY_USAGE_GLY"></span>**Расширенное использование ключа**</span><span class="sxs-lookup"><span data-stu-id="b629e-145"><span id="_security_enhanced_key_usage_gly"></span><span id="_SECURITY_ENHANCED_KEY_USAGE_GLY"></span>**enhanced key usage**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-146">EKU Расширение сертификата и значение расширенного свойства сертификата.</span><span class="sxs-lookup"><span data-stu-id="b629e-146">(EKU) Both a certificate extension and a certificate extended property value.</span></span> <span data-ttu-id="b629e-147">EKU задает использование, для которых сертификат является действительным.</span><span class="sxs-lookup"><span data-stu-id="b629e-147">An EKU specifies the uses for which a certificate is valid.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-148"><span id="_security_enveloped_data_content_type_gly"></span><span id="_SECURITY_ENVELOPED_DATA_CONTENT_TYPE_GLY"></span>**тип содержимого "Упакованные данные"**</span><span class="sxs-lookup"><span data-stu-id="b629e-148"><span id="_security_enveloped_data_content_type_gly"></span><span id="_SECURITY_ENVELOPED_DATA_CONTENT_TYPE_GLY"></span>**enveloped data content type**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-149">\#Расширенное содержимое PKCS 7, состоящее из зашифрованного содержимого (любого типа) и ключей шифрования содержимого (для одного или нескольких получателей).</span><span class="sxs-lookup"><span data-stu-id="b629e-149">A PKCS \#7 enhanced content that consists of encrypted content (of any type) and content-encryption keys (for one or more recipients).</span></span> <span data-ttu-id="b629e-150">Сочетание зашифрованного содержимого и ключа шифрования для получателя называется *цифровым конвертом* для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="b629e-150">The combination of encrypted content and encryption key for a recipient is called a *digital envelope* for that recipient.</span></span> <span data-ttu-id="b629e-151">Этот тип сообщений следует использовать, если необходимо хранить содержимое секрета сообщения и разрешить получение содержимого только определенным лицам или сущностям.</span><span class="sxs-lookup"><span data-stu-id="b629e-151">This type of message should be used when you want to keep the contents of the message secret and allow only specified persons or entities to retrieve the contents.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-152"><span id="_security_exchange_key_gly"></span><span id="_SECURITY_EXCHANGE_KEY_GLY"></span>**ключ обмена**</span><span class="sxs-lookup"><span data-stu-id="b629e-152"><span id="_security_exchange_key_gly"></span><span id="_SECURITY_EXCHANGE_KEY_GLY"></span>**exchange key**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-153">См. *раздел пара ключей Exchange*.</span><span class="sxs-lookup"><span data-stu-id="b629e-153">See *exchange key pair*.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-154"><span id="_security_exchange_key_pair_gly"></span><span id="_SECURITY_EXCHANGE_KEY_PAIR_GLY"></span>**пара ключей обмена**</span><span class="sxs-lookup"><span data-stu-id="b629e-154"><span id="_security_exchange_key_pair_gly"></span><span id="_SECURITY_EXCHANGE_KEY_PAIR_GLY"></span>**exchange key pair**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-155">Пара, состоящая из открытого и закрытого ключей, которая используется для шифрования сеансовых ключей с целью безопасного хранения этих ключей и обмена ими с другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="b629e-155">A public/private key pair used to encrypt session keys so that they can be safely stored and exchanged with other users.</span></span> <span data-ttu-id="b629e-156">Пары ключей обмена создаются путем вызова функции **криптженкэй** .</span><span class="sxs-lookup"><span data-stu-id="b629e-156">Exchange key pairs are created by calling the **CryptGenKey** function.</span></span>

<span data-ttu-id="b629e-157">Сравните [*пару ключей сигнатуры*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b629e-157">Compare [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b629e-158"><span id="_security_external_store_gly"></span><span id="_SECURITY_EXTERNAL_STORE_GLY"></span>**внешнее хранилище**</span><span class="sxs-lookup"><span data-stu-id="b629e-158"><span id="_security_external_store_gly"></span><span id="_SECURITY_EXTERNAL_STORE_GLY"></span>**external store**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-159">Хранилище сертификатов, в котором хранятся сертификаты, списки отзыва сертификатов и списки CTL в расположении, внешнем по отношению к кэшированной памяти, например в базе данных на сетевом сервере.</span><span class="sxs-lookup"><span data-stu-id="b629e-159">A certificate store that maintains its certificates, CRLs, and CTLs in a location external to cached memory, such as in a database on a network server.</span></span> <span data-ttu-id="b629e-160">Во внешнем хранилище не считываются и не декодируются сертификаты, списки отзыва сертификатов и CTL при вызове функции **цертопенсторе** .</span><span class="sxs-lookup"><span data-stu-id="b629e-160">An external store does not read and decode its certificates, CRLs, and CTL when the **CertOpenStore** function is called.</span></span> <span data-ttu-id="b629e-161">Чтение и декодирование откладывается до вызова метода перечисления или поиска.</span><span class="sxs-lookup"><span data-stu-id="b629e-161">Reading and decoding is deferred until an enumeration or find method is called.</span></span>

</dd> </dl>

 

 



