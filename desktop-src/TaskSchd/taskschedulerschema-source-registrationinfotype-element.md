---
title: Элемент Source (Регистратионинфотипе)
description: Указывает, откуда поступила задача. Например, из компонента, службы, приложения или пользователя.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- планировщик задач исходного элемента
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414969"
---
# <a name="source-registrationinfotype-element"></a><span data-ttu-id="22537-105">Элемент Source (Регистратионинфотипе)</span><span class="sxs-lookup"><span data-stu-id="22537-105">Source (registrationInfoType) Element</span></span>

<span data-ttu-id="22537-106">Указывает, откуда поступила задача.</span><span class="sxs-lookup"><span data-stu-id="22537-106">Specifies where the task originated from.</span></span> <span data-ttu-id="22537-107">Например, из компонента, службы, приложения или пользователя.</span><span class="sxs-lookup"><span data-stu-id="22537-107">For example, from a component, a service, an application, or a user.</span></span>

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="22537-108">Элемент **Source** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="22537-108">The **Source** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="22537-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="22537-109">Parent element</span></span>



| <span data-ttu-id="22537-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="22537-110">Element</span></span>                                                                           | <span data-ttu-id="22537-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="22537-111">Derived from</span></span>                                                                         | <span data-ttu-id="22537-112">Описание</span><span class="sxs-lookup"><span data-stu-id="22537-112">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22537-113">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="22537-113">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="22537-114">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="22537-114">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="22537-115">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="22537-115">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="22537-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22537-116">Remarks</span></span>

<span data-ttu-id="22537-117">Для разработки сценариев источник задачи указывается с помощью свойства [**регистратионинфо. Source**](registrationinfo-source.md) .</span><span class="sxs-lookup"><span data-stu-id="22537-117">For scripting development, the source of a task is specified using the [**RegistrationInfo.Source**](registrationinfo-source.md) property.</span></span>

<span data-ttu-id="22537-118">Для разработки на C++ источник задачи указывается с помощью свойства [**ирегистратионинфо:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .</span><span class="sxs-lookup"><span data-stu-id="22537-118">For C++ development, the source of a task is specified using the [**IRegistrationInfo::Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="22537-119">Требования</span><span class="sxs-lookup"><span data-stu-id="22537-119">Requirements</span></span>



| <span data-ttu-id="22537-120">Требование</span><span class="sxs-lookup"><span data-stu-id="22537-120">Requirement</span></span> | <span data-ttu-id="22537-121">Значение</span><span class="sxs-lookup"><span data-stu-id="22537-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22537-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22537-122">Minimum supported client</span></span><br/> | <span data-ttu-id="22537-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22537-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22537-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22537-124">Minimum supported server</span></span><br/> | <span data-ttu-id="22537-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22537-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22537-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22537-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22537-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="22537-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="22537-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="22537-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





