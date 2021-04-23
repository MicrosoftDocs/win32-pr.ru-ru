---
title: Создание сертификата для подписи пакета приложения
description: Узнайте, как использовать MakeCert.exe и Pvk2Pfx.exe для создания тестового сертификата подписи кода, чтобы можно было подписывать пакеты приложений Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069828"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a><span data-ttu-id="031f1-103">Создание сертификата для подписи пакета приложения</span><span class="sxs-lookup"><span data-stu-id="031f1-103">How to create an app package signing certificate</span></span>

> [!IMPORTANT]
> <span data-ttu-id="031f1-104">MakeCert.exe не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="031f1-104">MakeCert.exe is deprecated.</span></span> <span data-ttu-id="031f1-105">Текущие рекомендации по созданию сертификата см. в разделе [Создание сертификата для подписания пакета](/windows/msix/package/create-certificate-package-signing).</span><span class="sxs-lookup"><span data-stu-id="031f1-105">For current guidance on creating a certificate, see [Create a certificate for package signing](/windows/msix/package/create-certificate-package-signing).</span></span>

 

<span data-ttu-id="031f1-106">Узнайте, как использовать [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) для создания тестового сертификата подписи кода, чтобы можно было подписывать пакеты приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="031f1-106">Learn how to use [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your Windows app packages.</span></span>

<span data-ttu-id="031f1-107">Перед развертыванием пакетных приложений Windows необходимо выполнить цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="031f1-107">You must digitally sign your packaged Windows apps before you deploy them.</span></span> <span data-ttu-id="031f1-108">Если вы не используете Microsoft Visual Studio 2012 для создания и подписи пакетов приложений, необходимо создать собственные сертификаты для подписи кода и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="031f1-108">If you don't use Microsoft Visual Studio 2012 to create and sign your app packages, you need to create and manage your own code signing certificates.</span></span> <span data-ttu-id="031f1-109">Сертификаты можно создавать с помощью [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) из комплекта драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="031f1-109">You can create certificates by using [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) from the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="031f1-110">Затем можно использовать сертификаты для подписывания пакетов приложений, чтобы их можно было развернуть локально для тестирования.</span><span class="sxs-lookup"><span data-stu-id="031f1-110">Then you can use the certificates to sign the app packages, so they can be deployed locally for testing.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="031f1-111">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="031f1-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="031f1-112">Технологии</span><span class="sxs-lookup"><span data-stu-id="031f1-112">Technologies</span></span>

-   <span data-ttu-id="031f1-113">[Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="031f1-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="031f1-114">[Пакеты и развертывание приложений](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="031f1-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="031f1-115">Средства для подписывания драйверов</span><span class="sxs-lookup"><span data-stu-id="031f1-115">Tools for Signing Drivers</span></span>](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a><span data-ttu-id="031f1-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="031f1-116">Prerequisites</span></span>

-   <span data-ttu-id="031f1-117">Средства [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) из WDK</span><span class="sxs-lookup"><span data-stu-id="031f1-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools from the WDK</span></span>

## <a name="instructions"></a><span data-ttu-id="031f1-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="031f1-118">Instructions</span></span>

### <a name="step-1-determine-the-publisher-name-of-the-package"></a><span data-ttu-id="031f1-119">Шаг 1. Определение имени издателя пакета</span><span class="sxs-lookup"><span data-stu-id="031f1-119">Step 1: Determine the publisher name of the package</span></span>

<span data-ttu-id="031f1-120">Чтобы сделать сертификат подписи, который вы создадите, использовать с пакетом приложения, который необходимо подписать, имя субъекта сертификата подписи должно соответствовать атрибуту **издателя** элемента [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) в AppxManifest.xml этого приложения.</span><span class="sxs-lookup"><span data-stu-id="031f1-120">To make the signing certificate that you create usable with the app package that you want to sign, the subject name of the signing certificate must match the **Publisher** attribute of the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml for that app.</span></span> <span data-ttu-id="031f1-121">Например, предположим, что AppxManifest.xml содержит:</span><span class="sxs-lookup"><span data-stu-id="031f1-121">For example, suppose the AppxManifest.xml contains:</span></span>

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

<span data-ttu-id="031f1-122">Для параметра *publisherName* , указанного с помощью служебной программы [**MakeCert**](/windows-hardware/drivers/devtest/makecert) на следующем шаге, используйте "CN = Contoso Software, O = Contoso Corporation, C = US".</span><span class="sxs-lookup"><span data-stu-id="031f1-122">For the *publisherName* parameter that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility in the next step, use "CN=Contoso Software, O=Contoso Corporation, C=US".</span></span>

> [!Note]  
> <span data-ttu-id="031f1-123">Эта строка параметра указывается в кавычках и является учетом регистра и пробела.</span><span class="sxs-lookup"><span data-stu-id="031f1-123">This parameter string is specified in quotes and is both case and whitespace sensitive.</span></span>

 

<span data-ttu-id="031f1-124">Строка атрибута **издателя** , определенная для элемента [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) в AppxManifest.xml, должна совпадать со строкой, указанной в параметре [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n для имени субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="031f1-124">The **Publisher** attribute string that is defined for the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml must be identical to the string that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n parameter for the certificate subject name.</span></span> <span data-ttu-id="031f1-125">Скопируйте и вставьте строку, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="031f1-125">Copy and paste the string where possible.</span></span>

### <a name="step-2-create-a-private-key-using-makecertexe"></a><span data-ttu-id="031f1-126">Шаг 2. создание закрытого ключа с помощью MakeCert.exe</span><span class="sxs-lookup"><span data-stu-id="031f1-126">Step 2: Create a private key using MakeCert.exe</span></span>

<span data-ttu-id="031f1-127">Используйте служебную программу [**MakeCert**](/windows-hardware/drivers/devtest/makecert) для создания самозаверяющего тестового сертификата и закрытого ключа:</span><span class="sxs-lookup"><span data-stu-id="031f1-127">Use the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility to create a self-signed test certificate and private key:</span></span>

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

<span data-ttu-id="031f1-128">Эта команда предложит указать пароль для PVK-файла.</span><span class="sxs-lookup"><span data-stu-id="031f1-128">This command prompts you to provide a password for the .pvk file.</span></span> <span data-ttu-id="031f1-129">Рекомендуется выбрать [надежный пароль](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) и защитить закрытый ключ в безопасном месте.</span><span class="sxs-lookup"><span data-stu-id="031f1-129">We recommend that you choose a [strong password](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) and keep your private key in a secure location.</span></span>

<span data-ttu-id="031f1-130">Рекомендуется использовать предлагаемые параметры из предыдущего примера по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="031f1-130">We recommend that you use the suggested parameters in the preceding example for these reasons:</span></span>

<dl> <dt>

<span data-ttu-id="031f1-131"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="031f1-131"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="031f1-132">Создает самозаверяющий корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="031f1-132">Creates a self-signed root certificate.</span></span> <span data-ttu-id="031f1-133">Это упрощает управление тестовым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="031f1-133">This simplifies management for your test certificate.</span></span>

</dd> <dt>

<span data-ttu-id="031f1-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span><span class="sxs-lookup"><span data-stu-id="031f1-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span></span>
</dt> <dd>

<span data-ttu-id="031f1-135">Помечает базовое ограничение для сертификата как конечную сущность.</span><span class="sxs-lookup"><span data-stu-id="031f1-135">Marks the basic constraint for the certificate as an end-entity.</span></span> <span data-ttu-id="031f1-136">Это предотвращает использование сертификата в качестве центра сертификации (ЦС), который может выдавать другие сертификаты.</span><span class="sxs-lookup"><span data-stu-id="031f1-136">This prevents the certificate from being used as a Certification Authority (CA) that can issue other certificates.</span></span>

</dd> <dt>

<span data-ttu-id="031f1-137"><span id="_eku"></span><span id="_EKU"></span>**/еку**</span><span class="sxs-lookup"><span data-stu-id="031f1-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span></span>
</dt> <dd>

<span data-ttu-id="031f1-138">Задает значения расширенного использования ключа (EKU) для сертификата.</span><span class="sxs-lookup"><span data-stu-id="031f1-138">Sets the Enhanced Key Usage (EKU) values for the certificate.</span></span>

> [!Note]  
> <span data-ttu-id="031f1-139">Не ставьте пробел между двумя значениями, разделенными запятыми.</span><span class="sxs-lookup"><span data-stu-id="031f1-139">Don't put a space between the two comma-delimited values.</span></span>

 

-   <span data-ttu-id="031f1-140">1.3.6.1.5.5.7.3.3 указывает, что сертификат действителен для подписывания кода.</span><span class="sxs-lookup"><span data-stu-id="031f1-140">1.3.6.1.5.5.7.3.3 indicates that the certificate is valid for code signing.</span></span> <span data-ttu-id="031f1-141">Всегда указывайте это значение, чтобы ограничить предполагаемое использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="031f1-141">Always specify this value to limit the intended use for the certificate.</span></span>
-   <span data-ttu-id="031f1-142">1.3.6.1.4.1.311.10.3.13 указывает, что сертификат учитывает время существования подписи.</span><span class="sxs-lookup"><span data-stu-id="031f1-142">1.3.6.1.4.1.311.10.3.13 indicates that the certificate respects lifetime signing.</span></span> <span data-ttu-id="031f1-143">Как правило, если подпись имеет отметку времени, при условии, что сертификат был действителен в момент времени, подпись остается действительной, даже если срок действия сертификата истек.</span><span class="sxs-lookup"><span data-stu-id="031f1-143">Typically, if a signature is time stamped, as long as the certificate was valid at the point when it was time stamped, the signature remains valid even if the certificate expires.</span></span> <span data-ttu-id="031f1-144">Это расширенное EKU заставляет срок действия подписи истечь независимо от того, имеет ли подпись время отметки.</span><span class="sxs-lookup"><span data-stu-id="031f1-144">This EKU forces the signature to expire regardless of whether the signature is time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="031f1-145"><span id="_e"></span><span id="_E"></span>**/e**</span><span class="sxs-lookup"><span data-stu-id="031f1-145"><span id="_e"></span><span id="_E"></span>**/e**</span></span>
</dt> <dd>

<span data-ttu-id="031f1-146">Задает дату окончания срока действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="031f1-146">Sets the expiration date of the certificate.</span></span> <span data-ttu-id="031f1-147">Укажите значение параметра *expirationDate* в формате мм/дд/гггг.</span><span class="sxs-lookup"><span data-stu-id="031f1-147">Provide a value for the *expirationDate* parameter in the mm/dd/yyyy format.</span></span> <span data-ttu-id="031f1-148">Рекомендуется выбирать дату истечения срока действия, если это необходимо для целей тестирования, как правило, меньше года.</span><span class="sxs-lookup"><span data-stu-id="031f1-148">We recommend that you choose an expiration date only as long as necessary for your testing purposes, typically less than a year.</span></span> <span data-ttu-id="031f1-149">Эта дата окончания срока действия в сочетании с ключом времени существования подписывания может помочь ограничить окно, в котором сертификат может быть скомпрометирован и недоступен.</span><span class="sxs-lookup"><span data-stu-id="031f1-149">This expiration date in conjunction with the lifetime signing EKU can help to limit the window in which the certificate can be compromised and misused.</span></span>

</dd> </dl>

<span data-ttu-id="031f1-150">Дополнительные сведения о других параметрах см. в разделе [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span><span class="sxs-lookup"><span data-stu-id="031f1-150">For more info about other options, see [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span></span>

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a><span data-ttu-id="031f1-151">Шаг 3. Создание файла обмена личной информацией (PFX) с помощью Pvk2Pfx.exe</span><span class="sxs-lookup"><span data-stu-id="031f1-151">Step 3: Create a Personal Information Exchange (.pfx) file using Pvk2Pfx.exe</span></span>

<span data-ttu-id="031f1-152">Используйте служебную программу [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) для преобразования файлов. PVK и. cer, созданных средством [**MakeCert**](/windows-hardware/drivers/devtest/makecert) , в PFX-файл, который можно использовать с средством [SignTool](/windows/desktop/SecCrypto/signtool) для подписания пакета приложения:</span><span class="sxs-lookup"><span data-stu-id="031f1-152">Use the [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) utility to convert the .pvk and .cer files that [**MakeCert**](/windows-hardware/drivers/devtest/makecert) created to a .pfx file that you can use with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package:</span></span>

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

<span data-ttu-id="031f1-153">Файлы *MyKey. PVK* и *MyKey. cer* являются теми же файлами, которые [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) созданы на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="031f1-153">The *MyKey.pvk* and *MyKey.cer* files are the same files that [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) created in the previous step.</span></span> <span data-ttu-id="031f1-154">С помощью необязательного параметра/по можно указать другой пароль для результирующего PFX-файла; в противном случае PFX-файл имеет тот же пароль, что и *MyKey. PVK*.</span><span class="sxs-lookup"><span data-stu-id="031f1-154">By using the optional /po parameter, you can specify a different password for the resulting .pfx; otherwise, the .pfx has the same password as *MyKey.pvk*.</span></span>

<span data-ttu-id="031f1-155">Дополнительные сведения о других параметрах см. в разделе [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span><span class="sxs-lookup"><span data-stu-id="031f1-155">For more info about other options, see [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span></span>

## <a name="remarks"></a><span data-ttu-id="031f1-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="031f1-156">Remarks</span></span>

<span data-ttu-id="031f1-157">После создания PFX-файла можно использовать файл с помощью средства [SignTool](/windows/desktop/SecCrypto/signtool) для подписания пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="031f1-157">After you create the .pfx file, you can use the file with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package.</span></span> <span data-ttu-id="031f1-158">Дополнительные сведения см. [в разделе как подписать пакет приложения с помощью средства SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="031f1-158">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="031f1-159">Но сертификат по-прежнему не является доверенным для локального компьютера для развертывания пакетов приложений, пока он не будет установлен в хранилище доверенных сертификатов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="031f1-159">But the certificate is still not trusted by the local computer for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="031f1-160">Вы можете использовать [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), входящий в состав Windows.</span><span class="sxs-lookup"><span data-stu-id="031f1-160">You can use [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), which comes with Windows.</span></span>

<span data-ttu-id="031f1-161">**Установка сертификатов с помощью WindowsCertutil.exe**</span><span class="sxs-lookup"><span data-stu-id="031f1-161">**To install certificates with WindowsCertutil.exe**</span></span>

1.  <span data-ttu-id="031f1-162">Запустите **Cmd.exe** от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="031f1-162">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="031f1-163">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="031f1-163">Run this command:</span></span>

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

<span data-ttu-id="031f1-164">Рекомендуется удалить сертификаты, если они больше не используются.</span><span class="sxs-lookup"><span data-stu-id="031f1-164">We recommend that you remove the certificates if they are no longer in use.</span></span> <span data-ttu-id="031f1-165">В той же командной строке администратора выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="031f1-165">From the same administrator command prompt, run this command:</span></span>

``` syntax
Certutil -delStore TrustedPeople certID
```

<span data-ttu-id="031f1-166">**CertID** — серийный номер сертификата.</span><span class="sxs-lookup"><span data-stu-id="031f1-166">The **certID** is the serial number of the certificate.</span></span> <span data-ttu-id="031f1-167">Выполните следующую команду, чтобы определить серийный номер сертификата:</span><span class="sxs-lookup"><span data-stu-id="031f1-167">Run this command to determine the certificate serial number:</span></span>

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a><span data-ttu-id="031f1-168">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="031f1-168">Security Considerations</span></span>

<span data-ttu-id="031f1-169">Добавив сертификат в [хранилища сертификатов локальной машины](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), вы меняете доверие сертификатов всех пользователей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="031f1-169">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="031f1-170">Рекомендуется установить все сертификаты подписи кода, необходимые для тестирования пакетов приложений в хранилище сертификатов "Доверенные лица".</span><span class="sxs-lookup"><span data-stu-id="031f1-170">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="031f1-171">Немедленно удалите эти сертификаты, когда они больше не нужны, чтобы предотвратить их использование для компрометации доверия системы.</span><span class="sxs-lookup"><span data-stu-id="031f1-171">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span>

## <a name="related-topics"></a><span data-ttu-id="031f1-172">См. также</span><span class="sxs-lookup"><span data-stu-id="031f1-172">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="031f1-173">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="031f1-173">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="031f1-174">Пример создания пакета приложения</span><span class="sxs-lookup"><span data-stu-id="031f1-174">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="031f1-175">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="031f1-175">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="031f1-176">[Рекомендации по подписывания кода](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="031f1-176">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="031f1-177">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Подписывание пакета приложения с помощью SignTool)</span><span class="sxs-lookup"><span data-stu-id="031f1-177">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md)</span></span>
</dt> <dt>

<span data-ttu-id="031f1-178">[Подписание пакета приложения](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="031f1-178">[Signing an app package](/previous-versions/br230260(v=vs.110))</span></span>
</dt> </dl>

 

 