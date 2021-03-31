---
description: Авторы должны выполнить проверку каждого нового или недавно измененного модуля слияния, прежде чем пытаться объединить модуль в базу данных установки в первый раз.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Проверка модулей слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8bbe7f1c1ea32baa39cadd7c729f3a8ca3ac17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154787"
---
# <a name="validating-merge-modules"></a><span data-ttu-id="4ce7d-103">Проверка модулей слияния</span><span class="sxs-lookup"><span data-stu-id="4ce7d-103">Validating Merge Modules</span></span>

<span data-ttu-id="4ce7d-104">Авторы должны выполнить проверку каждого нового или недавно измененного модуля слияния, прежде чем пытаться объединить модуль в базу данных установки в первый раз.</span><span class="sxs-lookup"><span data-stu-id="4ce7d-104">Authors should run validation on every new, or newly modified, merge module before attempting to merge the module into an installation database for the first time.</span></span> <span data-ttu-id="4ce7d-105">Проверка модуля слияния работает так же, как [Проверка пакета](package-validation.md) , но использует другой набор внутренних средств [оценки согласованности](internal-consistency-evaluators-ices.md) (ICEs), характерных для модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="4ce7d-105">Merge module validation works in the same way as [package validation](package-validation.md) but uses a different set of [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) (ICEs) specific to merge modules.</span></span> <span data-ttu-id="4ce7d-106">Дополнительные сведения об этих модулях слияния (ICEs) см. в разделе [Справочник по модулю слияния Ice](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4ce7d-106">For more information about these merge module ICEs, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

<span data-ttu-id="4ce7d-107">Модуль слияния ICEs хранится в файле слияния Module. CUB, Мержемод. cub.</span><span class="sxs-lookup"><span data-stu-id="4ce7d-107">Merge module ICEs are stored in the merge module .cub file, Mergemod.cub.</span></span> <span data-ttu-id="4ce7d-108">При установке средства Orca или msival2 также предоставляются файлы Logo. CUB, Дарице. cub и Мержемод. cub.</span><span class="sxs-lookup"><span data-stu-id="4ce7d-108">The installation of the Orca tool or msival2 also provides the Logo.cub, Darice.cub, and Mergemod.cub files.</span></span>

<span data-ttu-id="4ce7d-109">Дополнительные сведения см. в разделе [Справочник по модулю слияния](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4ce7d-109">For more information, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

 

 



