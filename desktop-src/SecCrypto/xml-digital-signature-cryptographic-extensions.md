---
description: Криптксмл позволяет разработчикам расширять встроенные криптографические алгоритмы путем регистрации общесистемной библиотеки DLL расширения шифрования.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Криптографические расширения цифровых подписей XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913947"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a><span data-ttu-id="f81e6-103">Криптографические расширения цифровых подписей XML</span><span class="sxs-lookup"><span data-stu-id="f81e6-103">XML Digital Signature Cryptographic Extensions</span></span>

<span data-ttu-id="f81e6-104">Криптксмл позволяет разработчикам расширять встроенные криптографические алгоритмы путем регистрации общесистемной библиотеки DLL расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="f81e6-104">CryptXML allows developers to extend natively supported cryptographic algorithms by registering a system wide cryptographic extension DLL.</span></span> <span data-ttu-id="f81e6-105">Библиотеки DLL расширения расширяют алгоритмы, поддерживаемые XML-элементами **SignatureMethod** и **дижестмесод** .</span><span class="sxs-lookup"><span data-stu-id="f81e6-105">Extension DLLs extend the algorithms supported by **SignatureMethod** and **DigestMethod** XML elements.</span></span> <span data-ttu-id="f81e6-106">Библиотеки DLL расширения могут поддерживать алгоритмы, которые закодируются дополнительные параметры в цифровой подписи XML.</span><span class="sxs-lookup"><span data-stu-id="f81e6-106">Extension DLLs can support algorithms that encode additional parameters into the XML digital signature.</span></span>

