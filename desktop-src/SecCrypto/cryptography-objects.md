---
description: Перечисляет объекты, предоставляемые интерфейсом CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Криптографические объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423773"
---
# <a name="cryptography-objects"></a><span data-ttu-id="4772e-103">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="4772e-103">Cryptography Objects</span></span>

<span data-ttu-id="4772e-104">Объекты криптографии классифицируются по уровням использования следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4772e-104">Cryptography objects are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="4772e-105">Объекты хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="4772e-105">Certificate Store Objects</span></span>](#certificate-store-objects)
-   [<span data-ttu-id="4772e-106">Объекты цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="4772e-106">Digital Signature Objects</span></span>](#digital-signature-objects)
-   [<span data-ttu-id="4772e-107">Запечатанные объекты данных</span><span class="sxs-lookup"><span data-stu-id="4772e-107">Enveloped Data Objects</span></span>](#enveloped-data-objects)
-   [<span data-ttu-id="4772e-108">Объекты шифрования данных</span><span class="sxs-lookup"><span data-stu-id="4772e-108">Data Encryption Objects</span></span>](#data-encryption-objects)
-   [<span data-ttu-id="4772e-109">Вспомогательные объекты</span><span class="sxs-lookup"><span data-stu-id="4772e-109">Auxiliary Objects</span></span>](#auxiliary-objects)
-   [<span data-ttu-id="4772e-110">Объекты регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="4772e-110">Certificate Enrollment Objects</span></span>](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a><span data-ttu-id="4772e-111">Объекты хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="4772e-111">Certificate Store Objects</span></span>

<span data-ttu-id="4772e-112">Следующие объекты работают с [*хранилищами сертификатов*](../secgloss/c-gly.md) и сертификатами в этих хранилищах.</span><span class="sxs-lookup"><span data-stu-id="4772e-112">The following objects work with [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="4772e-113">CAPICOM поддерживает использование хранилищ сертификатов "текущий пользователь", "локальный компьютер", "память" и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4772e-113">CAPICOM supports the use of Current User, Local Machine, memory, and Active Directory certificate stores.</span></span>



| <span data-ttu-id="4772e-114">Объект</span><span class="sxs-lookup"><span data-stu-id="4772e-114">Object</span></span>                                             | <span data-ttu-id="4772e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4772e-115">Description</span></span>                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4772e-116">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="4772e-116">**Certificate**</span></span>](certificate.md)                 | <span data-ttu-id="4772e-117">Один цифровой сертификат.</span><span class="sxs-lookup"><span data-stu-id="4772e-117">A single digital certificate.</span></span>                                                                                           |
| [<span data-ttu-id="4772e-118">**цертификатеполиЦиес**</span><span class="sxs-lookup"><span data-stu-id="4772e-118">**CertificatePolicies**</span></span>](certificatepolicies.md) | <span data-ttu-id="4772e-119">Коллекция объектов [**полициинформатион**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-119">A collection of [**PolicyInformation**](policyinformation.md) objects.</span></span>                                                 |
| [<span data-ttu-id="4772e-120">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="4772e-120">**Certificates**</span></span>](certificates.md)               | <span data-ttu-id="4772e-121">Коллекция объектов [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-121">Collection of [**Certificate**](certificate.md) objects.</span></span>                                                               |
| [<span data-ttu-id="4772e-122">**цертификатестатус**</span><span class="sxs-lookup"><span data-stu-id="4772e-122">**CertificateStatus**</span></span>](certificatestatus.md)     | <span data-ttu-id="4772e-123">Предоставляет сведения о состоянии сертификата.</span><span class="sxs-lookup"><span data-stu-id="4772e-123">Provides status information on a certificate.</span></span>                                                                           |
| [<span data-ttu-id="4772e-124">**Цепочк**</span><span class="sxs-lookup"><span data-stu-id="4772e-124">**Chain**</span></span>](chain.md)                             | <span data-ttu-id="4772e-125">Создает и проверяет цепочку проверки сертификатов на основе цифрового сертификата.</span><span class="sxs-lookup"><span data-stu-id="4772e-125">Creates and checks a certificate validation chain based on a digital certificate.</span></span>                                       |
| [<span data-ttu-id="4772e-126">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="4772e-126">**ExtendedProperties**</span></span>](extendedproperties.md)   | <span data-ttu-id="4772e-127">Представляет коллекцию объектов [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-127">Represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span>                                        |
| [<span data-ttu-id="4772e-128">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="4772e-128">**ExtendedProperty**</span></span>](extendedproperties.md)     | <span data-ttu-id="4772e-129">Представляет свойство, расширенное корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="4772e-129">Represents a Microsoft-extended property.</span></span>                                                                               |
| [<span data-ttu-id="4772e-130">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="4772e-130">**Extension**</span></span>](extension.md)                     | <span data-ttu-id="4772e-131">Представляет одно расширение сертификата.</span><span class="sxs-lookup"><span data-stu-id="4772e-131">Represents a single certificate extension.</span></span>                                                                              |
| [<span data-ttu-id="4772e-132">**Модули**</span><span class="sxs-lookup"><span data-stu-id="4772e-132">**Extensions**</span></span>](extensions.md)                   | <span data-ttu-id="4772e-133">Представляет коллекцию объектов [**Extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-133">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                      |
| [<span data-ttu-id="4772e-134">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="4772e-134">**PrivateKey**</span></span>](privatekey.md)                   | <span data-ttu-id="4772e-135">Представляет закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="4772e-135">Represents a private key.</span></span>                                                                                               |
| [<span data-ttu-id="4772e-136">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="4772e-136">**PublicKey**</span></span>](publickey.md)                     | <span data-ttu-id="4772e-137">Представляет открытый ключ в объекте [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-137">Represents a public key in a [**Certificate**](certificate.md) object.</span></span>                                                 |
| [<span data-ttu-id="4772e-138">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="4772e-138">**Store**</span></span>](store.md)                             | <span data-ttu-id="4772e-139">Предоставляет свойства и методы для выбора, управления и использования хранилищ сертификатов и сертификатов в этих хранилищах.</span><span class="sxs-lookup"><span data-stu-id="4772e-139">Provides the properties and methods to choose, manage, and use certificate stores and the certificates in those stores.</span></span> |
| [<span data-ttu-id="4772e-140">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="4772e-140">**Template**</span></span>](template.md)                       | <span data-ttu-id="4772e-141">Представляет шаблон расширения сертификата для сертификата.</span><span class="sxs-lookup"><span data-stu-id="4772e-141">Represents the certificate extension template of the certificate.</span></span>                                                       |



 

## <a name="digital-signature-objects"></a><span data-ttu-id="4772e-142">Объекты цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="4772e-142">Digital Signature Objects</span></span>

<span data-ttu-id="4772e-143">Следующие объекты экспортируются в данные цифровой подписи и для проверки цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="4772e-143">The following objects are exported to digitally sign data and to verify digital signatures.</span></span>



| <span data-ttu-id="4772e-144">Объект</span><span class="sxs-lookup"><span data-stu-id="4772e-144">Object</span></span>                           | <span data-ttu-id="4772e-145">Описание</span><span class="sxs-lookup"><span data-stu-id="4772e-145">Description</span></span>                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4772e-146">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="4772e-146">**SignedCode**</span></span>](signedcode.md) | <span data-ttu-id="4772e-147">Объект, используемый для подписи кода с цифровой подписью Authenticode и для проверки подписи в подписанном коде.</span><span class="sxs-lookup"><span data-stu-id="4772e-147">Object used to sign code with an Authenticode digital signature and to verify the signature on signed code.</span></span> |
| [<span data-ttu-id="4772e-148">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="4772e-148">**SignedData**</span></span>](signeddata.md) | <span data-ttu-id="4772e-149">Объект, используемый для подписи данных и проверки подписи подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="4772e-149">Object used to sign data and to verify the signature on signed data.</span></span>                                        |
| [<span data-ttu-id="4772e-150">**Автор подписи**</span><span class="sxs-lookup"><span data-stu-id="4772e-150">**Signer**</span></span>](signer.md)         | <span data-ttu-id="4772e-151">Сведения об одном подписавшем данных, включая сертификат подписывающий.</span><span class="sxs-lookup"><span data-stu-id="4772e-151">Information on a single data signer, including the signer's certificate.</span></span>                                    |
| [<span data-ttu-id="4772e-152">**Подписавшими**</span><span class="sxs-lookup"><span data-stu-id="4772e-152">**Signers**</span></span>](signers.md)       | <span data-ttu-id="4772e-153">Коллекция объектов [**подписывающих**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-153">Collection of [**Signer**](signer.md) objects.</span></span>                                                             |



 

## <a name="enveloped-data-objects"></a><span data-ttu-id="4772e-154">Запечатанные объекты данных</span><span class="sxs-lookup"><span data-stu-id="4772e-154">Enveloped Data Objects</span></span>

<span data-ttu-id="4772e-155">Следующие объекты экспортируются для создания сообщений с запечатанными данными для обеспечения конфиденциальности и расшифровки данных в запечатанных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="4772e-155">The following objects are exported to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>



| <span data-ttu-id="4772e-156">Объект</span><span class="sxs-lookup"><span data-stu-id="4772e-156">Object</span></span>                                 | <span data-ttu-id="4772e-157">Описание</span><span class="sxs-lookup"><span data-stu-id="4772e-157">Description</span></span>                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4772e-158">**енвелопеддата**</span><span class="sxs-lookup"><span data-stu-id="4772e-158">**EnvelopedData**</span></span>](envelopeddata.md) | <span data-ttu-id="4772e-159">Объекты, используемые для создания, отправки и получения данных, упакованных в оболочку.</span><span class="sxs-lookup"><span data-stu-id="4772e-159">Objects used to create, send, and receive enveloped data.</span></span> <span data-ttu-id="4772e-160">Запечатанные данные шифруются таким образом, чтобы их могли расшифровывать только предполагаемые получатели.</span><span class="sxs-lookup"><span data-stu-id="4772e-160">Enveloped data is encrypted so that only the intended recipients can decrypt it.</span></span> |
| [<span data-ttu-id="4772e-161">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="4772e-161">**Recipients**</span></span>](recipients.md)       | <span data-ttu-id="4772e-162">Коллекция объектов [**сертификатов**](certificate.md) предполагаемых получателей запечатанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="4772e-162">Collection of the [**Certificate**](certificate.md) objects of the intended recipients of an enveloped message.</span></span>                           |



 

## <a name="data-encryption-objects"></a><span data-ttu-id="4772e-163">Объекты шифрования данных</span><span class="sxs-lookup"><span data-stu-id="4772e-163">Data Encryption Objects</span></span>

<span data-ttu-id="4772e-164">Следующий объект экспортируется для шифрования произвольных данных в целях конфиденциальности и расшифровки зашифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="4772e-164">The following object is exported to encrypt arbitrary data for privacy and to decrypt encrypted data.</span></span>



| <span data-ttu-id="4772e-165">Объект</span><span class="sxs-lookup"><span data-stu-id="4772e-165">Object</span></span>                                 | <span data-ttu-id="4772e-166">Описание</span><span class="sxs-lookup"><span data-stu-id="4772e-166">Description</span></span>                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4772e-167">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="4772e-167">**EncryptedData**</span></span>](encrypteddata.md) | <span data-ttu-id="4772e-168">Объекты, используемые для шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="4772e-168">Objects used to encrypt data.</span></span> <span data-ttu-id="4772e-169">Зашифрованные данные в объекте [**EncryptedData**](encrypteddata.md) можно расшифровать.</span><span class="sxs-lookup"><span data-stu-id="4772e-169">Encrypted data in an [**EncryptedData**](encrypteddata.md) object can be decrypted.</span></span> |



 

## <a name="auxiliary-objects"></a><span data-ttu-id="4772e-170">Вспомогательные объекты</span><span class="sxs-lookup"><span data-stu-id="4772e-170">Auxiliary Objects</span></span>

<span data-ttu-id="4772e-171">Следующие объекты экспортируются для изменения поведения по умолчанию других объектов, а также для управления сертификатами, хранилищами сертификатов и сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4772e-171">The following objects are exported to change default behaviors of other objects and to manage certificates, certificate stores, and messages.</span></span>



| <span data-ttu-id="4772e-172">Объект</span><span class="sxs-lookup"><span data-stu-id="4772e-172">Object</span></span>                                         | <span data-ttu-id="4772e-173">Описание</span><span class="sxs-lookup"><span data-stu-id="4772e-173">Description</span></span>                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4772e-174">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="4772e-174">**Algorithm**</span></span>](algorithm.md)                 | <span data-ttu-id="4772e-175">Задает алгоритм и [*длину ключа*](../secgloss/k-gly.md) для использования в криптографических операциях.</span><span class="sxs-lookup"><span data-stu-id="4772e-175">Sets the algorithm and [*key length*](../secgloss/k-gly.md) to be used in cryptographic operations.</span></span> |
| [<span data-ttu-id="4772e-176">**attribute**</span><span class="sxs-lookup"><span data-stu-id="4772e-176">**Attribute**</span></span>](attribute.md)                 | <span data-ttu-id="4772e-177">Предоставляет единую часть добавленных сведений о подписи, например время подписи.</span><span class="sxs-lookup"><span data-stu-id="4772e-177">Provides a single piece of added information about a signature, such as the time of signing.</span></span>                                                    |
| [<span data-ttu-id="4772e-178">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="4772e-178">**Attributes**</span></span>](attributes.md)               | <span data-ttu-id="4772e-179">Коллекция объектов [**Attribute**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-179">Collection of [**Attribute**](attribute.md) objects.</span></span>                                                                                           |
| [<span data-ttu-id="4772e-180">**басикконстраинтс**</span><span class="sxs-lookup"><span data-stu-id="4772e-180">**BasicConstraints**</span></span>](basicconstraints.md)   | <span data-ttu-id="4772e-181">Предоставляет доступ только для чтения к базовым ограничениям на использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="4772e-181">Provides read-only access to basic constraints on the uses of a certificate.</span></span>                                                                    |
| [<span data-ttu-id="4772e-182">**EKU**</span><span class="sxs-lookup"><span data-stu-id="4772e-182">**EKU**</span></span>](eku.md)                             | <span data-ttu-id="4772e-183">Предоставляет доступ к свойствам EKU сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4772e-183">Provides access to EKU properties of certificates.</span></span>                                                                                              |
| [<span data-ttu-id="4772e-184">**EKU**</span><span class="sxs-lookup"><span data-stu-id="4772e-184">**EKUs**</span></span>](ekus.md)                           | <span data-ttu-id="4772e-185">Коллекция объектов [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-185">Collection of [**EKU**](eku.md) objects.</span></span>                                                                                                       |
| [<span data-ttu-id="4772e-186">**енкодеддата**</span><span class="sxs-lookup"><span data-stu-id="4772e-186">**EncodedData**</span></span>](encodeddata.md)             | <span data-ttu-id="4772e-187">Представляет блок закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="4772e-187">Represents a block of encoded data.</span></span>                                                                                                             |
| [<span data-ttu-id="4772e-188">**екстендедкэйусаже**</span><span class="sxs-lookup"><span data-stu-id="4772e-188">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)   | <span data-ttu-id="4772e-189">Предоставляет доступ только для чтения к свойствам расширенного использования ключа сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4772e-189">Provides read-only access to the extended key usage properties of certificates.</span></span>                                                                 |
| [<span data-ttu-id="4772e-190">**хашеддата**</span><span class="sxs-lookup"><span data-stu-id="4772e-190">**HashedData**</span></span>](hasheddata.md)               | <span data-ttu-id="4772e-191">Предоставляет функциональные возможности для применения хэш-алгоритма к строке.</span><span class="sxs-lookup"><span data-stu-id="4772e-191">Provides functionality for applying a hash algorithm to a string.</span></span>                                                                               |
| [<span data-ttu-id="4772e-192">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="4772e-192">**KeyUsage**</span></span>](keyusage.md)                   | <span data-ttu-id="4772e-193">Предоставляет доступ только для чтения к свойствам использования ключа сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4772e-193">Provides read-only access to key usage properties of certificates.</span></span>                                                                              |
| [<span data-ttu-id="4772e-194">**нотиценумберс**</span><span class="sxs-lookup"><span data-stu-id="4772e-194">**NoticeNumbers**</span></span>](noticenumbers.md)         | <span data-ttu-id="4772e-195">Представляет коллекцию объектов [**Extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-195">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                                              |
| [<span data-ttu-id="4772e-196">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="4772e-196">**OID**</span></span>](oid.md)                             | <span data-ttu-id="4772e-197">Представляет идентификатор объекта, используемый несколькими свойствами CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="4772e-197">Represents an object identifier that is used by several CAPICOM properties.</span></span>                                                                     |
| [<span data-ttu-id="4772e-198">**OID**</span><span class="sxs-lookup"><span data-stu-id="4772e-198">**OIDs**</span></span>](oids.md)                           | <span data-ttu-id="4772e-199">Представляет коллекцию объектов [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="4772e-199">Represents a collection of [**OID**](oid.md) objects.</span></span>                                                                                          |
| [<span data-ttu-id="4772e-200">**полициинформатион**</span><span class="sxs-lookup"><span data-stu-id="4772e-200">**PolicyInformation**</span></span>](policyinformation.md) | <span data-ttu-id="4772e-201">Предоставляет доступ к идентификаторам OID политики расширения.</span><span class="sxs-lookup"><span data-stu-id="4772e-201">Provides access to the policy OIDs of an extension.</span></span>                                                                                             |
| [<span data-ttu-id="4772e-202">**Квалификатор**</span><span class="sxs-lookup"><span data-stu-id="4772e-202">**Qualifier**</span></span>](qualifier.md)                 | <span data-ttu-id="4772e-203">Представляет указатель на инструкцию по сертификации (CPS) или квалификатор уведомления пользователя.</span><span class="sxs-lookup"><span data-stu-id="4772e-203">Represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>                                                           |
| [<span data-ttu-id="4772e-204">**Квалификаторы**</span><span class="sxs-lookup"><span data-stu-id="4772e-204">**Qualifiers**</span></span>](qualifiers.md)               | <span data-ttu-id="4772e-205">Представляет коллекцию квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="4772e-205">Represents a collection of qualifiers.</span></span>                                                                                                          |
| [<span data-ttu-id="4772e-206">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="4772e-206">**Settings**</span></span>](settings.md)                   | <span data-ttu-id="4772e-207">Включение или отключение диалоговых окон для запроса удостоверения лица или отправителя, если это удостоверение не указано.</span><span class="sxs-lookup"><span data-stu-id="4772e-207">Enables or disables dialog boxes to prompt for signer or sender identity if that identity is not specified.</span></span>                                     |
| [<span data-ttu-id="4772e-208">**Служебные программы**</span><span class="sxs-lookup"><span data-stu-id="4772e-208">**Utilities**</span></span>](utilities.md)                 | <span data-ttu-id="4772e-209">Предоставляет функциональные возможности для распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="4772e-209">Provides functionality for common tasks.</span></span>                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a><span data-ttu-id="4772e-210">Объекты регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="4772e-210">Certificate Enrollment Objects</span></span>

<span data-ttu-id="4772e-211">Следующий объект используется для регистрации сертификата.</span><span class="sxs-lookup"><span data-stu-id="4772e-211">The following object is used for certificate enrollment.</span></span>



| <span data-ttu-id="4772e-212">Объект</span><span class="sxs-lookup"><span data-stu-id="4772e-212">Object</span></span>                     | <span data-ttu-id="4772e-213">Описание</span><span class="sxs-lookup"><span data-stu-id="4772e-213">Description</span></span>                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4772e-214">[**ценролл**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4772e-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span></span> | <span data-ttu-id="4772e-215">Объект, представляющий Управление регистрацией сертификата.</span><span class="sxs-lookup"><span data-stu-id="4772e-215">Object that represents the Certificate Enrollment Control.</span></span> <span data-ttu-id="4772e-216">Он используется в основном при программировании в Visual Basic или на другом языке автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4772e-216">It is primarily used when programming in Visual Basic or another Automation language.</span></span> |



 

 

 
