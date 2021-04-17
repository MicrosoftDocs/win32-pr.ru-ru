---
title: Включенный (Сеттингстипе) элемент
description: Указывает, что задача включена. Задачу можно выполнить, только если этот параметр имеет значение true.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Включенный элемент планировщик задач
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672848"
---
# <a name="enabled-settingstype-element"></a><span data-ttu-id="20176-105">Включенный (Сеттингстипе) элемент</span><span class="sxs-lookup"><span data-stu-id="20176-105">Enabled (settingsType) Element</span></span>

<span data-ttu-id="20176-106">Указывает, что задача включена.</span><span class="sxs-lookup"><span data-stu-id="20176-106">Specifies that the task is enabled.</span></span> <span data-ttu-id="20176-107">Задачу можно выполнить, только если этот параметр имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="20176-107">The task can be performed only when this setting is True.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

<span data-ttu-id="20176-108">Элемент **Enabled** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="20176-108">The **Enabled** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="20176-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="20176-109">Parent element</span></span>



| <span data-ttu-id="20176-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="20176-110">Element</span></span>                                                           | <span data-ttu-id="20176-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="20176-111">Derived from</span></span>                                                         | <span data-ttu-id="20176-112">Описание</span><span class="sxs-lookup"><span data-stu-id="20176-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="20176-113">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="20176-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="20176-114">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="20176-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="20176-115">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="20176-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="20176-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20176-116">Remarks</span></span>

<span data-ttu-id="20176-117">Сведения о разработке на языке C++ см. в разделе [**Enabled Property объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span><span class="sxs-lookup"><span data-stu-id="20176-117">For C++ development, see [**Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span></span>

<span data-ttu-id="20176-118">Сведения о разработке сценариев см. в разделе [**тасксеттингс. Enabled**](tasksettings-enabled.md).</span><span class="sxs-lookup"><span data-stu-id="20176-118">For script development, see [**TaskSettings.Enabled**](tasksettings-enabled.md).</span></span>

## <a name="examples"></a><span data-ttu-id="20176-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="20176-119">Examples</span></span>

<span data-ttu-id="20176-120">Полный пример XML-кода для включенной задачи см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="20176-120">For a complete example of the XML for a task that is enabled, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20176-121">Требования</span><span class="sxs-lookup"><span data-stu-id="20176-121">Requirements</span></span>



| <span data-ttu-id="20176-122">Требование</span><span class="sxs-lookup"><span data-stu-id="20176-122">Requirement</span></span> | <span data-ttu-id="20176-123">Значение</span><span class="sxs-lookup"><span data-stu-id="20176-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20176-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20176-124">Minimum supported client</span></span><br/> | <span data-ttu-id="20176-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20176-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="20176-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20176-126">Minimum supported server</span></span><br/> | <span data-ttu-id="20176-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20176-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





