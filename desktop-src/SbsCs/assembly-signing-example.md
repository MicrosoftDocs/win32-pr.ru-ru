---
description: В следующем примере рассматривается создание подписанной параллельной сборки, состоящей из манифеста сборки, каталога проверки и файлов сборки.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Пример подписывания сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105647801"
---
# <a name="assembly-signing-example"></a><span data-ttu-id="a83b2-103">Пример подписывания сборки</span><span class="sxs-lookup"><span data-stu-id="a83b2-103">Assembly Signing Example</span></span>

<span data-ttu-id="a83b2-104">В следующем примере рассматривается создание подписанной параллельной сборки, состоящей из манифеста сборки, каталога проверки и файлов сборки.</span><span class="sxs-lookup"><span data-stu-id="a83b2-104">The following example discusses how to generate a signed side-by-side assembly consisting of the assembly manifest, the verification catalog, and the assembly files.</span></span> <span data-ttu-id="a83b2-105">Совместно используемые параллельные сборки должны быть подписаны.</span><span class="sxs-lookup"><span data-stu-id="a83b2-105">Shared side-by-side assemblies should be signed.</span></span> <span data-ttu-id="a83b2-106">Операционная система проверяет подпись сборки перед установкой общей сборки в глобальном хранилище на стороне (WinSxS).</span><span class="sxs-lookup"><span data-stu-id="a83b2-106">The operating system verifies the assembly signature before installing a shared assembly to the global side-by-side store (WinSxS).</span></span> <span data-ttu-id="a83b2-107">Это затрудняет подмену издателя параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="a83b2-107">This makes it difficult to spoof the publisher of the side-by-side assembly.</span></span>

<span data-ttu-id="a83b2-108">Обратите внимание, что изменение файлов сборки или содержимого манифеста после создания каталога сборки сделает каталог и сборку недействительными.</span><span class="sxs-lookup"><span data-stu-id="a83b2-108">Note that changing the assembly files or the contents of the manifest after generating the assembly catalog invalidates the catalog and the assembly.</span></span> <span data-ttu-id="a83b2-109">Если необходимо обновить файлы сборки или манифест после создания и подписи каталога, необходимо снова подписать сборку и создать новый каталог.</span><span class="sxs-lookup"><span data-stu-id="a83b2-109">If you must update the assembly files or manifest after creating and signing the catalog, you must again sign the assembly and generate a new catalog.</span></span>

<span data-ttu-id="a83b2-110">Начните с файлов сборки, манифеста сборки и файла сертификата, который будет использоваться для подписания сборки.</span><span class="sxs-lookup"><span data-stu-id="a83b2-110">Start with the assembly files, assembly manifest, and the certificate file you will use to sign the assembly.</span></span> <span data-ttu-id="a83b2-111">Файл сертификата должен иметь размер 2048 или более.</span><span class="sxs-lookup"><span data-stu-id="a83b2-111">The certificate file must be 2048 bits or larger.</span></span> <span data-ttu-id="a83b2-112">Вы не обязаны использовать доверенный сертификат.</span><span class="sxs-lookup"><span data-stu-id="a83b2-112">You are not required to use a trusted certificate.</span></span> <span data-ttu-id="a83b2-113">Сертификат используется только для проверки того, что сборка не повреждена.</span><span class="sxs-lookup"><span data-stu-id="a83b2-113">The certificate is used only to verify that the assembly has not been damaged.</span></span>

<span data-ttu-id="a83b2-114">Запустите служебную программу [Pktextract.exe](pktextract-exe.md) , предоставляемую в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows, чтобы извлечь маркер открытого ключа из файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="a83b2-114">Run the [Pktextract.exe](pktextract-exe.md) utility provided in the Microsoft Windows Software Development Kit (SDK) to extract the public key token from the certificate file.</span></span> <span data-ttu-id="a83b2-115">Для правильной работы Пктекстракт файл сертификата должен находиться в том же каталоге, что и программа.</span><span class="sxs-lookup"><span data-stu-id="a83b2-115">For Pktextract to work properly, the certificate file must be present in the same directory as the utility.</span></span> <span data-ttu-id="a83b2-116">Используйте извлеченное значение токена открытого ключа, чтобы обновить атрибут **PublicKeyToken** элемента **assemblyIdentity** в файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="a83b2-116">Use the extracted public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>

<span data-ttu-id="a83b2-117">Ниже приведен пример файла манифеста с именем Мисамплеассембли. manifest.</span><span class="sxs-lookup"><span data-stu-id="a83b2-117">Here is an example of a manifest file named MySampleAssembly.manifest.</span></span> <span data-ttu-id="a83b2-118">Сборка Мисамплеассембли содержит только один файл, MYFILE.DLL.</span><span class="sxs-lookup"><span data-stu-id="a83b2-118">The MySampleAssembly assembly contains only one file, MYFILE.DLL.</span></span> <span data-ttu-id="a83b2-119">Обратите внимание, что значение атрибута **PublicKeyToken** элемента **assemblyIdentity** Обновлено значением маркера открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="a83b2-119">Note that the value for the **publicKeyToken** attribute of the **assemblyIdentity** element has been updated with the value of the public key token.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

<span data-ttu-id="a83b2-120">Затем запустите служебную программу [Mt.exe](mt-exe.md) , предоставленную в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a83b2-120">Next run the [Mt.exe](mt-exe.md) utility provided in the Windows SDK.</span></span> <span data-ttu-id="a83b2-121">Файлы сборки должны находиться в том же каталоге, что и манифест.</span><span class="sxs-lookup"><span data-stu-id="a83b2-121">The assembly files must be located in the same directory as the manifest.</span></span> <span data-ttu-id="a83b2-122">В этом примере это каталог Мисамплеассембли.</span><span class="sxs-lookup"><span data-stu-id="a83b2-122">In this example this is the MySampleAssembly directory.</span></span> <span data-ttu-id="a83b2-123">Вызовите Mt.exe для примера следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a83b2-123">Call Mt.exe for the example as follows:</span></span>

