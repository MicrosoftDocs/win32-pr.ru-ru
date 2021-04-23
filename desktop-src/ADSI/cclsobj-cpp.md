---
title: ККЛСОБЖ. CPP
description: В примере компонента поставщика функции для объекта класса схемы содержатся в кклсобж. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- ксампледскласс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654147"
---
# <a name="cclsobjcpp"></a><span data-ttu-id="48aa2-104">ККЛСОБЖ. CPP</span><span class="sxs-lookup"><span data-stu-id="48aa2-104">CCLSOBJ.CPP</span></span>

<span data-ttu-id="48aa2-105">В примере компонента поставщика функции для объекта класса схемы содержатся в кклсобж. cpp.</span><span class="sxs-lookup"><span data-stu-id="48aa2-105">In the example provider component, the functions for the schema class object are contained in cclsobj.cpp.</span></span>

<span data-ttu-id="48aa2-106">Класс **ксампледскласс** определен в этом файле.</span><span class="sxs-lookup"><span data-stu-id="48aa2-106">The **CSampleDSClass** class is defined in this file.</span></span> <span data-ttu-id="48aa2-107">**Ксампледскласс** определяется методами и свойствами, перечисленными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="48aa2-107">**CSampleDSClass** is defined with methods and properties listed in the following table.</span></span>



| <span data-ttu-id="48aa2-108">Метод</span><span class="sxs-lookup"><span data-stu-id="48aa2-108">Method</span></span>                      | <span data-ttu-id="48aa2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="48aa2-109">Description</span></span>                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48aa2-110">**ксампледскласс**</span><span class="sxs-lookup"><span data-stu-id="48aa2-110">**CSampleDSClass**</span></span>          | <span data-ttu-id="48aa2-111">Стандартный конструктор.</span><span class="sxs-lookup"><span data-stu-id="48aa2-111">Standard constructor.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="48aa2-112">**~ Ксампледскласс**</span><span class="sxs-lookup"><span data-stu-id="48aa2-112">**~CSampleDSClass**</span></span>         | <span data-ttu-id="48aa2-113">Стандартный деструктор.</span><span class="sxs-lookup"><span data-stu-id="48aa2-113">Standard destructor.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="48aa2-114">**креатекласс**</span><span class="sxs-lookup"><span data-stu-id="48aa2-114">**CreateClass**</span></span>             | <span data-ttu-id="48aa2-115">Создайте объект класса схемы ADs.</span><span class="sxs-lookup"><span data-stu-id="48aa2-115">Create an ADs schema class object.</span></span> <span data-ttu-id="48aa2-116">Определение атрибутов уточняющих запросов путем вызова **сампледсжетклассдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="48aa2-116">Lookup attribute definitions by calling **SampleDSGetClassDefinition**.</span></span>                                                                                                 |
| <span data-ttu-id="48aa2-117">**креатекласс**</span><span class="sxs-lookup"><span data-stu-id="48aa2-117">**CreateClass**</span></span>             | <span data-ttu-id="48aa2-118">Создайте объект класса схемы с учетом определений атрибутов, задав известные атрибуты, такие как перечисленные в [**иадскласс:: мандаторяттрибутес**](iadsclass-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="48aa2-118">Create a schema class object, given the attribute definitions, setting known attributes, such as those listed in [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md).</span></span>                     |
| <span data-ttu-id="48aa2-119">**аллокатеклассобжект**</span><span class="sxs-lookup"><span data-stu-id="48aa2-119">**AllocateClassObject**</span></span>     | <span data-ttu-id="48aa2-120">Создайте объект класса схемы и загрузите его данные типа.</span><span class="sxs-lookup"><span data-stu-id="48aa2-120">Create a schema class object and load its type data.</span></span>                                                                                                                                                       |
| <span data-ttu-id="48aa2-121">**QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="48aa2-121">**QueryInterface**</span></span>          | <span data-ttu-id="48aa2-122">Возвращает запрошенный указатель интерфейса, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="48aa2-122">Return the requested interface pointer, if available.</span></span>                                                                                                                                                      |
| <span data-ttu-id="48aa2-123">Стандартные методы IADs.</span><span class="sxs-lookup"><span data-stu-id="48aa2-123">Standard IADs methods.</span></span>      | <span data-ttu-id="48aa2-124">Стандартные методы интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) , входящие в этот файл.</span><span class="sxs-lookup"><span data-stu-id="48aa2-124">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface methods included in this file.</span></span>                                                                                                                                     |
| <span data-ttu-id="48aa2-125">Стандартные методы Иадскласс.</span><span class="sxs-lookup"><span data-stu-id="48aa2-125">Standard IADsClass methods.</span></span> | <span data-ttu-id="48aa2-126">Стандартные методы интерфейса [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) , входящие в этот файл.</span><span class="sxs-lookup"><span data-stu-id="48aa2-126">Standard [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface methods included in this file.</span></span>                                                                                                                           |
| <span data-ttu-id="48aa2-127">**креатепропертилист**</span><span class="sxs-lookup"><span data-stu-id="48aa2-127">**CreatePropertyList**</span></span>      | <span data-ttu-id="48aa2-128">Создайте список свойств, связанных с этим классом схемы, вызвав **креатепропертентри**.</span><span class="sxs-lookup"><span data-stu-id="48aa2-128">Create a list of properties associated with this schema class by calling **CreatePropertyEntry**.</span></span>                                                                                                          |
| <span data-ttu-id="48aa2-129">**креатепропертентри**</span><span class="sxs-lookup"><span data-stu-id="48aa2-129">**CreatePropertyEntry**</span></span>     | <span data-ttu-id="48aa2-130">Создайте один объект Property в этом классе схемы.</span><span class="sxs-lookup"><span data-stu-id="48aa2-130">Create one property object in this schema class.</span></span>                                                                                                                                                           |
| <span data-ttu-id="48aa2-131">**фрипропертентри**</span><span class="sxs-lookup"><span data-stu-id="48aa2-131">**FreePropertyEntry**</span></span>       | <span data-ttu-id="48aa2-132">Освободите запись, созданную в **креатепропертентри**.</span><span class="sxs-lookup"><span data-stu-id="48aa2-132">Free the entry made in **CreatePropertyEntry**.</span></span>                                                                                                                                                            |
| <span data-ttu-id="48aa2-133">**макевариантфромпроплист**</span><span class="sxs-lookup"><span data-stu-id="48aa2-133">**MakeVariantFromPropList**</span></span> | <span data-ttu-id="48aa2-134">Создайте массив вариантов из списка свойств, созданного с помощью **креатепропертилист**.</span><span class="sxs-lookup"><span data-stu-id="48aa2-134">Create an array of VARIANTS from the property list created by **CreatePropertyList**.</span></span> <span data-ttu-id="48aa2-135">Может использоваться в реализации [**иадскласс:: мандаторяттрибутес**](iadsclass-property-methods.md) и т. д.</span><span class="sxs-lookup"><span data-stu-id="48aa2-135">Can be used in the implementation of [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md) and so on.</span></span> |



 

 

 




