---
title: URI (Регистратионинфотипе), элемент
description: Указывает универсальный код ресурса (URI) задачи.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- планировщик задач элемента URI
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803964"
---
# <a name="uri-registrationinfotype-element"></a><span data-ttu-id="481b4-104">URI (Регистратионинфотипе), элемент</span><span class="sxs-lookup"><span data-stu-id="481b4-104">URI (registrationInfoType) Element</span></span>

<span data-ttu-id="481b4-105">Указывает универсальный код ресурса (URI) задачи.</span><span class="sxs-lookup"><span data-stu-id="481b4-105">Specifies the URI of the task.</span></span> <span data-ttu-id="481b4-106">Этот элемент используется для указания места размещения зарегистрированной задачи в иерархии папок задач.</span><span class="sxs-lookup"><span data-stu-id="481b4-106">This element is used to specify where the registered task is placed in the task folder hierarchy.</span></span>

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

<span data-ttu-id="481b4-107">Элемент **URI** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="481b4-107">The **URI** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="481b4-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="481b4-108">Parent element</span></span>



| <span data-ttu-id="481b4-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="481b4-109">Element</span></span>                                                                           | <span data-ttu-id="481b4-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="481b4-110">Derived from</span></span>                                                                         | <span data-ttu-id="481b4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="481b4-111">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="481b4-112">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="481b4-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="481b4-113">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="481b4-113">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="481b4-114">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="481b4-114">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="481b4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="481b4-115">Remarks</span></span>

<span data-ttu-id="481b4-116">Для разработки сценариев URI задачи указывается с помощью свойства [**регистратионинфо. URI**](registrationinfo-uri.md) .</span><span class="sxs-lookup"><span data-stu-id="481b4-116">For scripting development, the URI of the task is specified using the [**RegistrationInfo.URI**](registrationinfo-uri.md) property.</span></span>

<span data-ttu-id="481b4-117">Для разработки на C++ URI задачи указывается с помощью свойства [**ирегистратионинфо:: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .</span><span class="sxs-lookup"><span data-stu-id="481b4-117">For C++ development, the URI of the task is specified using the [**IRegistrationInfo::URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="481b4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="481b4-118">Requirements</span></span>



| <span data-ttu-id="481b4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="481b4-119">Requirement</span></span> | <span data-ttu-id="481b4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="481b4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="481b4-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="481b4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="481b4-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="481b4-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="481b4-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="481b4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="481b4-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="481b4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="481b4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="481b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="481b4-126">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="481b4-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="481b4-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="481b4-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





