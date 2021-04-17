---
description: Определяет метаданные размещения для реализуемого устройства. Этот элемент используется только для реализаций устройств (узлов).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: Хостметадата, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656697"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="76f7c-104">Хостметадата, элемент</span><span class="sxs-lookup"><span data-stu-id="76f7c-104">hostMetadata element</span></span>

<span data-ttu-id="76f7c-105">Определяет метаданные размещения для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="76f7c-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="76f7c-106">Этот элемент используется только для реализаций устройств (узлов).</span><span class="sxs-lookup"><span data-stu-id="76f7c-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="76f7c-107">Использование</span><span class="sxs-lookup"><span data-stu-id="76f7c-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="76f7c-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="76f7c-108">Attributes</span></span>

<span data-ttu-id="76f7c-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="76f7c-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="76f7c-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76f7c-110">Child elements</span></span>



| <span data-ttu-id="76f7c-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="76f7c-111">Element</span></span>                             | <span data-ttu-id="76f7c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="76f7c-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76f7c-113">**хост**</span><span class="sxs-lookup"><span data-stu-id="76f7c-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="76f7c-114">Определяет элементы ServiceID и [**types**](types.md) для узла службы.</span><span class="sxs-lookup"><span data-stu-id="76f7c-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="76f7c-115">Если не указано явно, WSDAPI не будет предоставлять данные по умолчанию в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="76f7c-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="76f7c-116">**внутрипроцессных**</span><span class="sxs-lookup"><span data-stu-id="76f7c-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="76f7c-117">Определяет элементы [**ServiceID**](serviceid.md) и [**types**](types.md) для служб, предоставляемых этим узлом службы.</span><span class="sxs-lookup"><span data-stu-id="76f7c-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="76f7c-118">Каждая служба, предоставляемая этим узлом службы, должна иметь собственные сведения о [**размещенном**](hosted.md) элементе, чтобы обеспечить правильную публикацию службы в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="76f7c-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="76f7c-119">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="76f7c-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="76f7c-120">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="76f7c-120">Parent elements</span></span>



| <span data-ttu-id="76f7c-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="76f7c-121">Element</span></span>                                                         | <span data-ttu-id="76f7c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="76f7c-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="76f7c-123">**релатионшипметадата**</span><span class="sxs-lookup"><span data-stu-id="76f7c-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="76f7c-124">Описывает размещение и размещение метаданных для устройства.</span><span class="sxs-lookup"><span data-stu-id="76f7c-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="76f7c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76f7c-125">Remarks</span></span>

<span data-ttu-id="76f7c-126">Метаданные размещения отображаются в этом элементе в форме, аналогичной указанной в профиле устройства.</span><span class="sxs-lookup"><span data-stu-id="76f7c-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="76f7c-127">**хостметадата** немного отличается от формата, описанного в профиле устройства, в том, что единственным ссылочным свойством, которое он поддерживает, является идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="76f7c-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="76f7c-128">Элемент [**релатионшипметадатадефинитион**](relationshipmetadatadefinition.md) используется впоследствии для создания константы C, содержащей эти сведения.</span><span class="sxs-lookup"><span data-stu-id="76f7c-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="76f7c-129">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="76f7c-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="76f7c-130">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="76f7c-130">Minimum supported system</span></span><br/> | <span data-ttu-id="76f7c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76f7c-131">Windows Vista</span></span> |
| <span data-ttu-id="76f7c-132">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="76f7c-132">Can be empty</span></span>                        | <span data-ttu-id="76f7c-133">Нет</span><span class="sxs-lookup"><span data-stu-id="76f7c-133">No</span></span>            |



 

 




