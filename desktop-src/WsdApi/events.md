---
description: Указывает, включаются ли в создаваемые функции связанные события.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: элемент Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263912"
---
# <a name="events-element"></a><span data-ttu-id="76a57-103">элемент Events</span><span class="sxs-lookup"><span data-stu-id="76a57-103">events element</span></span>

<span data-ttu-id="76a57-104">Указывает, включаются ли в создаваемые функции связанные события.</span><span class="sxs-lookup"><span data-stu-id="76a57-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="76a57-105">Использование</span><span class="sxs-lookup"><span data-stu-id="76a57-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="76a57-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="76a57-106">Attributes</span></span>

<span data-ttu-id="76a57-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="76a57-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="76a57-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76a57-108">Child elements</span></span>

<span data-ttu-id="76a57-109">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="76a57-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="76a57-110">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="76a57-110">Parent elements</span></span>



| <span data-ttu-id="76a57-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="76a57-111">Element</span></span>                                                                         | <span data-ttu-id="76a57-112">Описание</span><span class="sxs-lookup"><span data-stu-id="76a57-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76a57-113">**функтиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="76a57-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="76a57-114">Создает объявления реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="76a57-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="76a57-115">**идлфунктиондекларатионс**</span><span class="sxs-lookup"><span data-stu-id="76a57-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="76a57-116">Создает объявления IDL для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="76a57-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="76a57-117">**проксифунктионимплементатионс**</span><span class="sxs-lookup"><span data-stu-id="76a57-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="76a57-118">Создает реализации для функций-посредников для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="76a57-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="76a57-119">**стубдекларатионс**</span><span class="sxs-lookup"><span data-stu-id="76a57-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="76a57-120">Создает объявления для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="76a57-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="76a57-121">**стубдефинитионс**</span><span class="sxs-lookup"><span data-stu-id="76a57-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="76a57-122">Создает реализации для функций-заглушек для операций с типом порта.</span><span class="sxs-lookup"><span data-stu-id="76a57-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="76a57-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76a57-123">Remarks</span></span>

<span data-ttu-id="76a57-124">Возможные значения: 1 (события включены) и 0 (по умолчанию, события исключены).</span><span class="sxs-lookup"><span data-stu-id="76a57-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="76a57-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="76a57-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="76a57-126">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="76a57-126">Minimum supported system</span></span><br/> | <span data-ttu-id="76a57-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76a57-127">Windows Vista</span></span> |
| <span data-ttu-id="76a57-128">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="76a57-128">Can be empty</span></span>                        | <span data-ttu-id="76a57-129">Да</span><span class="sxs-lookup"><span data-stu-id="76a57-129">Yes</span></span>           |



 

 




