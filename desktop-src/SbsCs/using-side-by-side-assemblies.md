---
description: Следующая процедура используется для разработки нового приложения или обновления существующего приложения для использования параллельных сборок, доступных в Microsoft или других издателях параллельных сборок.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Использование параллельных сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897098"
---
# <a name="using-side-by-side-assemblies"></a><span data-ttu-id="11ecb-103">Использование параллельных сборок</span><span class="sxs-lookup"><span data-stu-id="11ecb-103">Using Side-by-side Assemblies</span></span>

<span data-ttu-id="11ecb-104">Следующая процедура используется для разработки нового приложения или обновления существующего приложения для использования [параллельных сборок](about-side-by-side-assemblies-.md) , доступных в Microsoft или других издателях параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="11ecb-104">Use the following procedure to develop a new application, or update an existing application, to use the [side-by-side assemblies](about-side-by-side-assemblies-.md) available from Microsoft or other side-by-side assembly publishers.</span></span> <span data-ttu-id="11ecb-105">Список параллельных сборок, предоставляемых корпорацией Майкрософт, см. в разделе [Поддерживаемые параллельные сборки Майкрософт](supported-microsoft-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-105">For a list of the side-by-side assemblies currently provided by Microsoft, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="11ecb-106">Обратите внимание, что приложение должно выполняться как минимум в Windows XP для установки сборок в качестве параллельных сборок.</span><span class="sxs-lookup"><span data-stu-id="11ecb-106">Note that the application must be run on at least Windows XP to install the assemblies as side-by-side assemblies.</span></span> <span data-ttu-id="11ecb-107">Дополнительные сведения см. в разделе [рекомендации по созданию параллельных сборок](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-107">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

<span data-ttu-id="11ecb-108">**Добавление параллельной сборки в приложение**</span><span class="sxs-lookup"><span data-stu-id="11ecb-108">**To add a side-by-side assembly to an application**</span></span>

1.  <span data-ttu-id="11ecb-109">Определяет параллельные сборки, необходимые для приложения.</span><span class="sxs-lookup"><span data-stu-id="11ecb-109">Identify the side-by-side assemblies that your application requires.</span></span> <span data-ttu-id="11ecb-110">Начиная с Windows XP эти параллельные сборки и их манифесты сборок устанавливаются вместе с операционной системой, но не регистрируются глобально.</span><span class="sxs-lookup"><span data-stu-id="11ecb-110">Starting with Windows XP, these side-by-side assemblies and their assembly manifests are installed with the operating system but are not globally registered.</span></span>
2.  <span data-ttu-id="11ecb-111">Используйте редактор XML для создания [манифеста приложения](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-111">Use an XML editor to create an [application manifest](application-manifests.md).</span></span> <span data-ttu-id="11ecb-112">См. пример манифеста приложения ниже.</span><span class="sxs-lookup"><span data-stu-id="11ecb-112">See the example application manifest below.</span></span> <span data-ttu-id="11ecb-113">Дополнительные сведения см. в разделе [манифесты приложений](application-manifests.md) в [справочнике по файлам манифеста](manifest-files-reference.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-113">For more information, see [Application Manifests](application-manifests.md) in the [Manifest Files Reference](manifest-files-reference.md).</span></span>
3.  <span data-ttu-id="11ecb-114">Введите значения атрибутов в вложенный элемент [*assemblyIdentity-context*](d-sbscs-gly.md) в манифесте приложения, который уникальным образом определяет приложение.</span><span class="sxs-lookup"><span data-stu-id="11ecb-114">Enter attribute values in the [*DEF-context assemblyIdentity*](d-sbscs-gly.md) subelement of the application manifest that uniquely defines the application.</span></span> <span data-ttu-id="11ecb-115">Дополнительные сведения о **теге**"DEF-контекст" см. в разделе [манифесты приложений](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-115">For more information about the DEF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>
4.  <span data-ttu-id="11ecb-116">Если сборка содержит зависимые сборки, введите значения атрибутов в соответствующие вложенные элементы [*assemblyIdentity ref-context*](r-sbscs-gly.md) манифеста приложения.</span><span class="sxs-lookup"><span data-stu-id="11ecb-116">If the assembly contains any dependent assemblies, enter attribute values into the corresponding [*REF-context assemblyIdentity*](r-sbscs-gly.md) subelements of the application manifest.</span></span> <span data-ttu-id="11ecb-117">Дополнительные сведения о **ТЕГЕ** ref-context см. в разделе [манифесты приложений](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-117">For more information about the REF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  <span data-ttu-id="11ecb-118">Манифест приложения можно включить в файл заголовков двоичного файла приложения.</span><span class="sxs-lookup"><span data-stu-id="11ecb-118">You may include the application manifest in the application's binary executable header file.</span></span>

    <span data-ttu-id="11ecb-119">В этом случае добавьте в файл заголовка приложения следующую строку:</span><span class="sxs-lookup"><span data-stu-id="11ecb-119">In this case, also add the following line to the application header file:</span></span>

    <dl> <span data-ttu-id="11ecb-120">\_Манифест для \_ ИД ресурса манифеста CREATEPROCESS \_ \_ "YourApp.exe. manifest"</span><span class="sxs-lookup"><span data-stu-id="11ecb-120">CREATEPROCESS\_MANIFEST\_RESOURCE\_ID RT\_MANIFEST "YourApp.exe.manifest"</span></span>  
    </dl>

    <span data-ttu-id="11ecb-121">В качестве альтернативы можно поместить отдельный файл манифеста в тот же каталог, где находится исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="11ecb-121">As an alternative, you can place a separate manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="11ecb-122">Операционная система сначала загружает манифест из файловой системы, а затем проверяет раздел ресурсов исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="11ecb-122">The operating system loads the manifest from the file system first, and then checks the resource section of the executable.</span></span> <span data-ttu-id="11ecb-123">Версия файловой системы имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="11ecb-123">The file system version takes precedence.</span></span>

6.  <span data-ttu-id="11ecb-124">[Общие сборки](/windows/desktop/Msi/shared-assemblies) следует устанавливать с помощью [установщик Windows](../msi/windows-installer-portal.md) версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="11ecb-124">[Shared assemblies](/windows/desktop/Msi/shared-assemblies) should be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="11ecb-125">Создайте пакет установщик Windows, как описано в разделе [как установить сборки Win32 для параллельного совместного использования в Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-125">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span></span>
7.  <span data-ttu-id="11ecb-126">[Закрытые сборки](/windows/desktop/Msi/private-assemblies) можно устанавливать с помощью [установщик Windows](../msi/windows-installer-portal.md) версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="11ecb-126">[Private assemblies](/windows/desktop/Msi/private-assemblies) can be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="11ecb-127">Создайте пакет установщик Windows, как описано в разделе [как установить сборки Win32 для частного использования приложения в Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="11ecb-127">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span></span> <span data-ttu-id="11ecb-128">Можно также использовать любой другой установщик для копирования закрытой сборки и ее манифеста в ту же папку, что и исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="11ecb-128">You can also use any other installer to copy a private assembly and its manifest into the same folder as the application's executable file.</span></span>
8.  <span data-ttu-id="11ecb-129">Тестирование приложения для проверки результатов.</span><span class="sxs-lookup"><span data-stu-id="11ecb-129">Test your application to ensure the results.</span></span> <span data-ttu-id="11ecb-130">Обратите внимание, что на тестовом компьютере не должна быть зарегистрирована параллельная сборка.</span><span class="sxs-lookup"><span data-stu-id="11ecb-130">Note that your test computer should not have the side-by-side assembly registered.</span></span>
9.  <span data-ttu-id="11ecb-131">Разверните приложение или обновите его как пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="11ecb-131">Deploy your application or update as a Windows Installer package.</span></span>

## <a name="example-application-manifest"></a><span data-ttu-id="11ecb-132">Пример манифеста приложения</span><span class="sxs-lookup"><span data-stu-id="11ecb-132">Example Application Manifest</span></span>

<span data-ttu-id="11ecb-133">Ниже приведен пример манифеста приложения.</span><span class="sxs-lookup"><span data-stu-id="11ecb-133">The following is an example of an application manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
