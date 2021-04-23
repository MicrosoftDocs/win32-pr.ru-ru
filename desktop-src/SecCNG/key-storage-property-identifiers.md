---
description: Используется для задания свойства хранилища ключей.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Идентификаторы свойств хранилища ключей (NCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664651"
---
# <a name="key-storage-property-identifiers"></a><span data-ttu-id="7694e-103">Идентификаторы свойств хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="7694e-103">Key Storage Property Identifiers</span></span>

<span data-ttu-id="7694e-104">Для задания свойства хранилища ключей используются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7694e-104">The following values are used to identify a key storage property.</span></span>

<dl> <dt>

<span data-ttu-id="7694e-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_свойство группы алгоритмов NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT\_ALGORITHM\_GROUP\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-106">L "Группа алгоритмов"</span><span class="sxs-lookup"><span data-stu-id="7694e-106">L"Algorithm Group"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-107">Строка в Юникоде, заканчивающаяся нулем и содержащая имя группы алгоритмов объекта.</span><span class="sxs-lookup"><span data-stu-id="7694e-107">A null-terminated Unicode string that contains the name of the object's algorithm group.</span></span> <span data-ttu-id="7694e-108">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-108">This property only applies to keys.</span></span> <span data-ttu-id="7694e-109">Поставщик хранилища ключей (Майкрософт) возвращает следующие идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="7694e-109">The following identifiers are returned by the Microsoft key storage provider.</span></span>



| <span data-ttu-id="7694e-110">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7694e-110">Identifier</span></span>                                     | <span data-ttu-id="7694e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7694e-111">Value</span></span>              | <span data-ttu-id="7694e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7694e-112">Description</span></span>                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| <span data-ttu-id="7694e-113">**\_ \_ Группа алгоритма NCRYPT RSA \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-113">**NCRYPT\_RSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="7694e-114">RSA</span><span class="sxs-lookup"><span data-stu-id="7694e-114">"RSA"</span></span><br/>   | <span data-ttu-id="7694e-115">Группа алгоритмов RSA.</span><span class="sxs-lookup"><span data-stu-id="7694e-115">The RSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="7694e-116">**\_DH- \_ Группа АЛГОРИТМа \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-116">**NCRYPT\_DH\_ALGORITHM\_GROUP**</span></span><br/>    | <span data-ttu-id="7694e-117">ХЕЛМАНА</span><span class="sxs-lookup"><span data-stu-id="7694e-117">"DH"</span></span><br/>    | <span data-ttu-id="7694e-118">Группа алгоритмов Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="7694e-118">The Diffie-Hellman algorithm group.</span></span><br/>                |
| <span data-ttu-id="7694e-119">**\_ \_ Группа алгоритмов NCRYPT DSA \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-119">**NCRYPT\_DSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="7694e-120">NИСХОДНЫЙ</span><span class="sxs-lookup"><span data-stu-id="7694e-120">"DSA"</span></span><br/>   | <span data-ttu-id="7694e-121">Группа алгоритмов DSA.</span><span class="sxs-lookup"><span data-stu-id="7694e-121">The DSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="7694e-122">**\_ \_ Группа алгоритмов NCRYPT ECDSA \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-122">**NCRYPT\_ECDSA\_ALGORITHM\_GROUP**</span></span><br/> | <span data-ttu-id="7694e-123">ECDSA</span><span class="sxs-lookup"><span data-stu-id="7694e-123">"ECDSA"</span></span><br/> | <span data-ttu-id="7694e-124">Группа алгоритмов DSA на эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="7694e-124">The elliptic curve DSA algorithm group.</span></span><br/>            |
| <span data-ttu-id="7694e-125">**\_ \_ Группа алгоритмов NCRYPT ECDH \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-125">**NCRYPT\_ECDH\_ALGORITHM\_GROUP**</span></span><br/>  | <span data-ttu-id="7694e-126">ECDH</span><span class="sxs-lookup"><span data-stu-id="7694e-126">"ECDH"</span></span><br/>  | <span data-ttu-id="7694e-127">Группа алгоритмов Diffie-Hellman эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="7694e-127">The elliptic curve Diffie-Hellman algorithm group.</span></span><br/> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_свойство алгоритма NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT\_ALGORITHM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-129">L "имя алгоритма"</span><span class="sxs-lookup"><span data-stu-id="7694e-129">L"Algorithm Name"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-130">Строка в Юникоде, заканчивающаяся нулем и содержащая имя алгоритма объекта.</span><span class="sxs-lookup"><span data-stu-id="7694e-130">A null-terminated Unicode string that contains the name of the object's algorithm.</span></span> <span data-ttu-id="7694e-131">Это может быть один из предопределенных [**идентификаторов алгоритма CNG**](cng-algorithm-identifiers.md) или другой зарегистрированный идентификатор алгоритма.</span><span class="sxs-lookup"><span data-stu-id="7694e-131">This can be one of the predefined [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or another registered algorithm identifier.</span></span> <span data-ttu-id="7694e-132">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-132">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT \_ связанный \_ \_ ключ ECDH**</span><span class="sxs-lookup"><span data-stu-id="7694e-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT\_ASSOCIATED\_ECDH\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-134">L "СмарткардассоЦиатедекдхкэй"</span><span class="sxs-lookup"><span data-stu-id="7694e-134">L"SmartCardAssociatedECDHKey"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-135">Значение **LPWSTR** , указывающее имя контейнера для ключа эллиптической кривой Diffie-Hellman (ECDH), используемого во время входа в систему для заданного маркера в ключе алгоритма цифровой подписи на основе эллиптических КРИВЫХ (ECDSA).</span><span class="sxs-lookup"><span data-stu-id="7694e-135">An **LPWSTR** value that indicates the container name of the Elliptic Curve Diffie-Hellman (ECDH) key to use during logon for a given handle to an Elliptic Curve Digital Signature Algorithm (ECDSA) key.</span></span> <span data-ttu-id="7694e-136">Если на карте нет ключей ECDH, [*поставщик хранилища ключей*](/windows/desktop/SecGloss/k-gly) (KSP) не будет иметь значение " **\_ не \_ Найдено**".</span><span class="sxs-lookup"><span data-stu-id="7694e-136">If there are no ECDH keys on the card, the [*key storage provider*](/windows/desktop/SecGloss/k-gly) (KSP) returns **NTE\_NOT\_FOUND**.</span></span> <span data-ttu-id="7694e-137">Это свойство применяется к ключам ECDSA для входа с помощью смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="7694e-137">This property applies to ECDSA keys for logon with smart cards.</span></span> <span data-ttu-id="7694e-138">Свойство поддерживается поставщиком хранилища ключей смарт-карт (Майкрософт), а не поставщиком хранилища ключей программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7694e-138">The property is supported by the Microsoft Smart Card key storage provider and not by the Microsoft Software key storage provider.</span></span>

<span data-ttu-id="7694e-139">**Windows Server 2008 и Windows Vista:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7694e-139">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_ \_ свойство длины блока \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT\_BLOCK\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-141">L "Длина блока"</span><span class="sxs-lookup"><span data-stu-id="7694e-141">L"Block Length"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-142">Значение **типа DWORD** , содержащее длину блока шифрования в байтах.</span><span class="sxs-lookup"><span data-stu-id="7694e-142">A **DWORD** that contains the length, in bytes, of the encryption block.</span></span> <span data-ttu-id="7694e-143">Это свойство применяется только к ключам, поддерживающим шифрование.</span><span class="sxs-lookup"><span data-stu-id="7694e-143">This property only applies to keys that support encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_свойство сертификата \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT\_CERTIFICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-145">L "Смарткардкэйцертификате"</span><span class="sxs-lookup"><span data-stu-id="7694e-145">L"SmartCardKeyCertificate"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-146">[*Большой двоичный объект*](/windows/desktop/SecGloss/b-gly) , содержащий сертификат X. 509, связанный с ключом.</span><span class="sxs-lookup"><span data-stu-id="7694e-146">A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains an X.509 certificate that is associated with the key.</span></span>

<span data-ttu-id="7694e-147">**Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** [*Большой двоичный объект*](/windows/desktop/SecGloss/b-gly) , содержащий [*сертификат*](/windows/desktop/SecGloss/c-gly)ключа [*смарт-карты*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="7694e-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains the [*smart card*](/windows/desktop/SecGloss/s-gly) key [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="7694e-148">Это свойство не поддерживается поставщиком хранилища ключей программного обеспечения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7694e-148">This property is not supported by the Microsoft Software Key Storage Provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT \_ DH- \_ Параметры, \_ свойство**</span><span class="sxs-lookup"><span data-stu-id="7694e-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT\_DH\_PARAMETERS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-150">L "Дхпараметерс"</span><span class="sxs-lookup"><span data-stu-id="7694e-150">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-151">Указывает параметры для использования с ключом Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="7694e-151">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="7694e-152">Этот тип данных является указателем на структуру [**\_ \_ \_ заголовков параметра BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="7694e-152">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="7694e-153">Это свойство может быть задано только и должно быть установлено для ключа до завершения выполнения ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-153">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT \_ Экспорт \_ политики, \_ свойство**</span><span class="sxs-lookup"><span data-stu-id="7694e-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT\_EXPORT\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-155">L "Экспорт политики"</span><span class="sxs-lookup"><span data-stu-id="7694e-155">L"Export Policy"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-156">Значение **типа DWORD** , содержащее набор флагов, указывающих политику экспорта для постоянного ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-156">A **DWORD** that contains a set of flags that specify the export policy for a persisted key.</span></span> <span data-ttu-id="7694e-157">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-157">This property only applies to keys.</span></span> <span data-ttu-id="7694e-158">Может содержать ноль или сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7694e-158">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="7694e-159">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7694e-159">Identifier</span></span>                                    | <span data-ttu-id="7694e-160">Значение</span><span class="sxs-lookup"><span data-stu-id="7694e-160">Value</span></span>      | <span data-ttu-id="7694e-161">Описание</span><span class="sxs-lookup"><span data-stu-id="7694e-161">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7694e-162">**NCRYPT \_ Разрешить \_ \_ флаг экспорта**</span><span class="sxs-lookup"><span data-stu-id="7694e-162">**NCRYPT\_ALLOW\_EXPORT\_FLAG**</span></span>               | <span data-ttu-id="7694e-163">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7694e-163">0x00000001</span></span> | <span data-ttu-id="7694e-164">Закрытый ключ можно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="7694e-164">The private key can be exported.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7694e-165">**NCRYPT \_ Разрешить \_ \_ флаг экспорта в формате обычного текста \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-165">**NCRYPT\_ALLOW\_PLAINTEXT\_EXPORT\_FLAG**</span></span>    | <span data-ttu-id="7694e-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7694e-166">0x00000002</span></span> | <span data-ttu-id="7694e-167">Закрытый ключ можно экспортировать в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="7694e-167">The private key can be exported in plaintext form.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7694e-168">**параметр NCRYPT \_ Разрешить \_ архивацию \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-168">**NCRYPT\_ALLOW\_ARCHIVING\_FLAG**</span></span>            | <span data-ttu-id="7694e-169">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7694e-169">0x00000004</span></span> | <span data-ttu-id="7694e-170">Закрытый ключ можно экспортировать в целях архивирования один раз.</span><span class="sxs-lookup"><span data-stu-id="7694e-170">The private key can be exported once for archiving purposes.</span></span> <span data-ttu-id="7694e-171">Этот флаг применяется только к исходному маркеру ключа, на котором он задан.</span><span class="sxs-lookup"><span data-stu-id="7694e-171">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="7694e-172">Эту политику можно применить только к исходному маркеру ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-172">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="7694e-173">После закрытия маркера ключа его нельзя экспортировать в целях архивирования.</span><span class="sxs-lookup"><span data-stu-id="7694e-173">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span>                   |
| <span data-ttu-id="7694e-174">**NCRYPT \_ Разрешить \_ \_ флаг архивации в виде обычного текста \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-174">**NCRYPT\_ALLOW\_PLAINTEXT\_ARCHIVING\_FLAG**</span></span> | <span data-ttu-id="7694e-175">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7694e-175">0x00000008</span></span> | <span data-ttu-id="7694e-176">Закрытый ключ можно экспортировать один раз в виде обычного текста в целях архивирования.</span><span class="sxs-lookup"><span data-stu-id="7694e-176">The private key can be exported once in plaintext form for archiving purposes.</span></span> <span data-ttu-id="7694e-177">Этот флаг применяется только к исходному маркеру ключа, на котором он задан.</span><span class="sxs-lookup"><span data-stu-id="7694e-177">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="7694e-178">Эту политику можно применить только к исходному маркеру ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-178">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="7694e-179">После закрытия маркера ключа его нельзя экспортировать в целях архивирования.</span><span class="sxs-lookup"><span data-stu-id="7694e-179">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_ \_ свойство типа Impl \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT\_IMPL\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-181">L "Impl Type"</span><span class="sxs-lookup"><span data-stu-id="7694e-181">L"Impl Type"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-182">Значение **типа DWORD** , содержащее набор флагов, определяющих сведения о реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="7694e-182">A **DWORD** that contains a set of flags that define implementation details of the provider.</span></span> <span data-ttu-id="7694e-183">Это свойство применимо только к поставщикам хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="7694e-183">This property only applies to key storage providers.</span></span> <span data-ttu-id="7694e-184">Может содержать ноль или сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7694e-184">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="7694e-185">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7694e-185">Identifier</span></span>                            | <span data-ttu-id="7694e-186">Значение</span><span class="sxs-lookup"><span data-stu-id="7694e-186">Value</span></span>      | <span data-ttu-id="7694e-187">Описание</span><span class="sxs-lookup"><span data-stu-id="7694e-187">Description</span></span>                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="7694e-188">**\_ \_ флаг оборудования NCRYPT \_ Impl**</span><span class="sxs-lookup"><span data-stu-id="7694e-188">**NCRYPT\_IMPL\_HARDWARE\_FLAG**</span></span>      | <span data-ttu-id="7694e-189">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7694e-189">0x00000001</span></span> | <span data-ttu-id="7694e-190">Поставщик зависит от оборудования.</span><span class="sxs-lookup"><span data-stu-id="7694e-190">The provider is hardware based.</span></span>                           |
| <span data-ttu-id="7694e-191">**\_ \_ флаг программного обеспечения NCRYPT Impl \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-191">**NCRYPT\_IMPL\_SOFTWARE\_FLAG**</span></span>      | <span data-ttu-id="7694e-192">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7694e-192">0x00000002</span></span> | <span data-ttu-id="7694e-193">Поставщик основан на программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="7694e-193">The provider is software based.</span></span>                           |
| <span data-ttu-id="7694e-194">**\_флаг NCRYPT Impl " \_ съемный" \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-194">**NCRYPT\_IMPL\_REMOVABLE\_FLAG**</span></span>     | <span data-ttu-id="7694e-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7694e-195">0x00000008</span></span> | <span data-ttu-id="7694e-196">Поставщик является съемным.</span><span class="sxs-lookup"><span data-stu-id="7694e-196">The provider is removable.</span></span>                                |
| <span data-ttu-id="7694e-197">**\_ \_ \_ флаг РНГ оборудования NCRYPT \_ Impl**</span><span class="sxs-lookup"><span data-stu-id="7694e-197">**NCRYPT\_IMPL\_HARDWARE\_RNG\_FLAG**</span></span> | <span data-ttu-id="7694e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7694e-198">0x00000010</span></span> | <span data-ttu-id="7694e-199">Поставщик является генератором случайных чисел на основе оборудования.</span><span class="sxs-lookup"><span data-stu-id="7694e-199">The provider is a hardware based random number generator.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_ \_ свойство типа ключа \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT\_KEY\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-201">L "тип ключа"</span><span class="sxs-lookup"><span data-stu-id="7694e-201">L"Key Type"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-202">Значение типа **DWORD** , содержащее набор флагов, определяющих тип ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-202">A **DWORD** that contains a set of flags that define the key type.</span></span> <span data-ttu-id="7694e-203">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-203">This property only applies to keys.</span></span> <span data-ttu-id="7694e-204">Может содержать ноль или следующее значение.</span><span class="sxs-lookup"><span data-stu-id="7694e-204">This can contain zero or the following value.</span></span>



| <span data-ttu-id="7694e-205">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7694e-205">Identifier</span></span>                     | <span data-ttu-id="7694e-206">Значение</span><span class="sxs-lookup"><span data-stu-id="7694e-206">Value</span></span>      | <span data-ttu-id="7694e-207">Описание</span><span class="sxs-lookup"><span data-stu-id="7694e-207">Description</span></span>                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7694e-208">**\_ \_ флаг ключа компьютера \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-208">**NCRYPT\_MACHINE\_KEY\_FLAG**</span></span> | <span data-ttu-id="7694e-209">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7694e-209">0x00000001</span></span> | <span data-ttu-id="7694e-210">Ключ применяется к локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="7694e-210">The key applies to the local computer.</span></span> <span data-ttu-id="7694e-211">Если этот флаг отсутствует, ключ применяется к текущему пользователю.</span><span class="sxs-lookup"><span data-stu-id="7694e-211">If this flag is not present, the key applies to the current user.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_ \_ свойство использования ключа \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT\_KEY\_USAGE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-213">L "использование ключа"</span><span class="sxs-lookup"><span data-stu-id="7694e-213">L"Key Usage"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-214">Значение **типа DWORD** , содержащее набор флагов, определяющих сведения об использовании для ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-214">A **DWORD** that contains a set of flags that define the usage details for a key.</span></span> <span data-ttu-id="7694e-215">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-215">This property only applies to keys.</span></span> <span data-ttu-id="7694e-216">Может содержать ноль или сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7694e-216">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="7694e-217">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7694e-217">Identifier</span></span>                              | <span data-ttu-id="7694e-218">Значение</span><span class="sxs-lookup"><span data-stu-id="7694e-218">Value</span></span>      | <span data-ttu-id="7694e-219">Описание</span><span class="sxs-lookup"><span data-stu-id="7694e-219">Description</span></span>                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| <span data-ttu-id="7694e-220">**NCRYPT \_ Разрешить \_ флаг расшифровки \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-220">**NCRYPT\_ALLOW\_DECRYPT\_FLAG**</span></span>        | <span data-ttu-id="7694e-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7694e-221">0x00000001</span></span> | <span data-ttu-id="7694e-222">Ключ можно использовать для расшифровки.</span><span class="sxs-lookup"><span data-stu-id="7694e-222">The key can be used for decryption.</span></span>                  |
| <span data-ttu-id="7694e-223">**NCRYPT \_ Разрешить \_ \_ флаг подписи**</span><span class="sxs-lookup"><span data-stu-id="7694e-223">**NCRYPT\_ALLOW\_SIGNING\_FLAG**</span></span>        | <span data-ttu-id="7694e-224">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7694e-224">0x00000002</span></span> | <span data-ttu-id="7694e-225">Ключ можно использовать для подписывания.</span><span class="sxs-lookup"><span data-stu-id="7694e-225">The key can be used for signing.</span></span>                     |
| <span data-ttu-id="7694e-226">**\_флаг разрешения \_ \_ соглашения \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-226">**NCRYPT\_ALLOW\_KEY\_AGREEMENT\_FLAG**</span></span> | <span data-ttu-id="7694e-227">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7694e-227">0x00000004</span></span> | <span data-ttu-id="7694e-228">Ключ можно использовать для шифрования секретного соглашения.</span><span class="sxs-lookup"><span data-stu-id="7694e-228">The key can be used for secret agreement encryption.</span></span> |
| <span data-ttu-id="7694e-229">**NCRYPT \_ Разрешить \_ все \_ случаи использования**</span><span class="sxs-lookup"><span data-stu-id="7694e-229">**NCRYPT\_ALLOW\_ALL\_USAGES**</span></span>          | <span data-ttu-id="7694e-230">0x00ffffff</span><span class="sxs-lookup"><span data-stu-id="7694e-230">0x00ffffff</span></span> | <span data-ttu-id="7694e-231">Ключ можно использовать для любой цели.</span><span class="sxs-lookup"><span data-stu-id="7694e-231">The key can be used for any purpose.</span></span>                 |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**\_свойство "Дата последнего \_ изменения NCRYPT" \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT\_LAST\_MODIFIED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-233">L "изменено"</span><span class="sxs-lookup"><span data-stu-id="7694e-233">L"Modified"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-234">Указывает время последнего изменения ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-234">Indicates when the key was last modified.</span></span> <span data-ttu-id="7694e-235">Этот тип данных является указателем на структуру [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="7694e-235">This data type is a pointer to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="7694e-236">Это свойство применяется только к материализованным ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-236">This property only applies to persisted keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_свойство длины \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-238">L "Длина"</span><span class="sxs-lookup"><span data-stu-id="7694e-238">L"Length"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-239">Значение **типа DWORD** , содержащее длину ключа в битах.</span><span class="sxs-lookup"><span data-stu-id="7694e-239">A **DWORD** that contains the length, in bits, of the key.</span></span> <span data-ttu-id="7694e-240">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-240">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_свойство длины \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT\_LENGTHS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-242">L "Длина"</span><span class="sxs-lookup"><span data-stu-id="7694e-242">L"Lengths"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-243">Указывает размеры ключей, поддерживаемые ключом.</span><span class="sxs-lookup"><span data-stu-id="7694e-243">Indicates the key sizes that are supported by the key.</span></span> <span data-ttu-id="7694e-244">Этот тип данных является указателем на [**поддерживаемую в NCRYPT структуру \_ \_ длин**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) , которая содержит эту информацию.</span><span class="sxs-lookup"><span data-stu-id="7694e-244">This data type is a pointer to an [**NCRYPT\_SUPPORTED\_LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) structure that contains this information.</span></span> <span data-ttu-id="7694e-245">Это свойство применяется только к ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-245">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT \_ . \_ Максимальное \_ значение длины имени \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT\_MAX\_NAME\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-247">L "максимальная длина имени"</span><span class="sxs-lookup"><span data-stu-id="7694e-247">L"Max Name Length"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-248">Значение **типа DWORD** , содержащее максимальную длину (в символах) имени постоянного ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-248">A **DWORD** that contains the maximum length, in characters, of the name of a persistent key.</span></span> <span data-ttu-id="7694e-249">Это свойство применяется только к поставщику.</span><span class="sxs-lookup"><span data-stu-id="7694e-249">This property only applies to a provider.</span></span>

<span data-ttu-id="7694e-250">Это свойство в основном предназначено для использования поставщиками хранилища ключей, которые хранят ключи на устройстве с ограниченным объемом доступной памяти, например смарт-картой.</span><span class="sxs-lookup"><span data-stu-id="7694e-250">This property is primarily intended to be used by key storage providers that store their keys on a device that has a limited amount of available memory, such as a smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_параметр имени \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-252">L "имя"</span><span class="sxs-lookup"><span data-stu-id="7694e-252">L"Name"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-253">Указатель на строку в Юникоде, заканчивающуюся нулем, которая содержит имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7694e-253">A pointer to a null-terminated Unicode string that contains the name of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT \_ , \_ свойство подсказки для закрепления \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT\_PIN\_PROMPT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-255">L "Смарткардпинпромпт"</span><span class="sxs-lookup"><span data-stu-id="7694e-255">L"SmartCardPinPrompt"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-256">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7694e-256">This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT, \_ свойство ПИН-кода \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-258">L "Смарткардпин"</span><span class="sxs-lookup"><span data-stu-id="7694e-258">L"SmartCardPin"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-259">Указатель на строку в Юникоде, заканчивающуюся нулем и содержащую ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="7694e-259">A pointer to a null-terminated Unicode string that contains the PIN.</span></span> <span data-ttu-id="7694e-260">ПИН-код используется для ключа смарт-карты или пароля защищенного паролем ключа, хранящегося в KSP на основе программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7694e-260">The PIN is used for a smart card key or the password for a password-protected key stored in a software-based KSP.</span></span> <span data-ttu-id="7694e-261">Это свойство можно задать только.</span><span class="sxs-lookup"><span data-stu-id="7694e-261">This property can only be set.</span></span> <span data-ttu-id="7694e-262">Microsoft KSP кэширует это значение, чтобы пользователю было предложено только один раз для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="7694e-262">Microsoft KSPs will cache this value so that the user is only prompted once per process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_ \_ свойство Handle поставщика \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT\_PROVIDER\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-264">L "маркер поставщика"</span><span class="sxs-lookup"><span data-stu-id="7694e-264">L"Provider Handle"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-265">**Обработчик NCRYPT \_ Prov \_** , который содержит маркер поставщика хранилища ключей CNG.</span><span class="sxs-lookup"><span data-stu-id="7694e-265">An **NCRYPT\_PROV\_HANDLE** that contains the handle of the CNG key storage provider.</span></span> <span data-ttu-id="7694e-266">По завершении использования маркера необходимо вызвать [**нкриптфриобжект**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) , чтобы освободить его.</span><span class="sxs-lookup"><span data-stu-id="7694e-266">When you are finished using the handle, you must call [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) to release it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_свойство считывателя NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT\_READER\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-268">L "Смарткардреадер"</span><span class="sxs-lookup"><span data-stu-id="7694e-268">L"SmartCardReader"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-269">Указатель на строку в Юникоде, завершающуюся нулем, которая содержит имя считывателя смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="7694e-269">A pointer to a null-terminated Unicode string that contains the name of the smart card reader.</span></span> <span data-ttu-id="7694e-270">Это свойство можно задать только.</span><span class="sxs-lookup"><span data-stu-id="7694e-270">This property can only be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_свойство root \_ ЦЕРТСТОРЕ для NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT\_ROOT\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-272">L "Смарткардрутцертсторе"</span><span class="sxs-lookup"><span data-stu-id="7694e-272">L"SmartcardRootCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-273">Объект **хцертсторе** , представляющий хранилище корневых сертификатов смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7694e-273">An **HCERTSTORE** that represents the smart card root certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_ \_ идентификатор ПИН-кода бросить**</span><span class="sxs-lookup"><span data-stu-id="7694e-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span> **NCRYPT\_SCARD\_PIN\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-275">L "Смарткардпинид"</span><span class="sxs-lookup"><span data-stu-id="7694e-275">L"SmartCardPinId"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-276">Указатель на значение **\_ идентификатора ПИН-кода** , связанное с заданным [*криптографическим ключом*](/windows/desktop/SecGloss/c-gly) на [*интеллектуальной карте*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="7694e-276">A pointer to the **PIN\_ID** value associated with a given [*cryptographic key*](/windows/desktop/SecGloss/c-gly) on a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="7694e-277">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7694e-277">This is a read-only property.</span></span> <span data-ttu-id="7694e-278">Тип данных **PIN \_ ID** определяется в Cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="7694e-278">The **PIN\_ID** data type is defined in Cardmod.h.</span></span>

<span data-ttu-id="7694e-279">**Windows Server 2008 и Windows Vista:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7694e-279">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**\_ \_ сведения о ПИН-коде для NCRYPT бросить \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT\_SCARD\_PIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-281">L "Смарткардпининфо"</span><span class="sxs-lookup"><span data-stu-id="7694e-281">L"SmartCardPinInfo"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-282">Указатель на [**\_ информационную**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) структуру ПИН-кода, связанный с заданным криптографическим ключом на смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="7694e-282">A pointer to [**PIN\_INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) structure of the PIN associated with a given cryptographic key on the smart card.</span></span> <span data-ttu-id="7694e-283">Вызывающий объект предоставляет маркер ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-283">The caller provides the key handle.</span></span> <span data-ttu-id="7694e-284">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7694e-284">This property is a read-only property.</span></span> <span data-ttu-id="7694e-285">**\_ Информационная структура ПИН-кода** определена в Cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="7694e-285">The **PIN\_INFO** structure is defined in Cardmod.h.</span></span>

<span data-ttu-id="7694e-286">**Windows Server 2008 и Windows Vista:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7694e-286">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_свойство безопасного \_ ПИН-кода NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT\_SECURE\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-288">L "Смарткардсекурепин"</span><span class="sxs-lookup"><span data-stu-id="7694e-288">L"SmartCardSecurePin"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-289">Указатель на строку в Юникоде, заканчивающуюся нулем, которая содержит ПИН-код сеанса для смарт карты.</span><span class="sxs-lookup"><span data-stu-id="7694e-289">A pointer to a null-terminated Unicode string that contains the smart card session PIN.</span></span> <span data-ttu-id="7694e-290">Это свойство можно задать только.</span><span class="sxs-lookup"><span data-stu-id="7694e-290">This property can only be set.</span></span>

<span data-ttu-id="7694e-291">**Windows Vista:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7694e-291">**Windows Vista:** This property is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT \_ Security \_ descr, \_ свойство**</span><span class="sxs-lookup"><span data-stu-id="7694e-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT\_SECURITY\_DESCR\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-293">L "Security Descr"</span><span class="sxs-lookup"><span data-stu-id="7694e-293">L"Security Descr"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-294">Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , которая содержит сведения об управлении доступом для ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-294">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains access control information for the key.</span></span> <span data-ttu-id="7694e-295">Это свойство применяется только к постоянным ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-295">This property only applies to persistent keys.</span></span> <span data-ttu-id="7694e-296">Параметр *dwFlags* функции [**нкриптжетпроперти**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) или [**нкриптсетпроперти**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) определяет часть дескриптора безопасности, которую необходимо получить или задать.</span><span class="sxs-lookup"><span data-stu-id="7694e-296">The *dwFlags* parameter of the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) or [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function identifies the part of the security descriptor to get or set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT \_ Security \_ Descr \_ , \_ свойство поддержки**</span><span class="sxs-lookup"><span data-stu-id="7694e-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT\_SECURITY\_DESCR\_SUPPORT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-298">L "Поддержка Descr безопасности"</span><span class="sxs-lookup"><span data-stu-id="7694e-298">L"Security Descr Support"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-299">Указывает, поддерживает ли поставщик дескрипторы безопасности для ключей.</span><span class="sxs-lookup"><span data-stu-id="7694e-299">Indicates whether the provider supports security descriptors for keys.</span></span> <span data-ttu-id="7694e-300">Это свойство имеет значение **типа DWORD** , содержащее 1, если поставщик поддерживает дескрипторы безопасности для ключей.</span><span class="sxs-lookup"><span data-stu-id="7694e-300">This property is a **DWORD** that contains 1 if the provider supports security descriptors for keys.</span></span> <span data-ttu-id="7694e-301">Если это свойство содержит любое другое значение или если функция [**нкриптжетпроперти**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) возвращает параметр " **\_ не \_ поддерживается**", поставщик не поддерживает дескрипторы безопасности для ключей.</span><span class="sxs-lookup"><span data-stu-id="7694e-301">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support security descriptors for keys.</span></span> <span data-ttu-id="7694e-302">Это свойство применяется только к поставщикам.</span><span class="sxs-lookup"><span data-stu-id="7694e-302">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_свойство GUID смарт-карты NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT\_SMARTCARD\_GUID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-304">L "Смарткардгуид"</span><span class="sxs-lookup"><span data-stu-id="7694e-304">L"SmartCardGuid"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-305">Большой двоичный объект, содержащий идентификатор смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7694e-305">A BLOB that contains the identifier of the smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**\_свойство политики пользовательского интерфейса NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT\_UI\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-307">L "политика пользовательского интерфейса"</span><span class="sxs-lookup"><span data-stu-id="7694e-307">L"UI Policy"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-308">Если используется с функцией [**нкриптсетпроперти**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) или [**нкриптжетпроперти**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , это указатель на структуру [**\_ \_ политики пользовательского интерфейса NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) , содержащую политику строгого ключа пользовательского интерфейса для ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-308">If used with the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) or [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function, this is a pointer to an [**NCRYPT\_UI\_POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) structure that contains the strong key user interface policy for the key.</span></span> <span data-ttu-id="7694e-309">Это свойство применяется только к постоянным ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-309">This property only applies to persistent keys.</span></span> <span data-ttu-id="7694e-310">Это свойство может быть задано только при создании ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-310">This property can only be set when the key is being generated.</span></span> <span data-ttu-id="7694e-311">После вызова функции [**нкриптфинализекэй**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) для этого ключа это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7694e-311">Once the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function has been called for this key, this property becomes read-only.</span></span>

<span data-ttu-id="7694e-312">Поставщик хранилища ключей может получить этот параметр с помощью функции обратного вызова [**нкриптсетпропертифн**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) .</span><span class="sxs-lookup"><span data-stu-id="7694e-312">A key storage provider can receive this parameter through an [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) callback function.</span></span> <span data-ttu-id="7694e-313">Значение параметра является \_ \_ \_ структурой больших двоичных объектов политики пользовательского интерфейса NCRYPT, содержащей ту же информацию.</span><span class="sxs-lookup"><span data-stu-id="7694e-313">The parameter value is an NCRYPT\_UI\_POLICY\_BLOB structure that contains the same information.</span></span> <span data-ttu-id="7694e-314">Аналогично, когда приложение выполняет запрос через Нкриптсетпропертифн к поставщику, чтобы вернуть это свойство, поставщик должен вернуть \_ \_ \_ структуру больших двоичных объектов в политике пользовательского интерфейса NCRYPT.</span><span class="sxs-lookup"><span data-stu-id="7694e-314">Similarly, when an application makes a request through NCryptSetPropertyFn to the provider to return this property, the provider is expected to return an NCRYPT\_UI\_POLICY\_BLOB structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_свойство уникального \_ имени NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT\_UNIQUE\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-316">L "уникальное имя"</span><span class="sxs-lookup"><span data-stu-id="7694e-316">L"Unique Name"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-317">Указатель на строку в Юникоде, завершающуюся нулем, которая содержит уникальное имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7694e-317">A pointer to a null-terminated Unicode string that contains the unique name of the object.</span></span> <span data-ttu-id="7694e-318">Это альтернативное имя, которое можно использовать при доступе к ключу.</span><span class="sxs-lookup"><span data-stu-id="7694e-318">This is an alternate name that can be used when accessing the key.</span></span> <span data-ttu-id="7694e-319">Это свойство используется, когда предполагается, что имя ключа, первоначально переданное в [**нкрипткреатеперсистедкэй**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) , недостаточно уникально для надежного обнаружения постоянного ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-319">This property is used when it is thought that the key name originally passed to [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) is not unique enough to reliably identify the persisted key.</span></span> <span data-ttu-id="7694e-320">Поставщик хранилища ключей (Майкрософт) возвратит имя файла ключа, как это свойство.</span><span class="sxs-lookup"><span data-stu-id="7694e-320">The Microsoft key storage provider will return the file name of the key as this property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ . \_ использование \_ свойства Context**</span><span class="sxs-lookup"><span data-stu-id="7694e-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT\_USE\_CONTEXT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-322">L "использовать контекст"</span><span class="sxs-lookup"><span data-stu-id="7694e-322">L"Use Context"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-323">Указатель на строку в Юникоде, завершающуюся нулем, которая описывает контекст операции.</span><span class="sxs-lookup"><span data-stu-id="7694e-323">A pointer to a null-terminated Unicode string that describes the context of the operation.</span></span> <span data-ttu-id="7694e-324">Это свойство не является постоянным и может быть задано либо для поставщика, либо для ключа.</span><span class="sxs-lookup"><span data-stu-id="7694e-324">This property is not persistent and can be set on either a provider or a key.</span></span> <span data-ttu-id="7694e-325">У ключа нет доступа к свойству **\_ \_ \_ свойства Context для использования в NCRYPT** , так как свойство характерно только для того обработчика, для которого он задан.</span><span class="sxs-lookup"><span data-stu-id="7694e-325">A key does not have access to the **NCRYPT\_USE\_CONTEXT\_PROPERTY** property of the provider because the property is specific only to the handle it is set for.</span></span>

<span data-ttu-id="7694e-326">Пример, в котором это свойство будет использоваться в контексте поставщика, — это поставщик хранилища ключей, который должен запрашивать пользователя при вызове [**нкриптопенкэй**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (например, "вставьте смарт-карту в модуль чтения").</span><span class="sxs-lookup"><span data-stu-id="7694e-326">An example where this property would be used in the context of a provider is a key storage provider that needs to prompt the user during a call to [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (for example, "Insert your smart card in the reader.").</span></span> <span data-ttu-id="7694e-327">Так как маркер ключа недоступен до тех пор, пока не будет возвращен **нкриптопенкэй** , приложение должно установить это свойство в обработчике поставщика перед вызовом **нкриптопенкэй**.</span><span class="sxs-lookup"><span data-stu-id="7694e-327">Because the key handle is not available until after **NCryptOpenKey** returns, the application should set this property on the provider handle prior to calling **NCryptOpenKey**.</span></span>

<span data-ttu-id="7694e-328">Примером, в котором это свойство будет использоваться в контексте маркера ключа, является поставщик хранилища ключей, который должен запрашивать пользователя во время операции с помощью ключа (например, "это приложение должно использовать этот ключ для подписания документа").</span><span class="sxs-lookup"><span data-stu-id="7694e-328">An example where this property would be used in the context of a key handle is a key storage provider that needs to prompt the user during an operation using the key (for example, "This application needs to use this key to sign a document.").</span></span> <span data-ttu-id="7694e-329">Поставщик может затем передать эту контекстную информацию пользователю в любом пользовательском интерфейсе, показанном во время операции.</span><span class="sxs-lookup"><span data-stu-id="7694e-329">The provider could then relay this context information to the user in any user interface shown during the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT \_ использование \_ \_ свойства с включенным счетчиком \_**</span><span class="sxs-lookup"><span data-stu-id="7694e-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-331">L "число включенных использований"</span><span class="sxs-lookup"><span data-stu-id="7694e-331">L"Enabled Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-332">Указывает, поддерживает ли поставщик подсчет использования для ключей.</span><span class="sxs-lookup"><span data-stu-id="7694e-332">Indicates whether the provider supports usage counting for keys.</span></span> <span data-ttu-id="7694e-333">Это свойство имеет значение **типа DWORD** , содержащее 1, если поставщик поддерживает подсчет использования ключей.</span><span class="sxs-lookup"><span data-stu-id="7694e-333">This property is a **DWORD** that contains 1 if the provider supports usage counting for keys.</span></span> <span data-ttu-id="7694e-334">Если это свойство содержит любое другое значение или если функция [**нкриптжетпроперти**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) возвращает параметр " **\_ не \_ поддерживается**", поставщик не поддерживает подсчет использования ключей.</span><span class="sxs-lookup"><span data-stu-id="7694e-334">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support usage counting for keys.</span></span> <span data-ttu-id="7694e-335">Это свойство применяется только к поставщикам.</span><span class="sxs-lookup"><span data-stu-id="7694e-335">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT \_ . \_ использование \_ свойства Count**</span><span class="sxs-lookup"><span data-stu-id="7694e-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT\_USE\_COUNT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-337">L "число использований"</span><span class="sxs-lookup"><span data-stu-id="7694e-337">L"Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-338">[**\_ Целочисленная переменная уларже**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) , содержащая количество операций, выполненных указанным [*закрытым ключом*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="7694e-338">A [**ULARGE\_INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) variable that contains the number of operations that the specified [*private key*](/windows/desktop/SecGloss/p-gly) has performed.</span></span> <span data-ttu-id="7694e-339">Это свойство является необязательным и может не поддерживаться всеми поставщиками.</span><span class="sxs-lookup"><span data-stu-id="7694e-339">This property is optional and may not be supported by all providers.</span></span> <span data-ttu-id="7694e-340">Поставщики, поддерживающие это свойство в ключах, должны также поддерживать свойство **\_ Свойства "число использований в соответствии с \_ \_ включенным \_ значением** " в обработчике поставщика.</span><span class="sxs-lookup"><span data-stu-id="7694e-340">Providers that support this property on keys should also support the **NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY** property on the provider handle.</span></span> <span data-ttu-id="7694e-341">Поставщик хранилища ключей (Майкрософт) не поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="7694e-341">The Microsoft key storage provider does not support this property.</span></span> <span data-ttu-id="7694e-342">Это свойство применяется только к постоянным ключам.</span><span class="sxs-lookup"><span data-stu-id="7694e-342">This property only applies to persistent keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_ \_ свойство ЦЕРТСТОРЕ пользователя \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT\_USER\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-344">L "Смарткардусерцертсторе"</span><span class="sxs-lookup"><span data-stu-id="7694e-344">L"SmartCardUserCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-345">Объект **хцертсторе** , представляющий хранилище сертификатов пользователя смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7694e-345">An **HCERTSTORE** that represents the smart card user certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_свойство версии \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="7694e-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT\_VERSION\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-347">L "версия"</span><span class="sxs-lookup"><span data-stu-id="7694e-347">L"Version"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-348">Значение **типа DWORD** , содержащее версию программного обеспечения поставщика.</span><span class="sxs-lookup"><span data-stu-id="7694e-348">A **DWORD** that contains the software version of the provider.</span></span> <span data-ttu-id="7694e-349">Верхнее слово содержит основную версию, а младшее слово содержит дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="7694e-349">The high word contains the major version and the low word contains the minor version.</span></span> <span data-ttu-id="7694e-350">Например, 0x00030033 = 3,51.</span><span class="sxs-lookup"><span data-stu-id="7694e-350">For example, 0x00030033 = 3.51.</span></span> <span data-ttu-id="7694e-351">Это свойство применяется только к поставщикам.</span><span class="sxs-lookup"><span data-stu-id="7694e-351">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7694e-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_свойство " \_ обработчик \_ окна NCRYPT"**</span><span class="sxs-lookup"><span data-stu-id="7694e-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT\_WINDOW\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7694e-353">L "дескриптор HWND"</span><span class="sxs-lookup"><span data-stu-id="7694e-353">L"HWND Handle"</span></span>
</dt> <dt>



<span data-ttu-id="7694e-354">Указатель на дескриптор окна (**HWND**), который будет использоваться как родительский для любого отображаемого интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="7694e-354">A pointer to the window handle (**HWND**) to be used as the parent of any user interface that is displayed.</span></span>

<span data-ttu-id="7694e-355">Поскольку нежелательное поведение может произойти при отображении пользовательского интерфейса с помощью **нулевого** маркера окна для родительского элемента, настоятельно рекомендуется, чтобы поставщик хранилища ключей не отображал пользовательский интерфейс, если это свойство не задано.</span><span class="sxs-lookup"><span data-stu-id="7694e-355">Because undesirable behavior can happen when a user interface is shown by using a **NULL** window handle for the parent, we strongly recommend that a key storage provider not display a user interface unless this property is set.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="7694e-356">Для определения ограничений данных свойств используются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7694e-356">The following values are used to define limits of property data.</span></span>



| <span data-ttu-id="7694e-357">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="7694e-357">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="7694e-358">Описание</span><span class="sxs-lookup"><span data-stu-id="7694e-358">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <span data-ttu-id="7694e-359"><dt>**NCRYPT \_ 0x100000 \_ \_ данных свойства Max**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7694e-359"><dt>**NCRYPT\_MAX\_PROPERTY\_DATA**</dt> <dt>0x100000</dt></span></span> </dl> | <span data-ttu-id="7694e-360">Задает максимальный размер значения свойства в байтах.</span><span class="sxs-lookup"><span data-stu-id="7694e-360">Specifies the maximum size of a property value, in bytes.</span></span><br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <span data-ttu-id="7694e-361"><dt>**NCRYPT \_ Максимальное \_ \_ имя свойства**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="7694e-361"><dt>**NCRYPT\_MAX\_PROPERTY\_NAME**</dt> <dt>64</dt></span></span> </dl>       | <span data-ttu-id="7694e-362">Задает максимальный размер имени свойства в символах.</span><span class="sxs-lookup"><span data-stu-id="7694e-362">Specifies the maximum size of a property name, in characters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7694e-363">Требования</span><span class="sxs-lookup"><span data-stu-id="7694e-363">Requirements</span></span>



| <span data-ttu-id="7694e-364">Требование</span><span class="sxs-lookup"><span data-stu-id="7694e-364">Requirement</span></span> | <span data-ttu-id="7694e-365">Значение</span><span class="sxs-lookup"><span data-stu-id="7694e-365">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7694e-366">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7694e-366">Minimum supported client</span></span><br/> | <span data-ttu-id="7694e-367">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7694e-367">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7694e-368">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7694e-368">Minimum supported server</span></span><br/> | <span data-ttu-id="7694e-369">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7694e-369">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7694e-370">Header</span><span class="sxs-lookup"><span data-stu-id="7694e-370">Header</span></span><br/>                   | <dl> <span data-ttu-id="7694e-371"><dt>NCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="7694e-371"><dt>Ncrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7694e-372">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7694e-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7694e-373">**нкриптжетпроперти**</span><span class="sxs-lookup"><span data-stu-id="7694e-373">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[<span data-ttu-id="7694e-374">**нкриптсетпроперти**</span><span class="sxs-lookup"><span data-stu-id="7694e-374">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

