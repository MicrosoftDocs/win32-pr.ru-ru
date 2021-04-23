---
description: Создание объектов временной шкалы
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Создание объектов временной шкалы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662013"
---
# <a name="creating-timeline-objects"></a><span data-ttu-id="bb8b2-103">Создание объектов временной шкалы</span><span class="sxs-lookup"><span data-stu-id="bb8b2-103">Creating Timeline Objects</span></span>

<span data-ttu-id="bb8b2-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="bb8b2-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="bb8b2-105">Пример кода, представленный в этой статье, начинается с пустой временной шкалы, но те же действия применяются, если вы загружаете существующий проект и хотите добавить в него объекты.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-105">The sample code presented in this article starts with an empty timeline, but the same steps apply if you load an existing project and want to add objects to it.</span></span>

<span data-ttu-id="bb8b2-106">Чтобы создать объект любого типа на временной шкале, вызовите метод [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="bb8b2-106">To create any type of object in the timeline, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="bb8b2-107">Например, следующий код создает новую группу:</span><span class="sxs-lookup"><span data-stu-id="bb8b2-107">For example, the following code creates a new group:</span></span>


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



<span data-ttu-id="bb8b2-108">Второй параметр является членом перечисления [**\_ основных \_ типов временной шкалы**](timeline-major-type.md) .</span><span class="sxs-lookup"><span data-stu-id="bb8b2-108">The second parameter is a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumeration.</span></span> <span data-ttu-id="bb8b2-109">Он указывает тип создаваемого объекта временной шкалы, например группу или запись.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-109">It specifies the type of timeline object to create, such as a group or a track.</span></span>

<span data-ttu-id="bb8b2-110">Метод **креатимптиноде** создает объект и возвращает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-110">The **CreateEmptyNode** method creates the object and returns a pointer to the object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="bb8b2-111">Он также увеличивает счетчик ссылок в интерфейсе **иамтимелинеобж** , поэтому при завершении его использования необходимо освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-111">It also increments the reference count on the **IAMTimelineObj** interface, so you must release the interface when you finish using it.</span></span> <span data-ttu-id="bb8b2-112">Не вызывайте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="bb8b2-112">Do not call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="bb8b2-113">Вместо этого всегда используйте **креатимптиноде** для создания объекта Timeline, так как он инициализирует новый объект для использования на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-113">Instead, always use **CreateEmptyNode** to create a timeline object, because it initializes the new object for use in a timeline.</span></span>

<span data-ttu-id="bb8b2-114">Интерфейс [**иамтимелинеобж**](iamtimelineobj.md) является универсальным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-114">The [**IAMTimelineObj**](iamtimelineobj.md) interface is a generic interface.</span></span> <span data-ttu-id="bb8b2-115">Он предоставляет методы, которые являются общими для всех типов объектов временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-115">It provides methods that are common to all types of timeline object.</span></span> <span data-ttu-id="bb8b2-116">Каждый тип объекта также предоставляет другие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-116">Each type of object exposes other interfaces as well.</span></span> <span data-ttu-id="bb8b2-117">Например, группы предоставляют интерфейс [**иамтимелинеграуп**](iamtimelinegroup.md) , а не другие.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-117">For example, groups expose the [**IAMTimelineGroup**](iamtimelinegroup.md) interface, among others.</span></span> <span data-ttu-id="bb8b2-118">Можно получить указатели на другие интерфейсы, вызвав **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-118">You can obtain pointers to the other interfaces by calling **QueryInterface**.</span></span>

<span data-ttu-id="bb8b2-119">После создания объект еще не является частью временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-119">After you create an object, it is not yet a part of the timeline.</span></span> <span data-ttu-id="bb8b2-120">Метод добавления объекта на временную шкалу зависит от типа объекта.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-120">The method to add an object to the timeline depends on the object type.</span></span> <span data-ttu-id="bb8b2-121">В следующем разделе описывается добавление групп, композиций и дорожек на временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="bb8b2-121">The following section describes how to add groups, compositions, and tracks to the timeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb8b2-122">См. также</span><span class="sxs-lookup"><span data-stu-id="bb8b2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb8b2-123">Создание временной шкалы</span><span class="sxs-lookup"><span data-stu-id="bb8b2-123">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
