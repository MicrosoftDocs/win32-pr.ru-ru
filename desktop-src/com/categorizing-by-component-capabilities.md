---
title: Категоризация по возможностям компонентов
description: Категории компонентов можно использовать для вывода подмножества всех установленных компонентов.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710049"
---
# <a name="categorizing-by-component-capabilities"></a><span data-ttu-id="c1cba-103">Категоризация по возможностям компонентов</span><span class="sxs-lookup"><span data-stu-id="c1cba-103">Categorizing by Component Capabilities</span></span>

<span data-ttu-id="c1cba-104">Категории компонентов можно использовать для вывода подмножества всех установленных компонентов.</span><span class="sxs-lookup"><span data-stu-id="c1cba-104">Component categories can be used to display a subset of all of the installed components.</span></span> <span data-ttu-id="c1cba-105">Каждая категория компонента идентифицируется по идентификатору GUID, называемому ИДЕНТИФИКАТОРом категории (CATID).</span><span class="sxs-lookup"><span data-stu-id="c1cba-105">Each component category is identified by a GUID, referred to as a Category ID (CATID).</span></span> <span data-ttu-id="c1cba-106">Каждый идентификатор CATID имеет список связанных с ним понятных имен.</span><span class="sxs-lookup"><span data-stu-id="c1cba-106">Each CATID has a list of locale-tagged, human-readable names associated with it.</span></span> <span data-ttu-id="c1cba-107">Список CATID и понятных для человека имен хранится в хорошо известном месте реестра.</span><span class="sxs-lookup"><span data-stu-id="c1cba-107">A listing of the CATIDs and the human-readable names is stored in a well-known location in the registry.</span></span>

<span data-ttu-id="c1cba-108">Например, все компоненты, реализующие функциональность для внедрения OLE-документов, можно классифицировать в категории компонентов.</span><span class="sxs-lookup"><span data-stu-id="c1cba-108">For example, all components that implement the functionality for OLE document embedding can be classified within a component category.</span></span> <span data-ttu-id="c1cba-109">В прошлом эти объекты были бы определены с помощью ключа "inserted" в реестре.</span><span class="sxs-lookup"><span data-stu-id="c1cba-109">In the past, these objects would have been identified by the "Insertable" key in the registry.</span></span> <span data-ttu-id="c1cba-110">Для использования категорий компонентов вместо этого в реестр добавляются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="c1cba-110">To use component categories instead, the following information would be added to the registry:</span></span>

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

<span data-ttu-id="c1cba-111">Каждый класс, реализующий функциональные возможности, соответствующие категории компонента, перечисляет идентификатор категории для этой категории в ключе CLSID в реестре.</span><span class="sxs-lookup"><span data-stu-id="c1cba-111">Each class that implements the functionality corresponding to a component category lists the category ID for that category within the CLSID key in the registry.</span></span> <span data-ttu-id="c1cba-112">Поскольку один компонент может поддерживать широкий спектр функций, компоненты могут принадлежать к нескольким категориям компонентов.</span><span class="sxs-lookup"><span data-stu-id="c1cba-112">Because a single component can support a wide range of functionality, components can belong to multiple component categories.</span></span> <span data-ttu-id="c1cba-113">Например, конкретный элемент управления OLE может поддерживать все функции, необходимые для участия в внедрении документов OLE, привязка данных Microsoft Visual Basic и функциональность Интернета.</span><span class="sxs-lookup"><span data-stu-id="c1cba-113">For example, a particular OLE control might support all of the functionality required to participate as OLE document embedding, Microsoft Visual Basic data binding, and Internet functionality.</span></span> <span data-ttu-id="c1cba-114">Такой элемент управления будет иметь в реестре следующие сведения, хранящиеся в его ключе CLSID:</span><span class="sxs-lookup"><span data-stu-id="c1cba-114">Such a control would have the following information stored in its CLSID key in the registry:</span></span>

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

<span data-ttu-id="c1cba-115">С помощью этих сведений контейнер может перечислить элементы управления, установленные в системе, и отобразить только те элементы управления, которые поддерживают функции, необходимые контейнеру.</span><span class="sxs-lookup"><span data-stu-id="c1cba-115">With this information, a container can enumerate the controls installed on a system and display only those controls that support the functionality required by the container.</span></span> <span data-ttu-id="c1cba-116">Использование категорий компонентов предоставляет способ классификации компонентов по реализованным функциональным возможностям компонента.</span><span class="sxs-lookup"><span data-stu-id="c1cba-116">The use of component categories provides a way to categorize components by the implemented functionality of the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1cba-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c1cba-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1cba-118">Связывание значков с категорией</span><span class="sxs-lookup"><span data-stu-id="c1cba-118">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="c1cba-119">Категоризация по возможностям контейнеров</span><span class="sxs-lookup"><span data-stu-id="c1cba-119">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="c1cba-120">Классы и ассоциации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c1cba-120">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="c1cba-121">Определение категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="c1cba-121">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="c1cba-122">Диспетчер категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="c1cba-122">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




