---
description: В Windows Server 2003 служба WinHTTP реализована как параллельная сборка и должна быть связана как таковая. Обратите внимание, что это не относится к Windows Vista и более поздним версиям.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Использование WinHTTP в качестве параллельной сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809784"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a><span data-ttu-id="94acb-104">Использование WinHTTP в качестве параллельной сборки</span><span class="sxs-lookup"><span data-stu-id="94acb-104">Using WinHTTP as a Side-by-side Assembly</span></span>

<span data-ttu-id="94acb-105">В Windows Server 2003 служба WinHTTP реализована как параллельная сборка и должна быть связана как таковая.</span><span class="sxs-lookup"><span data-stu-id="94acb-105">On Windows Server 2003, WinHTTP is implemented as a side-by-side assembly, and must be linked to as such.</span></span> <span data-ttu-id="94acb-106">Обратите внимание, что это не относится к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="94acb-106">Note that this does not apply to Windows Vista and later.</span></span>

## <a name="side-by-side-assemblies"></a><span data-ttu-id="94acb-107">Параллельные сборки</span><span class="sxs-lookup"><span data-stu-id="94acb-107">Side-by-side Assemblies</span></span>

<span data-ttu-id="94acb-108">Начиная с Microsoft Windows XP, был предоставлен механизм параллельных сборок для управления связыванием во время выполнения, чтобы избежать конфликтов управления версиями библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="94acb-108">Starting with Microsoft Windows XP, a side-by-side assemblies mechanism was provided to control run-time linking to avoid dynamic-link-library (DLL) versioning conflicts.</span></span> <span data-ttu-id="94acb-109">Сведения о параллельных сборках см. в разделе [о изолированных приложениях и параллельных сборках](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span><span class="sxs-lookup"><span data-stu-id="94acb-109">For information about side-by-side assemblies, see [About Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span></span>

<span data-ttu-id="94acb-110">Чтобы использовать этот механизм для связи с WinHTTP версии 5,1 на Windows Server 2003, приложение должно включать манифест, который указывает WinHTTP как зависимую сборку.</span><span class="sxs-lookup"><span data-stu-id="94acb-110">To use this mechanism to link to WinHTTP version 5.1 on Windows Server 2003, an application must incorporate a manifest that specifies WinHTTP as a dependent assembly.</span></span> <span data-ttu-id="94acb-111">Дополнительные сведения о том, как это сделать, см. в разделе [использование параллельных сборок](/windows/desktop/SbsCs/using-side-by-side-assemblies) .</span><span class="sxs-lookup"><span data-stu-id="94acb-111">See [Using Side-by-side Assemblies](/windows/desktop/SbsCs/using-side-by-side-assemblies) for more information about how to do this.</span></span>

## <a name="a-sample-winhttp-application-manifest"></a><span data-ttu-id="94acb-112">Пример манифеста приложения WinHTTP</span><span class="sxs-lookup"><span data-stu-id="94acb-112">A Sample WinHTTP Application Manifest</span></span>

<span data-ttu-id="94acb-113">В примере манифеста ниже показан манифест приложения, который можно использовать для связи с WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="94acb-113">The sample manifest below illustrates an application manifest that can be used for linking to WinHTTP.</span></span>

<span data-ttu-id="94acb-114">Все атрибуты, кроме "Type" для " <assembly> <assemblyIdentity> ", должны быть изменены в соответствии с конкретным приложением.</span><span class="sxs-lookup"><span data-stu-id="94acb-114">All attributes except "type" of the "<assembly><assemblyIdentity>" must be modified as appropriate for your particular application.</span></span> <span data-ttu-id="94acb-115">То же самое касается содержимого &lt; элемента «Description &gt; ».</span><span class="sxs-lookup"><span data-stu-id="94acb-115">The same goes for the contents of the "&lt;description&gt;" element.</span></span>

<span data-ttu-id="94acb-116">Кроме того, убедитесь, что атрибут "processorArchitecture" объекта " <dependentAssembly> <assemblyIdentity> " соответствует атрибуту "processorArchitecture" элемента " <assembly> <assemblyIdentity> ".</span><span class="sxs-lookup"><span data-stu-id="94acb-116">In addition, make sure that the "processorArchitecture" attribute of the "<dependentAssembly><assemblyIdentity>" matches the "processorArchitecture" attribute of the "<assembly><assemblyIdentity>".</span></span> <span data-ttu-id="94acb-117">Ниже, например, для обоих задано значение "x86".</span><span class="sxs-lookup"><span data-stu-id="94acb-117">Below, for example, both are set to "x86".</span></span>

<span data-ttu-id="94acb-118">Все значения, не относящиеся к конкретному приложению, должны принять формы, показанные ниже.</span><span class="sxs-lookup"><span data-stu-id="94acb-118">All values not specific to your application should take the forms shown below.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
