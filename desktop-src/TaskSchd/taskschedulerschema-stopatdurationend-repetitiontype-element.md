---
title: Стопатдуратионенд (Репетитионтипе), элемент
description: Указывает, что выполняющиеся экземпляры задачи останавливаются в конце шаблона повторения.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- планировщик задач элемента Стопатдуратионенд
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672899"
---
# <a name="stopatdurationend-repetitiontype-element"></a><span data-ttu-id="5d633-104">Стопатдуратионенд (Репетитионтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="5d633-104">StopAtDurationEnd (repetitionType) Element</span></span>

<span data-ttu-id="5d633-105">Указывает, что выполняющийся экземпляр задачи останавливается в конце срока действия шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="5d633-105">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span> <span data-ttu-id="5d633-106">Это применимо только в том случае, если заданы повторения.</span><span class="sxs-lookup"><span data-stu-id="5d633-106">This is applicable only if repetitions are set.</span></span>

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

<span data-ttu-id="5d633-107">Элемент **стопатдуратионенд** определяется сложным типом [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5d633-107">The **StopAtDurationEnd** element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5d633-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="5d633-108">Parent element</span></span>

| <span data-ttu-id="5d633-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="5d633-109">Element</span></span> | <span data-ttu-id="5d633-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="5d633-110">Derived from</span></span> | <span data-ttu-id="5d633-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5d633-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="5d633-112">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="5d633-112">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="5d633-113">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="5d633-113">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="5d633-114">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="5d633-114">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="5d633-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d633-115">Remarks</span></span>

<span data-ttu-id="5d633-116">Для разработки сценариев этот параметр указывается с помощью свойства [**репетитионпаттерн. стопатдуратионенд**](repetitionpattern-stopatdurationend.md) .</span><span class="sxs-lookup"><span data-stu-id="5d633-116">For scripting development, this setting is specified using the [**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) property.</span></span>

<span data-ttu-id="5d633-117">Для разработки на C++ этот параметр указывается с помощью свойства [**ирепетитионпаттерн:: стопатдуратионенд**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .</span><span class="sxs-lookup"><span data-stu-id="5d633-117">For C++ development, this setting is specified using the [**IRepetitionPattern::StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d633-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5d633-118">Requirements</span></span>

| <span data-ttu-id="5d633-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5d633-119">Requirement</span></span> | <span data-ttu-id="5d633-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5d633-120">Value</span></span> |
|-|-|
| <span data-ttu-id="5d633-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d633-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d633-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d633-122">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d633-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d633-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d633-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d633-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="5d633-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d633-125">See also</span></span>

[<span data-ttu-id="5d633-126">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="5d633-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="5d633-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5d633-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
