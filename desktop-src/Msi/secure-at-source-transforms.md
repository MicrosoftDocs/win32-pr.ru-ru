---
description: На преобразованиях с защитой по источнику должен находиться источник, расположенный в корне источника пакета.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Преобразования с защитой по источнику
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913660"
---
# <a name="secure-at-source-transforms"></a><span data-ttu-id="8c012-103">Преобразования с защитой по источнику</span><span class="sxs-lookup"><span data-stu-id="8c012-103">Secure-At-Source Transforms</span></span>

<span data-ttu-id="8c012-104">На преобразованиях с защитой по источнику должен находиться источник, расположенный в корне источника пакета.</span><span class="sxs-lookup"><span data-stu-id="8c012-104">Secure-at-source transforms must have a source located at the root of the source for the package.</span></span> <span data-ttu-id="8c012-105">При установке или объявлении пакета установщик сохраняет преобразования в кэше, где в защищенной файловой системе пользователь не имеет доступа на запись.</span><span class="sxs-lookup"><span data-stu-id="8c012-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="8c012-106">Если локальная копия преобразования становится недоступной, установщик выполняет поиск источника для восстановления кэша.</span><span class="sxs-lookup"><span data-stu-id="8c012-106">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="8c012-107">Метод аналогичен поиску в исходном списке для MSI-файла.</span><span class="sxs-lookup"><span data-stu-id="8c012-107">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="8c012-108">Дополнительные сведения см. в разделе [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="8c012-108">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="8c012-109">При удалении продукта любым пользователем все защищенные преобразования для этого продукта удаляются с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c012-109">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="8c012-110">Чтобы применить преобразования с защитой по источнику при установке пакета, установите [политику трансформссекуре](transformssecure-policy.md) или свойство [**трансформссекуре**](transformssecure.md) или сделайте @ первый символ, переданный в список преобразования.</span><span class="sxs-lookup"><span data-stu-id="8c012-110">To apply secure-at-source transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property, or make @ the first character passed in the transform list.</span></span> <span data-ttu-id="8c012-111">Каждое преобразование должно быть обозначается именем файла и должно находиться в корне источника пакета.</span><span class="sxs-lookup"><span data-stu-id="8c012-111">Each transform must be indicated by a file name and must be located at the root of the source for the package.</span></span> <span data-ttu-id="8c012-112">Если какой либо из преобразований не находится в корне источника пакета, установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="8c012-112">If any of the transforms are not located at the root of the package source, the installation fails.</span></span> <span data-ttu-id="8c012-113">Дополнительные сведения см. в разделе [применение преобразований](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="8c012-113">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



