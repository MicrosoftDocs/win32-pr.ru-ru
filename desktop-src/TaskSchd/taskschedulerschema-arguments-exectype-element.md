---
title: Элемент arguments (Ексектипе)
description: Задает аргументы, связанные с операцией командной строки.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Элемент arguments планировщик задач
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534580"
---
# <a name="arguments-exectype-element"></a><span data-ttu-id="32f43-104">Элемент arguments (Ексектипе)</span><span class="sxs-lookup"><span data-stu-id="32f43-104">Arguments (execType) Element</span></span>

<span data-ttu-id="32f43-105">Задает аргументы, связанные с операцией командной строки.</span><span class="sxs-lookup"><span data-stu-id="32f43-105">Specifies the arguments associated with the command-line operation.</span></span>

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

<span data-ttu-id="32f43-106">Элемент **arguments** определяется сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="32f43-106">The **Arguments** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="32f43-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="32f43-107">Parent element</span></span>



| <span data-ttu-id="32f43-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="32f43-108">Element</span></span>                                                      | <span data-ttu-id="32f43-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="32f43-109">Derived from</span></span>                                                 | <span data-ttu-id="32f43-110">Описание</span><span class="sxs-lookup"><span data-stu-id="32f43-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="32f43-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="32f43-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="32f43-112">**ексектипе**</span><span class="sxs-lookup"><span data-stu-id="32f43-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="32f43-113">Указывает действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="32f43-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="32f43-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32f43-114">Remarks</span></span>

<span data-ttu-id="32f43-115">Сведения о разработке на языке C++ см. в описании [**свойства arguments объекта иексекактион**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="32f43-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="32f43-116">Сведения о разработке скриптов см. в разделе [**ексекактион. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="32f43-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="32f43-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="32f43-117">Examples</span></span>

<span data-ttu-id="32f43-118">Полный пример XML-кода для задачи, использующей исполняемое действие, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="32f43-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32f43-119">Требования</span><span class="sxs-lookup"><span data-stu-id="32f43-119">Requirements</span></span>



| <span data-ttu-id="32f43-120">Требование</span><span class="sxs-lookup"><span data-stu-id="32f43-120">Requirement</span></span> | <span data-ttu-id="32f43-121">Значение</span><span class="sxs-lookup"><span data-stu-id="32f43-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32f43-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32f43-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32f43-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32f43-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32f43-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32f43-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32f43-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32f43-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32f43-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32f43-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f43-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="32f43-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





