---
title: Элемент Date (Регистратионинфотипе)
description: Указывает дату и время регистрации задачи.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Элемент Date планировщик задач
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136535"
---
# <a name="date-registrationinfotype-element"></a><span data-ttu-id="528d2-104">Элемент Date (Регистратионинфотипе)</span><span class="sxs-lookup"><span data-stu-id="528d2-104">Date (registrationInfoType) Element</span></span>

<span data-ttu-id="528d2-105">Указывает дату и время регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="528d2-105">Specifies the date and time when the task is registered.</span></span>

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

<span data-ttu-id="528d2-106">Элемент **Date** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="528d2-106">The **Date** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="528d2-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="528d2-107">Parent element</span></span>



| <span data-ttu-id="528d2-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="528d2-108">Element</span></span>                                                                           | <span data-ttu-id="528d2-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="528d2-109">Derived from</span></span>                                                                         | <span data-ttu-id="528d2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="528d2-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="528d2-111">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="528d2-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="528d2-112">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="528d2-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="528d2-113">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="528d2-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="528d2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="528d2-114">Remarks</span></span>

<span data-ttu-id="528d2-115">Для разработки сценариев Дата регистрации задачи указывается с помощью свойства [**регистратионинфо. Date**](registrationinfo-date.md) .</span><span class="sxs-lookup"><span data-stu-id="528d2-115">For scripting development, the registration date of a task is specified using the [**RegistrationInfo.Date**](registrationinfo-date.md) property.</span></span>

<span data-ttu-id="528d2-116">Для разработки на C++ Дата регистрации задачи указывается с помощью свойства [**ирегистратионинфо::D ATE**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .</span><span class="sxs-lookup"><span data-stu-id="528d2-116">For C++ development, the registration date of a task is specified using the [**IRegistrationInfo::Date**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="528d2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="528d2-117">Requirements</span></span>



| <span data-ttu-id="528d2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="528d2-118">Requirement</span></span> | <span data-ttu-id="528d2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="528d2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="528d2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="528d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="528d2-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="528d2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="528d2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="528d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="528d2-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="528d2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="528d2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="528d2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528d2-125">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="528d2-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="528d2-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="528d2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





