---
title: Определение категорий компонентов
description: Определение категорий компонентов
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259094"
---
# <a name="defining-component-categories"></a><span data-ttu-id="d8c04-103">Определение категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="d8c04-103">Defining Component Categories</span></span>

<span data-ttu-id="d8c04-104">Автор определения категории компонента создает уникальный идентификатор GUID (CATID), который публикуется вместе с определением.</span><span class="sxs-lookup"><span data-stu-id="d8c04-104">The author of a component category definition creates a unique GUID (the CATID) that is published along with the definition.</span></span> <span data-ttu-id="d8c04-105">Другие стороны узнают определение этого типа и могут использовать его Поддерживаемые классы соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="d8c04-105">Other parties know the definition of this type and can make use of its supported classes accordingly.</span></span> <span data-ttu-id="d8c04-106">Как и сигнатура метода интерфейса, семантика категории не должна изменяться после установки.</span><span class="sxs-lookup"><span data-stu-id="d8c04-106">Like the method signature of an interface, a category's semantics should not be modified after being installed.</span></span> <span data-ttu-id="d8c04-107">Лучше поддерживать обратную совместимость категории, вводя новый идентификатор категории с измененной семантикой.</span><span class="sxs-lookup"><span data-stu-id="d8c04-107">It is better to maintain backward compatibility of the category by introducing a new category identifier with revised semantics.</span></span>

<span data-ttu-id="d8c04-108">Поскольку идентификаторы интерфейса (IID) и идентификаторы категорий компонентов (CATID) существуют в разных пространствах имен, кажется, что можно использовать один и тот же идентификатор GUID как для IID, так и для идентификатора CATID.</span><span class="sxs-lookup"><span data-stu-id="d8c04-108">Because interface identifiers (IID) and component category identifiers (CATID) exist in different namespaces, it seems as if it would be possible to use the same GUID for both an IID and a CATID.</span></span> <span data-ttu-id="d8c04-109">Однако, так как идентификаторов IID часто используются для идентификатора CLSID прокси-сервера интерфейса/заглушки, существует вероятность конфликта.</span><span class="sxs-lookup"><span data-stu-id="d8c04-109">However, since IIDs are often used for the CLSID of the interface's proxy/stub server, there is the potential for conflict.</span></span> <span data-ttu-id="d8c04-110">Поэтому не используйте один и тот же идентификатор GUID для IID и CATID.</span><span class="sxs-lookup"><span data-stu-id="d8c04-110">Therefore, do not use the same GUID for an IID and CATID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8c04-111">См. также</span><span class="sxs-lookup"><span data-stu-id="d8c04-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8c04-112">Связывание значков с категорией</span><span class="sxs-lookup"><span data-stu-id="d8c04-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="d8c04-113">Категоризация по возможностям компонентов</span><span class="sxs-lookup"><span data-stu-id="d8c04-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="d8c04-114">Категоризация по возможностям контейнеров</span><span class="sxs-lookup"><span data-stu-id="d8c04-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="d8c04-115">Классы и ассоциации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d8c04-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="d8c04-116">Диспетчер категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="d8c04-116">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




