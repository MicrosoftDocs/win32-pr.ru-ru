---
title: Подписание пакета приложения с помощью SignTool
description: Узнайте, как подписывать пакеты приложений Windows с помощью средства SignTool, чтобы их можно было развернуть.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105700965"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a><span data-ttu-id="8de6e-103">Подписание пакета приложения с помощью SignTool</span><span class="sxs-lookup"><span data-stu-id="8de6e-103">How to sign an app package using SignTool</span></span>

> [!Note]  
> <span data-ttu-id="8de6e-104">Сведения о подписывании пакета приложений для Windows см. в статье подписывание [пакета приложения с помощью средства SignTool](/windows/msix/package/sign-app-package-using-signtool).</span><span class="sxs-lookup"><span data-stu-id="8de6e-104">For signing a Windows app package, see [Sign an app package using SignTool](/windows/msix/package/sign-app-package-using-signtool).</span></span>

 

<span data-ttu-id="8de6e-105">Узнайте, как подписывать пакеты приложений Windows с помощью средства [**SignTool**](/windows-hardware/drivers/devtest/signtool) , чтобы их можно было развернуть.</span><span class="sxs-lookup"><span data-stu-id="8de6e-105">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages so they can be deployed.</span></span> <span data-ttu-id="8de6e-106">Средство [**SignTool**](/windows-hardware/drivers/devtest/signtool) входит в состав пакета средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="8de6e-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) is part of the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="8de6e-107">Все пакеты приложений Windows должны иметь цифровую подпись, прежде чем их можно будет развернуть.</span><span class="sxs-lookup"><span data-stu-id="8de6e-107">All Windows app packages must be digitally signed before they can be deployed.</span></span> <span data-ttu-id="8de6e-108">Хотя Microsoft Visual Studio 2012 и более поздних версий могут подписывать пакет приложения во время его создания, пакеты, созданные с помощью средства [упаковщика приложений (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) из Windows SDK, не подписываются.</span><span class="sxs-lookup"><span data-stu-id="8de6e-108">While Microsoft Visual Studio 2012 and later can sign an app package during its creation, packages that you create by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool from the Windows SDK aren't signed.</span></span>

> [!Note]  
> <span data-ttu-id="8de6e-109">Средство [**SignTool**](/windows-hardware/drivers/devtest/signtool) можно использовать только для подписания пакетов приложений Windows в Windows 8 и более поздних версиях, а также в windows Server 2012 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8de6e-109">You can only use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages on Windows 8 and later or Windows Server 2012 and later.</span></span> <span data-ttu-id="8de6e-110">Средство **SignTool** нельзя использовать для подписывания пакетов приложений в операционных системах нижнего уровня, таких как Windows 7 или windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="8de6e-110">You can't use **SignTool** to sign app packages on down-level operating systems such as Windows 7 or Windows Server 2008 R2.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="8de6e-111">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="8de6e-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8de6e-112">Технологии</span><span class="sxs-lookup"><span data-stu-id="8de6e-112">Technologies</span></span>

