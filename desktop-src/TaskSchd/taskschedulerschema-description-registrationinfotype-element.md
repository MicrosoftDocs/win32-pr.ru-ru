---
title: Элемент Description (Регистратионинфотипе)
description: Указание описания задачи.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Элемент Description планировщик задач
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801768"
---
# <a name="description-registrationinfotype-element"></a><span data-ttu-id="701ac-104">Элемент Description (Регистратионинфотипе)</span><span class="sxs-lookup"><span data-stu-id="701ac-104">Description (registrationInfoType) Element</span></span>

<span data-ttu-id="701ac-105">Указание описания задачи.</span><span class="sxs-lookup"><span data-stu-id="701ac-105">Specifies the description of the task.</span></span>

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="701ac-106">Элемент **Description** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="701ac-106">The **Description** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="701ac-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="701ac-107">Parent element</span></span>



| <span data-ttu-id="701ac-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="701ac-108">Element</span></span>                                                                           | <span data-ttu-id="701ac-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="701ac-109">Derived from</span></span>                                                                         | <span data-ttu-id="701ac-110">Описание</span><span class="sxs-lookup"><span data-stu-id="701ac-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701ac-111">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="701ac-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="701ac-112">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="701ac-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="701ac-113">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="701ac-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="701ac-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="701ac-114">Remarks</span></span>

<span data-ttu-id="701ac-115">Для разработки сценариев описание задачи указывается с помощью свойства [**регистратионинфо. Description**](registrationinfo-description.md) .</span><span class="sxs-lookup"><span data-stu-id="701ac-115">For scripting development, the description of a task is specified using the [**RegistrationInfo.Description**](registrationinfo-description.md) property.</span></span>

<span data-ttu-id="701ac-116">Для разработки на C++ описание задачи указывается с помощью свойства [**ирегистратионинфо::D Описание**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) .</span><span class="sxs-lookup"><span data-stu-id="701ac-116">For C++ development, the description of a task is specified using the [**IRegistrationInfo::Description**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="701ac-117">Требования</span><span class="sxs-lookup"><span data-stu-id="701ac-117">Requirements</span></span>



| <span data-ttu-id="701ac-118">Требование</span><span class="sxs-lookup"><span data-stu-id="701ac-118">Requirement</span></span> | <span data-ttu-id="701ac-119">Значение</span><span class="sxs-lookup"><span data-stu-id="701ac-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="701ac-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="701ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="701ac-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="701ac-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="701ac-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="701ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="701ac-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="701ac-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="701ac-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="701ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701ac-125">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="701ac-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="701ac-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="701ac-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





