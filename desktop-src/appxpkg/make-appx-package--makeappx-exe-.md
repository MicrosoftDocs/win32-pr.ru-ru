---
title: Упаковщик приложений (MakeAppx.exe)
description: Упаковщик приложений (MakeAppx.exe) создает пакет приложения из файлов на диске или извлекает файлы из пакета приложения на диск.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133702"
---
# <a name="app-packager-makeappxexe"></a><span data-ttu-id="3d2a5-103">Упаковщик приложений (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-103">App packager (MakeAppx.exe)</span></span>

> [!Note]  
> <span data-ttu-id="3d2a5-104">Рекомендации по использованию этого средства для UWP см. в статье [Создание пакета приложения с помощью средства MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-104">For UWP guidance on using this tool, see [Create an app package with the MakeAppx.exe tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span></span>

 

<span data-ttu-id="3d2a5-105">Упаковщик приложений (MakeAppx.exe) создает пакет приложения из файлов на диске или извлекает файлы из пакета приложения на диск.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-105">App packager (MakeAppx.exe) creates an app package from files on disk or extracts the files from an app package to disk.</span></span> <span data-ttu-id="3d2a5-106">Начиная с Windows 8.1, упаковщик приложений также создает набор пакетов приложений из пакетов приложений на диске или извлекает пакеты приложений из пакета приложений на диск.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-106">Starting with Windows 8.1, App packager also creates an app package bundle from app packages on disk or extracts the app packages from an app package bundle to disk.</span></span> <span data-ttu-id="3d2a5-107">Он включен в Microsoft Visual Studio и пакет средств разработки программного обеспечения Windows (SDK) для Windows 8 или пакета средств разработки программного обеспечения Windows (SDK) для Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-107">It is included in Microsoft Visual Studio and the Windows Software Development Kit (SDK) for Windows 8 or Windows Software Development Kit (SDK) for Windows 8.1.</span></span> <span data-ttu-id="3d2a5-108">Посетите страницу [downloads для разработчиков]( https://msdn.microsoft.com/windows/apps/br229516.aspx) , чтобы получить их.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-108">Visit [Downloads for developers]( https://msdn.microsoft.com/windows/apps/br229516.aspx) to get them.</span></span>

<span data-ttu-id="3d2a5-109">Средство MakeAppx.exe обычно находится в следующих расположениях:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-109">The MakeAppx.exe tool is typically found at these locations:</span></span>

-   <span data-ttu-id="3d2a5-110">На x86: C: \\ Program Files (x86) \\ Windows Kit \\ 8,0 \\ bin \\ x86 \\makeappx.exe или C: \\ Program files (x86) \\ Windows Kit \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="3d2a5-110">On x86: C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
-   <span data-ttu-id="3d2a5-111">На x64 в двух местах:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-111">On x64 in two locations:</span></span>
    -   <span data-ttu-id="3d2a5-112">C: \\ Program Files (x86) \\ Windows Kit \\ 8,0 \\ bin \\ x86 \\makeappx.exe или C: \\ Program files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="3d2a5-112">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
    -   <span data-ttu-id="3d2a5-113">C: \\ Program Files (x86) \\ Windows Kit \\ 8,0 \\ bin \\ x64 \\makeappx.exe или C: \\ Program files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x64 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="3d2a5-113">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x64\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x64\\makeappx.exe</span></span>

<span data-ttu-id="3d2a5-114">Версия ARM средства отсутствует.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-114">There is no ARM version of the tool.</span></span>

-   [<span data-ttu-id="3d2a5-115">Создание пакета с помощью структуры каталогов</span><span class="sxs-lookup"><span data-stu-id="3d2a5-115">To create a package using a directory structure</span></span>](#to-create-a-package-using-a-directory-structure)
-   [<span data-ttu-id="3d2a5-116">Создание пакета с помощью файла сопоставления</span><span class="sxs-lookup"><span data-stu-id="3d2a5-116">To create a package using a mapping file</span></span>](#to-create-a-package-using-a-mapping-file)
-   [<span data-ttu-id="3d2a5-117">Подпись пакета с помощью средства SignTool</span><span class="sxs-lookup"><span data-stu-id="3d2a5-117">To sign the package using SignTool</span></span>](#to-sign-the-package-using-signtool)
-   [<span data-ttu-id="3d2a5-118">Извлечение файлов из пакета</span><span class="sxs-lookup"><span data-stu-id="3d2a5-118">To extract files from a package</span></span>](#to-extract-files-from-a-package)
-   [<span data-ttu-id="3d2a5-119">Создание пакета пакетов с помощью структуры каталогов</span><span class="sxs-lookup"><span data-stu-id="3d2a5-119">To create a package bundle using a directory structure</span></span>](#to-create-a-package-bundle-using-a-directory-structure)
-   [<span data-ttu-id="3d2a5-120">Создание пакета пакетов с помощью файла сопоставления</span><span class="sxs-lookup"><span data-stu-id="3d2a5-120">To create a package bundle using a mapping file</span></span>](#to-create-a-package-bundle-using-a-mapping-file)
-   [<span data-ttu-id="3d2a5-121">Извлечение пакетов из пакета</span><span class="sxs-lookup"><span data-stu-id="3d2a5-121">To extract packages from a bundle</span></span>](#to-extract-packages-from-a-bundle)
-   [<span data-ttu-id="3d2a5-122">Шифрование пакета с помощью файла ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-122">To encrypt a package with a key file</span></span>](#to-encrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="3d2a5-123">Шифрование пакета с помощью глобального тестового ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-123">To encrypt a package with a global test key</span></span>](#to-encrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="3d2a5-124">Расшифровка пакета с помощью файла ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-124">To decrypt a package with a key file</span></span>](#to-decrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="3d2a5-125">Расшифровка пакета с помощью глобального тестового ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-125">To decrypt a package with a global test key</span></span>](#to-decrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="3d2a5-126">Использование</span><span class="sxs-lookup"><span data-stu-id="3d2a5-126">Usage</span></span>](#usage)

## <a name="using-app-packager"></a><span data-ttu-id="3d2a5-127">Использование упаковщика приложений</span><span class="sxs-lookup"><span data-stu-id="3d2a5-127">Using App packager</span></span>

> [!Note]  
> <span data-ttu-id="3d2a5-128">Относительные пути поддерживаются во всем средстве.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-128">Relative paths are supported throughout the tool.</span></span>

 

### <a name="to-create-a-package-using-a-directory-structure"></a><span data-ttu-id="3d2a5-129">Создание пакета с помощью структуры каталогов</span><span class="sxs-lookup"><span data-stu-id="3d2a5-129">To create a package using a directory structure</span></span>

<span data-ttu-id="3d2a5-130">Поместите AppxManifest.xml в корневой каталог каталога, содержащего все полезные файлы приложения.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-130">Place the AppxManifest.xml in the root of a directory containing all of the payload files for your app.</span></span> <span data-ttu-id="3d2a5-131">Для пакета приложения создается идентичная структура каталога, которая будет доступна при извлечении пакета во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-131">An identical directory structure is created for the app package, and will be available when the package is extracted at deployment time.</span></span>

1.  <span data-ttu-id="3d2a5-132">Разместите все файлы в одной структуре каталогов, создавая нужные подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-132">Place all files in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="3d2a5-133">Создайте допустимый манифест пакета, AppxManifest.xml и поместите его в корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-133">Create a valid package manifest, AppxManifest.xml, and place it in the root directory.</span></span>

3.  <span data-ttu-id="3d2a5-134">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-134">Run this command:</span></span>

    <span data-ttu-id="3d2a5-135">**Программе makeappx Pack/d** *Вход \_ DirectoryPath* **/p** _FilePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-135">**MakeAppx pack /d** *input\_directorypath* **/p** _filepath_**.appx**</span></span>

### <a name="to-create-a-package-using-a-mapping-file"></a><span data-ttu-id="3d2a5-136">Создание пакета с помощью файла сопоставления</span><span class="sxs-lookup"><span data-stu-id="3d2a5-136">To create a package using a mapping file</span></span>

1.  <span data-ttu-id="3d2a5-137">Создайте допустимый манифест пакета, AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-137">Create a valid package manifest, AppxManifest.xml.</span></span>

2.  <span data-ttu-id="3d2a5-138">Создайте файл сопоставления.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-138">Create a mapping file.</span></span> <span data-ttu-id="3d2a5-139">В первой строке содержатся **\[ файлы \]** строк, а в строках, следующих за ними, указываются пути к источнику (диску) и месту назначения (пакетов) в строках в кавычках.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-139">The first line contains the string **\[Files\]**, and the lines that follow specify the source (disk) and destination (package) paths in quoted strings.</span></span>

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  <span data-ttu-id="3d2a5-140">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-140">Run this command:</span></span>

    <span data-ttu-id="3d2a5-141">**Программе makeappx Pack/f** *сопоставление \_ FilePath* **/p** _FilePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-141">**MakeAppx pack /f** *mapping\_filepath* **/p** _filepath_**.appx**</span></span>

### <a name="to-sign-the-package-using-signtool"></a><span data-ttu-id="3d2a5-142">Подпись пакета с помощью средства SignTool</span><span class="sxs-lookup"><span data-stu-id="3d2a5-142">To sign the package using SignTool</span></span>

1.  <span data-ttu-id="3d2a5-143">Создайте сертификат.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-143">Create the certificate.</span></span> <span data-ttu-id="3d2a5-144">Издатель, указанный в манифесте, должен соответствовать сведениям о субъекте издателя сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-144">The publisher listed in the manifest must match the publisher subject information of the signing certificate.</span></span> <span data-ttu-id="3d2a5-145">Дополнительные сведения о создании сертификата для подписи см. [в разделе Создание сертификата для подписи пакета приложения](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-145">For more info about creating a signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

2.  <span data-ttu-id="3d2a5-146">Запустите SignTool.exe, чтобы подписать пакет:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-146">Run SignTool.exe to sign the package:</span></span>

    <span data-ttu-id="3d2a5-147">**Подписывание SignTool/a/v/FD** *hashAlgorithm* **/f** *цертфиленаме* _FilePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-147">**SignTool sign /a /v /fd** *hashAlgorithm* **/f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="3d2a5-148">*HashAlgorithm* должен соответствовать хэш-алгоритму, используемому для создания блоккмап при упаковке приложения.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-148">The *hashAlgorithm* must match the hash algorithm used to create the blockmap when the app was packaged.</span></span> <span data-ttu-id="3d2a5-149">С помощью служебной программы упаковки программе makeappx по умолчанию алгоритм хеширования appx блоккмап имеет значение **SHA256**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-149">With the MakeAppx packaging utility, the default Appx blockmap hash algorithm is **SHA256**.</span></span> <span data-ttu-id="3d2a5-150">Запустите SignTool.exe указав **SHA256** в качестве алгоритма файлового дайджеста (/FD):</span><span class="sxs-lookup"><span data-stu-id="3d2a5-150">Run SignTool.exe specifying **SHA256** as the file digest (/fd) algorithm:</span></span>

    <span data-ttu-id="3d2a5-151">**Подписывание SignTool/a/v/FD SHA256/F** *цертфиленаме* _FilePath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-151">**SignTool sign /a /v /fd SHA256 /f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="3d2a5-152">Дополнительные сведения о том, как подписывать пакеты, см. [в разделе как подписать пакет приложения с помощью средства SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-152">For more info about how to sign packages, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>

### <a name="to-extract-files-from-a-package"></a><span data-ttu-id="3d2a5-153">Извлечение файлов из пакета</span><span class="sxs-lookup"><span data-stu-id="3d2a5-153">To extract files from a package</span></span>

1.  <span data-ttu-id="3d2a5-154">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-154">Run this command:</span></span>

    <span data-ttu-id="3d2a5-155">**Программе makeappx распаковки, параметр/p** _File_**. appx/d** *выходной \_ Каталог*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-155">**MakeAppx unpack /p** _file_**.appx /d** *output\_directory*</span></span>

2.  <span data-ttu-id="3d2a5-156">Распакованный пакет имеет ту же структуру, что и установленный пакет.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-156">The unpacked package has the same structure as the installed package.</span></span>

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a><span data-ttu-id="3d2a5-157">Создание пакета пакетов с помощью структуры каталогов</span><span class="sxs-lookup"><span data-stu-id="3d2a5-157">To create a package bundle using a directory structure</span></span>

<span data-ttu-id="3d2a5-158">Мы используем команду **пакета** для создания пакета приложений в</span><span class="sxs-lookup"><span data-stu-id="3d2a5-158">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="3d2a5-159">путем добавления всех пакетов <content directory> (включая вложенные папки).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-159">by adding all packages from <content directory> (including subfolders).</span></span> <span data-ttu-id="3d2a5-160">Если <content directory> содержит манифест пакета, AppxBundleManifest.xml, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-160">If <content directory> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="3d2a5-161">Разместите все пакеты в одной структуре каталогов, создавая нужные подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-161">Place all packages in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="3d2a5-162">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-162">Run this command:</span></span>

    <span data-ttu-id="3d2a5-163">**Программе makeappx пакета/d** *Вход \_ DirectoryPath* **/p** _FilePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-163">**MakeAppx bundle /d** *input\_directorypath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a><span data-ttu-id="3d2a5-164">Создание пакета пакетов с помощью файла сопоставления</span><span class="sxs-lookup"><span data-stu-id="3d2a5-164">To create a package bundle using a mapping file</span></span>

<span data-ttu-id="3d2a5-165">Мы используем команду **пакета** для создания пакета приложений в</span><span class="sxs-lookup"><span data-stu-id="3d2a5-165">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="3d2a5-166">путем добавления всех пакетов из списка пакетов в <mapping file> .</span><span class="sxs-lookup"><span data-stu-id="3d2a5-166">by adding all packages from a list of packages within <mapping file>.</span></span> <span data-ttu-id="3d2a5-167">Если <mapping file> содержит манифест пакета, AppxBundleManifest.xml, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-167">If <mapping file> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="3d2a5-168">Создайте таблицу <mapping file>.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-168">Create a <mapping file>.</span></span> <span data-ttu-id="3d2a5-169">Первая строка содержит **\[ файлы \]** строк, а следующие строки указывают пакеты для добавления в пакет.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-169">The first line contains the string **\[Files\]**, and the lines that follow specify the packages to add to the bundle.</span></span> <span data-ttu-id="3d2a5-170">Каждый пакет описывается парой путей в кавычках, разделенных пробелами или символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-170">Each package is described by a pair of paths in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="3d2a5-171">Пара путей представляет источник пакета (на диске) и назначение (в пакете).</span><span class="sxs-lookup"><span data-stu-id="3d2a5-171">The pair of paths represents the package's source (on disk) and destination (in bundle).</span></span> <span data-ttu-id="3d2a5-172">Все имена целевых пакетов должны иметь расширение Appx.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-172">All destination package names must have the .appx extension.</span></span>

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  <span data-ttu-id="3d2a5-173">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-173">Run this command:</span></span>

    <span data-ttu-id="3d2a5-174">**Программе makeappx пакет/f** *сопоставление \_ FilePath* **/p** _FilePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-174">**MakeAppx bundle /f** *mapping\_filepath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-extract-packages-from-a-bundle"></a><span data-ttu-id="3d2a5-175">Извлечение пакетов из пакета</span><span class="sxs-lookup"><span data-stu-id="3d2a5-175">To extract packages from a bundle</span></span>

1.  <span data-ttu-id="3d2a5-176">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-176">Run this command:</span></span>

    <span data-ttu-id="3d2a5-177">**Программе makeappx unbundle/p** _\_ имя пакета_**. appxbundle/d** *выходной \_ Каталог*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-177">**MakeAppx unbundle /p** _bundle\_name_**.appxbundle /d** *output\_directory*</span></span>

2.  <span data-ttu-id="3d2a5-178">Распакованный пакет имеет ту же структуру, что и установленный пакет пакетов.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-178">The unpacked bundle has the same structure as the installed package bundle.</span></span>

### <a name="to-encrypt-a-package-with-a-key-file"></a><span data-ttu-id="3d2a5-179">Шифрование пакета с помощью файла ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-179">To encrypt a package with a key file</span></span>

1.  <span data-ttu-id="3d2a5-180">Создайте файл ключа.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-180">Create a key file.</span></span> <span data-ttu-id="3d2a5-181">Файлы ключей должны начинаться со строки "Keys", содержащей строку " \[ ключи \] ", за которой следуют строки, описывающие ключи для шифрования пакета.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-181">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="3d2a5-182">Каждый ключ описывается парой строк в кавычках, разделенных пробелами или символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-182">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="3d2a5-183">Первая строка представляет идентификатор ключа, а вторая — ключ шифрования в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-183">The first string represents the key ID and the second string represents the encryption key in hexadecimal form.</span></span>

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  <span data-ttu-id="3d2a5-184">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-184">Run this command:</span></span>

    <span data-ttu-id="3d2a5-185">**MakeAppx.exe Encrypt/p** _\_ имя пакета_**. appx/EP** имя _зашифрованного \_ \_ пакета_**. еаппкс/КФ** _keyfile \_ Name_**. txt**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-185">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="3d2a5-186">Входной пакет будет зашифрован в указанный зашифрованный пакет с помощью указанного файла ключа.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-186">The input package will be encrypted into the specified encrypted package using the provided key file.</span></span>

### <a name="to-encrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="3d2a5-187">Шифрование пакета с помощью глобального тестового ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-187">To encrypt a package with a global test key</span></span>

1.  <span data-ttu-id="3d2a5-188">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-188">Run this command:</span></span>

    <span data-ttu-id="3d2a5-189">**MakeAppx.exe Encrypt/p** _\_ имя пакета_**. appx/EP** _\_ \_ имя зашифрованного пакета_**. еаппкс/КТ**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-189">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="3d2a5-190">Входной пакет будет зашифрован в указанный зашифрованный пакет с помощью глобального ключа теста.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-190">The input package will be encrypted into the specified encrypted package using the global test key.</span></span>

### <a name="to-decrypt-a-package-with-a-key-file"></a><span data-ttu-id="3d2a5-191">Расшифровка пакета с помощью файла ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-191">To decrypt a package with a key file</span></span>

1.  <span data-ttu-id="3d2a5-192">Создайте файл ключа.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-192">Create a key file.</span></span> <span data-ttu-id="3d2a5-193">Файлы ключей должны начинаться со строки "Keys", содержащей строку " \[ ключи \] ", за которой следуют строки, описывающие ключи для шифрования пакета.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-193">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="3d2a5-194">Каждый ключ описывается парой строк в кавычках, разделенных пробелами или символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-194">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="3d2a5-195">Первая строка представляет идентификатор ключа в кодировке Base64 (32-байт), а вторая строка представляет ключ шифрования 32-байт в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-195">The first string represents the base64 encoded 32-byte key ID and the second string represents the base64 encoded 32-byte encryption key.</span></span>

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  <span data-ttu-id="3d2a5-196">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-196">Run this command:</span></span>

    <span data-ttu-id="3d2a5-197">**MakeAppx.exe расшифровка/p** _\_ имя пакета_**. appx/EP** _незашифрованное \_ \_ имя пакета_**. еаппкс/КФ** _keyfile \_ Name_**. txt**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-197">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="3d2a5-198">Входной пакет будет расшифрован в указанный незашифрованный пакет с помощью указанного файла ключа.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-198">The input package will be decrypted into the specified unencrypted package using the provided key file.</span></span>

### <a name="to-decrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="3d2a5-199">Расшифровка пакета с помощью глобального тестового ключа</span><span class="sxs-lookup"><span data-stu-id="3d2a5-199">To decrypt a package with a global test key</span></span>

1.  <span data-ttu-id="3d2a5-200">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-200">Run this command:</span></span>

    <span data-ttu-id="3d2a5-201">**MakeAppx.exe расшифровка/p** _\_ имя пакета_**. appx/EP** _незашифрованное \_ \_ имя пакета_**. еаппкс/КТ**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-201">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="3d2a5-202">Входной пакет будет расшифрован в указанный незашифрованный пакет с помощью глобального ключа теста.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-202">The input package will be decrypted into the specified unencrypted package using the global test key.</span></span>

## <a name="usage"></a><span data-ttu-id="3d2a5-203">Использование</span><span class="sxs-lookup"><span data-stu-id="3d2a5-203">Usage</span></span>

<span data-ttu-id="3d2a5-204">Аргумент командной строки **/p** всегда является обязательным и имеет значение **/d**, **/f** или **/EP**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-204">The command line argument **/p** is always required, with either **/d**, **/f**, or **/ep**.</span></span> <span data-ttu-id="3d2a5-205">Обратите внимание, что **/d**, **/f** и **/EP** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-205">Note that **/d**, **/f**, and **/ep** are mutually exclusive.</span></span>

<span data-ttu-id="3d2a5-206">**\[ Параметры \] пакета программе makeappx** **/p** *\<output package name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-206">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="3d2a5-207">**\[ Параметры \] пакета программе makeappx** **/p** *\<output package name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-207">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="3d2a5-208">**Программе makeappx распаковки \[ параметров \]** **/p** *\<input package name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-208">**MakeAppx unpack \[options\]** **/p** *\<input package name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="3d2a5-209">**\[ Параметры \] пакета программе makeappx** **/p** *\<output bundle name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-209">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="3d2a5-210">**\[ Параметры \] пакета программе makeappx** **/p** *\<output bundle name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-210">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="3d2a5-211">**Программе makeappx \[ Параметры \] разпакета** **/p** *\<input bundle name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-211">**MakeAppx unbundle \[options\]** **/p** *\<input bundle name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="3d2a5-212">**\[ Параметры \] шифрования программе makeappx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-212">**MakeAppx encrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

<span data-ttu-id="3d2a5-213">**\[ Параметры \] расшифровки программе makeappx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-213">**MakeAppx decrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="3d2a5-214">Синтаксис для командной строки</span><span class="sxs-lookup"><span data-stu-id="3d2a5-214">Command-line Syntax</span></span>

<span data-ttu-id="3d2a5-215">Ниже приведен пример общего синтаксиса использования для программе makeappx в командной строке.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-215">Here is the command-line common usage syntax for MakeAppx.</span></span>

<span data-ttu-id="3d2a5-216">**Программе makeappx \[ пакет распаковки \| \| \| unpackть \| Encrypt \| \]** \[ **/h** **/КФ** **/КТ** **/l** **/o** **/но** **/НВ** **/v** **/ПФН** **/?**\]</span><span class="sxs-lookup"><span data-stu-id="3d2a5-216">**MakeAppx \[pack\|unpack\|bundle\|unbundle\|encrypt\|decrypt\]** \[**/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/?**\]</span></span>

<span data-ttu-id="3d2a5-217">**Программе makeappx** пакеты или распаковать файлы в пакете, упаковывает или раз пакеты в пакете, либо шифрует или расшифровывает пакет приложения или набор в указанном входном каталоге или файле сопоставления.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-217">**MakeAppx** packs or unpacks the files in a package, bundles or unbundles the packages in a bundle, or encrypts or decrypts the app package or bundle in the specified input directory or mapping file.</span></span> <span data-ttu-id="3d2a5-218">Ниже приведен список параметров, которые применяются к **пакету программе makeappx**, **программе makeappx распаковки**, пакету **программе makeappx**, **программе makeappx unpack**, **программе makeappx Encrypt** или **программе makeappx дешифровки**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-218">Here is the list of parameters that apply to **MakeAppx pack**, **MakeAppx unpack**, **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, or **MakeAppx decrypt**.</span></span>

<dl> <dt>

<span data-ttu-id="3d2a5-219"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-219"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-220">Этот параметр используется для локализованных пакетов.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-220">This option is used for localized packages.</span></span> <span data-ttu-id="3d2a5-221">Пути проверки по умолчанию для локализованных пакетов.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-221">The default validation trips on localized packages.</span></span> <span data-ttu-id="3d2a5-222">Этот параметр отключает только эту конкретную проверку без необходимости отключать все проверки.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-222">This option disables only that specific validation, without requiring that all validation be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="3d2a5-223"><span id="_o"></span><span id="_O"></span>**/o**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-223"><span id="_o"></span><span id="_O"></span>**/o**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-224">Перезапишите выходной файл, если он существует.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-224">Overwrite the output file if it exists.</span></span> <span data-ttu-id="3d2a5-225">Если вы не укажете этот параметр или параметр **/но** , пользователь получит запрос на перезапись файла.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-225">If you don't specify this option or the **/no** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="3d2a5-226">Этот параметр нельзя использовать с **/но**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-226">You can't use this option with **/no**.</span></span>

</dd> <dt>

<span data-ttu-id="3d2a5-227"><span id="_no"></span><span id="_NO"></span>**/но**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-227"><span id="_no"></span><span id="_NO"></span>**/no**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-228">Предотвращает перезапись выходного файла, если он существует.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-228">Prevents an overwrite of the output file if it exists.</span></span> <span data-ttu-id="3d2a5-229">Если не указать этот параметр или параметр **/o** , пользователь получит запрос на перезапись файла.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-229">If you don't specify this option or the **/o** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="3d2a5-230">Этот параметр нельзя использовать с **/o**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-230">You can't use this option with **/o**.</span></span>

</dd> <dt>

<span data-ttu-id="3d2a5-231"><span id="_nv"></span><span id="_NV"></span>**/нв**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-232">Пропустить семантическую проверку.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-232">Skip semantic validation.</span></span> <span data-ttu-id="3d2a5-233">Если не указать этот параметр, средство выполняет полную проверку пакета.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-233">If you don't specify this option, the tool performs a full validation of the package.</span></span>

</dd> <dt>

<span data-ttu-id="3d2a5-234"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-234"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-235">Включите подробный вывод журнала в консоль.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-235">Enable verbose logging output to the console.</span></span>

</dd> <dt>

<span data-ttu-id="3d2a5-236"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-236"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-237">Отображение текста справки.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-237">Display help text.</span></span>

</dd> </dl>

<span data-ttu-id="3d2a5-238">**Программе makeappx Pack** , **программе makeappx, распаковка** , **программе makeappx**, **программе makeappx unpack**, **программе makeappx Encrypt** и **программе makeappx дешифровки** являются взаимоисключающими командами.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-238">**MakeAppx pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, and **MakeAppx decrypt** are mutually exclusive commands.</span></span> <span data-ttu-id="3d2a5-239">Ниже приведены параметры командной строки, которые применяются специально для каждой команды:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-239">Here are the command-line parameters that apply specifically to each command:</span></span>

<span data-ttu-id="3d2a5-240">**Пакет программе makeappx** \[ **з**\]</span><span class="sxs-lookup"><span data-stu-id="3d2a5-240">**MakeAppx pack** \[**h**\]</span></span>

<span data-ttu-id="3d2a5-241">Создает пакет.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-241">Creates a package.</span></span>

<dl> <dt>

<span data-ttu-id="3d2a5-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span> *алгоритм* /h</span><span class="sxs-lookup"><span data-stu-id="3d2a5-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *algorithm*</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-243">Указывает хэш-алгоритм, используемый при создании сопоставления блоков.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-243">Specifies the hash algorithm to use when creating the block map.</span></span> <span data-ttu-id="3d2a5-244">Ниже приведены допустимые значения для *алгоритма*.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-244">Here are valid values for *algorithm*:</span></span>

<dl> <dd><span data-ttu-id="3d2a5-245">SHA256 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d2a5-245">SHA256 (default)</span></span></dd> <dd><span data-ttu-id="3d2a5-246">SHA384</span><span class="sxs-lookup"><span data-stu-id="3d2a5-246">SHA384</span></span></dd> <dd><span data-ttu-id="3d2a5-247">SHA512</span><span class="sxs-lookup"><span data-stu-id="3d2a5-247">SHA512</span></span></dd> </dl>

<span data-ttu-id="3d2a5-248">Этот параметр нельзя использовать с командой **unpack** .</span><span class="sxs-lookup"><span data-stu-id="3d2a5-248">You can't use this option with the **unpack** command.</span></span>

</dd> </dl>

<span data-ttu-id="3d2a5-249">**Программе makeappx распаковать** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="3d2a5-249">**MakeAppx unpack** \[**pfn**\]</span></span>

<span data-ttu-id="3d2a5-250">Извлекает все файлы в указанном пакете в указанный выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-250">Extracts all files in the specified package to the specified output directory.</span></span> <span data-ttu-id="3d2a5-251">Выходные данные имеют ту же структуру каталогов, что и пакет.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-251">The output has the same directory structure as the package.</span></span>

<dl> <dt>

<span data-ttu-id="3d2a5-252"><span id="_pfn"></span><span id="_PFN"></span>**/пфн**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-253">Указывает каталог с именем с полным именем пакета.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-253">Specifies a directory named with the package full name.</span></span> <span data-ttu-id="3d2a5-254">Этот каталог создается в указанном расположении выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-254">This directory is created under the provided output location.</span></span> <span data-ttu-id="3d2a5-255">Этот параметр нельзя использовать с командой **Pack** .</span><span class="sxs-lookup"><span data-stu-id="3d2a5-255">You can't use this option with the **pack** command.</span></span>

</dd> </dl>

<span data-ttu-id="3d2a5-256">**Программе makeappx распакетировать** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="3d2a5-256">**MakeAppx unbundle** \[**pfn**\]</span></span>

<span data-ttu-id="3d2a5-257">Распаковать все пакеты в подкаталог с указанным выходным путем, названный после полного имени пакета.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-257">Unpacks all packages to a subdirectory under the specified output path, named after the bundle full name.</span></span> <span data-ttu-id="3d2a5-258">Выходные данные имеют ту же структуру каталогов, что и установленный пакет пакетов.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-258">The output has the same directory structure as the installed package bundle.</span></span>

<dl> <dt>

<span data-ttu-id="3d2a5-259"><span id="_pfn"></span><span id="_PFN"></span>**/пфн**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-260">Указывает каталог с именем с полным именем пакета пакетов.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-260">Specifies a directory named with the package bundle full name.</span></span> <span data-ttu-id="3d2a5-261">Этот каталог создается в указанном расположении выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-261">This directory is created under the provided output location.</span></span> <span data-ttu-id="3d2a5-262">Этот параметр нельзя использовать с командой **пакета** .</span><span class="sxs-lookup"><span data-stu-id="3d2a5-262">You can't use this option with the **bundle** command.</span></span>

</dd> </dl>

<span data-ttu-id="3d2a5-263">**Программе makeappx шифрование** \[ **КФ**, **kt**\]</span><span class="sxs-lookup"><span data-stu-id="3d2a5-263">**MakeAppx encrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="3d2a5-264">Создает зашифрованный пакет приложения из указанного входного пакета приложения в указанном выходном пакете.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-264">Creates an encrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="3d2a5-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/КФ\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-266">Шифрует пакет или набор с помощью ключа из указанного файла ключей.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-266">Encrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="3d2a5-267">Этот параметр нельзя использовать с **kt**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-267">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="3d2a5-268"><span id="_kt"></span><span id="_KT"></span>**/кт**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-269">Шифрует пакет или набор с помощью глобального тестового ключа.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-269">Encrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="3d2a5-270">Этот параметр нельзя использовать с **КФ**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-270">You can't use this option with **kf**.</span></span>

</dd> </dl>

<span data-ttu-id="3d2a5-271">**Программе makeappx расшифровку** \[ **КФ**, **kt**\]</span><span class="sxs-lookup"><span data-stu-id="3d2a5-271">**MakeAppx decrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="3d2a5-272">Создает незашифрованный пакет приложения из указанного входного пакета приложения в указанном выходном пакете.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-272">Creates an unencrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="3d2a5-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/КФ\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="3d2a5-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-274">Расшифровывает пакет или набор с помощью ключа из указанного файла ключей.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-274">Decrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="3d2a5-275">Этот параметр нельзя использовать с **kt**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-275">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="3d2a5-276"><span id="_kt"></span><span id="_KT"></span>**/кт**</span><span class="sxs-lookup"><span data-stu-id="3d2a5-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="3d2a5-277">Расшифровывает пакет или набор с помощью глобального тестового ключа.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-277">Decrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="3d2a5-278">Этот параметр нельзя использовать с **КФ**.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-278">You can't use this option with **kf**.</span></span>

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a><span data-ttu-id="3d2a5-279">Семантическая проверка, выполняемая программе makeappx</span><span class="sxs-lookup"><span data-stu-id="3d2a5-279">Semantic validation performed by MakeAppx</span></span>

<span data-ttu-id="3d2a5-280">Программе makeappx выполняет ограниченную семантическую проверку, которая предназначена для перехвата наиболее распространенных ошибок развертывания и обеспечения допустимости пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-280">MakeAppx performs limited semantic validation that is designed to catch the most common deployment errors and help ensure that the app package is valid.</span></span>

<span data-ttu-id="3d2a5-281">Эта проверка гарантирует следующее:</span><span class="sxs-lookup"><span data-stu-id="3d2a5-281">This validation ensures that:</span></span>

-   <span data-ttu-id="3d2a5-282">все файлы, ссылки на которые присутствуют в манифесте пакета, входят в состав пакета приложения;</span><span class="sxs-lookup"><span data-stu-id="3d2a5-282">All files referenced in the package manifest are included in the app package.</span></span>
-   <span data-ttu-id="3d2a5-283">в приложении нет двух идентичных ключей;</span><span class="sxs-lookup"><span data-stu-id="3d2a5-283">An application does not have two identical keys.</span></span>
-   <span data-ttu-id="3d2a5-284">Приложение не регистрируется для запрещенного протокола из этого списка: SMB, FILE, MS-ВВА-WEB, MS-ВВА.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-284">An application does not register for a forbidden protocol from this list: SMB , FILE, MS-WWA-WEB, MS-WWA.</span></span>

<span data-ttu-id="3d2a5-285">Эта семантическая проверка не завершена, и пакеты, созданные программе makeappx, не гарантированно будут устанавливаться.</span><span class="sxs-lookup"><span data-stu-id="3d2a5-285">This semantic validation is not complete, and packages built by MakeAppx are not guaranteed to be installable.</span></span>

 

 