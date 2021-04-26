---
description: URI, представляющий идентификатор службы.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995111"
---
# <a name="serviceid-element"></a><span data-ttu-id="bca42-103">ServiceID, элемент</span><span class="sxs-lookup"><span data-stu-id="bca42-103">ServiceID element</span></span>

<span data-ttu-id="bca42-104">URI, представляющий идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="bca42-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="bca42-105">Использование</span><span class="sxs-lookup"><span data-stu-id="bca42-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="bca42-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bca42-106">Attributes</span></span>

<span data-ttu-id="bca42-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="bca42-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bca42-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bca42-108">Child elements</span></span>

<span data-ttu-id="bca42-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="bca42-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="bca42-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bca42-110">Parent elements</span></span>



| <span data-ttu-id="bca42-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="bca42-111">Element</span></span>                             | <span data-ttu-id="bca42-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bca42-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bca42-113">**хост**</span><span class="sxs-lookup"><span data-stu-id="bca42-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="bca42-114">Определяет элементы **ServiceID** и [**types**](types.md) для узла службы.</span><span class="sxs-lookup"><span data-stu-id="bca42-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="bca42-115">Если не указано явно, WSDAPI не будет предоставлять данные по умолчанию в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="bca42-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="bca42-116">**внутрипроцессных**</span><span class="sxs-lookup"><span data-stu-id="bca42-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="bca42-117">Определяет элементы **ServiceID** и [**types**](types.md) для служб, предоставляемых этим узлом службы.</span><span class="sxs-lookup"><span data-stu-id="bca42-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="bca42-118">Каждая служба, предоставляемая этим узлом службы, должна иметь собственные сведения о [**размещенном**](hosted.md) элементе, чтобы обеспечить правильную публикацию службы в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="bca42-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="bca42-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bca42-119">Element information</span></span>



| <span data-ttu-id="bca42-120">Метка</span><span class="sxs-lookup"><span data-stu-id="bca42-120">Label</span></span> | <span data-ttu-id="bca42-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bca42-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="bca42-122">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="bca42-122">Minimum supported system</span></span><br/> | <span data-ttu-id="bca42-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bca42-123">Windows Vista</span></span> |
| <span data-ttu-id="bca42-124">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="bca42-124">Can be empty</span></span>                        | <span data-ttu-id="bca42-125">Да</span><span class="sxs-lookup"><span data-stu-id="bca42-125">Yes</span></span>           |



 

 




