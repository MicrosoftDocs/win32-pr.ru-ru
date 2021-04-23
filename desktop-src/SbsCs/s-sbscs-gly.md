---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: S (изолированные приложения и параллельные сборки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9727db4c2db522b0bbb88eccf89481a61a75d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817080"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="2e6ad-103">S (изолированные приложения и параллельные сборки)</span><span class="sxs-lookup"><span data-stu-id="2e6ad-103">S (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="2e6ad-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) р [. J K](i-sbscs-gly.md) L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="2e6ad-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2e6ad-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**Общая параллельная сборка**</span><span class="sxs-lookup"><span data-stu-id="2e6ad-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**shared side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ad-106">Совместно используемая параллельная сборка доступна для использования несколькими приложениями на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-106">A shared side-by-side assembly is available for use by multiple applications on the computer.</span></span> <span data-ttu-id="2e6ad-107">Он устанавливается в папку WinSxS каталога Windows.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-107">It is installed in the Winsxs folder of the Windows directory.</span></span> <span data-ttu-id="2e6ad-108">Приложения и администраторы могут управлять версией общей сборки для использования путем указания конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-108">Applications and administrators can manage the version of a shared assembly to be used by specifying the application configuration.</span></span> <span data-ttu-id="2e6ad-109">Параллельные сборки всегда сопровождаются файлами манифеста, которые предоставляют сведения о сборке операционной системе.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-109">Side-by-side assemblies are always accompanied by manifest files that provide information about the assembly to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2e6ad-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**Параллельная сборка**</span><span class="sxs-lookup"><span data-stu-id="2e6ad-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ad-111">Параллельная сборка — это сборка Win32, сопровождающая манифестами.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-111">A side-by-side assembly is a Win32 assembly accompanied by manifests.</span></span> <span data-ttu-id="2e6ad-112">Параллельная сборка содержит коллекцию ресурсов (группу библиотек DLL, классов Windows, серверов COM, библиотек типов или интерфейсов), которые всегда предоставляются приложениям вместе.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-112">A side-by-side assembly contains a collection of resources—a group of DLLs, windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span>

</dd> <dt>

<span data-ttu-id="2e6ad-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**Совместное использование сборок параллельно**</span><span class="sxs-lookup"><span data-stu-id="2e6ad-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**side-by-side assembly sharing**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ad-114">Использование параллельных сборок для безопасного совместного использования сборок несколькими приложениями и смещения негативных последствий общего доступа, таких как конфликты DLL.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-114">Use of side-by-side assemblies to safely share assemblies among multiple applications and to offset the negative effects of sharing, such as DLL conflicts.</span></span> <span data-ttu-id="2e6ad-115">Вместо единственной версии сборки, которая предполагает обратную совместимость со всеми приложениями, параллельное совместное использование сборок позволяет нескольким версиям сборки Win32 выполняться одновременно в системе.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-115">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="2e6ad-116">Параллельные сборки всегда сопровождаются файлами манифеста сборки, которые предоставляют сведения о сборке операционной системе.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-116">Side-by-side assemblies are always accompanied by assembly manifest files that provide information about the assembly to the operating system.</span></span> <span data-ttu-id="2e6ad-117">Приложения и администраторы могут управлять параллельным доступом к сборкам после развертывания путем обновления конфигурации приложения на глобальном уровне или отдельно для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="2e6ad-117">Applications and administrators can manage side-by-side assembly sharing after deployment by updating the application configuration on either a global or per-application basis.</span></span>

</dd> </dl>

 

 



