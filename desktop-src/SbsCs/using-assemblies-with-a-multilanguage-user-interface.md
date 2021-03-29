---
description: Если вы хотите, чтобы пользователи приложения или основной библиотеки DLL могли изменять язык пользовательского интерфейса, рекомендуется разместить языковые ресурсы в отдельных вспомогательных библиотеках ресурсов.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Использование сборок с многоязыковым пользовательским интерфейсом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809359"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a><span data-ttu-id="6bd74-103">Использование сборок с многоязыковым пользовательским интерфейсом</span><span class="sxs-lookup"><span data-stu-id="6bd74-103">Using Assemblies with a Multilanguage User Interface</span></span>

<span data-ttu-id="6bd74-104">Если вы хотите, чтобы пользователи приложения или основной библиотеки DLL могли изменять язык пользовательского интерфейса, рекомендуется разместить языковые ресурсы в отдельных вспомогательных библиотеках ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bd74-104">If you want users of your application, or core DLL, to be capable of changing the language of the user interface, you should consider placing language resources into separate satellite resource DLLs.</span></span> <span data-ttu-id="6bd74-105">Дополнительные сведения об использовании вспомогательных библиотек ресурсов см. в разделе [многоязычный пользовательский интерфейс (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="6bd74-105">For more information about using satellite resource DLLs, see [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="6bd74-106">Каждая вспомогательная библиотека DLL содержит ресурсы для другого языка.</span><span class="sxs-lookup"><span data-stu-id="6bd74-106">Each satellite DLL contains the resources for a different language.</span></span> <span data-ttu-id="6bd74-107">Основная библиотека DLL может быть предоставлена как сборка, а каждая вспомогательная библиотека DLL может предоставляться в виде отдельных вспомогательных сборок.</span><span class="sxs-lookup"><span data-stu-id="6bd74-107">The core DLL may be provided as an assembly and each of the satellite DLLs may be provided as separate satellite assemblies.</span></span> <span data-ttu-id="6bd74-108">В этом случае каждая вспомогательная сборка должна иметь собственный манифест сборки с самоописанием.</span><span class="sxs-lookup"><span data-stu-id="6bd74-108">In this case, each satellite assembly should have its own self-describing assembly manifest.</span></span> <span data-ttu-id="6bd74-109">Манифест вспомогательной сборки не должен описывать зависимости от других сборок.</span><span class="sxs-lookup"><span data-stu-id="6bd74-109">The satellite assembly's manifest should not describe any dependency on other assemblies.</span></span> <span data-ttu-id="6bd74-110">Все зависимости вспомогательных сборок в других сборках следует описывать в манифесте основной сборки.</span><span class="sxs-lookup"><span data-stu-id="6bd74-110">Any dependency of satellite assemblies on other assemblies should instead be described in the core assembly's manifest.</span></span>

<span data-ttu-id="6bd74-111">Версия Windows для [многоязычного пользовательского интерфейса (MUI)](/windows/desktop/Intl/multilingual-user-interface) позволяет пользователям указывать язык интерфейса пользователя в соответствии с их предпочтениями при условии, что в систему добавлен требуемый язык.</span><span class="sxs-lookup"><span data-stu-id="6bd74-111">The [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) version of Windows enables users to specify the user-interface language according to their preferences, provided the required language has been added to the system.</span></span> <span data-ttu-id="6bd74-112">Основная сборка может поддерживать несколько языков с помощью нескольких сборок MUI.</span><span class="sxs-lookup"><span data-stu-id="6bd74-112">A core assembly can support multiple languages by using multiple MUI assemblies.</span></span> <span data-ttu-id="6bd74-113">В этом случае каждая сборка MUI должна иметь собственный манифест, и все зависимости от других сборок следует описывать только в манифесте основной сборки.</span><span class="sxs-lookup"><span data-stu-id="6bd74-113">In this case, each MUI assembly should have its own manifest and any dependencies on other assemblies should only be described in the core assembly's manifest.</span></span>

