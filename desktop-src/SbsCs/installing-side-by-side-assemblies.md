---
description: Параллельные сборки можно устанавливать как общие сборки или как закрытые сборки. Дополнительные сведения см. в разделе Установка параллельных сборок в качестве частных сборок и установка параллельных сборок в качестве общих сборок.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Установка параллельных сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497232"
---
# <a name="installing-side-by-side-assemblies"></a><span data-ttu-id="09a0b-104">Установка параллельных сборок</span><span class="sxs-lookup"><span data-stu-id="09a0b-104">Installing Side-by-side Assemblies</span></span>

<span data-ttu-id="09a0b-105">Параллельные сборки можно устанавливать как [Общие сборки](/windows/desktop/Msi/shared-assemblies) или как [закрытые сборки](/windows/desktop/Msi/private-assemblies).</span><span class="sxs-lookup"><span data-stu-id="09a0b-105">You may install side-by-side assemblies as [shared assemblies](/windows/desktop/Msi/shared-assemblies) or as [private assemblies](/windows/desktop/Msi/private-assemblies).</span></span> <span data-ttu-id="09a0b-106">Дополнительные сведения см. в разделе [Установка параллельных сборок в качестве частных сборок](installing-side-by-side-assemblies-as-private-assemblies.md) и [Установка параллельных сборок в качестве общих сборок](installing-side-by-side-assemblies-as-shared-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="09a0b-106">For more information, see [Installing Side-by-Side Assemblies as Private Assemblies](installing-side-by-side-assemblies-as-private-assemblies.md) and [Installing Side-by-side Assemblies as Shared Assemblies](installing-side-by-side-assemblies-as-shared-assemblies.md).</span></span>

<span data-ttu-id="09a0b-107">Обратите внимание на следующее.</span><span class="sxs-lookup"><span data-stu-id="09a0b-107">Note that:</span></span>

-   <span data-ttu-id="09a0b-108">Сборки, установленные в глобальный кэш сборок установкой с использованием [контекста установки](/windows/desktop/Msi/installation-context) «на пользователя», не защищаются с помощью защиты файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="09a0b-108">Assemblies installed to the global assembly cache by an installation using the per-user [installation context](/windows/desktop/Msi/installation-context) are not protected by Windows File Protection.</span></span>
-   <span data-ttu-id="09a0b-109">Сборки, которые устанавливаются в глобальный кэш сборок установкой с использованием [контекста установки](/windows/desktop/Msi/installation-context) для компьютера, защищаются с помощью защиты файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="09a0b-109">Assemblies that are installed to the global assembly cache by an installation using the per-machine [installation context](/windows/desktop/Msi/installation-context) are protected by Windows File Protection.</span></span>

 

 
