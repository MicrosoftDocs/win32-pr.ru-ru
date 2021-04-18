---
title: Алловхардтерминате (Сеттингстипе), элемент
description: Указывает, что задачу можно завершить с помощью Терминатепроцесс.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Элемент Алловхардтерминате (Сеттингстипе) планировщик задач
- планировщик задач элемента Алловхардтерминате
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681815"
---
# <a name="allowhardterminate-settingstype-element"></a><span data-ttu-id="34045-105">Алловхардтерминате (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="34045-105">AllowHardTerminate (settingsType) Element</span></span>

<span data-ttu-id="34045-106">Указывает, что задачу можно завершить с помощью Терминатепроцесс.</span><span class="sxs-lookup"><span data-stu-id="34045-106">Specifies that the task may be terminated using TerminateProcess.</span></span>

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="34045-107">Элемент **алловхардтерминате** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="34045-107">The **AllowHardTerminate** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="34045-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="34045-108">Parent element</span></span>



| <span data-ttu-id="34045-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="34045-109">Element</span></span>                                                           | <span data-ttu-id="34045-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="34045-110">Derived from</span></span>                                                 | <span data-ttu-id="34045-111">Описание</span><span class="sxs-lookup"><span data-stu-id="34045-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="34045-112">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="34045-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="34045-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="34045-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="34045-114">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="34045-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="34045-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34045-115">Remarks</span></span>

<span data-ttu-id="34045-116">Сведения о разработке на C++ см. в описании [**Свойства алловхардтерминате объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span><span class="sxs-lookup"><span data-stu-id="34045-116">For C++ development, see the [**AllowHardTerminate property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span></span>

<span data-ttu-id="34045-117">Сведения о разработке сценариев см. в разделе [**тасксеттингс. алловхардтерминате**](tasksettings-allowhardterminate.md).</span><span class="sxs-lookup"><span data-stu-id="34045-117">For script development, see [**TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).</span></span>

## <a name="examples"></a><span data-ttu-id="34045-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="34045-118">Examples</span></span>

<span data-ttu-id="34045-119">Полный пример XML-кода для задачи, которая допускает жесткое завершение работы, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="34045-119">For a complete example of the XML for a task that allows hard termination, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34045-120">Требования</span><span class="sxs-lookup"><span data-stu-id="34045-120">Requirements</span></span>



| <span data-ttu-id="34045-121">Требование</span><span class="sxs-lookup"><span data-stu-id="34045-121">Requirement</span></span> | <span data-ttu-id="34045-122">Значение</span><span class="sxs-lookup"><span data-stu-id="34045-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="34045-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34045-123">Minimum supported client</span></span><br/> | <span data-ttu-id="34045-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34045-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="34045-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34045-125">Minimum supported server</span></span><br/> | <span data-ttu-id="34045-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34045-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34045-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34045-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34045-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="34045-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