-   <span data-ttu-id="8de6e-113">[Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8de6e-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="8de6e-114">[Пакеты и развертывание приложений](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="8de6e-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="8de6e-115">Средства для подписывания файлов и проверки подписей</span><span class="sxs-lookup"><span data-stu-id="8de6e-115">Tools to Sign Files and Check Signatures</span></span>](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a><span data-ttu-id="8de6e-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="8de6e-116">Prerequisites</span></span>

-   <span data-ttu-id="8de6e-117">Средство [**SignTool**](/windows-hardware/drivers/devtest/signtool), являющееся частью Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8de6e-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), which is part of the Windows SDK</span></span>
-   <span data-ttu-id="8de6e-118">Допустимый сертификат подписи кода, например файл обмена личной информацией (PFX), созданный с помощью средств [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)</span><span class="sxs-lookup"><span data-stu-id="8de6e-118">A valid code signing certificate, for example, a Personal Information Exchange (.pfx) file created with the [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools</span></span>

    <span data-ttu-id="8de6e-119">Сведения о создании допустимого сертификата подписи кода см. [в разделе Создание сертификата для подписи пакета приложения](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="8de6e-119">For info about creating a valid code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

-   <span data-ttu-id="8de6e-120">Упакованное приложение Windows, например appx-файл, созданный с помощью средства [упаковщика приложений (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) .</span><span class="sxs-lookup"><span data-stu-id="8de6e-120">A packaged Windows app, for example, an .appx file created by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool</span></span>

<span data-ttu-id="8de6e-121">**Дополнительные рекомендации**</span><span class="sxs-lookup"><span data-stu-id="8de6e-121">**Additional considerations**</span></span>

<span data-ttu-id="8de6e-122">Сертификат, используемый для подписи пакета приложения, должен соответствовать следующим критериям:</span><span class="sxs-lookup"><span data-stu-id="8de6e-122">The certificate that you use to sign the app package must meet these criteria:</span></span>

-   <span data-ttu-id="8de6e-123">Имя субъекта сертификата должно соответствовать атрибуту **издателя** , содержащемуся в элементе [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) файла AppxManifest.xml, который хранится в пакете.</span><span class="sxs-lookup"><span data-stu-id="8de6e-123">The subject name of the certificate must match the **Publisher** attribute that is contained in the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element of the AppxManifest.xml file that is stored within the package.</span></span> <span data-ttu-id="8de6e-124">Имя издателя является частью удостоверения упакованного приложения Windows, поэтому необходимо сделать имя субъекта сертификата соответствующим имени издателя приложения.</span><span class="sxs-lookup"><span data-stu-id="8de6e-124">The publisher name is part of the identity of a packaged Windows app, so you have to make the subject name of the certificate match the publisher name of the app.</span></span> <span data-ttu-id="8de6e-125">Это позволяет проверять подлинность подписанных пакетов по цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="8de6e-125">This allows the identity of signed packages to be checked against the digital signature.</span></span> <span data-ttu-id="8de6e-126">Сведения об ошибках подписывания, которые могут возникнуть при подписывании пакета приложения с помощью средства [**SignTool**](/windows-hardware/drivers/devtest/signtool), см. в разделе "Примечания" статьи [Создание сертификата для подписи пакета приложения](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="8de6e-126">For info about signing errors that can arise from signing an app package using [**SignTool**](/windows-hardware/drivers/devtest/signtool), see the Remarks section of [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>
-   <span data-ttu-id="8de6e-127">Сертификат должен быть допустимым для подписывания кода.</span><span class="sxs-lookup"><span data-stu-id="8de6e-127">The certificate must be valid for code signing.</span></span> <span data-ttu-id="8de6e-128">Это означает, что оба этих элемента должны быть истинными:</span><span class="sxs-lookup"><span data-stu-id="8de6e-128">This means that both of these items must be true:</span></span>

    -   <span data-ttu-id="8de6e-129">Поле расширенного использования ключа (EKU) сертификата должно быть либо не установлено, либо содержать значение EKU для подписывания кода (1.3.6.1.5.5.7.3.3).</span><span class="sxs-lookup"><span data-stu-id="8de6e-129">The Extended Key Usage (EKU) field of the certificate must either be unset or contain the EKU value for code signing (1.3.6.1.5.5.7.3.3).</span></span>
    -   <span data-ttu-id="8de6e-130">Поле "использование ключа" (EKU) сертификата должно быть либо неопределенным, либо содержать бит использования для цифровой подписи (0x80).</span><span class="sxs-lookup"><span data-stu-id="8de6e-130">The Key Usage (KU) field of the certificate must either be unset or contain the usage bit for digital signature (0x80).</span></span>

-   <span data-ttu-id="8de6e-131">Сертификат содержит закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="8de6e-131">The certificate contains a private key.</span></span>
-   <span data-ttu-id="8de6e-132">Сертификат действителен.</span><span class="sxs-lookup"><span data-stu-id="8de6e-132">The certificate is valid.</span></span> <span data-ttu-id="8de6e-133">Он активен, не просрочен и не был отозван.</span><span class="sxs-lookup"><span data-stu-id="8de6e-133">It is active, hasn't expired, and hasn't been revoked.</span></span>

## <a name="instructions"></a><span data-ttu-id="8de6e-134">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8de6e-134">Instructions</span></span>

### <a name="step-1-determine-the-hash-algorithm-to-use"></a><span data-ttu-id="8de6e-135">Шаг 1. Определение хэш-алгоритма для использования</span><span class="sxs-lookup"><span data-stu-id="8de6e-135">Step 1: Determine the hash algorithm to use</span></span>

<span data-ttu-id="8de6e-136">При подписывании пакета приложения необходимо использовать тот же хэш-алгоритм, который использовался при создании пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="8de6e-136">When you sign the app package, you must use the same hash algorithm that you used when you created the app package.</span></span> <span data-ttu-id="8de6e-137">Если для создания пакета приложения использовались параметры по умолчанию, то используется алгоритм хэширования SHA256.</span><span class="sxs-lookup"><span data-stu-id="8de6e-137">If you used default settings to create the app package, the hash algorithm used is SHA256.</span></span>

<span data-ttu-id="8de6e-138">Если для создания пакета приложения использовался упаковщик приложений с конкретным алгоритмом хэширования, то для подписывания пакета используйте тот же алгоритм.</span><span class="sxs-lookup"><span data-stu-id="8de6e-138">If you used the app packager with a specific hash algorithm to create the app package, use the same algorithm to sign the package.</span></span> <span data-ttu-id="8de6e-139">Чтобы определить хэш-алгоритм, используемый для подписывания пакета, можно извлечь содержимое пакета и проверить файл AppxBlockMap.xml.</span><span class="sxs-lookup"><span data-stu-id="8de6e-139">To determine the hash algorithm to use for signing a package, you can extract the package contents and inspect the AppxBlockMap.xml file.</span></span> <span data-ttu-id="8de6e-140">Атрибут **хашмесод** элемента [**блоккмап**](/uwp/schemas/blockmapschema/element-blockmap) Указывает хэш-алгоритм, который использовался при создании пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="8de6e-140">The **HashMethod** attribute of the [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates the hash algorithm that was used when creating the app package.</span></span> <span data-ttu-id="8de6e-141">Пример:</span><span class="sxs-lookup"><span data-stu-id="8de6e-141">For example:</span></span>

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

<span data-ttu-id="8de6e-142">Предыдущий элемент [**блоккмап**](/uwp/schemas/blockmapschema/element-blockmap) указывает, что использовался алгоритм SHA256.</span><span class="sxs-lookup"><span data-stu-id="8de6e-142">The preceding [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates that the SHA256 algorithm was used.</span></span> <span data-ttu-id="8de6e-143">В следующей таблице приведено сопоставление доступных в настоящее время алгоритмов:</span><span class="sxs-lookup"><span data-stu-id="8de6e-143">This table lists the mapping of the currently available algorithms:</span></span>

| <span data-ttu-id="8de6e-144">Значение **хашмесод**</span><span class="sxs-lookup"><span data-stu-id="8de6e-144">**HashMethod** value</span></span>                            | <span data-ttu-id="8de6e-145">*hashAlgorithm* для использования</span><span class="sxs-lookup"><span data-stu-id="8de6e-145">*hashAlgorithm* to use</span></span> |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | <span data-ttu-id="8de6e-146">SHA256 (по умолчанию. appx)</span><span class="sxs-lookup"><span data-stu-id="8de6e-146">SHA256 (.appx default)</span></span> |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | <span data-ttu-id="8de6e-147">SHA384</span><span class="sxs-lookup"><span data-stu-id="8de6e-147">SHA384</span></span>                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | <span data-ttu-id="8de6e-148">SHA512</span><span class="sxs-lookup"><span data-stu-id="8de6e-148">SHA512</span></span>                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a><span data-ttu-id="8de6e-149">Шаг 2. Запуск SignTool.exe для подписания пакета</span><span class="sxs-lookup"><span data-stu-id="8de6e-149">Step 2: Run SignTool.exe to sign the package</span></span>

<span data-ttu-id="8de6e-150">**Подписание пакета сертификатом подписи из PFX-файла**</span><span class="sxs-lookup"><span data-stu-id="8de6e-150">**To sign the package with a signing certificate from a .pfx file**</span></span>

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

<span data-ttu-id="8de6e-151">Средство [**SignTool**](/windows-hardware/drivers/devtest/signtool) по умолчанию принимает параметр/FD *HASHALGORITHM* в значение SHA1, если он не указан, а SHA1 не подходит для подписывания пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="8de6e-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) defaults the /fd *hashAlgorithm* parameter to SHA1 if it's not specified, and SHA1 isn't valid for signing app packages.</span></span> <span data-ttu-id="8de6e-152">Поэтому этот параметр необходимо указать при подписании пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="8de6e-152">So, you must specify this parameter when you sign an app package.</span></span> <span data-ttu-id="8de6e-153">Чтобы подписать пакет приложения, созданный с помощью хэша SHA256 по умолчанию, укажите параметр/FD *hashAlgorithm* в качестве значения SHA256:</span><span class="sxs-lookup"><span data-stu-id="8de6e-153">To sign an app package that was created with the default SHA256 hash, you specify the /fd *hashAlgorithm* parameter as SHA256:</span></span>

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

<span data-ttu-id="8de6e-154">Параметр/p *Password* можно опустить, если используется PFX-файл, который не защищен паролем.</span><span class="sxs-lookup"><span data-stu-id="8de6e-154">You can omit the /p *password* parameter if you use a .pfx file that isn't password protected.</span></span> <span data-ttu-id="8de6e-155">Можно также использовать другие параметры выбора сертификатов, которые поддерживаются средством [**SignTool**](/windows-hardware/drivers/devtest/signtool) для подписывания пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="8de6e-155">You can also use other certificate selection options that are supported by [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign app packages.</span></span> <span data-ttu-id="8de6e-156">Дополнительные сведения об этих параметрах см. в разделе [SignTool](/windows/desktop/SecCrypto/signtool).</span><span class="sxs-lookup"><span data-stu-id="8de6e-156">For more info about these options, see [SignTool](/windows/desktop/SecCrypto/signtool).</span></span>

> [!Note]  
> <span data-ttu-id="8de6e-157">В подписанном пакете приложения нельзя использовать операцию неоднократной отметки времени [**SignTool**](/windows-hardware/drivers/devtest/signtool) . операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8de6e-157">You can't use the [**SignTool**](/windows-hardware/drivers/devtest/signtool) time stamp operation on a signed app package; the operation isn't supported.</span></span>

 

<span data-ttu-id="8de6e-158">Если вы хотите отметку времени для пакета приложения, необходимо сделать это во время операции входа.</span><span class="sxs-lookup"><span data-stu-id="8de6e-158">If you want to time stamp the app package, you must do it during the sign operation.</span></span> <span data-ttu-id="8de6e-159">Пример:</span><span class="sxs-lookup"><span data-stu-id="8de6e-159">For example:</span></span>

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

<span data-ttu-id="8de6e-160">Установите параметр/tr *тиместампсерверурл* равным URL-адресу для сервера отметок времени RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="8de6e-160">Make the /tr *timestampServerUrl* parameter equal to the URL for an RFC 3161 time stamp server.</span></span>

## <a name="remarks"></a><span data-ttu-id="8de6e-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8de6e-161">Remarks</span></span>

<span data-ttu-id="8de6e-162">В этом разделе обсуждаются ошибки подписывания для пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="8de6e-162">This section discusses troubleshooting signing errors for app packages.</span></span>

### <a name="troubleshooting-app-package-signing-errors"></a><span data-ttu-id="8de6e-163">Устранение ошибок подписывания пакета приложения</span><span class="sxs-lookup"><span data-stu-id="8de6e-163">Troubleshooting app package signing errors</span></span>

<span data-ttu-id="8de6e-164">Помимо ошибок подписывания, которые может возвращать средство [**SignTool**](/windows-hardware/drivers/devtest/signtool) , средство **SignTool** может также возвращать ошибки, характерные для подписывания пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="8de6e-164">In addition to the signing errors that [**SignTool**](/windows-hardware/drivers/devtest/signtool) can return, **SignTool** can also return errors that are specific to the signing of app packages.</span></span> <span data-ttu-id="8de6e-165">Эти ошибки обычно отображаются в виде внутренних ошибок:</span><span class="sxs-lookup"><span data-stu-id="8de6e-165">These errors usually appear as internal errors:</span></span>

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

<span data-ttu-id="8de6e-166">Если код ошибки начинается с 0x8008, например 0x80080206 APPX \_ E \_ поврежденного \_ содержимого, это означает, что подписанный пакет является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="8de6e-166">If the error code starts with 0x8008, such as 0x80080206 APPX\_E\_CORRUPT\_CONTENT), it indicates that the package being signed is invalid.</span></span> <span data-ttu-id="8de6e-167">В этом случае, прежде чем можно будет подписать пакет, необходимо перестроить пакет.</span><span class="sxs-lookup"><span data-stu-id="8de6e-167">In this case, before you can sign the package, you must rebuild the package.</span></span> <span data-ttu-id="8de6e-168">Полный список \* ошибок 0x8008 см. в разделе [**коды ошибок COM (безопасность и настройка)**](/windows/desktop/com/com-error-codes-4).</span><span class="sxs-lookup"><span data-stu-id="8de6e-168">For the full list of 0x8008\* errors, see [**COM Error Codes (Security and Setup)**](/windows/desktop/com/com-error-codes-4).</span></span>

<span data-ttu-id="8de6e-169">Чаще всего это ошибка 0x8007000b (ошибочный \_ Формат ошибки \_ ).</span><span class="sxs-lookup"><span data-stu-id="8de6e-169">More commonly, the error is 0x8007000b (ERROR\_BAD\_FORMAT).</span></span> <span data-ttu-id="8de6e-170">В этом случае можно найти более подробные сведения об ошибке в журнале событий:</span><span class="sxs-lookup"><span data-stu-id="8de6e-170">In this case, you can find more specific error information in the event log:</span></span>

<span data-ttu-id="8de6e-171">**Поиск в журнале событий**</span><span class="sxs-lookup"><span data-stu-id="8de6e-171">**To search the event log**</span></span>

1.  <span data-ttu-id="8de6e-172">Запустите eventvwr. msc.</span><span class="sxs-lookup"><span data-stu-id="8de6e-172">Run Eventvwr.msc.</span></span>
2.  <span data-ttu-id="8de6e-173">Откройте журнал событий: Просмотр событий (локальный) > журналы приложений и служб > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-Аппкспаккагинг/эксплуатация.</span><span class="sxs-lookup"><span data-stu-id="8de6e-173">Open the event log: Event Viewer (Local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span></span>
3.  <span data-ttu-id="8de6e-174">Найдите Последнее событие ошибки.</span><span class="sxs-lookup"><span data-stu-id="8de6e-174">Look for the most recent error event.</span></span>

<span data-ttu-id="8de6e-175">Внутренняя ошибка обычно соответствует одному из следующих:</span><span class="sxs-lookup"><span data-stu-id="8de6e-175">The internal error usually corresponds to one of these:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8de6e-176">Идентификатор события</span><span class="sxs-lookup"><span data-stu-id="8de6e-176">Event ID</span></span></th>
<th><span data-ttu-id="8de6e-177">Пример строки события</span><span class="sxs-lookup"><span data-stu-id="8de6e-177">Example event string</span></span></th>
<th><span data-ttu-id="8de6e-178">Предложение</span><span class="sxs-lookup"><span data-stu-id="8de6e-178">Suggestion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8de6e-179">150</span><span class="sxs-lookup"><span data-stu-id="8de6e-179">150</span></span></td>
<td><span data-ttu-id="8de6e-180">ошибка 0x8007000B: имя издателя манифеста приложения (CN=Contoso) должно соответствовать имени субъекта сертификата подписи (CN=Contoso, C=US).</span><span class="sxs-lookup"><span data-stu-id="8de6e-180">error 0x8007000B: The app manifest publisher name (CN=Contoso) must match the subject name of the signing certificate (CN=Contoso, C=US).</span></span></td>
<td><span data-ttu-id="8de6e-181">Имя издателя манифеста приложения должно точно соответствовать имени субъекта подписи.</span><span class="sxs-lookup"><span data-stu-id="8de6e-181">The app manifest publisher name must exactly match the subject name of the signing.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8de6e-182">Эти имена задаются в кавычках и являются чувствительными к регистру и пробелами.</span><span class="sxs-lookup"><span data-stu-id="8de6e-182">These names are specified in quotes and are both case and whitespace sensitive.</span></span>
</blockquote>
<br/> <span data-ttu-id="8de6e-183">Вы можете обновить строку атрибута <strong>издателя</strong> , определенную для элемента <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> в файле AppxManifest.xml, в соответствии с именем субъекта предполагаемого сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="8de6e-183">You can update the <strong>Publisher</strong> attribute string that is defined for the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> element in the AppxManifest.xml file to match the subject name of the intended signing certificate.</span></span> <span data-ttu-id="8de6e-184">Или выберите другой сертификат подписи с именем субъекта, совпадающим с именем издателя манифеста приложения.</span><span class="sxs-lookup"><span data-stu-id="8de6e-184">Or, select a different signing certificate with a subject name that matches the app manifest publisher name.</span></span> <span data-ttu-id="8de6e-185">Имя издателя манифеста и имя субъекта сертификата указаны в сообщении о событии.</span><span class="sxs-lookup"><span data-stu-id="8de6e-185">The manifest publisher name and the certificate subject name are both listed in the event message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8de6e-186">151</span><span class="sxs-lookup"><span data-stu-id="8de6e-186">151</span></span></td>
<td><span data-ttu-id="8de6e-187">ошибка 0x8007000B: указанный хэш-метод подписи (SHA512) должен соответствовать хэш-методу, использованному в схеме блоков пакета приложения (SHA256).</span><span class="sxs-lookup"><span data-stu-id="8de6e-187">error 0x8007000B: The signature hash method specified (SHA512) must match the hash method used in the app package block map (SHA256).</span></span></td>
<td><span data-ttu-id="8de6e-188">Неверное значение hashAlgorithm, указанное в параметре/FD (см. шаг 1. Определение хэш-алгоритма для использования).</span><span class="sxs-lookup"><span data-stu-id="8de6e-188">The hashAlgorithm specified in the /fd parameter is incorrect (see Step 1: Determine the hash algorithm to use).</span></span> <span data-ttu-id="8de6e-189">Повторно запустите средство <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> с hashAlgorithm, которое соответствует сопоставлению блоков пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="8de6e-189">Rerun <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> with the hashAlgorithm that matches the app package block map.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8de6e-190">152</span><span class="sxs-lookup"><span data-stu-id="8de6e-190">152</span></span></td>
<td><span data-ttu-id="8de6e-191">Ошибка 0x8007000B: содержимого пакета приложения должно подходить под схему блоков.</span><span class="sxs-lookup"><span data-stu-id="8de6e-191">error 0x8007000B: The app package contents must validate against its block map.</span></span></td>
<td><span data-ttu-id="8de6e-192">Пакет приложения поврежден и его необходимо перестроить для формирования новой схемы блока.</span><span class="sxs-lookup"><span data-stu-id="8de6e-192">The app package is corrupt and needs to be rebuilt to generate a new block map.</span></span> <span data-ttu-id="8de6e-193">Дополнительные сведения о создании пакета приложения см. в статьях создание пакета приложения с помощью <a href="make-appx-package--makeappx-exe-.md">диспетчера приложений</a> или <a href="/previous-versions/hh975357(v=vs.110)">Создание пакета приложения с помощью Visual Studio 2012</a>.</span><span class="sxs-lookup"><span data-stu-id="8de6e-193">For more info about creating an app package, see creating an app package with <a href="make-appx-package--makeappx-exe-.md">app packager</a> or <a href="/previous-versions/hh975357(v=vs.110)">Creating an app package with Visual Studio 2012</a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a><span data-ttu-id="8de6e-194">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="8de6e-194">Security Considerations</span></span>

<span data-ttu-id="8de6e-195">После подписания пакета сертификат, использованный для подписания пакета, должен быть доверенным для компьютера, на котором будет развернут пакет.</span><span class="sxs-lookup"><span data-stu-id="8de6e-195">After the package is signed, the certificate that you used to sign the package must still be trusted by the computer on which the package is to be deployed.</span></span> <span data-ttu-id="8de6e-196">Добавив сертификат в [хранилища сертификатов локальной машины](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), вы меняете доверие сертификатов всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8de6e-196">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="8de6e-197">Рекомендуется установить все сертификаты подписи кода, необходимые для тестирования пакетов приложений в хранилище сертификатов "Доверенные лица", и немедленно удалить эти сертификаты, если они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="8de6e-197">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store, and promptly remove those certificates when no longer necessary.</span></span> <span data-ttu-id="8de6e-198">Если вы создаете собственные тестовые сертификаты для подписи пакетов приложений, мы также рекомендуем ограничить привилегии, связанные с тестовым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="8de6e-198">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges associated with the test certificate.</span></span> <span data-ttu-id="8de6e-199">Дополнительные сведения о создании тестовых сертификатов для подписи пакетов приложений см. [в разделе Создание сертификата для подписи пакета приложения](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="8de6e-199">For more info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8de6e-200">См. также</span><span class="sxs-lookup"><span data-stu-id="8de6e-200">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8de6e-201">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="8de6e-201">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="8de6e-202">Пример создания пакета приложения</span><span class="sxs-lookup"><span data-stu-id="8de6e-202">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="8de6e-203">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="8de6e-203">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="8de6e-204">[Рекомендации по подписывания кода](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8de6e-204">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8de6e-205">[Подписывание пакета в Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="8de6e-205">[Signing a package in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span></span>
</dt> <dt>

[<span data-ttu-id="8de6e-206">SignTool</span><span class="sxs-lookup"><span data-stu-id="8de6e-206">SignTool</span></span>](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[<span data-ttu-id="8de6e-207">Упаковщик приложений (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="8de6e-207">App packager (MakeAppx.exe)</span></span>](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[<span data-ttu-id="8de6e-208">Создание сертификата для подписи пакета приложения</span><span class="sxs-lookup"><span data-stu-id="8de6e-208">How to create an app package signing certificate</span></span>](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

