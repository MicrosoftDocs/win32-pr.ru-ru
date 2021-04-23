---
description: Содержит определения терминов безопасности, начинающихся с буквы P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911248"
---
# <a name="p-security-glossary"></a><span data-ttu-id="d5f76-103">P (глоссарий по безопасности)</span><span class="sxs-lookup"><span data-stu-id="d5f76-103">P (Security Glossary)</span></span>

<span data-ttu-id="d5f76-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [р](h-gly.md) [.](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="d5f76-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d5f76-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**заполнение**</span><span class="sxs-lookup"><span data-stu-id="d5f76-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**padding**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-106">Строка, обычно добавляемая в случае, когда последний блок текста оказывается слишком коротким.</span><span class="sxs-lookup"><span data-stu-id="d5f76-106">A string, typically added when the last plaintext block is short.</span></span> <span data-ttu-id="d5f76-107">Например, если длина блока составляет 64 бит, а последний блок содержит только 40 бит, то в последний блок должны быть добавлены 24 бита заполнения.</span><span class="sxs-lookup"><span data-stu-id="d5f76-107">For example, if the block length is 64 bits and the last block contains only 40 bits, then 24 bits of padding must be added to the last block.</span></span> <span data-ttu-id="d5f76-108">Строка заполнения может содержать нули, чередующиеся нули и единицы или другой шаблон.</span><span class="sxs-lookup"><span data-stu-id="d5f76-108">The padding string may contain zeros, alternating zeros and ones, or some other pattern.</span></span> <span data-ttu-id="d5f76-109">Приложения, использующие [*CryptoAPI*](c-gly.md) , не должны добавлять дополнения к их открытым текстам перед их шифрованием, а также удалять их после расшифровки.</span><span class="sxs-lookup"><span data-stu-id="d5f76-109">Applications that use [*CryptoAPI*](c-gly.md) need not add padding to their plaintext before it is encrypted, nor do they have to remove it after decrypting.</span></span> <span data-ttu-id="d5f76-110">Все это обрабатывается автоматически.</span><span class="sxs-lookup"><span data-stu-id="d5f76-110">This is all handled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**фильтр паролей**</span><span class="sxs-lookup"><span data-stu-id="d5f76-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**password filter**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-112">Библиотека DLL, которая обеспечивает принудительное применение политики паролей и уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="d5f76-112">A DLL that provides password policy enforcement and change notification.</span></span> <span data-ttu-id="d5f76-113">Функции, реализованные фильтрами паролей, вызываются [*локальным центром безопасности*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-113">The functions implemented by password filters are called by the [*Local Security Authority*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**постоянное хранилище**</span><span class="sxs-lookup"><span data-stu-id="d5f76-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-115">Любая среда хранения, которая остается неизменной при отключении питания.</span><span class="sxs-lookup"><span data-stu-id="d5f76-115">Any storage medium that remains intact when the power to it is disconnected.</span></span> <span data-ttu-id="d5f76-116">Многие базы данных [*хранилища сертификатов*](c-gly.md) являются формами постоянного хранилища.</span><span class="sxs-lookup"><span data-stu-id="d5f76-116">Many [*certificate store*](c-gly.md) databases are forms of persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span><span class="sxs-lookup"><span data-stu-id="d5f76-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-118">См. раздел *стандарты криптографии с открытым ключом*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-118">See *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**</span><span class="sxs-lookup"><span data-stu-id="d5f76-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \#1**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-120">Рекомендуемые стандарты для реализации шифрования с открытым ключом на основе алгоритма RSA, как определено в [RFC 3447](https://tools.ietf.org/html/rfc3447).</span><span class="sxs-lookup"><span data-stu-id="d5f76-120">The recommended standards for the implementation of public-key cryptography based on the RSA algorithm as defined in [RFC 3447](https://tools.ietf.org/html/rfc3447).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**</span><span class="sxs-lookup"><span data-stu-id="d5f76-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \#12**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-122">Стандартный синтаксис обмена личной информацией, разработанный и поддерживаемый RSA Data Security, Inc. Этот стандартный синтаксис определяет переносимый формат для хранения и передачи закрытых ключей, сертификатов и прочих секретов пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5f76-122">The Personal Information Exchange Syntax Standard, developed and maintained by RSA Data Security, Inc. This syntax standard specifies a portable format for storing or transporting a user's private keys, certificates, and miscellaneous secrets.</span></span>

<span data-ttu-id="d5f76-123">См. также стандарты шифрования [*сертификатов*](c-gly.md) и *открытого ключа*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-123">See also [*certificate*](c-gly.md) and *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Данные, подписанные PKCS 7**</span><span class="sxs-lookup"><span data-stu-id="d5f76-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \#7 Signed Data**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-125">Объект данных, подписанный с помощью стандарта шифрования с открытым ключом \# 7 (PKCS \# 7) и инкапсулирующий сведения, используемые для подписания файла.</span><span class="sxs-lookup"><span data-stu-id="d5f76-125">A data object that is signed with the Public Key Cryptography Standard \#7 (PKCS \#7) and that encapsulates the information used to sign a file.</span></span> <span data-ttu-id="d5f76-126">Как правило, он включает сертификат и [*корневой сертификат*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-126">Typically, it includes the signer's certificate and the [*root certificate*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**</span><span class="sxs-lookup"><span data-stu-id="d5f76-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \#7**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-128">Стандарт Cryptographic Message Syntax.</span><span class="sxs-lookup"><span data-stu-id="d5f76-128">The Cryptographic Message Syntax Standard.</span></span> <span data-ttu-id="d5f76-129">Определяет общий синтаксис для данных, к которым могут применяться криптографические функции, например цифровая сигнатура и шифрование.</span><span class="sxs-lookup"><span data-stu-id="d5f76-129">A general syntax for data to which cryptography may be applied, such as digital signatures and encryption.</span></span> <span data-ttu-id="d5f76-130">Он также предоставляет синтаксис для распространения сертификатов или списков отзыва сертификатов и других атрибутов сообщений, таких как метки времени, в сообщение.</span><span class="sxs-lookup"><span data-stu-id="d5f76-130">It also provides a syntax for disseminating certificates or certificate revocation lists and other message attributes, such as time stamps, to the message.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**\_ \_ Кодировка PKCS 7 ASN \_**</span><span class="sxs-lookup"><span data-stu-id="d5f76-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS\_7\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-132">[*Тип кодирования сообщений*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-132">A [*message encoding type*](m-gly.md).</span></span> <span data-ttu-id="d5f76-133">Типы кодирования сообщений хранятся в слове типа **DWORD** в высоком порядке (значение: 0x00010000).</span><span class="sxs-lookup"><span data-stu-id="d5f76-133">Message encoding types are stored in the high-order word of a **DWORD** (value is: 0x00010000).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**обычн**</span><span class="sxs-lookup"><span data-stu-id="d5f76-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**plaintext**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-135">Сообщение в незашифрованном виде.</span><span class="sxs-lookup"><span data-stu-id="d5f76-135">A message that is not encrypted.</span></span> <span data-ttu-id="d5f76-136">Незашифрованные сообщения также называют сообщениями с открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="d5f76-136">Plaintext messages are sometimes referred to as cleartext messages.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Переносимый исполняемый образ (PE)**</span><span class="sxs-lookup"><span data-stu-id="d5f76-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Portable Executable (PE) Image**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-138">Стандартный исполняемый формат Windows.</span><span class="sxs-lookup"><span data-stu-id="d5f76-138">The standard Windows executable format.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**УКАЗАННЫЙ**</span><span class="sxs-lookup"><span data-stu-id="d5f76-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-140">См. *функцию псевдо-Random*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-140">See *Pseudo-Random Function*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**основные учетные данные**</span><span class="sxs-lookup"><span data-stu-id="d5f76-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primary credentials**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-142">\_Пакет проверки подлинности MsV1 0 определяет строку основного ключа учетных данных: основная строка учетных данных содержит учетные данные, предоставленные при первоначальном входе в систему.</span><span class="sxs-lookup"><span data-stu-id="d5f76-142">The MsV1\_0 authentication package defines a primary credential key string value: The primary credentials string holds the credentials provided at initial logon time.</span></span> <span data-ttu-id="d5f76-143">Он включает в себя имя пользователя, а также формы с учетом регистра и без учета регистра для пароля пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5f76-143">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

<span data-ttu-id="d5f76-144">См. также [*дополнительные учетные данные*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-144">See also [*supplemental credentials*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**первичный поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="d5f76-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primary service provider**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-146">Поставщик услуг, предоставляющий интерфейсы элемента управления карточке.</span><span class="sxs-lookup"><span data-stu-id="d5f76-146">The service provider that supplies the control interfaces to the card.</span></span> <span data-ttu-id="d5f76-147">Каждая смарт-карта может зарегистрировать своего основного поставщика услуг в базе данных смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d5f76-147">Each smart card can register its primary service provider in the smart card database.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**основной токен**</span><span class="sxs-lookup"><span data-stu-id="d5f76-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primary token**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-149">Маркер доступа, который обычно создается только ядром Windows.</span><span class="sxs-lookup"><span data-stu-id="d5f76-149">An access token that is typically created only by the Windows kernel.</span></span> <span data-ttu-id="d5f76-150">Он может быть назначен процессу для представления сведений о безопасности по умолчанию для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="d5f76-150">It may be assigned to a process to represent the default security information for that process.</span></span>

<span data-ttu-id="d5f76-151">См. также [*маркер доступа*](a-gly.md) и [*маркер олицетворения*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-151">See also [*access token*](a-gly.md) and [*impersonation token*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**основного**</span><span class="sxs-lookup"><span data-stu-id="d5f76-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principal**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-153">См. раздел [*субъект безопасности*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-153">See [*security principal*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**уровень**</span><span class="sxs-lookup"><span data-stu-id="d5f76-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-155">Состояние изолирования от представления или секрета.</span><span class="sxs-lookup"><span data-stu-id="d5f76-155">The condition of being isolated from view or secret.</span></span> <span data-ttu-id="d5f76-156">В отношении сообщений конфиденциальные сообщения — это зашифрованные сообщения, текст которых скрыт от представления.</span><span class="sxs-lookup"><span data-stu-id="d5f76-156">With respect to messages, private messages are encrypted messages whose text is hidden from view.</span></span> <span data-ttu-id="d5f76-157">В отношении ключей закрытый ключ является секретным ключом, который скрыт от других.</span><span class="sxs-lookup"><span data-stu-id="d5f76-157">With respect to keys, a private key is a secret key concealed from others.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**закрытый ключ**</span><span class="sxs-lookup"><span data-stu-id="d5f76-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**private key**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-159">Секретная половина пары ключей, используемой в алгоритме открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="d5f76-159">The secret half of a key pair used in a public key algorithm.</span></span> <span data-ttu-id="d5f76-160">Закрытые ключи обычно используются для шифрования симметричных сеансовых ключей, создания цифровой подписи сообщения или расшифрования сообщения, зашифрованного с помощью соответствующего открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="d5f76-160">Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding public key.</span></span>

<span data-ttu-id="d5f76-161">См. также *открытый ключ*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-161">See also *public key*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB-объект закрытого ключа**</span><span class="sxs-lookup"><span data-stu-id="d5f76-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-163">Ключевой BLOB-объект, содержащий полную пару открытого и закрытого ключей.</span><span class="sxs-lookup"><span data-stu-id="d5f76-163">A key BLOB that contains a complete public/private key pair.</span></span> <span data-ttu-id="d5f76-164">BLOB-объекты с закрытыми ключами используются программами администрирования для передачи пар ключей.</span><span class="sxs-lookup"><span data-stu-id="d5f76-164">Private key BLOBs are used by administrative programs to transport key pairs.</span></span> <span data-ttu-id="d5f76-165">Так как закрытый ключ пары ключей является чрезвычайно конфиденциальным, эти большие двоичные объекты обычно хранятся в зашифрованном виде с помощью симметричного шифра.</span><span class="sxs-lookup"><span data-stu-id="d5f76-165">As the private key portion of the key pair is extremely confidential, these BLOBs are typically kept encrypted with a symmetric cipher.</span></span> <span data-ttu-id="d5f76-166">Эти ключевые BLOB-объекты также могут использоваться расширенными приложениями, в которых пары ключей хранятся в приложении, а не полагаться на механизм хранения CSP.</span><span class="sxs-lookup"><span data-stu-id="d5f76-166">These key BLOBs can also be used by advanced applications where the key pairs are stored within the application, rather than relying on the CSP's storage mechanism.</span></span> <span data-ttu-id="d5f76-167">Большой двоичный объект ключа создается путем вызова функции **криптекспорткэй** .</span><span class="sxs-lookup"><span data-stu-id="d5f76-167">A key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**правом**</span><span class="sxs-lookup"><span data-stu-id="d5f76-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilege**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-169">Право пользователя выполнять различные системные операции, такие как завершение работы системы, загрузка драйверов устройств или изменение системного времени.</span><span class="sxs-lookup"><span data-stu-id="d5f76-169">The right of a user to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span> <span data-ttu-id="d5f76-170">Маркер доступа пользователя содержит список привилегий, которыми владеет пользователь или группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="d5f76-170">A user's access token contains a list of the privileges held by either the user or the user's groups.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**процесс**</span><span class="sxs-lookup"><span data-stu-id="d5f76-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**process**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-172">Контекст безопасности, в рамках которого выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="d5f76-172">The security context under which an application runs.</span></span> <span data-ttu-id="d5f76-173">Как правило, контекст безопасности связывается с пользователем, поэтому все приложения, выполняющиеся в рамках заданного процесса, получают разрешения и привилегии владеющего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5f76-173">Typically, the security context is associated with a user, so all applications running under a given process take on the permissions and privileges of the owning user.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV \_ DSS**</span><span class="sxs-lookup"><span data-stu-id="d5f76-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV\_DSS**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-175">См. раздел *\_ тип поставщика Prov DSS*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-175">See *PROV\_DSS provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**\_Тип поставщика Prov DSS**</span><span class="sxs-lookup"><span data-stu-id="d5f76-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**PROV\_DSS Provider Type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-177">Предопределенный тип поставщика, который поддерживает только цифровые подписи и хэши.</span><span class="sxs-lookup"><span data-stu-id="d5f76-177">Predefined provider type that only supports digital signatures and hashes.</span></span> <span data-ttu-id="d5f76-178">Он определяет алгоритм подписи DSA, а также алгоритмы хэширования MD5 и SHA-1.</span><span class="sxs-lookup"><span data-stu-id="d5f76-178">It specifies the DSA signature algorithm, and the MD5 and SHA-1 hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV \_ DSS \_ DH**</span><span class="sxs-lookup"><span data-stu-id="d5f76-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV\_DSS\_DH**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-180">См. раздел *\_ \_ тип поставщика DH Prov DSS*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-180">See *PROV\_DSS\_DH provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_ \_ Тип поставщика DH Prov DSS**</span><span class="sxs-lookup"><span data-stu-id="d5f76-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**PROV\_DSS\_DH provider type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-182">Предопределенный тип поставщика, обеспечивающий обмен ключами, цифровую подпись и алгоритмы хэширования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-182">Predefined provider type that provides key exchange, digital signature, and hashing algorithms.</span></span> <span data-ttu-id="d5f76-183">Он аналогичен \_ типу поставщика Prov DSS.</span><span class="sxs-lookup"><span data-stu-id="d5f76-183">It is similar to the PROV\_DSS provider type.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV \_ Fortezza**</span><span class="sxs-lookup"><span data-stu-id="d5f76-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV\_FORTEZZA**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-185">См. раздел *\_ тип поставщика Prov Fortezza*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-185">See *PROV\_FORTEZZA provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**\_Тип поставщика Prov Fortezza**</span><span class="sxs-lookup"><span data-stu-id="d5f76-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**PROV\_FORTEZZA provider type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-187">Предопределенный тип поставщика, обеспечивающий обмен ключами, цифровую подпись, шифрование и алгоритмы хэширования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-187">Predefined provider type that provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="d5f76-188">Криптографические протоколы и алгоритмы, заданные этим типом поставщика, принадлежат национальным институтам стандартов и технологий (NIST).</span><span class="sxs-lookup"><span data-stu-id="d5f76-188">The cryptographic protocols and algorithms specified by this provider type are owned by the National Institute of Standards and Technology (NIST).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV \_ MS \_ Exchange**</span><span class="sxs-lookup"><span data-stu-id="d5f76-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV\_MS\_EXCHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-190">См. раздел *\_ \_ тип поставщика Prov MS Exchange*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-190">See *PROV\_MS\_EXCHANGE provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**\_ \_ Тип поставщика Prov MS Exchange**</span><span class="sxs-lookup"><span data-stu-id="d5f76-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**PROV\_MS\_EXCHANGE provider type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-192">Предопределенный тип поставщика, предназначенный для нужд Microsoft Exchange, а также для других приложений, совместимых с Microsoft Mail.</span><span class="sxs-lookup"><span data-stu-id="d5f76-192">Predefined provider type designed for the needs of Microsoft Exchange, as well as other applications that are compatible with Microsoft Mail.</span></span> <span data-ttu-id="d5f76-193">Он обеспечивает обмен ключами, цифровую подпись, шифрование и алгоритмы хэширования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-193">It provides key exchange, digital signature, encryption, and hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV \_ RSA \_ Full**</span><span class="sxs-lookup"><span data-stu-id="d5f76-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV\_RSA\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-195">См. раздел *Prov \_ RSA \_ Full Provider Type*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-195">See *PROV\_RSA\_FULL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_ \_ Тип поставщика Prov RSA**</span><span class="sxs-lookup"><span data-stu-id="d5f76-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_FULL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-197">Предопределенный тип поставщика, определяемый корпорацией Майкрософт и RSA Data Security, Inc. Этот тип поставщика общего назначения обеспечивает обмен ключами, цифровую подпись, шифрование и алгоритмы хэширования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-197">Predefined provider type defined by Microsoft and RSA Data Security, Inc. This general purpose provider type provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="d5f76-198">Обмен ключами, цифровая подпись и алгоритмы шифрования основаны на криптографии с открытым ключом RSA.</span><span class="sxs-lookup"><span data-stu-id="d5f76-198">The key exchange, digital signature, and encryption algorithms are based on RSA public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV \_ RSA \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="d5f76-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV\_RSA\_SIG**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-200">См. раздел *\_ \_ тип поставщика SIG Prov RSA*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-200">See *PROV\_RSA\_SIG provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_ \_ Тип поставщика SIG Prov RSA**</span><span class="sxs-lookup"><span data-stu-id="d5f76-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_SIG provider type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-202">Предопределенный тип поставщика, определяемый корпорацией Майкрософт и RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="d5f76-202">Predefined provider type defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="d5f76-203">Этот тип поставщика является подмножеством PROV \_ RSA \_ Full, предоставляющей только цифровые подписи и алгоритмы хэширования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-203">This provider type is a subset of PROV\_RSA\_FULL that provides only digital signature and hashing algorithms.</span></span> <span data-ttu-id="d5f76-204">Алгоритм цифровых подписей — это алгоритм открытого ключа RSA.</span><span class="sxs-lookup"><span data-stu-id="d5f76-204">The digital signature algorithm is an RSA public key algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="d5f76-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV\_SSL**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-206">См. раздел *\_ тип поставщика SSL Prov*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-206">See *PROV\_SSL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**\_Тип поставщика SSL Prov**</span><span class="sxs-lookup"><span data-stu-id="d5f76-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**PROV\_SSL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-208">Предопределенный тип поставщика, поддерживающий протокол SSL (SSL).</span><span class="sxs-lookup"><span data-stu-id="d5f76-208">Predefined provider type that supports the Secure Sockets Layer (SSL) protocol.</span></span> <span data-ttu-id="d5f76-209">Этот тип обеспечивает шифрование ключей, цифровую подпись, шифрование и алгоритмы хэширования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-209">This type provides key encryption, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="d5f76-210">Спецификация, описывающая протокол SSL, доступна в сети Netscape Communications Corp.</span><span class="sxs-lookup"><span data-stu-id="d5f76-210">A specification explaining SSL is available from Netscape Communications Corp.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**поставщики**</span><span class="sxs-lookup"><span data-stu-id="d5f76-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-212">См. раздел [*поставщик служб шифрования*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-212">See [*Cryptographic Service Provider*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**имя поставщика**</span><span class="sxs-lookup"><span data-stu-id="d5f76-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**provider name**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-214">Имя, используемое для распознавания CSP.</span><span class="sxs-lookup"><span data-stu-id="d5f76-214">A name used to identify a CSP.</span></span> <span data-ttu-id="d5f76-215">Например, базовый поставщик служб шифрования Майкрософт версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="d5f76-215">For example, the Microsoft Base Cryptographic Provider version 1.0.</span></span> <span data-ttu-id="d5f76-216">Имя поставщика обычно используется при вызове функции **CryptAcquireContext** для подключения к CSP.</span><span class="sxs-lookup"><span data-stu-id="d5f76-216">The provider name is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**Тип поставщика**</span><span class="sxs-lookup"><span data-stu-id="d5f76-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**provider type**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-218">Термин, используемый для распознавания типа поставщика служб шифрования (CSP).</span><span class="sxs-lookup"><span data-stu-id="d5f76-218">A term used to identify a type of cryptographic service provider (CSP).</span></span> <span data-ttu-id="d5f76-219">CSP группируются в различные типы поставщиков, представляющие определенные семейства стандартных форматов данных и протоколов.</span><span class="sxs-lookup"><span data-stu-id="d5f76-219">CSPs are grouped into different provider types that represent a specific families of standard data formats and protocols.</span></span> <span data-ttu-id="d5f76-220">В отличие от уникального имени поставщика CSP, типы поставщиков не уникальны для данного CSP.</span><span class="sxs-lookup"><span data-stu-id="d5f76-220">In contrast to a CSP's unique provider name, provider types are not unique for a given CSP.</span></span> <span data-ttu-id="d5f76-221">Тип поставщика обычно используется при вызове функции **CryptAcquireContext** для подключения к CSP.</span><span class="sxs-lookup"><span data-stu-id="d5f76-221">The provider type is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**Функция псевдо-Random**</span><span class="sxs-lookup"><span data-stu-id="d5f76-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**pseudo-random function**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-223">УКАЗАННЫЙ Функция, которая принимает ключ, метку и начальное значение в качестве входных данных, а затем выдает выходные данные произвольной длины.</span><span class="sxs-lookup"><span data-stu-id="d5f76-223">(PRF) A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**пара открытого и закрытого ключей**</span><span class="sxs-lookup"><span data-stu-id="d5f76-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**public/private key pair**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-225">Набор ключей шифрования, используемых в алгоритмах асимметричного шифрования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-225">A set of cryptographic keys used for public key cryptography.</span></span> <span data-ttu-id="d5f76-226">Для каждого пользователя CSP обычно поддерживает две пары открытого и закрытого ключей: пару ключей Exchange и пару ключей цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="d5f76-226">For each user, a CSP usually maintains two public/private key pairs: an exchange key pair and a digital signature key pair.</span></span> <span data-ttu-id="d5f76-227">Обе пары сохраняются от сеанса к сеансу.</span><span class="sxs-lookup"><span data-stu-id="d5f76-227">Both key pairs are maintained from session to session.</span></span>

<span data-ttu-id="d5f76-228">См. раздел пара [*ключей Exchange*](e-gly.md) и пары [*ключей подписи*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5f76-228">See [*exchange key pair*](e-gly.md) and [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**Открытый ключ**</span><span class="sxs-lookup"><span data-stu-id="d5f76-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**public key**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-230">Ключ шифрования, который обычно используется для расшифрования сеансового ключа или цифровой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="d5f76-230">A cryptographic key typically used when decrypting a session key or a digital signature.</span></span> <span data-ttu-id="d5f76-231">Открытый ключ также можно использовать для зашифрования сообщения, которое сможет расшифровать только владелец соответствующего закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="d5f76-231">The public key can also be used to encrypt a message, guaranteeing that only the person with the corresponding private key can decrypt the message.</span></span>

<span data-ttu-id="d5f76-232">См. также *закрытый ключ*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-232">See also *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**алгоритм открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="d5f76-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**public key algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-234">Асимметричный шифр, использующий два ключа: один для шифрования, Открытый ключ, а другой — для расшифровки — закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="d5f76-234">An asymmetric cipher that uses two keys, one for encryption, the public key, and the other for decryption, the private key.</span></span> <span data-ttu-id="d5f76-235">Как видно из имен ключей, Открытый ключ, используемый для кодирования открытого текста, можно сделать доступным для любого.</span><span class="sxs-lookup"><span data-stu-id="d5f76-235">As implied by the key names, the public key used to encode plaintext can be made available to anyone.</span></span> <span data-ttu-id="d5f76-236">Однако закрытый ключ должен оставаться секретным.</span><span class="sxs-lookup"><span data-stu-id="d5f76-236">However, the private key must remain secret.</span></span> <span data-ttu-id="d5f76-237">Только закрытый ключ может расшифровать зашифрованный текст.</span><span class="sxs-lookup"><span data-stu-id="d5f76-237">Only the private key can decrypt the ciphertext.</span></span> <span data-ttu-id="d5f76-238">Алгоритм открытого ключа, используемый в этом процессе, работает медленно (в порядке 1 000 раз медленнее симметричных алгоритмов) и обычно используется для шифрования ключей сеанса или цифровой подписи сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5f76-238">The public key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.</span></span>

<span data-ttu-id="d5f76-239">См. также *открытый* и *закрытый ключи*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-239">See also *public key* and *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB-объект открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="d5f76-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-241">Большой двоичный объект, используемый для хранения открытого ключа в паре открытого и закрытого ключей.</span><span class="sxs-lookup"><span data-stu-id="d5f76-241">A BLOB used to store the public key portion of a public/private key pair.</span></span> <span data-ttu-id="d5f76-242">Большие двоичные объекты с открытым ключом не шифруются, так как открытый ключ, содержащийся в, не является секретным.</span><span class="sxs-lookup"><span data-stu-id="d5f76-242">Public key BLOBs are not encrypted as the public key contained within is not secret.</span></span> <span data-ttu-id="d5f76-243">Большой двоичный объект открытого ключа создается путем вызова функции **криптекспорткэй** .</span><span class="sxs-lookup"><span data-stu-id="d5f76-243">A public key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Стандарты шифрования с открытым ключом**</span><span class="sxs-lookup"><span data-stu-id="d5f76-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Public Key Cryptography Standards**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-245">PKCS Набор стандартов синтаксиса для шифрования с открытым ключом, охватывающий функции безопасности, включая методы для подписывания данных, обмена ключами, запроса сертификатов, шифрования и расшифровки открытого ключа и других функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="d5f76-245">(PKCS) A set of syntax standards for public key cryptography covering security functions, including methods for signing data, exchanging keys, requesting certificates, public key encryption and decryption, and other security functions.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**шифрование с открытым ключом**</span><span class="sxs-lookup"><span data-stu-id="d5f76-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**public key encryption**</span></span>
</dt> <dd>

<span data-ttu-id="d5f76-247">Способ шифрования, в котором используется пара ключей; один ключ используется для зашифрования данных, а другой - для их расшифрования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-247">Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data.</span></span> <span data-ttu-id="d5f76-248">В противоположность этому в алгоритмах симметричного шифрования для зашифрования и расшифрования данных используется один и тот же ключ.</span><span class="sxs-lookup"><span data-stu-id="d5f76-248">In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption.</span></span> <span data-ttu-id="d5f76-249">На практике шифрование с открытым ключом обычно используется для защиты ключа сеанса, используемого алгоритмом симметричного шифрования.</span><span class="sxs-lookup"><span data-stu-id="d5f76-249">In practice, public key cryptography is typically used to protect the session key used by a symmetric encryption algorithm.</span></span> <span data-ttu-id="d5f76-250">В этом случае открытый ключ используется для зашифрования сеансовым ключом, который, в свою очередь, используется для шифрования некоторых данных, а закрытый ключ используется для расшифрования ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="d5f76-250">In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption.</span></span> <span data-ttu-id="d5f76-251">Кроме защиты сеансовых ключей алгоритмы асимметричного шифрования можно также использовать для создания сигнатуры сообщения (с помощью закрытого ключа) и проверки сигнатуры (с помощью открытого ключа).</span><span class="sxs-lookup"><span data-stu-id="d5f76-251">In addition to protecting session keys, public key cryptography may also be used to digitally sign a message (using the private key) and validate the signature (using the public key).</span></span>

<span data-ttu-id="d5f76-252">См. также *алгоритм открытого ключа*.</span><span class="sxs-lookup"><span data-stu-id="d5f76-252">See also *public key algorithm*.</span></span>

</dd> </dl>

 

 



