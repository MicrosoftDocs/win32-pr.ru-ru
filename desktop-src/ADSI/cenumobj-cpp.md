---
title: ЦЕНУМОБЖ. CPP
description: В примере компонента поставщика перечисление объекта-контейнера использует подпрограммы из ценумобж. cpp, перечисленные в следующей таблице.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793795"
---
# <a name="cenumobjcpp"></a><span data-ttu-id="076da-103">ЦЕНУМОБЖ. CPP</span><span class="sxs-lookup"><span data-stu-id="076da-103">CENUMOBJ.CPP</span></span>

<span data-ttu-id="076da-104">В примере компонента поставщика перечисление объекта-контейнера использует подпрограммы из ценумобж. cpp, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="076da-104">In the example provider component, the enumeration of a container object uses the routines, from cenumobj.cpp, listed in the following table.</span></span>



| <span data-ttu-id="076da-105">Метод</span><span class="sxs-lookup"><span data-stu-id="076da-105">Method</span></span>                                                 | <span data-ttu-id="076da-106">Описание</span><span class="sxs-lookup"><span data-stu-id="076da-106">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076da-107">**Ксампледсженобжектенум:: Create**</span><span class="sxs-lookup"><span data-stu-id="076da-107">**CSampleDSGenObjectEnum::Create**</span></span>                     | <span data-ttu-id="076da-108">Создайте объект, чтобы включить перечисление универсальных объектов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="076da-108">Create an object to enable enumeration of generic Active Directory objects.</span></span>                                                                                           |
| <span data-ttu-id="076da-109">**Ксампледсженобжектенум:: Ксампледсженобжектенум**</span><span class="sxs-lookup"><span data-stu-id="076da-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span></span>     | <span data-ttu-id="076da-110">Инициализация.</span><span class="sxs-lookup"><span data-stu-id="076da-110">Initialization.</span></span>                                                                                                                                                       |
| <span data-ttu-id="076da-111">**Ксампледсженобжектенум:: Енумженерикобжектс**</span><span class="sxs-lookup"><span data-stu-id="076da-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="076da-112">Управление получением объектов.</span><span class="sxs-lookup"><span data-stu-id="076da-112">Manage retrieval of objects.</span></span>                                                                                                                                          |
| <span data-ttu-id="076da-113">**Ксампледсженобжектенум:: Фетчобжектс**</span><span class="sxs-lookup"><span data-stu-id="076da-113">**CSampleDSGenObjectEnum::FetchObjects**</span></span>               | <span data-ttu-id="076da-114">Получение набора указателей [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , соответствующих фильтру.</span><span class="sxs-lookup"><span data-stu-id="076da-114">Retrieve the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers that match the filter.</span></span>                                                             |
| <span data-ttu-id="076da-115">**Ксампледсженобжектенум:: Фетчнекстобжект**</span><span class="sxs-lookup"><span data-stu-id="076da-115">**CSampleDSGenObjectEnum::FetchNextObject**</span></span>            | <span data-ttu-id="076da-116">Получение объекта и совпадение с фильтром.</span><span class="sxs-lookup"><span data-stu-id="076da-116">Retrieve an object and match against the filter.</span></span> <span data-ttu-id="076da-117">Если он соответствует, заключите его в универсальный объект и возвратите указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="076da-117">If it matches, wrap it in generic object and return a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |
| <span data-ttu-id="076da-118">**Ксампледсженобжектенум:: Енумженерикобжектс**</span><span class="sxs-lookup"><span data-stu-id="076da-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="076da-119">Управление получением объектов.</span><span class="sxs-lookup"><span data-stu-id="076da-119">Manage retrieving the objects.</span></span>                                                                                                                                        |
| <span data-ttu-id="076da-120">**Ксампледсженобжектенум:: Next**</span><span class="sxs-lookup"><span data-stu-id="076da-120">**CSampleDSGenObjectEnum::Next**</span></span>                       | <span data-ttu-id="076da-121">Извлечение указанного числа элементов из указанного объекта перечисления.</span><span class="sxs-lookup"><span data-stu-id="076da-121">Retrieve the specified number of elements from the enumeration object indicated.</span></span>                                                                                      |
| <span data-ttu-id="076da-122">**Ксампледсженобжектенум:: Исвалиддсфилтер**</span><span class="sxs-lookup"><span data-stu-id="076da-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span></span>            | <span data-ttu-id="076da-123">Убедитесь, что класс объектов соответствует одному в списке фильтров.</span><span class="sxs-lookup"><span data-stu-id="076da-123">Verify that object class matches one in the filter list.</span></span>                                                                                                              |
| <span data-ttu-id="076da-124">**Ксампледсженобжектенум:: Буилддсфилтераррай**</span><span class="sxs-lookup"><span data-stu-id="076da-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span></span>         | <span data-ttu-id="076da-125">Управление массивом фильтров.</span><span class="sxs-lookup"><span data-stu-id="076da-125">Manage the filter array.</span></span>                                                                                                                                              |
| <span data-ttu-id="076da-126">**Ксампледсженобжектенум:: Креатеандаппендфилтерентри**</span><span class="sxs-lookup"><span data-stu-id="076da-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span></span> | <span data-ttu-id="076da-127">Добавьте новый класс объекта в фильтр и установите фильтр как смежный.</span><span class="sxs-lookup"><span data-stu-id="076da-127">Add a new object class to the filter and set the filter as contiguous.</span></span>                                                                                                |
| <span data-ttu-id="076da-128">**фрифилтерлист**</span><span class="sxs-lookup"><span data-stu-id="076da-128">**FreeFilterList**</span></span>                                     | <span data-ttu-id="076da-129">Освободите фильтр.</span><span class="sxs-lookup"><span data-stu-id="076da-129">Free the filter.</span></span>                                                                                                                                                      |



 

 

 