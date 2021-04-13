---
description: Для обеспечения безопасной преобразования с полными путями необходимо, чтобы источник находился по полному пути, указанному в свойстве TRANSFORMs.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Безопасные преобразования с полными путями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547095"
---
# <a name="secure-full-path-transforms"></a><span data-ttu-id="25761-103">Безопасные преобразования с полными путями</span><span class="sxs-lookup"><span data-stu-id="25761-103">Secure-Full-Path Transforms</span></span>

<span data-ttu-id="25761-104">Для обеспечения безопасной преобразования с полными путями необходимо, чтобы источник находился по полному пути, указанному в свойстве [**TRANSFORMS**](transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="25761-104">Secure-full-path transforms must have a source located at the full path specified in the [**TRANSFORMS**](transforms.md) property.</span></span> <span data-ttu-id="25761-105">При установке или объявлении пакета установщик сохраняет преобразования в кэше, где в защищенной файловой системе пользователь не имеет доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="25761-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="25761-106">Если локальная копия преобразования становится недоступной, она может восстановить только кэш по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="25761-106">If the local copy of the transform becomes unavailable, it may only restore the cache using the specified path.</span></span> <span data-ttu-id="25761-107">При удалении продукта любым пользователем все защищенные преобразования для этого продукта удаляются с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="25761-107">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="25761-108">Чтобы применить преобразования с безопасными путями при установке пакета, задайте [политику трансформссекуре](transformssecure-policy.md) или свойство [**трансформссекуре**](transformssecure.md) или сделайте \| первый символ, передаваемый в список преобразования.</span><span class="sxs-lookup"><span data-stu-id="25761-108">To apply secure-full-paths transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property or make \| the first character passed in the transform list.</span></span> <span data-ttu-id="25761-109">Полные пути к источнику каждого преобразования должны передаваться в строке преобразований.</span><span class="sxs-lookup"><span data-stu-id="25761-109">The full paths to the source of each transform must be passed in the transforms string.</span></span> <span data-ttu-id="25761-110">Если в списке есть относительные пути, установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="25761-110">If any relative paths are in the list, the installation fails.</span></span> <span data-ttu-id="25761-111">Источник преобразования не должен располагаться с источником пакета.</span><span class="sxs-lookup"><span data-stu-id="25761-111">The transform source does not have to be located with the source of the package.</span></span>

 

 



