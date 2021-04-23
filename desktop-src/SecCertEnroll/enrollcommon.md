---
description: Папка Енроллкоммон содержит следующие вспомогательные функции и макросы, используемые в примерах, предоставляемых с помощью пакета SDK для регистрации сертификатов.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: енроллкоммон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542690"
---
# <a name="enrollcommon"></a><span data-ttu-id="d5a16-103">енроллкоммон</span><span class="sxs-lookup"><span data-stu-id="d5a16-103">enrollCommon</span></span>

<span data-ttu-id="d5a16-104">Папка Енроллкоммон содержит следующие вспомогательные функции и макросы, используемые в примерах, предоставляемых с помощью пакета SDK для регистрации сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d5a16-104">The enrollCommon folder contains the following helper functions and macros used by the samples provided with the Certificate Enrollment SDK.</span></span> <span data-ttu-id="d5a16-105">Он устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ Certificate енроллкоммон сертификата \\ X509 \\ .</span><span class="sxs-lookup"><span data-stu-id="d5a16-105">It is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCommon folder.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5a16-106">Функция</span><span class="sxs-lookup"><span data-stu-id="d5a16-106">Function</span></span></th>
<th><span data-ttu-id="d5a16-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d5a16-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5a16-108">_JumpIfError</span><span class="sxs-lookup"><span data-stu-id="d5a16-108">_JumpIfError</span></span></td>
<td><span data-ttu-id="d5a16-109">Макрос, принимающий значение <strong>HRESULT</strong> , метку и строку ошибки, выводит строку и передает управление программой первому оператору, следующему за меткой.</span><span class="sxs-lookup"><span data-stu-id="d5a16-109">Macro that accepts an <strong>HRESULT</strong> value, a label, and an error string, prints the string, and transfers program control to the first statement following the label.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-110">_JumpError</span><span class="sxs-lookup"><span data-stu-id="d5a16-110">_JumpError</span></span></td>
<td><span data-ttu-id="d5a16-111">То же, что и макрос _JumpIfError.</span><span class="sxs-lookup"><span data-stu-id="d5a16-111">Same as the _JumpIfError macro.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-112">_PrintIfError</span><span class="sxs-lookup"><span data-stu-id="d5a16-112">_PrintIfError</span></span></td>
<td><span data-ttu-id="d5a16-113">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="d5a16-113">Not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-114">_PrintError</span><span class="sxs-lookup"><span data-stu-id="d5a16-114">_PrintError</span></span></td>
<td><span data-ttu-id="d5a16-115">Макрос, который выводит сообщение об ошибке и значение <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="d5a16-115">Macro that prints an error message and an <strong>HRESULT</strong> value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-116">конвертвсзтосз</span><span class="sxs-lookup"><span data-stu-id="d5a16-116">convertWszToSz</span></span></td>
<td><span data-ttu-id="d5a16-117">Преобразует строку расширенных символов в строку символов ASCII с помощью функции <strong>WideCharToMultiByte</strong> и текущего идентификатора кодовой страницы ANSI для системы.</span><span class="sxs-lookup"><span data-stu-id="d5a16-117">Converts a wide-character string to an ASCII character string by using the <strong>WideCharToMultiByte</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="d5a16-118">Эта функция используется функциями Декконвертфромуникоде и Финдоидфромтемплатенаме, определенными в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="d5a16-118">This function is used by the decConvertFromUnicode and findOIDFromTemplateName functions defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-119">конвертсзтовсз</span><span class="sxs-lookup"><span data-stu-id="d5a16-119">convertSzToWsz</span></span></td>
<td><span data-ttu-id="d5a16-120">Преобразует строку ASCII в строку расширенных символов с помощью функции <strong>MultiByteToWideChar</strong> и идентификатора текущей кодовой страницы ANSI для системы.</span><span class="sxs-lookup"><span data-stu-id="d5a16-120">Converts an ASCII string to a wide-character string by using the <strong>MultiByteToWideChar</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="d5a16-121">Эта функция используется функцией Финдцертбитемплате, определенной в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="d5a16-121">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-122">конвертсзтобстр</span><span class="sxs-lookup"><span data-stu-id="d5a16-122">convertSzToBstr</span></span></td>
<td><span data-ttu-id="d5a16-123">Преобразует строку ASCII в <strong>BSTR</strong> с помощью функции <strong>MultiByteToWideChar</strong> .</span><span class="sxs-lookup"><span data-stu-id="d5a16-123">Converts an ASCII string to a <strong>BSTR</strong> by using the <strong>MultiByteToWideChar</strong> function.</span></span> <span data-ttu-id="d5a16-124">Эта функция в настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="d5a16-124">This function is not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-125">конвертвсзтобстр</span><span class="sxs-lookup"><span data-stu-id="d5a16-125">convertWszToBstr</span></span></td>
<td><span data-ttu-id="d5a16-126">Преобразует строку расширенных символов в <strong>BSTR</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5a16-126">Converts a wide-character string to a <strong>BSTR</strong>.</span></span> <span data-ttu-id="d5a16-127">Эта функция используется примером Инсталлреспонсефромпфкс.</span><span class="sxs-lookup"><span data-stu-id="d5a16-127">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-128">чеккенроллстатус</span><span class="sxs-lookup"><span data-stu-id="d5a16-128">checkEnrollStatus</span></span></td>
<td><span data-ttu-id="d5a16-129">Проверяет состояние процесса регистрации сертификата с помощью интерфейсов <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> и <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5a16-129">Checks the status of the certificate enrollment process by using the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> and <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> interfaces.</span></span> <span data-ttu-id="d5a16-130">Эта функция используется в примерах Енроллеобокмк, enrollPKCS7, enrollRenewalPKCS7, Енроллсимплемачинецерт и Енроллсимплеусерцерт.</span><span class="sxs-lookup"><span data-stu-id="d5a16-130">This function is used by the enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert, and enrollSimpleUserCert samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-131">финдцертбикэйусаже</span><span class="sxs-lookup"><span data-stu-id="d5a16-131">findCertByKeyUsage</span></span></td>
<td><span data-ttu-id="d5a16-132">Перечисляет личное хранилище сертификатов текущего пользователя, чтобы найти первый сертификат, для которого предполагаемое использование открытого ключа соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="d5a16-132">Enumerates the personal certificate store of the current user to find the first certificate for which the intended use of the public key matches a specified value.</span></span> <span data-ttu-id="d5a16-133">Указанное значение может быть побитовым сочетанием следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="d5a16-133">The value specified can be a bitwise combination of the following flags:</span></span>
<ul>
<li><span data-ttu-id="d5a16-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="d5a16-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="d5a16-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="d5a16-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span></span></li>
<li><span data-ttu-id="d5a16-136">CERT_KEY_AGREEMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="d5a16-136">CERT_KEY_AGREEMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="d5a16-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="d5a16-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span></span></li>
<li><span data-ttu-id="d5a16-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="d5a16-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="d5a16-139">CERT_NON_REPUDIATION_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="d5a16-139">CERT_NON_REPUDIATION_KEY_USAGE</span></span></li>
<li><span data-ttu-id="d5a16-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="d5a16-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span></span></li>
</ul>
<span data-ttu-id="d5a16-141">Эта функция используется примером Енроллфромпубликкэй.</span><span class="sxs-lookup"><span data-stu-id="d5a16-141">This function is used by the enrollFromPublicKey sample.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-142">финдцертбеку</span><span class="sxs-lookup"><span data-stu-id="d5a16-142">findCertByEKU</span></span></td>
<td><span data-ttu-id="d5a16-143">Перечисляет личное хранилище сертификатов текущего пользователя, чтобы найти первый сертификат, для которого расширение расширенного использования ключа (EKU) соответствует указанному во входных данных.</span><span class="sxs-lookup"><span data-stu-id="d5a16-143">Enumerates the personal certificate store of the current user to find the first certificate for which the Enhanced Key Usage (EKU) extension matches that specified on input.</span></span> <span data-ttu-id="d5a16-144">Дополнительные сведения о расширении EKU см. в разделе интерфейс <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5a16-144">For more information about the EKU extension, see the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> interface.</span></span> <span data-ttu-id="d5a16-145">Эта функция используется примером Енроллеобокмк.</span><span class="sxs-lookup"><span data-stu-id="d5a16-145">This function is used by the enrollEOBOCMC sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-146">финдцертбитемплате</span><span class="sxs-lookup"><span data-stu-id="d5a16-146">findCertByTemplate</span></span></td>
<td><span data-ttu-id="d5a16-147">Перечисляет личное хранилище сертификатов текущего пользователя, чтобы найти первый сертификат, для которого шаблон соответствует указанному по имени, на входе.</span><span class="sxs-lookup"><span data-stu-id="d5a16-147">Enumerates the personal certificate store of the current user to find the first certificate for which the template matches that specified, by name, on input.</span></span> <span data-ttu-id="d5a16-148">Эта функция используется в примерах enrollPKCS7 и enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="d5a16-148">This function is used by the enrollPKCS7 and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-149">енроллцертбитемплате</span><span class="sxs-lookup"><span data-stu-id="d5a16-149">enrollCertByTemplate</span></span></td>
<td><span data-ttu-id="d5a16-150">Инициализирует объект <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> с помощью шаблона, пытается зарегистрировать неявно созданный запрос на сертификат и отслеживает состояние процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="d5a16-150">Initializes an <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> object by using a template, attempts to enroll the implicitly created certificate request, and monitors the status of the enrollment process.</span></span> <span data-ttu-id="d5a16-151">Эта функция используется в примерах Енроллеобокмк, Енроллфромпубликкэй, enrollPKCS7 и enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="d5a16-151">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-152">верифицертконтекст</span><span class="sxs-lookup"><span data-stu-id="d5a16-152">verifyCertContext</span></span></td>
<td><span data-ttu-id="d5a16-153">Проверяет соответствие цепочки сертификатов указанной (базовой) политике и (необязательно) для указанного расширения расширенного использования ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="d5a16-153">Verifies compliance of the certificate chain against the specified (base) policy and, optionally, against a specified Enhanced Key Usage (EKU) extension.</span></span> <span data-ttu-id="d5a16-154">Дополнительные сведения см. в разделе Функция <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>цертверифицертификатечаинполици</strong></a> и структуры <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> и <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5a16-154">For more information, see the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> function and the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> structures.</span></span> <span data-ttu-id="d5a16-155">Эта функция используется в примерах Енроллеобокмк, Енроллфромпубликкэй, enrollPKCS7 и enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="d5a16-155">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-156">декконвертфромуникоде</span><span class="sxs-lookup"><span data-stu-id="d5a16-156">decConvertFromUnicode</span></span></td>
<td><span data-ttu-id="d5a16-157">Преобразует строку двухбайтовых символов Юникода в строку однобайтовых символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="d5a16-157">Converts a string of double-byte Unicode characters to a string of single-byte ANSI characters.</span></span> <span data-ttu-id="d5a16-158">Эта функция используется функцией Декодефилев, определенной в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="d5a16-158">This function is used by the DecodeFileW function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-159">декодефилев</span><span class="sxs-lookup"><span data-stu-id="d5a16-159">DecodeFileW</span></span></td>
<td><span data-ttu-id="d5a16-160">Декодирует закодированный сертификат или файл запроса на сертификат в массив байтов.</span><span class="sxs-lookup"><span data-stu-id="d5a16-160">Decodes an encoded certificate or certificate request file to a byte array.</span></span> <span data-ttu-id="d5a16-161">Эта функция используется примером Инсталлреспонсефромпфкс.</span><span class="sxs-lookup"><span data-stu-id="d5a16-161">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a16-162">енкодетофилев</span><span class="sxs-lookup"><span data-stu-id="d5a16-162">EncodeToFileW</span></span></td>
<td><span data-ttu-id="d5a16-163">Кодирует сертификат или запрос на сертификат и сохраняет его в файл.</span><span class="sxs-lookup"><span data-stu-id="d5a16-163">Encodes a certificate or certificate request and saves it to a file.</span></span> <span data-ttu-id="d5a16-164">Эта функция используется в примерах Креатекнгкустомкмк, Енроллеобокмк и Енроллфромпубликкэй.</span><span class="sxs-lookup"><span data-stu-id="d5a16-164">This function is used by the createCNGCustomCMC, enrollEOBOCMC, and enrollFromPublicKey samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a16-165">финдоидфромтемплатенаме</span><span class="sxs-lookup"><span data-stu-id="d5a16-165">findOIDFromTemplateName</span></span></td>
<td><span data-ttu-id="d5a16-166">Возвращает идентификатор объекта для шаблона, указанного по имени.</span><span class="sxs-lookup"><span data-stu-id="d5a16-166">Retrieves the object identifier for a template specified by name.</span></span> <span data-ttu-id="d5a16-167">Эта функция используется функцией Финдцертбитемплате, определенной в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="d5a16-167">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d5a16-168">См. также</span><span class="sxs-lookup"><span data-stu-id="d5a16-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5a16-169">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="d5a16-169">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