<span data-ttu-id="a83b2-124">**c: \\ мисамплеассембли>mt.exe-manifest мисамплеассембли. manifest-хашупдате-макекдфс**</span><span class="sxs-lookup"><span data-stu-id="a83b2-124">**c:\\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**</span></span>

<span data-ttu-id="a83b2-125">Вот как выглядит пример манифеста после выполнения Mt.exe.</span><span class="sxs-lookup"><span data-stu-id="a83b2-125">Here is how the example manifest looks after running Mt.exe.</span></span> <span data-ttu-id="a83b2-126">Обратите внимание, что выполнение Mt.exe с параметром хашупдате добавляет хэш SHA-1 файла.</span><span class="sxs-lookup"><span data-stu-id="a83b2-126">Notice that running Mt.exe with the hashupdate option adds the SHA-1 hash of the file.</span></span> <span data-ttu-id="a83b2-127">Не изменяйте это значение.</span><span class="sxs-lookup"><span data-stu-id="a83b2-127">Do not change this value.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

<span data-ttu-id="a83b2-128">Выполнение Mt.exe с параметром-макекдфс создает файл с именем Мисамплеассембли. manifest. CDF, описывающий содержимое каталога безопасности, который будет использоваться для проверки манифеста.</span><span class="sxs-lookup"><span data-stu-id="a83b2-128">Running Mt.exe with the -makecdfs option generates a file named MySampleAssembly.manifest.cdf that describes the contents of the security catalog that will be used to validate the manifest.</span></span>

<span data-ttu-id="a83b2-129">Чтобы создать каталог безопасности для сборки, необходимо выполнить Makecat.exe. CDF.</span><span class="sxs-lookup"><span data-stu-id="a83b2-129">The next step is to run Makecat.exe over this .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="a83b2-130">Вызов Makecat.exe для этого примера будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a83b2-130">The call to Makecat.exe for this example would appear as follows:</span></span>

<span data-ttu-id="a83b2-131">**c: \\ мисамплеассембли>Макекат мисамплеассембли. manifest. CDF**</span><span class="sxs-lookup"><span data-stu-id="a83b2-131">**c:\\MySampleAssembly>makecat MySampleAssembly.manifest.cdf**</span></span>

<span data-ttu-id="a83b2-132">Последним шагом является запуск SignTool.exe для подписывания файла каталога с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="a83b2-132">The final step is to run SignTool.exe to sign the catalog file with the certificate.</span></span> <span data-ttu-id="a83b2-133">Это должен быть тот же сертификат, который использовался в предыдущем примере для создания токена открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="a83b2-133">This should be the same certificate that was used in the preceding to generate the public key token.</span></span> <span data-ttu-id="a83b2-134">Дополнительные сведения о SignTool.exe см. в разделе средство [**SignTool**](../seccrypto/signtool.md) .</span><span class="sxs-lookup"><span data-stu-id="a83b2-134">For more information about SignTool.exe see the [**SignTool**](../seccrypto/signtool.md) topic.</span></span> <span data-ttu-id="a83b2-135">Вызов **SignTool** для примера будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a83b2-135">The call to **SignTool** for the example would appear as follows:</span></span>

<span data-ttu-id="a83b2-136">**c: \\ мисамплеассембли>средство SignTool с подписью/f \<fullpath> MyCompany. pfx/du HTTPS: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.DigiCert.com MySampleAssembly.cat**</span><span class="sxs-lookup"><span data-stu-id="a83b2-136">**c:\\MySampleAssembly>signtool sign /f \<fullpath>mycompany.pfx /du https:\//www.mycompany.com/MySampleAssembly /t https:\//timestamp.digicert.com MySampleAssembly.cat**</span></span>

<span data-ttu-id="a83b2-137">Если у вас есть цифровой сертификат, прошедший проверку подлинности, и в центре сертификации для хранения закрытого ключа используется формат PVK-файла, можно использовать импортер файлов цифровых сертификатов (pvkimprt.exe), чтобы импортировать ключ в поставщик служб шифрования (CSP).</span><span class="sxs-lookup"><span data-stu-id="a83b2-137">If you have an authenticated digital certificate, and your certification authority uses the PVK file format to store the private key, you can use the PVK Digital Certificate Files Importer (pvkimprt.exe) to import the key into your cryptographic service provider (CSP).</span></span> <span data-ttu-id="a83b2-138">Эта служебная программа позволяет экспортировать в формат PFX/P12 отраслевого стандарта.</span><span class="sxs-lookup"><span data-stu-id="a83b2-138">This utility enables you to export to the industry standard format of PFX/P12.</span></span> <span data-ttu-id="a83b2-139">Дополнительные сведения об импортере файлов цифровых сертификатов PVK см. в разделе ресурсы развертывания библиотеки MSDN или в центре сертификации.</span><span class="sxs-lookup"><span data-stu-id="a83b2-139">For more information about the PVK Digital Certificate Files Importer, see the Deployment Resources section of the MSDN library or contact your certification authority.</span></span> <span data-ttu-id="a83b2-140">Возможно, вы сможете получить pvkimprt.exe из https://office.microsoft.com/downloads/2000/pvkimprt.aspx .</span><span class="sxs-lookup"><span data-stu-id="a83b2-140">You may be able to obtain pvkimprt.exe from https://office.microsoft.com/downloads/2000/pvkimprt.aspx.</span></span>

<span data-ttu-id="a83b2-141">См. также [Создание подписанных файлов и каталогов](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="a83b2-141">See also, [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

 

 
