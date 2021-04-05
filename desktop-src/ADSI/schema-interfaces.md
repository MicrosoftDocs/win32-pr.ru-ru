---
title: Интерфейсы схемы
description: Интерфейсы схемы
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- интерфейсы схемы ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986093"
---
# <a name="schema-interfaces"></a><span data-ttu-id="a71ce-104">Интерфейсы схемы</span><span class="sxs-lookup"><span data-stu-id="a71ce-104">Schema Interfaces</span></span>

<span data-ttu-id="a71ce-105">Контейнер схемы содержит набор определений схемы, присоединенных к части дерева пространства имен поставщика.</span><span class="sxs-lookup"><span data-stu-id="a71ce-105">The schema container contains a set of schema definitions that are attached to part of the namespace tree of the provider.</span></span> <span data-ttu-id="a71ce-106">Как правило, каждый экземпляр пространства имен имеет собственную схему.</span><span class="sxs-lookup"><span data-stu-id="a71ce-106">Typically, each instance of a namespace has its own schema.</span></span> <span data-ttu-id="a71ce-107">Например, на следующем рисунке поставщик примера ADSI определяет контейнер схемы в каждом из корневых узлов «Сиэтл» и «Торонто».</span><span class="sxs-lookup"><span data-stu-id="a71ce-107">For example, in the following figure, the ADSI example provider defines a schema container in each of the root nodes "Seattle" and "Toronto".</span></span>

![Включение схемы](images/schemacont.png)

<span data-ttu-id="a71ce-109">Чтобы создать реализацию ADSI для поставщика, необходимо предоставить объекты управления схемой, отражающие базовое пространство имен поставщика и поддерживающее интерфейсы схемы ADSI.</span><span class="sxs-lookup"><span data-stu-id="a71ce-109">To create an ADSI implementation for a provider, you need to supply schema management objects that reflect the underlying namespace of the provider and which support ADSI schema interfaces.</span></span> <span data-ttu-id="a71ce-110">Ниже приведен список интерфейсов схемы ADSI, содержащихся в контейнере схемы.</span><span class="sxs-lookup"><span data-stu-id="a71ce-110">The following is a list of the ADSI schema interfaces, which are contained in the schema container.</span></span>

-   <span data-ttu-id="a71ce-111">[**Иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) представляет классы службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="a71ce-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) represents directory service classes.</span></span>
-   <span data-ttu-id="a71ce-112">[**Иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty) представляет свойства службы каталогов, имеющие одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="a71ce-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) represents directory service properties that have single or multiple values.</span></span>
-   <span data-ttu-id="a71ce-113">[**Иадссинтакс**](/windows/desktop/api/Iads/nn-iads-iadssyntax) представляет один тип Variant.</span><span class="sxs-lookup"><span data-stu-id="a71ce-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) represents the single VARIANT type.</span></span>

<span data-ttu-id="a71ce-114">Интерфейсы, определенные интерфейсом ADSI, могут поддерживать определенные свойства и синтаксис для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a71ce-114">Interfaces defined by ADSI can support specific properties and syntaxes for your provider.</span></span> <span data-ttu-id="a71ce-115">Поставщики могут расширить определение ADSI с помощью методов, которые создают свойства и обращаются к ним, например, можно использовать методы интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) , такие как [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) [**, WHERE**](/windows/desktop/api/Iads/nf-iads-iads-put) и [**путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span><span class="sxs-lookup"><span data-stu-id="a71ce-115">Providers can choose to extend an ADSI definition by using the methods that create and access properties, for example, you can use the methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span></span> <span data-ttu-id="a71ce-116">Поставщики также могут поддерживать дополнительные свойства через дополнительные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a71ce-116">Providers can also support additional properties through additional interfaces.</span></span> <span data-ttu-id="a71ce-117">Полный список интерфейсов ADSI см. в разделе [интерфейсы ADSI](adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a71ce-117">For a complete list of ADSI interfaces, see [ADSI Interfaces](adsi-interfaces.md).</span></span>

<span data-ttu-id="a71ce-118">Компонент поставщика ADSI с сложным пространством имен может содержать несколько схем в экземпляре пространства имен, каждый из которых находится в другой части дерева.</span><span class="sxs-lookup"><span data-stu-id="a71ce-118">An ADSI provider component with a complex namespace might allow multiple schemas to exist in a namespace instance, each at a different part of the tree.</span></span> <span data-ttu-id="a71ce-119">Однако свойство [**iAds:: schema**](iads-property-methods.md) объекта всегда имеет имя, соответствующее определению схемы.</span><span class="sxs-lookup"><span data-stu-id="a71ce-119">The [**IADs::Schema**](iads-property-methods.md) property of an object, however, always names its own schema definition.</span></span>

 

 




