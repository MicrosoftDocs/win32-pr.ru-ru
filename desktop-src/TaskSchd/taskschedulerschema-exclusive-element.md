---
title: Эксклюзивный элемент
description: Указывает, должна ли планировщик задач запускать задачу во время автоматического обслуживания в монопольном режиме.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- планировщик задач исключающих элементов
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681790"
---
# <a name="exclusive-element"></a><span data-ttu-id="52186-104">Эксклюзивный элемент</span><span class="sxs-lookup"><span data-stu-id="52186-104">Exclusive Element</span></span>

<span data-ttu-id="52186-105">Указывает, должна ли планировщик задач запускать задачу во время автоматического обслуживания в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="52186-105">Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.</span></span>

<span data-ttu-id="52186-106">Исключительные права гарантируется только между другими задачами обслуживания и не предоставляет приоритет выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="52186-106">The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task.</span></span> <span data-ttu-id="52186-107">Если исключительные права не указан, задача запускается параллельно с другими задачами обслуживания.</span><span class="sxs-lookup"><span data-stu-id="52186-107">If exclusivity is not specified, the task is started in parallel with other maintenance tasks.</span></span>

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="52186-108">**Эксклюзивный** элемент определяется сложным типом [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="52186-108">The **Exclusive** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="52186-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="52186-109">Parent element</span></span>



| <span data-ttu-id="52186-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="52186-110">Element</span></span>                                                                                                                          | <span data-ttu-id="52186-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="52186-111">Derived from</span></span>                                                                               | <span data-ttu-id="52186-112">Описание</span><span class="sxs-lookup"><span data-stu-id="52186-112">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52186-113">**Маинтенанцесеттингс (Маинтенанцесеттингстипе)**</span><span class="sxs-lookup"><span data-stu-id="52186-113">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="52186-114">**маинтенанцесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="52186-114">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="52186-115">Задает параметры задачи, которые планировщик задач будет использовать для запуска задачи во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="52186-115">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="52186-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52186-116">Remarks</span></span>

<span data-ttu-id="52186-117">При программировании на C++ этот параметр простоя указывается с помощью свойства [**имаинтенанцесеттингс:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .</span><span class="sxs-lookup"><span data-stu-id="52186-117">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) property.</span></span>

## <a name="examples"></a><span data-ttu-id="52186-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="52186-118">Examples</span></span>

<span data-ttu-id="52186-119">Следующий код XML определяет задачу обслуживания с требованием крайнего срока, равным 15 дням.</span><span class="sxs-lookup"><span data-stu-id="52186-119">The following XML defines maintenance task with deadline requirement set to 15 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="52186-120">Требования</span><span class="sxs-lookup"><span data-stu-id="52186-120">Requirements</span></span>



| <span data-ttu-id="52186-121">Требование</span><span class="sxs-lookup"><span data-stu-id="52186-121">Requirement</span></span> | <span data-ttu-id="52186-122">Значение</span><span class="sxs-lookup"><span data-stu-id="52186-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52186-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52186-123">Minimum supported client</span></span><br/> | <span data-ttu-id="52186-124">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="52186-124">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="52186-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52186-125">Minimum supported server</span></span><br/> | <span data-ttu-id="52186-126">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="52186-126">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52186-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52186-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52186-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="52186-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="52186-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="52186-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





