---
description: URI, представляющий идентификатор службы.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703162"
---
# <a name="serviceid-element"></a><span data-ttu-id="9896a-103">ServiceID, элемент</span><span class="sxs-lookup"><span data-stu-id="9896a-103">ServiceID element</span></span>

<span data-ttu-id="9896a-104">URI, представляющий идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="9896a-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="9896a-105">Использование</span><span class="sxs-lookup"><span data-stu-id="9896a-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="9896a-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9896a-106">Attributes</span></span>

<span data-ttu-id="9896a-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9896a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9896a-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9896a-108">Child elements</span></span>

<span data-ttu-id="9896a-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="9896a-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9896a-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9896a-110">Parent elements</span></span>



| <span data-ttu-id="9896a-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="9896a-111">Element</span></span>                             | <span data-ttu-id="9896a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9896a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9896a-113">**хост**</span><span class="sxs-lookup"><span data-stu-id="9896a-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="9896a-114">Определяет элементы **ServiceID** и [**types**](types.md) для узла службы.</span><span class="sxs-lookup"><span data-stu-id="9896a-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="9896a-115">Если не указано явно, WSDAPI не будет предоставлять данные по умолчанию в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="9896a-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="9896a-116">**внутрипроцессных**</span><span class="sxs-lookup"><span data-stu-id="9896a-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="9896a-117">Определяет элементы **ServiceID** и [**types**](types.md) для служб, предоставляемых этим узлом службы.</span><span class="sxs-lookup"><span data-stu-id="9896a-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="9896a-118">Каждая служба, предоставляемая этим узлом службы, должна иметь собственные сведения о [**размещенном**](hosted.md) элементе, чтобы обеспечить правильную публикацию службы в ответ на запросы метаданных.</span><span class="sxs-lookup"><span data-stu-id="9896a-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9896a-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9896a-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9896a-120">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="9896a-120">Minimum supported system</span></span><br/> | <span data-ttu-id="9896a-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9896a-121">Windows Vista</span></span> |
| <span data-ttu-id="9896a-122">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="9896a-122">Can be empty</span></span>                        | <span data-ttu-id="9896a-123">Да</span><span class="sxs-lookup"><span data-stu-id="9896a-123">Yes</span></span>           |



 

 




