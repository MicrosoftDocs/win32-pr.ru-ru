---
title: Интерфейс Ирдвтаскплугиннотифисинк
description: Интерфейс Ирдвтаскплугиннотифисинк используется агентом задач для взаимодействия с агентом триггера.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк, описание
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802704"
---
# <a name="irdvtaskpluginnotifysink-interface"></a><span data-ttu-id="5d9b6-105">Интерфейс Ирдвтаскплугиннотифисинк</span><span class="sxs-lookup"><span data-stu-id="5d9b6-105">IRDVTaskPluginNotifySink interface</span></span>

<span data-ttu-id="5d9b6-106">Интерфейс **ирдвтаскплугиннотифисинк** используется агентом задач для взаимодействия с агентом триггера.</span><span class="sxs-lookup"><span data-stu-id="5d9b6-106">The **IRDVTaskPluginNotifySink** interface is used by the task agent to communicate with the trigger agent.</span></span> <span data-ttu-id="5d9b6-107">Указатель на этот интерфейс передается агенту задачи в методе [**ирдвтаскплугин:: Initialize**](irdvtaskplugin-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="5d9b6-107">A pointer to this interface is passed to the task agent in the [**IRDVTaskPlugin::Initialize**](irdvtaskplugin-initialize.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="5d9b6-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5d9b6-108">Members</span></span>

<span data-ttu-id="5d9b6-109">Интерфейс **ирдвтаскплугиннотифисинк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5d9b6-109">The **IRDVTaskPluginNotifySink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d9b6-110">**Ирдвтаскплугиннотифисинк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d9b6-110">**IRDVTaskPluginNotifySink** also has these types of members:</span></span>

-   [<span data-ttu-id="5d9b6-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5d9b6-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d9b6-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5d9b6-112">Methods</span></span>

<span data-ttu-id="5d9b6-113">Интерфейс **ирдвтаскплугиннотифисинк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5d9b6-113">The **IRDVTaskPluginNotifySink** interface has these methods.</span></span>



| <span data-ttu-id="5d9b6-114">Метод</span><span class="sxs-lookup"><span data-stu-id="5d9b6-114">Method</span></span>                                                                  | <span data-ttu-id="5d9b6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5d9b6-115">Description</span></span>                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="5d9b6-116">**DeleteSchedule**</span><span class="sxs-lookup"><span data-stu-id="5d9b6-116">**DeleteSchedule**</span></span>](irdvtaskpluginnotifysink-deleteschedule.md)       | <span data-ttu-id="5d9b6-117">Вызывается агентом задачи для удаления запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="5d9b6-117">Called by the task agent to delete a scheduled task.</span></span><br/>                   |
| [<span data-ttu-id="5d9b6-118">**онтаскстатечанже**</span><span class="sxs-lookup"><span data-stu-id="5d9b6-118">**OnTaskStateChange**</span></span>](irdvtaskpluginnotifysink-ontaskstatechange.md) | <span data-ttu-id="5d9b6-119">Используется для уведомления агента активации о том, что состояние задачи изменилось.</span><span class="sxs-lookup"><span data-stu-id="5d9b6-119">Used to notify the trigger agent that the state of a task has changed.</span></span><br/> |
| [<span data-ttu-id="5d9b6-120">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="5d9b6-120">**OnTerminated**</span></span>](irdvtaskpluginnotifysink-onterminated.md)           | <span data-ttu-id="5d9b6-121">Вызывается агентом задачи для запроса завершения работы агента задачи.</span><span class="sxs-lookup"><span data-stu-id="5d9b6-121">Called by the task agent to request that the task agent be shut down.</span></span><br/>  |
| [<span data-ttu-id="5d9b6-122">**ScheduleTask**</span><span class="sxs-lookup"><span data-stu-id="5d9b6-122">**ScheduleTask**</span></span>](irdvtaskpluginnotifysink-scheduletask.md)           | <span data-ttu-id="5d9b6-123">Вызывается агентом задачи для планирования задачи.</span><span class="sxs-lookup"><span data-stu-id="5d9b6-123">Called by the task agent to schedule a task.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="5d9b6-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d9b6-124">Remarks</span></span>

<span data-ttu-id="5d9b6-125">Хотя этот интерфейс поддерживается в операционных системах, указанных в приведенных ниже требованиях, он будет использоваться только в том случае, если виртуальная машина размещена на Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5d9b6-125">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d9b6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5d9b6-126">Requirements</span></span>



| <span data-ttu-id="5d9b6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5d9b6-127">Requirement</span></span> | <span data-ttu-id="5d9b6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5d9b6-128">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="5d9b6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d9b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5d9b6-130">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="5d9b6-130">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="5d9b6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d9b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5d9b6-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d9b6-132">Windows Server 2008 R2</span></span><br/> |



 