<span data-ttu-id="6bd74-114">Например, proseware. Sample. POP может быть основной параллельной сборкой, которая зависит от сборки proseware. Research. Самплеассембли.</span><span class="sxs-lookup"><span data-stu-id="6bd74-114">For example, Proseware.Sample.Pop may be a core side-by-side assembly which happens to be dependent on the Proseware.Research.SampleAssembly assembly.</span></span> <span data-ttu-id="6bd74-115">Если proseware. Sample. POP использует многоязыковый интерфейс пользователя для поддержки нескольких языков, для каждого языка можно предоставить отдельные сборки MUI.</span><span class="sxs-lookup"><span data-stu-id="6bd74-115">If Proseware.Sample.Pop uses MUI to support multiple languages, separate MUI assemblies can be provided for each language.</span></span> <span data-ttu-id="6bd74-116">Каждая сборка MUI должна иметь собственный манифест, описывающий эту конкретную вспомогательную БИБЛИОТЕКУ ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bd74-116">Each MUI assembly should have its own manifest describing this particular satellite resource DLL.</span></span> <span data-ttu-id="6bd74-117">Манифесты сборки MUI не должны включать ссылки на зависимости от других сборок.</span><span class="sxs-lookup"><span data-stu-id="6bd74-117">The MUI assembly manifests should not include any reference to dependencies on other assemblies.</span></span> <span data-ttu-id="6bd74-118">Манифест, описывающий основную сборку proseware. Sample. POP, должен описывать зависимость proseware. Sample. POP в сборке proseware. Research. Самплеассембли.</span><span class="sxs-lookup"><span data-stu-id="6bd74-118">The manifest describing the core assembly, Proseware.Sample.Pop, should describe the dependency of Proseware.Sample.Pop on the Proseware.Research.SampleAssembly assembly.</span></span>

<span data-ttu-id="6bd74-119">Атрибуты элемента **assemblyIdentity** вспомогательной сборки аналогичны атрибутам в манифесте базовой сборки.</span><span class="sxs-lookup"><span data-stu-id="6bd74-119">The attributes of the **assemblyIdentity** element of a satellite assembly are similar to those in the manifest of the base assembly.</span></span> <span data-ttu-id="6bd74-120">Атрибут **Name** должен быть таким же, как и базовая сборка с добавлением "Resources".</span><span class="sxs-lookup"><span data-stu-id="6bd74-120">The **name** attribute should be the same as the base assembly with the addition of "Resources."</span></span> <span data-ttu-id="6bd74-121">Например, если в базовой сборке указано имя «proseware. Tools. проверкой. Runtime-Library», то имя в сборке ресурса будет иметь вид «proseware. Tools.. Runtime-Librarys. Resources».</span><span class="sxs-lookup"><span data-stu-id="6bd74-121">For example, if the name is "Proseware.Tools.SpellCheck.Runtime-Libraries" in the base assembly, the name in the resource assembly would be "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources."</span></span> <span data-ttu-id="6bd74-122">Атрибут **Language** должен обозначать язык сборки ресурса.</span><span class="sxs-lookup"><span data-stu-id="6bd74-122">The **language** attribute should identify the language of the resource assembly.</span></span> <span data-ttu-id="6bd74-123">Атрибут **File** должен включать список файлов, которые являются библиотеками DLL ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bd74-123">The **file** attribute should include the list of files that are resource DLLs.</span></span>

<span data-ttu-id="6bd74-124">Ниже приведен пример манифеста для сборки ресурсов proseware. Tools. проверкой среды выполнения. Runtime-Librarys.</span><span class="sxs-lookup"><span data-stu-id="6bd74-124">The following is an example of the manifest for Proseware.Tools.SpellCheck.Runtime-Libraries resources assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

<span data-ttu-id="6bd74-125">Базовая сборка описывает необязательную зависимость от сборки ресурса.</span><span class="sxs-lookup"><span data-stu-id="6bd74-125">The base assembly describes an optional dependency on the resource assembly.</span></span> <span data-ttu-id="6bd74-126">В этом примере, если пользователь работает под Windows с языковым стандартом, обозначенным как немецкий, приложение, использующее сборку proseware. Tools. проверкой орфографии, будет отображать текст на немецком языке.</span><span class="sxs-lookup"><span data-stu-id="6bd74-126">In this example, if a user is running Windows with the locale designated as German, an application using the Proseware.Tools.SpellCheck assembly would display text in German.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
