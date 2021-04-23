---
description: Каждая параллельная сборка должна иметь версию.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Версии сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814777"
---
# <a name="assembly-versions"></a><span data-ttu-id="84c07-103">Версии сборки</span><span class="sxs-lookup"><span data-stu-id="84c07-103">Assembly Versions</span></span>

<span data-ttu-id="84c07-104">Каждая параллельная сборка должна иметь версию.</span><span class="sxs-lookup"><span data-stu-id="84c07-104">Every side-by-side assembly must have a version.</span></span> <span data-ttu-id="84c07-105">Каждая версия сборки связана с номером версии, у которого есть четыре части, разделенные точками: *основной. дополнительный. сборка. Редакция*.</span><span class="sxs-lookup"><span data-stu-id="84c07-105">Each assembly version is associated with a version number having four parts separated by periods: *major.minor.build.revision*.</span></span> <span data-ttu-id="84c07-106">Если в сборку вносятся изменения, что делает ее несовместимой с существующими версиями, необходимо изменить *основную* или *дополнительную* части номера версии.</span><span class="sxs-lookup"><span data-stu-id="84c07-106">If a change is made to an assembly making it incompatible with existing versions, the *major* or *minor* parts of the version number must be changed.</span></span> <span data-ttu-id="84c07-107">Номер версии, который изменяется только в компонентах *сборки* или *редакции* , указывает на обратную совместимость сборки с предыдущими версиями.</span><span class="sxs-lookup"><span data-stu-id="84c07-107">A version number that changes only in the *build* or *revision* parts indicates that the assembly is backward compatible with prior versions.</span></span>

<span data-ttu-id="84c07-108">Версия должна быть указана в элементах " **assemblyIdentity** " [манифестов](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="84c07-108">The version must be specified in **assemblyIdentity** elements of [manifests](manifests.md).</span></span> <span data-ttu-id="84c07-109">Используйте формат версии из четырех частей: оближешь. nnnnn. ууо. ппппп.</span><span class="sxs-lookup"><span data-stu-id="84c07-109">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="84c07-110">Каждая из частей, разделенных точками, может быть 0-65535 включительно.</span><span class="sxs-lookup"><span data-stu-id="84c07-110">Each of the parts separated by periods can be 0-65535 inclusive.</span></span>

 

 



