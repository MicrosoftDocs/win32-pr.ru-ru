---
title: Стопифгоингонбаттериес (Сеттингстипе), элемент
description: Указывает, что задача будет остановлена при переходе компьютера на питание.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- планировщик задач элемента Стопифгоингонбаттериес
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681844"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a><span data-ttu-id="e573b-104">Стопифгоингонбаттериес (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="e573b-104">StopIfGoingOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="e573b-105">Указывает, что задача будет остановлена при переходе компьютера на питание.</span><span class="sxs-lookup"><span data-stu-id="e573b-105">Specifies that the task will be stopped if the computer is going onto batteries.</span></span>

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="e573b-106">Элемент **стопифгоингонбаттериес** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e573b-106">The **StopIfGoingOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e573b-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e573b-107">Parent element</span></span>



| <span data-ttu-id="e573b-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e573b-108">Element</span></span>                                                           | <span data-ttu-id="e573b-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="e573b-109">Derived from</span></span>                                                         | <span data-ttu-id="e573b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e573b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e573b-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="e573b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e573b-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="e573b-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e573b-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="e573b-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e573b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e573b-114">Remarks</span></span>

<span data-ttu-id="e573b-115">Значение по умолчанию для этого элемента — false.</span><span class="sxs-lookup"><span data-stu-id="e573b-115">The default setting for this element is False.</span></span> <span data-ttu-id="e573b-116">Обратите внимание, что значение по умолчанию изменилось по сравнению с предыдущими версиями планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="e573b-116">Note that the default value has changed from previous versions of Task Scheduler.</span></span>

<span data-ttu-id="e573b-117">Для разработки сценариев этот параметр указывается с помощью свойства [**тасксеттингс. стопифгоингонбаттериес**](tasksettings-stopifgoingonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="e573b-117">For scripting development, this setting is specified using the [**TaskSettings.StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) property.</span></span>

<span data-ttu-id="e573b-118">Для разработки на C++ этот параметр указывается с помощью свойства [**итасксеттингс:: стопифгоингонбаттериес**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="e573b-118">For C++ development, this setting is specified using the [**ITaskSettings::StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e573b-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="e573b-119">Examples</span></span>

<span data-ttu-id="e573b-120">Следующий XML-код определяет элемент Settings, который разрешает жесткое завершение задачи.</span><span class="sxs-lookup"><span data-stu-id="e573b-120">The following XML defines a settings element that allows a hard termination of the task.</span></span>


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e573b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e573b-121">Requirements</span></span>



| <span data-ttu-id="e573b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e573b-122">Requirement</span></span> | <span data-ttu-id="e573b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e573b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e573b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e573b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e573b-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e573b-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e573b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e573b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e573b-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e573b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e573b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e573b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e573b-129">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="e573b-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