<span data-ttu-id="f81e6-107">Все библиотеки DLL расширений должны поддерживать функцию [**криптксмлдллжетинтерфаце**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , которая возвращает указатель на [**понятную структуру \_ \_ \_ интерфейса шифрования XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) .</span><span class="sxs-lookup"><span data-stu-id="f81e6-107">All extensions DLLs must support the [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) function, which returns a pointer to a [**CRYPT\_XML\_CRYPTOGRAPHIC\_INTERFACE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) structure.</span></span> <span data-ttu-id="f81e6-108">Эта структура предоставляет указатели на функции для реализованных функций криптографических расширений.</span><span class="sxs-lookup"><span data-stu-id="f81e6-108">This structure provides function pointers to implemented cryptographic extension functions.</span></span> <span data-ttu-id="f81e6-109">Поддерживаемые функции зависят от типа поддерживаемого алгоритма шифрования и от того, должен ли алгоритм кодировать параметры в цифровой подписи XML.</span><span class="sxs-lookup"><span data-stu-id="f81e6-109">The functions supported depend on the type of cryptographic algorithm supported and whether the algorithm must encode parameters into the XML digital signature.</span></span>

<span data-ttu-id="f81e6-110">К функциям расширений шифрования относятся следующие указатели функций:</span><span class="sxs-lookup"><span data-stu-id="f81e6-110">Cryptographic extensions functions include the following function pointers:</span></span>

<dl> <dt>

<span data-ttu-id="f81e6-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Обязательные функции</span><span class="sxs-lookup"><span data-stu-id="f81e6-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Required functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="f81e6-112">**криптксмлдллжетинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="f81e6-112">**CryptXmlDllGetInterface**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [<span data-ttu-id="f81e6-113">**криптксмлдллжеталгорисминфо**</span><span class="sxs-lookup"><span data-stu-id="f81e6-113">**CryptXmlDllGetAlgorithmInfo**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span data-ttu-id="f81e6-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Функции метода дайджеста</span><span class="sxs-lookup"><span data-stu-id="f81e6-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest Method functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="f81e6-115">**криптксмлдллклоседижест**</span><span class="sxs-lookup"><span data-stu-id="f81e6-115">**CryptXmlDllCloseDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [<span data-ttu-id="f81e6-116">**криптксмлдллкреатедижест**</span><span class="sxs-lookup"><span data-stu-id="f81e6-116">**CryptXmlDllCreateDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [<span data-ttu-id="f81e6-117">**криптксмлдллдижестдата**</span><span class="sxs-lookup"><span data-stu-id="f81e6-117">**CryptXmlDllDigestData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [<span data-ttu-id="f81e6-118">**криптксмлдллфинализедижест**</span><span class="sxs-lookup"><span data-stu-id="f81e6-118">**CryptXmlDllFinalizeDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span data-ttu-id="f81e6-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Функции метода подписи</span><span class="sxs-lookup"><span data-stu-id="f81e6-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature Method Functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="f81e6-120">**криптксмлдллсигндата**</span><span class="sxs-lookup"><span data-stu-id="f81e6-120">**CryptXmlDllSignData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [<span data-ttu-id="f81e6-121">**криптксмлдллверифисигнатуре**</span><span class="sxs-lookup"><span data-stu-id="f81e6-121">**CryptXmlDllVerifySignature**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [<span data-ttu-id="f81e6-122">**криптксмлдллкреатекэй**</span><span class="sxs-lookup"><span data-stu-id="f81e6-122">**CryptXmlDllCreateKey**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [<span data-ttu-id="f81e6-123">**криптксмлдлленкодекэйвалуе**</span><span class="sxs-lookup"><span data-stu-id="f81e6-123">**CryptXmlDllEncodeKeyValue**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span data-ttu-id="f81e6-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Для алгоритмов с закодированными параметрами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f81e6-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>For algorithms with default encoded parameters</span></span>
</dt> <dd>

-   [<span data-ttu-id="f81e6-125">**криптксмлдлленкодеалгорисм**</span><span class="sxs-lookup"><span data-stu-id="f81e6-125">**CryptXmlDllEncodeAlgorithm**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

<span data-ttu-id="f81e6-126">Библиотеки DLL расширения шифрования регистрируются на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="f81e6-126">Cryptographic extension DLLs are registered on a system-wide basis.</span></span> <span data-ttu-id="f81e6-127">Для регистрации библиотеки DLL расширения шифрования требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="f81e6-127">Administrator privileges are required to register a cryptographic extension DLL.</span></span>

<span data-ttu-id="f81e6-128">Все криптографические расширения Криптксмл регистрируются значением URI, заданным в поле **SignatureMethod** или атрибутом Algorithm элемента **дижестмесод** .</span><span class="sxs-lookup"><span data-stu-id="f81e6-128">All CryptXML cryptographic extensions are registered by the URI value set in the **SignatureMethod** or the algorithm attribute field of the **DigestMethod** element.</span></span>

<span data-ttu-id="f81e6-129">Ниже приведены пути реестра для библиотек DLL расширения.</span><span class="sxs-lookup"><span data-stu-id="f81e6-129">The registry paths for the extension DLLs are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="f81e6-130"><span id="32-bit"></span><span id="32-BIT"></span>32-разрядный</span><span class="sxs-lookup"><span data-stu-id="f81e6-130"><span id="32-bit"></span><span id="32-BIT"></span>32-bit</span></span>
</dt> <dd>

<span data-ttu-id="f81e6-131">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ (**Microsoft** \\ **Cryptography** \\ **криптксмл** \\ **URI)** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="f81e6-131">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> <dt>

<span data-ttu-id="f81e6-132"><span id="64-bit"></span><span id="64-BIT"></span>64-разрядный</span><span class="sxs-lookup"><span data-stu-id="f81e6-132"><span id="64-bit"></span><span id="64-BIT"></span>64-bit</span></span>
</dt> <dd>

<span data-ttu-id="f81e6-133">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ (**Microsoft** \\ **Cryptography** \\ **криптксмл** \\ **URI)** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="f81e6-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

<span data-ttu-id="f81e6-134">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **криптксмл** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="f81e6-134">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**WOW6432NODE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> </dl>

<span data-ttu-id="f81e6-135">Каждый ключ содержит следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="f81e6-135">Each key contains the following settings.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f81e6-136">Имя</span><span class="sxs-lookup"><span data-stu-id="f81e6-136">Name</span></span></th>
<th><span data-ttu-id="f81e6-137">Тип</span><span class="sxs-lookup"><span data-stu-id="f81e6-137">Type</span></span></th>
<th><span data-ttu-id="f81e6-138">Данные</span><span class="sxs-lookup"><span data-stu-id="f81e6-138">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f81e6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f81e6-139">DLL</span></span><br/></td>
<td><span data-ttu-id="f81e6-140">Расширяемая строка</span><span class="sxs-lookup"><span data-stu-id="f81e6-140">Expandable string</span></span><br/></td>
<td><span data-ttu-id="f81e6-141">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f81e6-141">Required.</span></span><br/><span data-ttu-id="f81e6-142">Абсолютный путь к библиотеке DLL поставщика служб шифрования XML.</span><span class="sxs-lookup"><span data-stu-id="f81e6-142">The absolute path to the XML Cryptographic Provider DLL.</span></span>
<blockquote>
<p><span data-ttu-id="f81e6-143"><b>Примечание. </b> Рекомендуется размещать библиотеки DLL расширения шифрования в каталогах, которые могут быть записаны только приложениями с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="f81e6-143"><b>Note: </b>We recommend that cryptographic extension DLLs be located in directories that can only be written to by applications with administrative privilege.</span></span></p>
<p><span data-ttu-id="f81e6-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> используется для загрузки библиотеки DLL расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="f81e6-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> is used to load the cryptographic extension DLL.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f81e6-145">Имя</span><span class="sxs-lookup"><span data-stu-id="f81e6-145">Name</span></span><br/></td>
<td><span data-ttu-id="f81e6-146"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f81e6-146"><strong>String</strong></span></span></td>
<td><span data-ttu-id="f81e6-147">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f81e6-147">Optional.</span></span><br/> <span data-ttu-id="f81e6-148">Отображаемое имя, связанное с этим URI.</span><span class="sxs-lookup"><span data-stu-id="f81e6-148">The display name associated with this URI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f81e6-149">GroupId</span><span class="sxs-lookup"><span data-stu-id="f81e6-149">GroupId</span></span><br/></td>
<td><span data-ttu-id="f81e6-150"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f81e6-150"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="f81e6-151">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f81e6-151">Required.</span></span><br/> <span data-ttu-id="f81e6-152">Идентификатор группы, связанный с этим алгоритмом шифрования.</span><span class="sxs-lookup"><span data-stu-id="f81e6-152">The group identifier associated with this cryptographic algorithm.</span></span> <span data-ttu-id="f81e6-153">Возможные значения включают следующие:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1.</span><span class="sxs-lookup"><span data-stu-id="f81e6-153">Possible values include the following:<strong>CRYPT_XML_GROUP_ID_HASH</strong>\<strong></strong> = 1</span></span><br/><span data-ttu-id="f81e6-154"><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2</span><span class="sxs-lookup"><span data-stu-id="f81e6-154"><strong>CRYPT_XML_GROUP_ID_SIGN</strong>\<strong></strong> = 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f81e6-155">кнгалгид</span><span class="sxs-lookup"><span data-stu-id="f81e6-155">CNGAlgid</span></span><br/></td>
<td><span data-ttu-id="f81e6-156"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f81e6-156"><strong>String</strong></span></span></td>
<td><span data-ttu-id="f81e6-157">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="f81e6-157">Required.</span></span><br/> <span data-ttu-id="f81e6-158">Имя алгоритма CNG, которое будет передано функциям BCrypt или NCrypt.</span><span class="sxs-lookup"><span data-stu-id="f81e6-158">The CNG algorithm name to be passed to BCrypt or NCrypt functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f81e6-159">кнжекстраалгид</span><span class="sxs-lookup"><span data-stu-id="f81e6-159">CNGExtraAlgid</span></span><br/></td>
<td><span data-ttu-id="f81e6-160"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f81e6-160"><strong>String</strong></span></span></td>
<td><span data-ttu-id="f81e6-161">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f81e6-161">Optional.</span></span><br/> <span data-ttu-id="f81e6-162">Дополнительные строки алгоритма, отличные от строки в члене Кнгалгид, которые могут быть переданы в функции CNG.</span><span class="sxs-lookup"><span data-stu-id="f81e6-162">An extra algorithm string, other than the string in the CNGAlgid member, that can be passed to the CNG functions.</span></span><br/> <span data-ttu-id="f81e6-163">Для алгоритмов подписи (CRYPT_XML_GROUP_ID_SIGN) этот член является строкой алгоритма открытого ключа для передачи в функции CNG.</span><span class="sxs-lookup"><span data-stu-id="f81e6-163">For the signature algorithms (CRYPT_XML_GROUP_ID_SIGN), this member is the public key algorithm string to pass to the CNG functions.</span></span><br/> <span data-ttu-id="f81e6-164">Для других значений GroupId присвойте элементу <strong>пвсзкнжекстраалгид</strong> пустую строку L &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="f81e6-164">For the other values of GroupId, set the <strong>pwszCNGExtraAlgid</strong> member to the empty string, L&quot;&quot;.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f81e6-165">См. также</span><span class="sxs-lookup"><span data-stu-id="f81e6-165">Related topics</span></span>

<dl> <span data-ttu-id="f81e6-166"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f81e6-166"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f81e6-167">Алгоритмы шифрования цифровых подписей XML</span><span class="sxs-lookup"><span data-stu-id="f81e6-167">XML Digital Signature Cryptographic Algorithms</span></span>](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
