---
description: Исправление установщик Windows (MSP) можно применить при первой установке приложения с помощью свойства PATCH.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Установка исправлений первоначальных установок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999589"
---
# <a name="patching-initial-installations"></a><span data-ttu-id="947d6-103">Установка исправлений первоначальных установок</span><span class="sxs-lookup"><span data-stu-id="947d6-103">Patching Initial Installations</span></span>

<span data-ttu-id="947d6-104">Исправление установщик Windows (MSP) можно применить при первой установке приложения с помощью свойства [**Patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="947d6-104">A Windows Installer Patch (MSP) can be applied when installing an application for the first time by using the [**PATCH**](patch.md) property.</span></span>

<span data-ttu-id="947d6-105">Чтобы применить исправление при первом установке приложения, необходимо установить свойство [**Patch**](patch.md) в командной строке.</span><span class="sxs-lookup"><span data-stu-id="947d6-105">To apply a patch the first time the application is installed, the [**PATCH**](patch.md) property must be set on the command line.</span></span> <span data-ttu-id="947d6-106">Укажите полный путь к исправлению в командной строке в виде пары "свойство-значение" PATCH = {*путь к исправлению*} ".</span><span class="sxs-lookup"><span data-stu-id="947d6-106">Specify the full path to the patch on the command line as the "PATCH={*path to patch*}" property-value pair.</span></span>

<span data-ttu-id="947d6-107">Обратите внимание, что указание свойства [**Patch**](patch.md) в командной строке переопределяет проверки применимости исправления, выполняемые при использовании [**Мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) или [параметра командной строки](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="947d6-107">Note that specifying the [**PATCH**](patch.md) property on the command line overrides the patch applicability checks performed when using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md).</span></span>

<span data-ttu-id="947d6-108">Если исправление применяется с помощью [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) или [параметра командной строки](command-line-options.md)/p, установщик сравнивает приложения, установленные в настоящее время на компьютере, со списком кодов продуктов, доступных для получения исправления, в свойстве [**Сводка шаблона**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="947d6-108">If a patch is applied using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md), the installer compares the applications currently installed on the computer to the list of product codes eligible to receive the patch in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="947d6-109">При установке свойства [**Patch**](patch.md) в командной строке для установки при первой установке приложения, подходящие для получения исправления, определяются условиями проверки для преобразований, внедренных в пакет исправлений.</span><span class="sxs-lookup"><span data-stu-id="947d6-109">When you set the [**PATCH**](patch.md) property on the command line to install on first installation, the applications eligible to receive the patch is determined by validation conditions on the transforms embedded in the patch package.</span></span> <span data-ttu-id="947d6-110">Рекомендуемым методом для создания пакета исправлений является использование средства создания исправлений, такого как [Msimsp.exe](msimsp-exe.md) и [PATCHWIZ.DLL](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="947d6-110">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and [PATCHWIZ.DLL](patchwiz-dll.md).</span></span> <span data-ttu-id="947d6-111">Условия проверки для преобразований в исправлении берутся из столбца Продуктвалидатефлагс таблицы [таржетимажес](targetimages-table-patchwiz-dll-.md) в файле свойств создания исправления (PCP).</span><span class="sxs-lookup"><span data-stu-id="947d6-111">The validation conditions on transforms in the patch originate from the ProductValidateFlags column in the [TargetImages](targetimages-table-patchwiz-dll-.md) table of the Patch Creation Properties (.pcp) file.</span></span>

<span data-ttu-id="947d6-112">Исправление можно применить при первом запуске приложения с помощью командной строки, другого приложения или сценария.</span><span class="sxs-lookup"><span data-stu-id="947d6-112">The patch can be applied the first time the application is installed by a command line, another application, or script.</span></span>

<span data-ttu-id="947d6-113">Ниже показаны предварительные исправления из командной строки.</span><span class="sxs-lookup"><span data-stu-id="947d6-113">The following shows first-time patching from the command line.</span></span>

<span data-ttu-id="947d6-114">**msiexec/i** *package.msi* **исправление =**_"c: \\ Directory \\ patch. MSP"_</span><span class="sxs-lookup"><span data-stu-id="947d6-114">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp"_</span></span>

<span data-ttu-id="947d6-115">Ниже показаны предварительные исправления из другого приложения.</span><span class="sxs-lookup"><span data-stu-id="947d6-115">The following shows first-time patching from another application.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

<span data-ttu-id="947d6-116">Ниже показаны предварительные исправления из сценария.</span><span class="sxs-lookup"><span data-stu-id="947d6-116">The following shows first-time patching from script.</span></span>


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



<span data-ttu-id="947d6-117">\* \* Установщик Windows 3,0 и более поздних версий: \* \*</span><span class="sxs-lookup"><span data-stu-id="947d6-117">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="947d6-118">Начиная с версии установщик Windows 3,0, при первой установке приложения можно применить несколько исправлений.</span><span class="sxs-lookup"><span data-stu-id="947d6-118">Beginning with Windows Installer version 3.0, multiple patches can be applied when installing an application for the first time.</span></span> <span data-ttu-id="947d6-119">Задайте для свойства [**Patch**](patch.md) разделенный точками с запятой список полных путей исправления.</span><span class="sxs-lookup"><span data-stu-id="947d6-119">Set the [**PATCH**](patch.md) property to a semicolon delimited list of the patches' full paths.</span></span> <span data-ttu-id="947d6-120">Ниже показаны предварительные исправления нескольких исправлений из командной строки.</span><span class="sxs-lookup"><span data-stu-id="947d6-120">The following shows first-time patching of multiple patches from the command line.</span></span>

<span data-ttu-id="947d6-121">**msiexec/i** *package.msi* **исправление =**_"c: \\ Directory \\ patch. MSP; c: \\ Directory \\ Patch2. MSP; c: \\ Directory \\ patch3. MSP"_</span><span class="sxs-lookup"><span data-stu-id="947d6-121">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp;c:\\directory\\patch2.msp;c:\\directory\\patch3.msp"_</span></span>

 

 



