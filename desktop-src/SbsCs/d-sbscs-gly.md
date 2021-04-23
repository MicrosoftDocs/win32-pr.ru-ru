---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3A4C5579-7543-4E0B-921D-BED42C2583D9
title: D (изолированные приложения и параллельные сборки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c8912f24478f79be8aa00c963dc27cb46ec756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080914"
---
# <a name="d-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="e63aa-103">D (изолированные приложения и параллельные сборки)</span><span class="sxs-lookup"><span data-stu-id="e63aa-103">D (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="e63aa-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) р [. J K](i-sbscs-gly.md) L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="e63aa-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e63aa-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF — контекст assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="e63aa-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-context assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="e63aa-106">Вложенный элемент **assemblyIdentity** , определяющий параллельную сборку, описываемую манифестом.</span><span class="sxs-lookup"><span data-stu-id="e63aa-106">An **assemblyIdentity** subelement defining the side-by-side assembly described by the manifest.</span></span> <span data-ttu-id="e63aa-107">Вложенный элемент **assemblyIdentity** в DEF всегда является первым подэлементом элемента **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="e63aa-107">A DEF-context **assemblyIdentity** subelement is always the first subelement of an **assembly** element.</span></span>

</dd> <dt>

<span data-ttu-id="e63aa-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**Конфликт версий DLL**</span><span class="sxs-lookup"><span data-stu-id="e63aa-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL versioning conflict**</span></span>
</dt> <dd>

<span data-ttu-id="e63aa-109">Проблема совместимости.</span><span class="sxs-lookup"><span data-stu-id="e63aa-109">Compatibility problem.</span></span> <span data-ttu-id="e63aa-110">Проблемы совместного использования сборок возникают, когда приложение устанавливает версию общей сборки, которая не обратно совместима с ранее установленной версией.</span><span class="sxs-lookup"><span data-stu-id="e63aa-110">Assembly sharing problems occur when an application installs a version of a shared assembly that is not backward compatible with the previously installed version.</span></span> <span data-ttu-id="e63aa-111">Решение о конфликтах версий библиотек DLL заключается в использовании параллельного общего доступа к сборкам и изолированных приложений.</span><span class="sxs-lookup"><span data-stu-id="e63aa-111">A solution to DLL versioning conflicts is to use side-by-side assembly sharing and isolated applications.</span></span> <span data-ttu-id="e63aa-112">При совместном использовании параллельных сборок несколько версий одной и той же сборки Windows могут выполняться одновременно.</span><span class="sxs-lookup"><span data-stu-id="e63aa-112">With side-by-side assembly sharing, multiple versions of the same Windows assembly can run simultaneously.</span></span> <span data-ttu-id="e63aa-113">Разработчики могут выбрать, какую параллельную сборку использовать.</span><span class="sxs-lookup"><span data-stu-id="e63aa-113">Developers can choose which side-by-side assembly to use.</span></span>

</dd> </dl>

 

 



