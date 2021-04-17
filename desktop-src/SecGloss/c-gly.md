---
description: Содержит определения терминов безопасности, начинающихся с буквы C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: db46def4-bfdc-4801-a57d-d568e94a2dbb
title: C (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863422525326ec0a04a597d33a29553006bb014b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663810"
---
# <a name="c-security-glossary"></a><span data-ttu-id="2dccb-103">C (глоссарий по безопасности)</span><span class="sxs-lookup"><span data-stu-id="2dccb-103">C (Security Glossary)</span></span>

<span data-ttu-id="2dccb-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [р](h-gly.md) [.](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="2dccb-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2dccb-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**Корнев**</span><span class="sxs-lookup"><span data-stu-id="2dccb-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**CA**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-106">См. раздел *центр сертификации*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-106">See *certification authority*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**Сертификат ЦС**</span><span class="sxs-lookup"><span data-stu-id="2dccb-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**CA certificate**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-108">Определяет центр сертификации (ЦС), который выдает сертификаты проверки подлинности сервера и клиента серверам и клиентам, запрашивающим эти сертификаты.</span><span class="sxs-lookup"><span data-stu-id="2dccb-108">Identifies the certification authority (CA) that issues server and client authentication certificates to the servers and clients that request these certificates.</span></span> <span data-ttu-id="2dccb-109">Поскольку в сертификате содержится открытый ключ, используемый в цифровых подписях, его также называют сертификатом сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="2dccb-109">Because it contains a public key used in digital signatures, it is also referred to as a signature certificate.</span></span> <span data-ttu-id="2dccb-110">Если центр сертификации является корневым, сертификат ЦС может называться корневым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="2dccb-110">If the CA is a root authority, the CA certificate may be referred to as a root certificate.</span></span> <span data-ttu-id="2dccb-111">Кроме того, иногда его называют сертификатом узла.</span><span class="sxs-lookup"><span data-stu-id="2dccb-111">Also sometimes known as a site certificate.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**Иерархия ЦС**</span><span class="sxs-lookup"><span data-stu-id="2dccb-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**CA hierarchy**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-113">Иерархия центра сертификации (ЦС) содержит несколько центров сертификации.</span><span class="sxs-lookup"><span data-stu-id="2dccb-113">A certification authority (CA) hierarchy contains multiple CAs.</span></span> <span data-ttu-id="2dccb-114">Он организован таким образом, что каждый центр сертификации сертифицирован другим центром сертификации на более высоком уровне иерархии до тех пор, пока не будет достигнут верхний уровень иерархии, также известный как корневой центр.</span><span class="sxs-lookup"><span data-stu-id="2dccb-114">It is organized such that each CA is certified by another CA in a higher level of the hierarchy until the top of the hierarchy, also known as the root authority, is reached.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**КАЛГ \_ DH \_ ефем**</span><span class="sxs-lookup"><span data-stu-id="2dccb-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG\_DH\_EPHEM**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-116">Идентификатор алгоритма CryptoAPI для Diffie-Hellman алгоритма обмена ключами при использовании для создания временных ключей.</span><span class="sxs-lookup"><span data-stu-id="2dccb-116">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of ephemeral keys.</span></span>

<span data-ttu-id="2dccb-117">См. также [*алгоритм обмена ключами Диффи-Хелмана (эфемерный)*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-117">See also [*Diffie-Hellman (ephemeral) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**КАЛГ \_ DH \_ SF**</span><span class="sxs-lookup"><span data-stu-id="2dccb-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG\_DH\_SF**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-119">Идентификатор алгоритма CryptoAPI для Diffie-Hellman алгоритма обмена ключами при использовании для создания ключей хранения и перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2dccb-119">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of store-and-forward keys.</span></span>

<span data-ttu-id="2dccb-120">См. также [*алгоритм обмена ключами Диффи-Хелмана (хранение и переадресация)*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-120">See also [*Diffie-Hellman (store and forward) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**КАЛГ \_ HMAC**</span><span class="sxs-lookup"><span data-stu-id="2dccb-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG\_HMAC**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-122">Идентификатор алгоритма CryptoAPI для алгоритма код проверки подлинности сообщения на основе хэша.</span><span class="sxs-lookup"><span data-stu-id="2dccb-122">The CryptoAPI algorithm identifier for the hash-based Message Authentication Code algorithm.</span></span>

<span data-ttu-id="2dccb-123">См. также [*код проверки подлинности сообщения на основе хэша*](h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-123">See also [*Hash-Based Message Authentication Code*](h-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**КАЛГ \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="2dccb-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG\_MAC**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-125">Идентификатор алгоритма CryptoAPI для алгоритма код проверки подлинности сообщения.</span><span class="sxs-lookup"><span data-stu-id="2dccb-125">The CryptoAPI algorithm identifier for the Message Authentication Code algorithm.</span></span>

<span data-ttu-id="2dccb-126">См. также [*код проверки подлинности сообщения*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-126">See also [*Message Authentication Code*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**КАЛГ \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="2dccb-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG\_MD2**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-128">Идентификатор алгоритма CryptoAPI для хэш-алгоритма MD2.</span><span class="sxs-lookup"><span data-stu-id="2dccb-128">The CryptoAPI algorithm identifier for the MD2 hash algorithm.</span></span>

<span data-ttu-id="2dccb-129">См. также [*алгоритм MD2*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-129">See also [*MD2 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**\_MD5 калг**</span><span class="sxs-lookup"><span data-stu-id="2dccb-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-131">Идентификатор алгоритма CryptoAPI для хэш-алгоритма MD5.</span><span class="sxs-lookup"><span data-stu-id="2dccb-131">The CryptoAPI algorithm identifier for the MD5 hash algorithm.</span></span>

<span data-ttu-id="2dccb-132">См. также [*алгоритм MD5*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-132">See also [*MD5 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**КАЛГ \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="2dccb-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG\_RC2**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-134">Идентификатор алгоритма CryptoAPI для алгоритма блочного шифра RC2.</span><span class="sxs-lookup"><span data-stu-id="2dccb-134">The CryptoAPI algorithm identifier for the RC2 block cipher algorithm.</span></span>

<span data-ttu-id="2dccb-135">См. также [*алгоритм блокировки RC2*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-135">See also [*RC2 block algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**КАЛГ \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="2dccb-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG\_RC4**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-137">Идентификатор алгоритма CryptoAPI для алгоритма потокового шифра RC4.</span><span class="sxs-lookup"><span data-stu-id="2dccb-137">The CryptoAPI algorithm identifier for the RC4 stream cipher algorithm.</span></span>

<span data-ttu-id="2dccb-138">См. также [*алгоритм потока RC4*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-138">See also [*RC4 stream algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**КАЛГ \_ RSA \_ KEYX**</span><span class="sxs-lookup"><span data-stu-id="2dccb-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG\_RSA\_KEYX**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-140">Идентификатор алгоритма CryptoAPI для алгоритма открытого ключа RSA при использовании для обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="2dccb-140">The CryptoAPI algorithm identifier for the RSA public key algorithm when used for key exchange.</span></span>

<span data-ttu-id="2dccb-141">См. также [*алгоритм открытого ключа RSA*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-141">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**КАЛГ \_ RSA \_ Sign**</span><span class="sxs-lookup"><span data-stu-id="2dccb-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG\_RSA\_SIGN**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-143">Идентификатор алгоритма CryptoAPI для алгоритма открытого ключа RSA при использовании для создания цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="2dccb-143">The CryptoAPI algorithm identifier for the RSA public key algorithm when used to generate digital signatures.</span></span>

<span data-ttu-id="2dccb-144">См. также [*алгоритм открытого ключа RSA*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-144">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**\_SHA калг**</span><span class="sxs-lookup"><span data-stu-id="2dccb-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG\_SHA**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-146">Идентификатор алгоритма CryptoAPI для алгоритма безопасного хэширования (SHA-1).</span><span class="sxs-lookup"><span data-stu-id="2dccb-146">The CryptoAPI algorithm identifier for the Secure Hash Algorithm (SHA-1).</span></span>

<span data-ttu-id="2dccb-147">См. также [*безопасный алгоритм хэширования*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-147">See also [*Secure Hash Algorithm*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**ПРИВЕДЕНИЕ**</span><span class="sxs-lookup"><span data-stu-id="2dccb-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**CAST**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-149">Группа симметричных блочных шифров, подобных DES, разработанных C. M.</span><span class="sxs-lookup"><span data-stu-id="2dccb-149">A group of DES-like symmetric block ciphers developed by C. M.</span></span> <span data-ttu-id="2dccb-150">Адамс и S. E.</span><span class="sxs-lookup"><span data-stu-id="2dccb-150">Adams and S. E.</span></span> <span data-ttu-id="2dccb-151">Таваресу.</span><span class="sxs-lookup"><span data-stu-id="2dccb-151">Tavares.</span></span> <span data-ttu-id="2dccb-152">\_ \_ Типы поставщиков Prov MS Exchange указывают КОНКРЕТНЫЙ алгоритм приведения, который использует 64-разрядный размер блока.</span><span class="sxs-lookup"><span data-stu-id="2dccb-152">PROV\_MS\_EXCHANGE provider types specify a particular CAST algorithm that uses a 64-bit block size.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span><span class="sxs-lookup"><span data-stu-id="2dccb-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-154">См. раздел *Шифрование блоков шифра*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-154">See *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**Certificate**</span><span class="sxs-lookup"><span data-stu-id="2dccb-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**certificate**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-156">Документ с цифровой подписью, содержащий информацию о сущности и открытом ключе сущности и привязывающих эти данные друг у другу.</span><span class="sxs-lookup"><span data-stu-id="2dccb-156">A digitally signed statement that contains information about an entity and the entity's public key, thus binding these two pieces of information together.</span></span> <span data-ttu-id="2dccb-157">Сертификат выдается доверенной организацией (или сущностью), называемой *центром сертификации* (ЦС) после того, как центр сертификации проверит, что сущность имеет имя.</span><span class="sxs-lookup"><span data-stu-id="2dccb-157">A certificate is issued by a trusted organization (or entity) called a *certification authority* (CA) after the CA has verified that the entity is who it says it is.</span></span>

<span data-ttu-id="2dccb-158">В сертификатах могут содержаться различные типы данных.</span><span class="sxs-lookup"><span data-stu-id="2dccb-158">Certificates can contain different types of data.</span></span> <span data-ttu-id="2dccb-159">Например, сертификат X.509 включает формат сертификата, серийный номер сертификата, алгоритм сигнатуры сертификата, имя ЦС, которым был издан сертификат, имя и открытый ключ сущности, запрашивающей сертификат, а также сигнатура центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="2dccb-159">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the CA that issued the certificate, the name and public key of the entity requesting the certificate, and the CA's signature.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**большой двоичный объект сертификата**</span><span class="sxs-lookup"><span data-stu-id="2dccb-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**certificate BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-161">Большой двоичный объект, содержащий данные сертификата.</span><span class="sxs-lookup"><span data-stu-id="2dccb-161">A BLOB that contains the certificate data.</span></span>

<span data-ttu-id="2dccb-162">Большой двоичный объект сертификата создается с помощью вызовов **CryptEncodeObject**.</span><span class="sxs-lookup"><span data-stu-id="2dccb-162">A certificate BLOB is created by calls to **CryptEncodeObject**.</span></span> <span data-ttu-id="2dccb-163">Процесс завершается, когда выходные данные вызова содержат все данные сертификата.</span><span class="sxs-lookup"><span data-stu-id="2dccb-163">The process is complete when the output of the call contains all the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="2dccb-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**certificate context**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-165">\_Структура контекста сертификата, которая содержит маркер хранилища сертификатов, указатель на исходный BLOB-объект закодированного сертификата, указатель на \_ структуру сведений о сертификате и член типа кодировки.</span><span class="sxs-lookup"><span data-stu-id="2dccb-165">A CERT\_CONTEXT structure that contains a handle to a certificate store, a pointer to the original encoded certificate BLOB, a pointer to a CERT\_INFO structure, and an encoding type member.</span></span> <span data-ttu-id="2dccb-166">Это структура **\_ сведений** о сертификате, которая содержит большую часть информации сертификата.</span><span class="sxs-lookup"><span data-stu-id="2dccb-166">It is the **CERT\_INFO** structure that contains most of the certificate information.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**функции шифрования и расшифровки сертификатов**</span><span class="sxs-lookup"><span data-stu-id="2dccb-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**certificate encode/decode functions**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-168">Функции, управляющие переводом сертификатов и связанных материалов в стандартные двоичные форматы, которые могут использоваться в разных средах.</span><span class="sxs-lookup"><span data-stu-id="2dccb-168">Functions that manage the translation of certificates and related material into standard, binary formats that can be used in different environments.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**тип кодировки сертификата**</span><span class="sxs-lookup"><span data-stu-id="2dccb-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**certificate encoding type**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-170">Определяет, как кодируется сертификат.</span><span class="sxs-lookup"><span data-stu-id="2dccb-170">Defines how the certificate is encoded.</span></span> <span data-ttu-id="2dccb-171">Тип кодирования сертификата хранится в младшем слове структуры типа кодирования (**DWORD**).</span><span class="sxs-lookup"><span data-stu-id="2dccb-171">The certificate encoding type is stored in the low-order word of the encoding type (**DWORD**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Управление сертификатами через CMS**</span><span class="sxs-lookup"><span data-stu-id="2dccb-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Certificate Management over CMS**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-173">Шифрован.</span><span class="sxs-lookup"><span data-stu-id="2dccb-173">CMC.</span></span> <span data-ttu-id="2dccb-174">Управление сертификатами через CMS.</span><span class="sxs-lookup"><span data-stu-id="2dccb-174">Certificate Management over CMS.</span></span> <span data-ttu-id="2dccb-175">CMC — это протокол управления сертификатами, использующий синтаксис сообщений шифрования (CMS).</span><span class="sxs-lookup"><span data-stu-id="2dccb-175">CMC is a certificate management protocol that uses Cryptographic Message Syntax (CMS).</span></span> <span data-ttu-id="2dccb-176">Корпорация Майкрософт заключает запросы на сертификат CMC в объект запроса [*PKCS \# 7*](p-gly.md) (CMS) перед отправкой запроса на сервер регистрации.</span><span class="sxs-lookup"><span data-stu-id="2dccb-176">Microsoft wraps CMC certificate requests in a [*PKCS \#7*](p-gly.md) (CMS) request object before sending the request to an enrollment server.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**BLOB-объект имени сертификата**</span><span class="sxs-lookup"><span data-stu-id="2dccb-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**certificate name BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-178">Закодированное представление сведений о имени, включенных в сертификаты.</span><span class="sxs-lookup"><span data-stu-id="2dccb-178">An encoded representation of the name information that is included in certificates.</span></span> <span data-ttu-id="2dccb-179">Каждый BLOB-объект имени сопоставляется со структурой **\_ \_ большого двоичного объекта имени сертификата** .</span><span class="sxs-lookup"><span data-stu-id="2dccb-179">Each name BLOB is mapped to a **CERT\_NAME\_BLOB** structure.</span></span>

<span data-ttu-id="2dccb-180">Например, сведения об издателе и субъекте, на которые ссылается структура **\_ сведений о сертификате** , хранятся в двух структурах **\_ \_ больших двоичных объектов сертификатов** .</span><span class="sxs-lookup"><span data-stu-id="2dccb-180">For example, the issuer and subject information referenced by a **CERT\_INFO** structure is stored in two **CERT\_NAME\_BLOB** structures.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**Политика сертификата**</span><span class="sxs-lookup"><span data-stu-id="2dccb-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**certificate policy**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-182">Именованный набор правил, указывающий применимость сертификатов для определенного класса приложений с общими требованиями к безопасности.</span><span class="sxs-lookup"><span data-stu-id="2dccb-182">A named set of rules that indicate the applicability of certificates for a specific class of applications with common security requirements.</span></span> <span data-ttu-id="2dccb-183">Например, такая политика может, например, ограничить определенные сертификаты для транзакций обмена электронными данными в пределах заданных пределов цен.</span><span class="sxs-lookup"><span data-stu-id="2dccb-183">Such a policy might, for example, limit certain certificates to electronic data interchange transactions within given price limits.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**запрос сертификата**</span><span class="sxs-lookup"><span data-stu-id="2dccb-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**certificate request**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-185">Специально отформатированное электронное сообщение (отправленное в ЦС), используемое для запроса сертификата.</span><span class="sxs-lookup"><span data-stu-id="2dccb-185">A specially formatted electronic message (sent to a CA) used to request a certificate.</span></span> <span data-ttu-id="2dccb-186">Запрос должен содержать сведения, необходимые ЦС для проверки подлинности запроса, а также открытый ключ сущности, запрашивающей сертификат.</span><span class="sxs-lookup"><span data-stu-id="2dccb-186">The request must contain the information required by the CA to authenticate the request, plus the public key of the entity requesting the certificate.</span></span>

<span data-ttu-id="2dccb-187">Все сведения, необходимые для создания запроса, сопоставляются со структурой **\_ \_ сведений о запросе сертификата** .</span><span class="sxs-lookup"><span data-stu-id="2dccb-187">All the information necessary to create the request is mapped to a **CERT\_REQUEST\_INFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**список отзыва сертификатов**</span><span class="sxs-lookup"><span data-stu-id="2dccb-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**certificate revocation list**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-189">СПИСКОМ Документ, обслуживаемый и опубликованный центром сертификации (ЦС), который перечисляет сертификаты, выданные ЦС, которые больше не действительны.</span><span class="sxs-lookup"><span data-stu-id="2dccb-189">(CRL) A document maintained and published by a certification authority (CA) that lists certificates issued by the CA that are no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**сервер сертификатов**</span><span class="sxs-lookup"><span data-stu-id="2dccb-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**certificate server**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-191">Сервер, выкоторый выдает сертификаты для определенного ЦС.</span><span class="sxs-lookup"><span data-stu-id="2dccb-191">A server that issues certificates for a particular CA.</span></span> <span data-ttu-id="2dccb-192">Программное обеспечение сервера сертификатов предоставляет настраиваемые службы для выдачи и управления сертификатами, используемыми в системах безопасности, использующих шифрование с открытым ключом.</span><span class="sxs-lookup"><span data-stu-id="2dccb-192">The certificate server software provides customizable services for issuing and managing certificates used in security systems that employ public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Службы сертификатов**</span><span class="sxs-lookup"><span data-stu-id="2dccb-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Certificate Services**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-194">Служба программного обеспечения, которая выдает сертификаты для определенного *центра сертификации* (ЦС).</span><span class="sxs-lookup"><span data-stu-id="2dccb-194">A software service that issues certificates for a particular *certification authority* (CA).</span></span> <span data-ttu-id="2dccb-195">Он предоставляет настраиваемые службы для выдачи сертификатов для предприятия и управления ими.</span><span class="sxs-lookup"><span data-stu-id="2dccb-195">It provides customizable services for issuing and managing certificates for the enterprise.</span></span> <span data-ttu-id="2dccb-196">Сертификаты можно использовать для обеспечения поддержки проверки подлинности, включая безопасную электронную почту, веб-аутентификацию и проверку подлинности с помощью смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="2dccb-196">Certificates can be used to provide authentication support, including secure email, web-based authentication, and smart card authentication.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**хранилище сертификатов**</span><span class="sxs-lookup"><span data-stu-id="2dccb-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-198">Как правило, постоянное хранилище, в котором хранятся сертификаты, списки отзыва сертификатов и списки доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2dccb-198">Typically, a permanent storage where certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs) are stored.</span></span> <span data-ttu-id="2dccb-199">Тем не менее, при работе с сертификатами, которые не требуется помещать в постоянное хранилище, можно создать и открыть хранилище сертификатов, полностью находящееся в оперативной памяти.</span><span class="sxs-lookup"><span data-stu-id="2dccb-199">It is possible, however, to create and open a certificate store solely in memory when working with certificates that do not need to be put in permanent storage.</span></span>

<span data-ttu-id="2dccb-200">Хранилище сертификатов является центральным для большинства функций сертификатов в CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="2dccb-200">The certificate store is central to much of the certificate functionality in CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**функции хранилища сертификатов**</span><span class="sxs-lookup"><span data-stu-id="2dccb-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**certificate store functions**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-202">Функции, управляющие хранением и извлечением данных, таких как сертификаты, списки отзыва сертификатов (CRL) и списки доверия сертификатов (CTL).</span><span class="sxs-lookup"><span data-stu-id="2dccb-202">Functions that manage the storage and retrieval data such as certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs).</span></span> <span data-ttu-id="2dccb-203">Эти функции можно разделить на общие функции сертификатов, функции списка отзыва сертификатов и функции списков доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2dccb-203">These functions can be separated into common certificate functions, certificate revocation list functions, and certificate trust list functions.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="2dccb-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**certificate template**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-205">Конструкция Windows, которая позволяет профилировать сертификаты (т. е. формат и содержимое) на основе их предполагаемого использования.</span><span class="sxs-lookup"><span data-stu-id="2dccb-205">A Windows construct that profiles certificates (that is, it prespecifies the format and content) based on their intended usage.</span></span> <span data-ttu-id="2dccb-206">При запросе [*сертификата*](/windows) из *центра сертификации* (ЦС) Windows Enterprise инициаторы запроса сертификатов, в зависимости от прав доступа, могут выбирать из множества типов сертификатов, основанных на шаблонах сертификатов, таких как подпись пользователя и кода.</span><span class="sxs-lookup"><span data-stu-id="2dccb-206">When requesting a [*certificate*](/windows) from a Windows enterprise *certification authority* (CA), certificate requesters are, depending on their access rights, able to select from a variety of certificate types that are based on certificate templates, such as User and Code Signing.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**список доверия сертификатов**</span><span class="sxs-lookup"><span data-stu-id="2dccb-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**certificate trust list**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-208">ДОВЕРИЯ Предопределенный список элементов, подписанных доверенным лицом.</span><span class="sxs-lookup"><span data-stu-id="2dccb-208">(CTL) A predefined list of items that have been signed by a trusted entity.</span></span> <span data-ttu-id="2dccb-209">Список доверия сертификатов может быть представлен в произвольной форме, например, он может быть задан в виде списка хэш-значений сертификатов или списка имен файлов.</span><span class="sxs-lookup"><span data-stu-id="2dccb-209">A CTL can be anything, such as a list of hashes of certificates, or a list of file names.</span></span> <span data-ttu-id="2dccb-210">Все элементы списка прошли проверку подлинности (утверждены) подписывающей сущностью.</span><span class="sxs-lookup"><span data-stu-id="2dccb-210">All the items in the list are authenticated (approved) by the signing entity.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="2dccb-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-212">Корнев Сущность сохранность для выдачи сертификатов, которые подтверждают, что индивидуальный получатель, компьютер или организация, запрашивающие сертификат, удовлетворяют условиям установленной политики.</span><span class="sxs-lookup"><span data-stu-id="2dccb-212">(CA) An entity entrusted to issue certificates that assert that the recipient individual, computer, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span><span class="sxs-lookup"><span data-stu-id="2dccb-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-214">См. раздел *отзыв шифра*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-214">See *Cipher Feedback*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**режим цепочки**</span><span class="sxs-lookup"><span data-stu-id="2dccb-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**chaining mode**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-216">Режим блочного шифра, который представляет отзыв, сочетая зашифрованный текст и обычный текст.</span><span class="sxs-lookup"><span data-stu-id="2dccb-216">A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="2dccb-217">См. также *цепочки блочных блоков*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-217">See also *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**шифр**</span><span class="sxs-lookup"><span data-stu-id="2dccb-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**cipher**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-219">Криптографический алгоритм, используемый для шифрования данных; то есть, для преобразования открытого текста в зашифрованный текст с помощью предопределенного ключа.</span><span class="sxs-lookup"><span data-stu-id="2dccb-219">A cryptographic algorithm used to encrypt data; that is, to transform plaintext into ciphertext using a predefined key.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Цепочка блоков шифра**</span><span class="sxs-lookup"><span data-stu-id="2dccb-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Cipher Block Chaining**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-221">CBC Метод работы симметричного блочного шифра, который использует отзыв для объединения ранее созданного зашифрованного текста с новым открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="2dccb-221">(CBC) A method of operating a symmetric block cipher that uses feedback to combine previously generated ciphertext with new plaintext.</span></span>

<span data-ttu-id="2dccb-222">Каждый блок открытого текста объединяется с зашифрованным текстом предыдущего блока с помощью операции побитового **исключающего** , прежде чем она будет зашифрована.</span><span class="sxs-lookup"><span data-stu-id="2dccb-222">Each plaintext block is combined with the ciphertext of the previous block by a bitwise-**XOR** operation before it is encrypted.</span></span> <span data-ttu-id="2dccb-223">Сочетание зашифрованного текста и текста гарантирует, что даже если открытый текст содержит много одинаковых блоков, они будут шифроваться в другой блок зашифрованного текста.</span><span class="sxs-lookup"><span data-stu-id="2dccb-223">Combining ciphertext and plaintext ensures that even if the plaintext contains many identical blocks, they will each encrypt to a different ciphertext block.</span></span>

<span data-ttu-id="2dccb-224">При использовании базового поставщика служб шифрования Майкрософт CBC является режимом шифрования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2dccb-224">When the Microsoft Base Cryptographic Provider is used, CBC is the default cipher mode.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Цепочка блочных компьютеров MAC**</span><span class="sxs-lookup"><span data-stu-id="2dccb-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Cipher Block Chaining MAC**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-226">Метод блочного шифра, который шифрует базовые данные с помощью блочного шифра, а затем использует последний зашифрованный блок в качестве хэш-значения.</span><span class="sxs-lookup"><span data-stu-id="2dccb-226">A block cipher method that encrypts the base data with a block cipher and then uses the last encrypted block as the hash value.</span></span> <span data-ttu-id="2dccb-227">Алгоритм шифрования, используемый для создания [*код проверки подлинности сообщения*](m-gly.md) (Mac), указан при создании ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="2dccb-227">The encryption algorithm used to build the [*Message Authentication Code*](m-gly.md) (MAC) is the one that was specified when the session key was created.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Отзыв шифра**</span><span class="sxs-lookup"><span data-stu-id="2dccb-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Cipher Feedback**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-229">CFB Режим блочного шифрования, который обрабатывает небольшие приращения открытого текста в зашифрованном тексте вместо обработки всего блока за раз.</span><span class="sxs-lookup"><span data-stu-id="2dccb-229">(CFB) A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="2dccb-230">В этом режиме используется регистр сдвига, который имеет размер одного блока в длину и разделяется на разделы.</span><span class="sxs-lookup"><span data-stu-id="2dccb-230">This mode uses a shift register that is one block size in length and divided into sections.</span></span> <span data-ttu-id="2dccb-231">Например, если размер блока составляет 64 бит с обработкой восьми бит за раз, регистр сдвига будет разделен на восемь разделов.</span><span class="sxs-lookup"><span data-stu-id="2dccb-231">For example, if the block size is 64 bits with eight bits processed at a time, then the shift register would be divided into eight sections.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**режим шифрования**</span><span class="sxs-lookup"><span data-stu-id="2dccb-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**cipher mode**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-233">Режим блочного шифрования (каждый блок шифруется по отдельности), который можно указать с помощью функции **криптсеткэйпарам** .</span><span class="sxs-lookup"><span data-stu-id="2dccb-233">A block cipher mode (each block is encrypted individually) that can be specified by using the **CryptSetKeyParam** function.</span></span> <span data-ttu-id="2dccb-234">Если в приложении явно не указан один из этих режимов, используется режим шифрования сцепления блоков шифра (CBC).</span><span class="sxs-lookup"><span data-stu-id="2dccb-234">If the application does not explicitly specify one of these modes, then the cipher block chaining (CBC) cipher mode is used.</span></span>

<span data-ttu-id="2dccb-235">ECB: режим блочного шифрования без обратной связи.</span><span class="sxs-lookup"><span data-stu-id="2dccb-235">ECB: A block cipher mode that uses no feedback.</span></span>

<span data-ttu-id="2dccb-236">CBC — режим блочного шифрования, который представляет отзыв путем объединения зашифрованного текста и обычного текста.</span><span class="sxs-lookup"><span data-stu-id="2dccb-236">CBC: A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="2dccb-237">CFB: режим блочного шифрования, который обрабатывает небольшие приращения открытого текста в зашифрованном тексте вместо обработки всего блока за раз.</span><span class="sxs-lookup"><span data-stu-id="2dccb-237">CFB: A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="2dccb-238">ОФБ: режим блочного шифрования, который использует обратную связь, похожую на CFB.</span><span class="sxs-lookup"><span data-stu-id="2dccb-238">OFB: A block cipher mode that uses feedback similar to CFB.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**зашифрованного текста**</span><span class="sxs-lookup"><span data-stu-id="2dccb-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**ciphertext**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-240">Зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2dccb-240">A message that has been encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**виде открытого текста**</span><span class="sxs-lookup"><span data-stu-id="2dccb-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**cleartext**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-242">См. [*открытый текст*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-242">See [*plaintext*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**компьютера**</span><span class="sxs-lookup"><span data-stu-id="2dccb-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-244">Приложение, а не серверное приложение, которое инициирует соединение с сервером.</span><span class="sxs-lookup"><span data-stu-id="2dccb-244">The application, rather than the server application, that initiates a connection to a server.</span></span>

<span data-ttu-id="2dccb-245">Сравните с [*сервером*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2dccb-245">Compare with [*server*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**сертификат клиента**</span><span class="sxs-lookup"><span data-stu-id="2dccb-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**client certificate**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-247">Относится к сертификату, используемому для проверки подлинности клиента, например к проверке подлинности веб-браузера на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="2dccb-247">Refers to a certificate used for client authentication, such as authenticating a web browser on a web server.</span></span> <span data-ttu-id="2dccb-248">Когда клиент веб-браузера пытается получить доступ к защищенному веб-серверу, клиент отправляет свой сертификат на сервер, чтобы разрешить ему проверять удостоверение клиента.</span><span class="sxs-lookup"><span data-stu-id="2dccb-248">When a web browser client attempts to access a secured web server, the client sends its certificate to the server to allow it to verify the client's identity.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**ШИФРОВАН**</span><span class="sxs-lookup"><span data-stu-id="2dccb-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**CMC**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-250">См. раздел *Управление сертификатами через CMS*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-250">See *Certificate Management over CMS*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**Пример**</span><span class="sxs-lookup"><span data-stu-id="2dccb-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-252">См. раздел *API шифрования: следующее поколение*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-252">See *Cryptography API: Next Generation*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**Протокол связи**</span><span class="sxs-lookup"><span data-stu-id="2dccb-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**communication protocol**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-254">Метод, в котором данные сериализуются (преобразуются в строку с единицами и нулями) и десериализуются.</span><span class="sxs-lookup"><span data-stu-id="2dccb-254">The method in which data is serialized (converted to a string of ones and zeros) and deserialized.</span></span> <span data-ttu-id="2dccb-255">Протокол управляется программным обеспечением и оборудованием передачи данных.</span><span class="sxs-lookup"><span data-stu-id="2dccb-255">The protocol is controlled by both software and data-transmission hardware.</span></span>

<span data-ttu-id="2dccb-256">Упрощенный протокол связи, как правило, рассматривается как уровень приложения, уровень кодирования и декодирования, а также аппаратный уровень.</span><span class="sxs-lookup"><span data-stu-id="2dccb-256">Typically discussed in terms of layers, a simplified communication protocol might consist of an application layer, encode/decode layer, and hardware layer.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**ограниченное делегирование**</span><span class="sxs-lookup"><span data-stu-id="2dccb-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**constrained delegation**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-258">Поведение, которое позволяет серверу пересылать запросы от имени клиента только указанному списку служб.</span><span class="sxs-lookup"><span data-stu-id="2dccb-258">Behavior that allows the server to forward requests on behalf of the client only to a specified list of services.</span></span>

<span data-ttu-id="2dccb-259">**Windows XP:** Ограниченное делегирование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2dccb-259">**Windows XP:** Constrained delegation is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**локального**</span><span class="sxs-lookup"><span data-stu-id="2dccb-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-261">Данные безопасности, относящиеся к соединению.</span><span class="sxs-lookup"><span data-stu-id="2dccb-261">The security data relevant to a connection.</span></span> <span data-ttu-id="2dccb-262">Контекст содержит такие сведения, как ключ сеанса и длительность сеанса.</span><span class="sxs-lookup"><span data-stu-id="2dccb-262">A context contains information such as a session key and duration of the session.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**Контекстная функция**</span><span class="sxs-lookup"><span data-stu-id="2dccb-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**context function**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-264">Функции, используемые для подключения к поставщику служб шифрования (CSP).</span><span class="sxs-lookup"><span data-stu-id="2dccb-264">Functions used to connect to a cryptographic service provider (CSP).</span></span> <span data-ttu-id="2dccb-265">Эти функции позволяют приложениям выбрать конкретного CSP по имени или получить его с требуемым классом функциональности.</span><span class="sxs-lookup"><span data-stu-id="2dccb-265">These functions enable applications to choose a specific CSP by name or get one with a needed class of functionality.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**подпись другой стороны**</span><span class="sxs-lookup"><span data-stu-id="2dccb-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**countersignature**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-267">Подпись существующей подписи и сообщения или сигнатуры существующей подписи.</span><span class="sxs-lookup"><span data-stu-id="2dccb-267">A signature of an existing signature and message or a signature of an existing signature.</span></span> <span data-ttu-id="2dccb-268">Подпись другой стороны используется для подписи зашифрованного хэша существующей подписи или отметки времени сообщения.</span><span class="sxs-lookup"><span data-stu-id="2dccb-268">A countersignature is used to sign the encrypted hash of an existing signature or to time stamp a message.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**информации**</span><span class="sxs-lookup"><span data-stu-id="2dccb-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**credentials**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-270">Ранее проверенные данные входа, используемые [*субъектом безопасности*](s-gly.md) для установления собственного удостоверения, например пароля или билета протокола Kerberos.</span><span class="sxs-lookup"><span data-stu-id="2dccb-270">Previously authenticated logon data used by a [*security principal*](s-gly.md) to establish its own identity, such as a password, or a Kerberos protocol ticket.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**СПИСКОМ**</span><span class="sxs-lookup"><span data-stu-id="2dccb-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**CRL**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-272">См. *список отзыва сертификатов*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-272">See *certificate revocation list*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**\_ \_ Шифрование кодировки ASN**</span><span class="sxs-lookup"><span data-stu-id="2dccb-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**CRYPT\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-274">Тип кодировки, указывающий кодировку сертификата.</span><span class="sxs-lookup"><span data-stu-id="2dccb-274">Encoding type that specifies certificate encoding.</span></span> <span data-ttu-id="2dccb-275">Типы кодирования сертификатов хранятся в младшем слове типа **DWORD** (значение: 0x00000001).</span><span class="sxs-lookup"><span data-stu-id="2dccb-275">Certificate encoding types are stored in the low-order word of a **DWORD** (value is: 0x00000001).</span></span> <span data-ttu-id="2dccb-276">Этот тип кодировки функционально аналогичен \_ \_ типу кодирования X509 ASN Encoding.</span><span class="sxs-lookup"><span data-stu-id="2dccb-276">This encoding type is functionally the same as the X509\_ASN\_ENCODING encoding type.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**криптаналисис**</span><span class="sxs-lookup"><span data-stu-id="2dccb-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**cryptanalysis**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-278">Криптаналисис — это искусство и наука о нарушении зашифрованного текста.</span><span class="sxs-lookup"><span data-stu-id="2dccb-278">Cryptanalysis is the art and science of breaking ciphertext.</span></span> <span data-ttu-id="2dccb-279">В отличие от этого, искусство и научные хранение сообщений в безопасности — это криптография.</span><span class="sxs-lookup"><span data-stu-id="2dccb-279">In contrast, the art and science of keeping messages secure is cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span><span class="sxs-lookup"><span data-stu-id="2dccb-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-281">Прикладной программный интерфейс, позволяющий разработчикам приложений добавлять проверку подлинности, кодирование и шифрование приложений на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="2dccb-281">Application programming interface that enables application developers to add authentication, encoding, and encryption to Windows-based applications.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**алгоритм шифрования**</span><span class="sxs-lookup"><span data-stu-id="2dccb-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**cryptographic algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-283">Математическая функция, используемая для шифрования и расшифровки.</span><span class="sxs-lookup"><span data-stu-id="2dccb-283">A mathematical function used for encryption and decryption.</span></span> <span data-ttu-id="2dccb-284">Большинство алгоритмов шифрования основаны на шифре подстановки, транспоситион шифре или их сочетании.</span><span class="sxs-lookup"><span data-stu-id="2dccb-284">Most cryptographic algorithms are based on a substitution cipher, a transposition cipher, or a combination of both.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Дайджест шифрования**</span><span class="sxs-lookup"><span data-stu-id="2dccb-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Cryptographic Digest**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-286">Односторонняя хэш-функция, которая принимает входную строку переменной длины и преобразует ее в выходную строку фиксированной длины (называемую криптографическим дайджестом). Эта выходная строка фиксированной длины является probabilistically уникальной для каждой входной строки и, таким образом, может действовать как отпечаток файла.</span><span class="sxs-lookup"><span data-stu-id="2dccb-286">A one-way hash function that takes a variable-length input string and converts it to a fixed-length output string (called a cryptographic digest.) This fixed-length output string is probabilistically unique for every different input string and thus can act as a fingerprint of a file.</span></span> <span data-ttu-id="2dccb-287">При скачивании файла с дайджестом шифрования получатель повторно выполняет вычисление дайджеста.</span><span class="sxs-lookup"><span data-stu-id="2dccb-287">When a file with a cryptographic digest is downloaded, the receiver recomputes the digest.</span></span> <span data-ttu-id="2dccb-288">Если выходная строка соответствует дайджесту, содержащемуся в файле, получатель подтверждает, что полученный файл не был изменен и идентичен первоначально отправленному файлу.</span><span class="sxs-lookup"><span data-stu-id="2dccb-288">If the output string matches the digest contained in the file, the receiver has proof that the received file was not tampered with and is identical to the file originally sent.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**криптографический ключ**</span><span class="sxs-lookup"><span data-stu-id="2dccb-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**cryptographic key**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-290">Криптографический ключ — это часть данных, необходимая для инициализации алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="2dccb-290">A cryptographic key is a piece of data that is required to initialize a cryptographic algorithm.</span></span> <span data-ttu-id="2dccb-291">Криптографические системы обычно спроектированы таким образом, что их безопасность зависит только от безопасности криптографических ключей, а не от, например от сохранения секрета своих алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="2dccb-291">Cryptographic systems are generally designed so that their security depends only on the security of their cryptographic keys and not, for example, on keeping their algorithms secret.</span></span>

<span data-ttu-id="2dccb-292">Существует множество различных типов криптографических ключей, соответствующих широкому спектру алгоритмов шифрования.</span><span class="sxs-lookup"><span data-stu-id="2dccb-292">There are many different types of cryptographic keys, corresponding to the wide variety of cryptographic algorithms.</span></span> <span data-ttu-id="2dccb-293">Ключи можно классифицировать в соответствии с типом алгоритма, с которым они используются (например, симметричными или асимметричными ключами).</span><span class="sxs-lookup"><span data-stu-id="2dccb-293">Keys can be classified according to the type of algorithm they are used with (for example, as symmetric or asymmetric keys).</span></span> <span data-ttu-id="2dccb-294">Они также могут быть классифицированы на основе времени существования в системе (например, в качестве длительных сеансов или ключей сеанса).</span><span class="sxs-lookup"><span data-stu-id="2dccb-294">They can also be classified based on their lifetime within a system (for example, as long-lived or session keys).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**поставщик служб шифрования**</span><span class="sxs-lookup"><span data-stu-id="2dccb-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**cryptographic service provider**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-296">CSP Независимый программный модуль, который фактически выполняет алгоритмы шифрования для проверки подлинности, кодирования и шифрования.</span><span class="sxs-lookup"><span data-stu-id="2dccb-296">(CSP) An independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**классы**</span><span class="sxs-lookup"><span data-stu-id="2dccb-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**cryptography**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-298">Искусство и наука информационной безопасности.</span><span class="sxs-lookup"><span data-stu-id="2dccb-298">The art and science of information security.</span></span> <span data-ttu-id="2dccb-299">Она включает в себя конфиденциальность информации, целостность данных, проверку подлинности сущностей и проверку подлинности источника данных.</span><span class="sxs-lookup"><span data-stu-id="2dccb-299">It includes information confidentiality, data integrity, entity authentication, and data origin authentication.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**API шифрования**</span><span class="sxs-lookup"><span data-stu-id="2dccb-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**Cryptography API**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-301">См. раздел *CryptoAPI*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-301">See *CryptoAPI*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**API шифрования: следующее поколение**</span><span class="sxs-lookup"><span data-stu-id="2dccb-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**Cryptography API: Next Generation**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-303">Пример Второе поколение *CryptoAPI*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-303">(CNG) The second generation of the *CryptoAPI*.</span></span> <span data-ttu-id="2dccb-304">CNG позволяет заменить существующие поставщики алгоритмов собственными поставщиками и добавить новые алгоритмы по мере их появления.</span><span class="sxs-lookup"><span data-stu-id="2dccb-304">CNG allows you to replace existing algorithm providers with your own providers and add new algorithms as they become available.</span></span> <span data-ttu-id="2dccb-305">CNG также позволяет использовать одни и те же API из приложений для пользователей и режимов ядра.</span><span class="sxs-lookup"><span data-stu-id="2dccb-305">CNG also allows the same APIs to be used from user and kernel mode applications.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**криптологи**</span><span class="sxs-lookup"><span data-stu-id="2dccb-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**cryptology**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-307">Ветвь математики, охватывающая как криптографию, так и криптаналисис.</span><span class="sxs-lookup"><span data-stu-id="2dccb-307">The branch of mathematics that encompasses both cryptography and cryptanalysis.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**криптоспи**</span><span class="sxs-lookup"><span data-stu-id="2dccb-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-309">Системный интерфейс программы, используемый *поставщиком служб шифрования* (CSP).</span><span class="sxs-lookup"><span data-stu-id="2dccb-309">The system program interface used with a *cryptographic service provider* (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span><span class="sxs-lookup"><span data-stu-id="2dccb-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-311">См. раздел *поставщик служб шифрования*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-311">See *cryptographic service provider*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**Семейство CSP**</span><span class="sxs-lookup"><span data-stu-id="2dccb-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP family**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-313">Уникальная группа CSP, использующая один и тот же набор форматов данных и выполняющая их функции аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="2dccb-313">A unique group of CSPs that use the same set of data formats and perform their function in the same way.</span></span> <span data-ttu-id="2dccb-314">Даже если два семейства CSP используют один и тот же алгоритм (например, блочный шифр RC2), их различные схемы заполнения, длины ключей или режимы по умолчанию выполняют разные группы.</span><span class="sxs-lookup"><span data-stu-id="2dccb-314">Even when two CSP families use the same algorithm (for example, the RC2 block cipher), their different padding schemes, keys lengths, or default modes make each group distinct.</span></span> <span data-ttu-id="2dccb-315">Интерфейс CryptoAPI спроектирован так, что каждый тип CSP представляет конкретное семейство.</span><span class="sxs-lookup"><span data-stu-id="2dccb-315">CryptoAPI has been designed so that each CSP type represents a particular family.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**Имя CSP**</span><span class="sxs-lookup"><span data-stu-id="2dccb-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP name**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-317">Текстовое имя CSP.</span><span class="sxs-lookup"><span data-stu-id="2dccb-317">The textual name of the CSP.</span></span> <span data-ttu-id="2dccb-318">Если поставщик удостоверений (CSP) подписан корпорацией Майкрософт, это имя должно точно совпадать с именем CSP, указанным в сертификате соответствия экспорта (ECC).</span><span class="sxs-lookup"><span data-stu-id="2dccb-318">If the CSP has been signed by Microsoft, this name must exactly match the CSP name that was specified in the Export Compliance Certificate (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**Тип CSP**</span><span class="sxs-lookup"><span data-stu-id="2dccb-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP type**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-320">Указывает семейство CSP, связанное с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2dccb-320">Indicates the CSP family associated with a provider.</span></span> <span data-ttu-id="2dccb-321">Когда приложение подключается к CSP определенного типа, каждая из функций CryptoAPI по умолчанию будет работать так, как это было определено семейством, которое соответствует этому типу CSP.</span><span class="sxs-lookup"><span data-stu-id="2dccb-321">When an application connects to a CSP of a particular type, each of the CryptoAPI functions will, by default, operate in a way prescribed by the family that corresponds to that CSP type.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**ДОВЕРИЯ**</span><span class="sxs-lookup"><span data-stu-id="2dccb-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CTL**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-323">См. *список доверия сертификатов*.</span><span class="sxs-lookup"><span data-stu-id="2dccb-323">See *certificate trust list*.</span></span>

</dd> <dt>

<span data-ttu-id="2dccb-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**ЦИЛИНК \_ главный ключ шифрования**</span><span class="sxs-lookup"><span data-stu-id="2dccb-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK\_MEK**</span></span>
</dt> <dd>

<span data-ttu-id="2dccb-325">Алгоритм шифрования, использующий 40-разрядный вариант ключа DES, в котором 16 бит 56-разрядного ключа DES имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="2dccb-325">An encryption algorithm that uses a 40-bit variant of a DES key where 16 bits of the 56-bit DES key are set to zero.</span></span> <span data-ttu-id="2dccb-326">Этот алгоритм реализуется, как указано в спецификации черновика IETF для 40-разрядного алгоритма DES.</span><span class="sxs-lookup"><span data-stu-id="2dccb-326">This algorithm is implemented as specified in the IETF Draft specification for 40-bit DES.</span></span> <span data-ttu-id="2dccb-327">Спецификация черновика на момент написания этой статьи можно найти по адресу ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span><span class="sxs-lookup"><span data-stu-id="2dccb-327">The draft specification, at the time of this writing can be found at ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span></span> <span data-ttu-id="2dccb-328">Этот алгоритм используется со значением **\_ идентификатора ALG** калг \_ цилинк \_ главный ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="2dccb-328">This algorithm is used with the **ALG\_ID** value CALG\_CYLINK\_MEK.</span></span>

</dd> </dl>

 

 
