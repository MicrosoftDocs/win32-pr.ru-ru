---
description: Ресурсы, необходимые для настройки приложения, такие как корпоративные шаблоны, можно развернуть вместе с приложением, включив преобразование в пакет установки приложения.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Использование преобразований для добавления ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673814"
---
# <a name="using-transforms-to-add-resources"></a><span data-ttu-id="71c8b-103">Использование преобразований для добавления ресурсов</span><span class="sxs-lookup"><span data-stu-id="71c8b-103">Using Transforms to Add Resources</span></span>

<span data-ttu-id="71c8b-104">Ресурсы, необходимые для настройки приложения, такие как корпоративные шаблоны, можно развернуть вместе с приложением, включив преобразование в пакет установки приложения.</span><span class="sxs-lookup"><span data-stu-id="71c8b-104">Resources that are needed for the customization of an application, such as corporate templates, can be deployed with the application by including a transform with the application's installation package.</span></span> <span data-ttu-id="71c8b-105">При развертывании ресурсов, таких как файлы, разделы реестра или ярлыки, следует соблюдать следующие правила, используя преобразование.</span><span class="sxs-lookup"><span data-stu-id="71c8b-105">The following rules should be followed when deploying resources, such as files, registry keys, or shortcuts, using a transform.</span></span>

-   <span data-ttu-id="71c8b-106">Преобразование должно добавить один или несколько новых компонентов в базу данных установки, чтобы они содержали дополнительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="71c8b-106">The transform should add one or more new components to the installation database to contain the additional resources.</span></span> <span data-ttu-id="71c8b-107">Преобразование не должно добавлять ресурсы в компонент, который уже существует в установке.</span><span class="sxs-lookup"><span data-stu-id="71c8b-107">The transform should not add resources to a component that already exists in the installation.</span></span>
-   <span data-ttu-id="71c8b-108">Преобразование должно добавить в базу данных установки один или несколько новых компонентов, которые будут содержать эти новые компоненты.</span><span class="sxs-lookup"><span data-stu-id="71c8b-108">The transform should add one or more new features to the installation database to contain these new components.</span></span> <span data-ttu-id="71c8b-109">Эти новые функции не должны быть родителями каких бы то ни было функций, но новые родительские и дочерние функции могут быть добавлены вместе.</span><span class="sxs-lookup"><span data-stu-id="71c8b-109">These new features should not be the parents of any existing features, but new parent and child features may be introduced together.</span></span> <span data-ttu-id="71c8b-110">Новым функциям должны быть присвоены имена, уникальные для всех других преобразований этого продукта.</span><span class="sxs-lookup"><span data-stu-id="71c8b-110">New features should be given names that are unique across all other transforms for this product.</span></span> <span data-ttu-id="71c8b-111">Ни один из двух преобразований не должен добавлять в этот продукт функцию с тем же именем, которая указана в столбце "компонент" [таблицы функций](feature-table.md) и содержит различные компоненты или ресурсы.</span><span class="sxs-lookup"><span data-stu-id="71c8b-111">No two transforms should ever add a feature to this product that has the same name listed in the Feature column of the [Feature table](feature-table.md) and containing different components or resources.</span></span>

 

 



