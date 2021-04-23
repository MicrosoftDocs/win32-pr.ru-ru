---
title: Дисалловстартонремотеаппсессион (Сеттингстипе), элемент
description: Указывает, что задача не будет запущена, если она запускается в удаленном сеансе, интегрированном локально.
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- планировщик задач элемента Дисалловстартонремотеаппсессион
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681851"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a><span data-ttu-id="c3ed8-104">Дисалловстартонремотеаппсессион (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="c3ed8-104">DisallowStartOnRemoteAppSession (settingsType) Element</span></span>

<span data-ttu-id="c3ed8-105">Указывает, что задача не будет запущена, если она запускается в удаленном сеансе, интегрированном локально.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-105">Specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span>

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="c3ed8-106">Элемент **дисалловстартонремотеаппсессион** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c3ed8-106">The **DisallowStartOnRemoteAppSession** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c3ed8-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c3ed8-107">Parent element</span></span>



| <span data-ttu-id="c3ed8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="c3ed8-108">Element</span></span>                                                           | <span data-ttu-id="c3ed8-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c3ed8-109">Derived from</span></span>                                                         | <span data-ttu-id="c3ed8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c3ed8-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3ed8-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="c3ed8-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c3ed8-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="c3ed8-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c3ed8-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c3ed8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3ed8-114">Remarks</span></span>

<span data-ttu-id="c3ed8-115">Значение по умолчанию для этого элемента — false.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-115">The default setting for this element is False.</span></span>

<span data-ttu-id="c3ed8-116">Для разработки на C++ эта информация доступна через свойство [**ITaskSettings2::D исалловстартонремотеаппсессион**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .</span><span class="sxs-lookup"><span data-stu-id="c3ed8-116">For C++ development, this information is accessed through the [**ITaskSettings2::DisallowStartOnRemoteAppSession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c3ed8-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="c3ed8-117">Examples</span></span>

<span data-ttu-id="c3ed8-118">Следующий XML-код определяет элемент Settings, который не разрешает запуск задачи, если задача запускается в сеансе на границе.</span><span class="sxs-lookup"><span data-stu-id="c3ed8-118">The following XML defines a settings element that does not allow the task to start if the task is triggered to run in a RAIL session.</span></span>


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="c3ed8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c3ed8-119">Requirements</span></span>



| <span data-ttu-id="c3ed8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c3ed8-120">Requirement</span></span> | <span data-ttu-id="c3ed8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ed8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c3ed8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3ed8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ed8-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c3ed8-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c3ed8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3ed8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ed8-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3ed8-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3ed8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3ed8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ed8-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="c3ed8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





