---
title: Дисалловстартифонбаттериес (Сеттингстипе), элемент
description: Указывает, что задача не будет запущена, если компьютер работает от батарей.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- планировщик задач элемента Дисалловстартифонбаттериес
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803982"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a><span data-ttu-id="5c956-104">Дисалловстартифонбаттериес (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="5c956-104">DisallowStartIfOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="5c956-105">Указывает, что задача не будет запущена, если компьютер работает от батарей.</span><span class="sxs-lookup"><span data-stu-id="5c956-105">Specifies that the task will not be started if the computer is running on batteries.</span></span>

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

<span data-ttu-id="5c956-106">Элемент **дисалловстартифонбаттериес** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5c956-106">The **DisallowStartIfOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5c956-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="5c956-107">Parent element</span></span>



| <span data-ttu-id="5c956-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="5c956-108">Element</span></span>                                                           | <span data-ttu-id="5c956-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="5c956-109">Derived from</span></span>                                                         | <span data-ttu-id="5c956-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5c956-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c956-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="5c956-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="5c956-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="5c956-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="5c956-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="5c956-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c956-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c956-114">Remarks</span></span>

<span data-ttu-id="5c956-115">Значение по умолчанию для этого элемента — true.</span><span class="sxs-lookup"><span data-stu-id="5c956-115">The default setting for this element is True.</span></span>

<span data-ttu-id="5c956-116">Для разработки сценариев эти сведения доступны через свойство [**тасксеттингс. дисалловстартифонбаттериес**](tasksettings-disallowstartifonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="5c956-116">For scripting development, this information is accessed through the [**TaskSettings.DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) property.</span></span>

<span data-ttu-id="5c956-117">Для разработки на C++ эта информация доступна через свойство [**итасксеттингс::D исалловстартифонбаттериес**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="5c956-117">For C++ development, this information is accessed through the [**ITaskSettings::DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5c956-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="5c956-118">Examples</span></span>

<span data-ttu-id="5c956-119">Следующий XML-код определяет элемент Settings, который не разрешает выполнение задачи, если компьютер работает под управлением батарей.</span><span class="sxs-lookup"><span data-stu-id="5c956-119">The following XML defines a settings element that does not allow the task to run if the computer is running on batteries.</span></span>


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="5c956-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5c956-120">Requirements</span></span>



| <span data-ttu-id="5c956-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5c956-121">Requirement</span></span> | <span data-ttu-id="5c956-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5c956-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c956-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c956-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5c956-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c956-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c956-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c956-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5c956-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c956-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c956-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c956-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c956-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="5c956-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





