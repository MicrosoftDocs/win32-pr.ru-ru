---
title: Классификация компонентов
description: Классификация компонентов
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888852"
---
# <a name="classifying-components"></a><span data-ttu-id="6ce34-103">Классификация компонентов</span><span class="sxs-lookup"><span data-stu-id="6ce34-103">Classifying Components</span></span>

<span data-ttu-id="6ce34-104">В то время как клиент может просматривать список идентификаторов CLSID в реестре и выбирать используемый компонент, Загрузка каждого компонента в реестре и запрос его поддерживаемых интерфейсов занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="6ce34-104">While a client is able to browse through the list of CLSIDs in the registry and select a component to use, loading each component in the registry and querying it for its supported interfaces is very time-consuming.</span></span> <span data-ttu-id="6ce34-105">Чтобы определить, поддерживает ли компонент интерфейсы, необходимые перед созданием экземпляра компонента, был разработан метод классификации компонентов по категориям.</span><span class="sxs-lookup"><span data-stu-id="6ce34-105">To determine whether a component supports the interfaces required before creating an instance of the component, a method to classify components into categories was developed.</span></span>

<span data-ttu-id="6ce34-106">Категория компонента — это набор интерфейсов, которым был назначен GUID с именем CATID.</span><span class="sxs-lookup"><span data-stu-id="6ce34-106">A component category is a set of interfaces that have been assigned a GUID named CATID.</span></span> <span data-ttu-id="6ce34-107">Компоненты, реализующие все интерфейсы в категории компонента, регистрируются как члены этой категории компонента.</span><span class="sxs-lookup"><span data-stu-id="6ce34-107">Components that implement all of the interfaces in a component category register themselves as members of that component category.</span></span> <span data-ttu-id="6ce34-108">Затем в реестре можно выбрать компоненты, принадлежащие к определенной категории компонентов.</span><span class="sxs-lookup"><span data-stu-id="6ce34-108">Components that belong to a certain component category can then be selected from the registry.</span></span> <span data-ttu-id="6ce34-109">Зарегистрировавши себя как член категории компонента, компонент гарантирует, что он поддерживает все интерфейсы членов в категории Component.</span><span class="sxs-lookup"><span data-stu-id="6ce34-109">By registering itself as a member of a component category, the component is guaranteeing that it supports all of the member interfaces in the component category.</span></span>

<span data-ttu-id="6ce34-110">Компонент может быть членом нескольких категорий.</span><span class="sxs-lookup"><span data-stu-id="6ce34-110">A component can be a member of many categories.</span></span> <span data-ttu-id="6ce34-111">Он не ограничен вспомогательными интерфейсами в категории компонента.</span><span class="sxs-lookup"><span data-stu-id="6ce34-111">It is not limited to supporting interfaces in a component category.</span></span> <span data-ttu-id="6ce34-112">Он может поддерживать любой интерфейс, помимо тех, которые находятся в категории компонента.</span><span class="sxs-lookup"><span data-stu-id="6ce34-112">It can support any interface, in addition to those in a component category.</span></span>

<span data-ttu-id="6ce34-113">В отличие от стандартной регистрации компонентов, в которой разработчики должны написать код, который вручную регистрирует объекты, категории компонентов автоматизируют большую часть этой работы.</span><span class="sxs-lookup"><span data-stu-id="6ce34-113">In contrast to the standard registration of components, in which developers must write code that manually registers objects, component categories automates much of this work.</span></span> <span data-ttu-id="6ce34-114">Шесть методов интерфейса [**икатрегистер**](/windows/desktop/api/ComCat/nn-comcat-icatregister) определяют категории компонентов и регистрируют объекты, реализующие или необходимые для них.</span><span class="sxs-lookup"><span data-stu-id="6ce34-114">The six methods of the [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) interface define component categories and register objects that implement or require them.</span></span> <span data-ttu-id="6ce34-115">Объект [диспетчера категорий компонентов](the-component-categories-manager.md) реализует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6ce34-115">The [Component Categories Manager](the-component-categories-manager.md) object implements this interface.</span></span> <span data-ttu-id="6ce34-116">Дополнительные сведения об использовании категорий компонентов см. в разделе **икатрегистер** и [**икатинформатион**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) .</span><span class="sxs-lookup"><span data-stu-id="6ce34-116">See **ICatRegister** and [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) for additional information on using component categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ce34-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6ce34-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce34-118">Регистрация приложений COM</span><span class="sxs-lookup"><span data-stu-id="6ce34-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




