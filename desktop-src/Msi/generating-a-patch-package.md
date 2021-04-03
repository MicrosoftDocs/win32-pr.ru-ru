---
description: Рекомендуемым методом для создания пакета исправлений является использование средства создания исправлений, например Msimsp.exe для вызова Уикреатепатчпаккаже в Patchwiz.dll. Msimsp.exe и PatchWiz.dll предоставляются в пакете SDK для установщик Windows.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Создание пакета исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998809"
---
# <a name="generating-a-patch-package"></a><span data-ttu-id="37b52-104">Создание пакета исправлений</span><span class="sxs-lookup"><span data-stu-id="37b52-104">Generating a Patch Package</span></span>

<span data-ttu-id="37b52-105">Рекомендуемым методом для создания пакета исправлений является использование средства создания исправлений, например [Msimsp.exe](msimsp-exe.md) для вызова [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) в [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="37b52-105">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) to call [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="37b52-106">Msimsp.exe и PatchWiz.dll предоставляются в пакете SDK для установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="37b52-106">Msimsp.exe and PatchWiz.dll are provided in the Windows Installer SDK.</span></span>

<span data-ttu-id="37b52-107">В следующем примере командная строка использует Msimsp.exe и файл PCP, созданный при [создании файла свойств создания исправления](creating-a-patch-creation-properties-file.md) , чтобы создать пример пакета исправлений MNP2000. MSP.</span><span class="sxs-lookup"><span data-stu-id="37b52-107">The following example command line uses Msimsp.exe and the .pcp file created in [Creating a Patch Creation Properties File](creating-a-patch-creation-properties-file.md) to generate the sample patch package MNP2000.msp.</span></span>

<span data-ttu-id="37b52-108">**Msimsp.exe-s C: \\ Примечание \_ установщика \\ Patch \\ MNP2000. PCP-p C: \\ Замечание \_ установщика \\ Patch \\ MNP2000. MSP**</span><span class="sxs-lookup"><span data-stu-id="37b52-108">**Msimsp.exe -s C:\\Note\_Installer\\Patch\\MNP2000.pcp -p C:\\Note\_Installer\\Patch\\MNP2000.msp**</span></span>

<span data-ttu-id="37b52-109">Созданное средство создания исправлений может создать пакет исправлений, вызвав [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="37b52-109">An authored patch creation tool may generate the patch package by calling [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) as follows.</span></span>

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[<span data-ttu-id="37b52-110">Продолжить</span><span class="sxs-lookup"><span data-stu-id="37b52-110">Continue</span></span>](applying-a-patch-package-to-a-local-installation.md)

 

 



