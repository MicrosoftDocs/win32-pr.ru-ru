---
title: КПРОПС. CPP
description: В примере компонента поставщика пример реализации кэша свойств можно найти в кпропс. cpp. Поддерживаемые методы перечислены в следующей таблице.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887568"
---
# <a name="cpropscpp"></a><span data-ttu-id="f56c3-104">КПРОПС. CPP</span><span class="sxs-lookup"><span data-stu-id="f56c3-104">CPROPS.CPP</span></span>

<span data-ttu-id="f56c3-105">В примере компонента поставщика пример реализации кэша свойств можно найти в кпропс. cpp.</span><span class="sxs-lookup"><span data-stu-id="f56c3-105">In the example provider component, an example of a property cache implementation can be found in cprops.cpp.</span></span> <span data-ttu-id="f56c3-106">Поддерживаемые методы перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f56c3-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="f56c3-107">Метод</span><span class="sxs-lookup"><span data-stu-id="f56c3-107">Method</span></span>                                           | <span data-ttu-id="f56c3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f56c3-108">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f56c3-109">**Кпропертикаче:: AddProperty**</span><span class="sxs-lookup"><span data-stu-id="f56c3-109">**CPropertyCache::addproperty**</span></span>                  | <span data-ttu-id="f56c3-110">Расширьте кэш свойств, добавив новый.</span><span class="sxs-lookup"><span data-stu-id="f56c3-110">Extend the property cache by adding a new one.</span></span>                                                                      |
| <span data-ttu-id="f56c3-111">**Кпропертикаче:: упдатепроперти**</span><span class="sxs-lookup"><span data-stu-id="f56c3-111">**CPropertyCache::updateproperty**</span></span>               | <span data-ttu-id="f56c3-112">Найдите свойство, освободите его содержимое и используйте вместо него новые значения. Затем пометьте измененный кэш для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f56c3-112">Look up the property, free its contents, and use new values instead; then mark the cache changed for this property.</span></span> |
| <span data-ttu-id="f56c3-113">**Кпропертикаче:: финдпроперти**</span><span class="sxs-lookup"><span data-stu-id="f56c3-113">**CPropertyCache::findproperty**</span></span>                 | <span data-ttu-id="f56c3-114">Поиск этого свойства по имени; Сохраните индекс.</span><span class="sxs-lookup"><span data-stu-id="f56c3-114">Look up this property by name; save its index.</span></span>                                                                      |
| <span data-ttu-id="f56c3-115">**Кпропертикаче:: Property**</span><span class="sxs-lookup"><span data-stu-id="f56c3-115">**CPropertyCache::getproperty**</span></span>                  | <span data-ttu-id="f56c3-116">Найдите свойство в кэше, если доступно, в противном случае **— Call.**</span><span class="sxs-lookup"><span data-stu-id="f56c3-116">Find the property in the cache if available, otherwise call **GetInfo**.</span></span> <span data-ttu-id="f56c3-117">Задайте индекс и скопируйте новые значения.</span><span class="sxs-lookup"><span data-stu-id="f56c3-117">Set the index and copy in the new values.</span></span>  |
| <span data-ttu-id="f56c3-118">**Кпропертикаче::p утпроперти**</span><span class="sxs-lookup"><span data-stu-id="f56c3-118">**CPropertyCache::putproperty**</span></span>                  | <span data-ttu-id="f56c3-119">Найдите свойство.</span><span class="sxs-lookup"><span data-stu-id="f56c3-119">Find the property.</span></span> <span data-ttu-id="f56c3-120">Бесплатная и поставьте новые значения.</span><span class="sxs-lookup"><span data-stu-id="f56c3-120">Free what was there and put in new values.</span></span>                                                       |
| <span data-ttu-id="f56c3-121">**Кпропертикаче:: Кпропертикаче**</span><span class="sxs-lookup"><span data-stu-id="f56c3-121">**CPropertyCache::CPropertyCache**</span></span>               | <span data-ttu-id="f56c3-122">Стандартный конструктор.</span><span class="sxs-lookup"><span data-stu-id="f56c3-122">Standard constructor.</span></span>                                                                                               |
| <span data-ttu-id="f56c3-123">**Кпропертикаче:: ~ Кпропертикаче**</span><span class="sxs-lookup"><span data-stu-id="f56c3-123">**CPropertyCache::~CPropertyCache**</span></span>              | <span data-ttu-id="f56c3-124">Стандартный деструктор.</span><span class="sxs-lookup"><span data-stu-id="f56c3-124">Standard destructor.</span></span>                                                                                                |
| <span data-ttu-id="f56c3-125">**Кпропертикаче:: креатепропертикаче**</span><span class="sxs-lookup"><span data-stu-id="f56c3-125">**CPropertyCache::createpropertycache**</span></span>          | <span data-ttu-id="f56c3-126">Создайте кэш.</span><span class="sxs-lookup"><span data-stu-id="f56c3-126">Create the cache.</span></span>                                                                                                   |
| <span data-ttu-id="f56c3-127">**Кпропертикаче:: унбаунджетпроперти**</span><span class="sxs-lookup"><span data-stu-id="f56c3-127">**CPropertyCache::unboundgetproperty**</span></span>           | <span data-ttu-id="f56c3-128">Найдите свойство в кэше и задайте для него эти значения.</span><span class="sxs-lookup"><span data-stu-id="f56c3-128">Find the property in the cache and set it to these values.</span></span>                                                          |
| <span data-ttu-id="f56c3-129">**Кпропертикаче:: Сампледсмаршаллпропертиес**</span><span class="sxs-lookup"><span data-stu-id="f56c3-129">**CPropertyCache::SampleDSMarshallProperties**</span></span>   | <span data-ttu-id="f56c3-130">Маршалирует данные и значения свойств.</span><span class="sxs-lookup"><span data-stu-id="f56c3-130">Marshal property data and values.</span></span>                                                                                   |
| <span data-ttu-id="f56c3-131">**Кпропертикаче:: маршаллпроперти**</span><span class="sxs-lookup"><span data-stu-id="f56c3-131">**CPropertyCache::marshallproperty**</span></span>             | <span data-ttu-id="f56c3-132">Маршалирует свойство.</span><span class="sxs-lookup"><span data-stu-id="f56c3-132">Marshal a property.</span></span>                                                                                                 |
| <span data-ttu-id="f56c3-133">**Кпропертикаче:: Сампледсунмаршаллпропертиес**</span><span class="sxs-lookup"><span data-stu-id="f56c3-133">**CPropertyCache::SampleDSUnMarshallProperties**</span></span> | <span data-ttu-id="f56c3-134">Распаковать данные и значения свойств.</span><span class="sxs-lookup"><span data-stu-id="f56c3-134">Unmarshal property data and values.</span></span>                                                                                 |
| <span data-ttu-id="f56c3-135">**Кпропертикаче:: унмаршаллпроперти**</span><span class="sxs-lookup"><span data-stu-id="f56c3-135">**CPropertyCache::unmarshallproperty**</span></span>           | <span data-ttu-id="f56c3-136">Распаковать свойство.</span><span class="sxs-lookup"><span data-stu-id="f56c3-136">Unmarshal a property.</span></span>                                                                                               |



 

 

 




