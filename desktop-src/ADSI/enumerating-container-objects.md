---
title: Перечисление объектов контейнера
description: По соглашению все элементы в перечислении в ADSI должны иметь один и тот же тип данных автоматизации. Например, перечисление не должно возвращать некоторые элементы в качестве варианта типа VT \_ I4 и других в качестве варианта типа VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654137"
---
# <a name="enumerating-container-objects"></a><span data-ttu-id="a7751-104">Перечисление объектов контейнера</span><span class="sxs-lookup"><span data-stu-id="a7751-104">Enumerating Container Objects</span></span>

<span data-ttu-id="a7751-105">По соглашению все элементы в перечислении в ADSI должны иметь один и тот же тип данных автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a7751-105">By convention, all items in an enumeration in ADSI must be of the same Automation data type.</span></span> <span data-ttu-id="a7751-106">Например, перечисление не должно возвращать некоторые элементы в качестве **варианта** типа **VT \_ I4** и других в качестве **варианта** типа **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="a7751-106">For example, an enumeration should not return some items as a **VARIANT** of type **VT\_I4** and others as a **VARIANT** of type **VT\_BSTR**.</span></span>

<span data-ttu-id="a7751-107">Чтобы перечислить список элементов, поддерживаемых объектом, клиент запрашивает создание объекта перечисления для указанного типа информации.</span><span class="sxs-lookup"><span data-stu-id="a7751-107">To enumerate a list of items that an object maintains, a client requests the creation of an enumeration object for the specific type of information being listed.</span></span> <span data-ttu-id="a7751-108">В ADSI клиент может перечислить объекты в объектах пространства имен, универсальных объектах контейнера, объектах коллекции, объектах элементов или объектах схемы.</span><span class="sxs-lookup"><span data-stu-id="a7751-108">In ADSI, the client may list the objects in namespace objects, generic container objects, collection objects, member objects, or schema objects.</span></span> <span data-ttu-id="a7751-109">ADSI предоставляет фильтр, который можно задать и изменить для ограничения совпадений в любом перечислении, несмотря на то, что свойство [**иадсконтаинер. Filter**](iadscontainer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="a7751-109">ADSI provides a filter that can be set and modified to limit the matches in any enumeration though the [**IADsContainer.Filter**](iadscontainer-property-methods.md) property.</span></span> <span data-ttu-id="a7751-110">Примеры реализаций объектов перечислителя можно найти в примере кода компонента поставщика для следующих объектов контейнера ADs.</span><span class="sxs-lookup"><span data-stu-id="a7751-110">Examples of implementations of enumerator objects can be found in the example provider component code for the following ADs container objects.</span></span>



| <span data-ttu-id="a7751-111">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="a7751-111">Object type</span></span>         | <span data-ttu-id="a7751-112">code</span><span class="sxs-lookup"><span data-stu-id="a7751-112">code</span></span>         |
|---------------------|--------------|
| <span data-ttu-id="a7751-113">Универсальный контейнер</span><span class="sxs-lookup"><span data-stu-id="a7751-113">Generic Container</span></span>   | <span data-ttu-id="a7751-114">ценумобж. cpp</span><span class="sxs-lookup"><span data-stu-id="a7751-114">cenumobj.cpp</span></span> |
| <span data-ttu-id="a7751-115">Контейнер пространства имен</span><span class="sxs-lookup"><span data-stu-id="a7751-115">Namespace Container</span></span> | <span data-ttu-id="a7751-116">ценумнс. cpp</span><span class="sxs-lookup"><span data-stu-id="a7751-116">cenumns.cpp</span></span>  |
| <span data-ttu-id="a7751-117">Контейнер схемы</span><span class="sxs-lookup"><span data-stu-id="a7751-117">Schema Container</span></span>    | <span data-ttu-id="a7751-118">ценумсч. cpp</span><span class="sxs-lookup"><span data-stu-id="a7751-118">cenumsch.cpp</span></span> |



 

<span data-ttu-id="a7751-119">Сведения на стороне клиента см. в разделе [коллекции и группы](collections-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a7751-119">For client-side information, see [Collections and Groups](collections-and-groups.md).</span></span>

 

 




