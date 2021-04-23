---
description: Интерфейс Икатегори определяет следующие свойства.
ms.assetid: aa9c4dbb-5e33-47b7-ae6c-8d83010e205b
title: Свойства Икатегори
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d01e5b5eac4701ebdff4c79981ee91806a18329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662421"
---
# <a name="icategory-properties"></a><span data-ttu-id="660b0-103">Свойства Икатегори</span><span class="sxs-lookup"><span data-stu-id="660b0-103">ICategory Properties</span></span>

<span data-ttu-id="660b0-104">Интерфейс [**икатегори**](/windows/desktop/api/Wuapi/nn-wuapi-icategory) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="660b0-104">The [**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory) interface defines the following properties.</span></span>



| <span data-ttu-id="660b0-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="660b0-105">Property</span></span>                                     | <span data-ttu-id="660b0-106">Описание</span><span class="sxs-lookup"><span data-stu-id="660b0-106">Description</span></span>                                                                                       |
|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="660b0-107">**CategoryID**</span><span class="sxs-lookup"><span data-stu-id="660b0-107">**CategoryID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_categoryid)   | <span data-ttu-id="660b0-108">Возвращает идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="660b0-108">Gets the identifier of the category.</span></span>                                                              |
| [<span data-ttu-id="660b0-109">**Дети**</span><span class="sxs-lookup"><span data-stu-id="660b0-109">**Children**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_children)       | <span data-ttu-id="660b0-110">Возвращает коллекцию интерфейсов, содержащую дочерние категории этой категории.</span><span class="sxs-lookup"><span data-stu-id="660b0-110">Gets an interface collection that contains the child categories of this category.</span></span>                 |
| [<span data-ttu-id="660b0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="660b0-111">**Description**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_description) | <span data-ttu-id="660b0-112">Возвращает описание категории.</span><span class="sxs-lookup"><span data-stu-id="660b0-112">Gets the description of the category.</span></span>                                                             |
| [<span data-ttu-id="660b0-113">**Образ**</span><span class="sxs-lookup"><span data-stu-id="660b0-113">**Image**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_image)             | <span data-ttu-id="660b0-114">Возвращает интерфейс, содержащий сведения об изображении, связанном с категорией.</span><span class="sxs-lookup"><span data-stu-id="660b0-114">Gets an interface that contains information about the image that is associated with the category.</span></span> |
| [<span data-ttu-id="660b0-115">**Имя**</span><span class="sxs-lookup"><span data-stu-id="660b0-115">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_name)               | <span data-ttu-id="660b0-116">Возвращает локализованное имя категории.</span><span class="sxs-lookup"><span data-stu-id="660b0-116">Gets the localized name of the category.</span></span>                                                          |
| [<span data-ttu-id="660b0-117">**Заказ**</span><span class="sxs-lookup"><span data-stu-id="660b0-117">**Order**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_order)             | <span data-ttu-id="660b0-118">Возвращает рекомендуемый порядок вывода этой категории среди категорий того же уровня.</span><span class="sxs-lookup"><span data-stu-id="660b0-118">Gets the recommended display order of this category among its sibling categories.</span></span>                 |
| [<span data-ttu-id="660b0-119">**Parent**</span><span class="sxs-lookup"><span data-stu-id="660b0-119">**Parent**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_parent)           | <span data-ttu-id="660b0-120">Возвращает интерфейс, описывающий родительскую категорию этой категории.</span><span class="sxs-lookup"><span data-stu-id="660b0-120">Gets an interface that describes the parent category of this category.</span></span>                            |
| [<span data-ttu-id="660b0-121">**Тип**</span><span class="sxs-lookup"><span data-stu-id="660b0-121">**Type**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_type)               | <span data-ttu-id="660b0-122">Возвращает тип категории.</span><span class="sxs-lookup"><span data-stu-id="660b0-122">Gets the type of the category.</span></span>                                                                    |
| [<span data-ttu-id="660b0-123">**Обновления**</span><span class="sxs-lookup"><span data-stu-id="660b0-123">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_updates)         | <span data-ttu-id="660b0-124">Возвращает интерфейс, содержащий коллекцию обновлений, которые непосредственно принадлежат к категории.</span><span class="sxs-lookup"><span data-stu-id="660b0-124">Gets an interface that contains a collection of updates that immediately belong to the category.</span></span>  |



 

 

 



