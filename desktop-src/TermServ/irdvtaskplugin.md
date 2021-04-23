---
title: Интерфейс Ирдвтаскплугин
description: Интерфейс Ирдвтаскплугин реализуется агентом задачи обновления виртуальной машины, что позволяет агенту задач управлять обновлениями системы для виртуальной машины.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Ирдвтаскплугин
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугин, описание
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989340"
---
# <a name="irdvtaskplugin-interface"></a><span data-ttu-id="83562-105">Интерфейс Ирдвтаскплугин</span><span class="sxs-lookup"><span data-stu-id="83562-105">IRDVTaskPlugin interface</span></span>

<span data-ttu-id="83562-106">Интерфейс **ирдвтаскплугин** реализуется *агентом задачи* обновления виртуальной машины, что позволяет агенту задач управлять обновлениями системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="83562-106">The **IRDVTaskPlugin** interface is implemented by a virtual machine update *task agent* to allow the task agent to manage system updates for a virtual machine.</span></span> <span data-ttu-id="83562-107">Этот интерфейс используется *агентом триггера*, который реализуется хост-системой.</span><span class="sxs-lookup"><span data-stu-id="83562-107">This interface is used by the *trigger agent*, which is implemented by the host system.</span></span>

## <a name="members"></a><span data-ttu-id="83562-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="83562-108">Members</span></span>

<span data-ttu-id="83562-109">Интерфейс **ирдвтаскплугин** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="83562-109">The **IRDVTaskPlugin** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="83562-110">**Ирдвтаскплугин** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="83562-110">**IRDVTaskPlugin** also has these types of members:</span></span>

-   [<span data-ttu-id="83562-111">Методы</span><span class="sxs-lookup"><span data-stu-id="83562-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="83562-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="83562-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="83562-113">Методы</span><span class="sxs-lookup"><span data-stu-id="83562-113">Methods</span></span>

<span data-ttu-id="83562-114">Интерфейс **ирдвтаскплугин** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="83562-114">The **IRDVTaskPlugin** interface has these methods.</span></span>



| <span data-ttu-id="83562-115">Метод</span><span class="sxs-lookup"><span data-stu-id="83562-115">Method</span></span>                                          | <span data-ttu-id="83562-116">Описание</span><span class="sxs-lookup"><span data-stu-id="83562-116">Description</span></span>                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="83562-117">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="83562-117">**Initialize**</span></span>](irdvtaskplugin-initialize.md) | <span data-ttu-id="83562-118">Вызывается для инициализации агента задачи.</span><span class="sxs-lookup"><span data-stu-id="83562-118">Called to initialize the task agent.</span></span><br/>                    |
| [<span data-ttu-id="83562-119">**StartTask**</span><span class="sxs-lookup"><span data-stu-id="83562-119">**StartTask**</span></span>](irdvtaskplugin-starttask.md)   | <span data-ttu-id="83562-120">Вызывается для запуска задачи обновления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="83562-120">Called to start the update task on the virtual machine.</span></span><br/> |
| [<span data-ttu-id="83562-121">**Завершение**</span><span class="sxs-lookup"><span data-stu-id="83562-121">**Terminate**</span></span>](irdvtaskplugin-terminate.md)   | <span data-ttu-id="83562-122">Вызывается при завершении работы агента задачи.</span><span class="sxs-lookup"><span data-stu-id="83562-122">Called when the task agent is being shut down.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="83562-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="83562-123">Properties</span></span>

<span data-ttu-id="83562-124">Интерфейс **ирдвтаскплугин** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="83562-124">The **IRDVTaskPlugin** interface has these properties.</span></span>



| <span data-ttu-id="83562-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="83562-125">Property</span></span>                                                   | <span data-ttu-id="83562-126">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="83562-126">Access type</span></span>          | <span data-ttu-id="83562-127">Описание</span><span class="sxs-lookup"><span data-stu-id="83562-127">Description</span></span>                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [<span data-ttu-id="83562-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="83562-128">**PluginName**</span></span>](irdvtaskplugin-pluginname.md)<br/> | <span data-ttu-id="83562-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="83562-129">Read-only</span></span><br/> | <span data-ttu-id="83562-130">Содержит отображаемое имя агента задач.</span><span class="sxs-lookup"><span data-stu-id="83562-130">Contains the display name of the task agent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83562-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83562-131">Remarks</span></span>

<span data-ttu-id="83562-132">Агент задачи выполняется на виртуальной машине, когда для этой виртуальной машины запланировано обновление системы.</span><span class="sxs-lookup"><span data-stu-id="83562-132">The task agent is run on the virtual machine when that virtual machine is scheduled for a system update.</span></span> <span data-ttu-id="83562-133">Агент задач обновляет виртуальную машину при вызове метода [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="83562-133">The task agent updates the virtual machine when the [**StartTask**](irdvtaskplugin-starttask.md) method is called.</span></span>

<span data-ttu-id="83562-134">Чтобы зарегистрировать агент задач, добавьте следующий ключ в реестр виртуальной машины:</span><span class="sxs-lookup"><span data-stu-id="83562-134">To register the task agent, add the following key to the registry of the virtual machine:</span></span>

<span data-ttu-id="83562-135">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера — \\  \\  \\  \\  \\  \\ **подключаемые модули** задач сервера терминалов \\  Microsoft Windows NT CurrentVersion таскажентнаме</span><span class="sxs-lookup"><span data-stu-id="83562-135">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Terminal Server**\\**Task**\\**Plugins**\\**TaskAgentName**</span></span>

<span data-ttu-id="83562-136">В разделе этого раздела реестра добавьте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="83562-136">Under this registry key, add the following values:</span></span>



| <span data-ttu-id="83562-137">Имя</span><span class="sxs-lookup"><span data-stu-id="83562-137">Name</span></span>                     | <span data-ttu-id="83562-138">Тип</span><span class="sxs-lookup"><span data-stu-id="83562-138">Type</span></span>                      | <span data-ttu-id="83562-139">Описание</span><span class="sxs-lookup"><span data-stu-id="83562-139">Description</span></span>                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="83562-140">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="83562-140">**CLSID**</span></span><br/>     | <span data-ttu-id="83562-141">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="83562-141">**REG\_SZ**</span></span><br/>    | <span data-ttu-id="83562-142">Строка, представляющая **идентификатор CLSID** агента задачи.</span><span class="sxs-lookup"><span data-stu-id="83562-142">A string that represents the **CLSID** of the task agent.</span></span><br/>          |
| <span data-ttu-id="83562-143">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="83562-143">**IsEnabled**</span></span><br/> | <span data-ttu-id="83562-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="83562-144">**REG\_DWORD**</span></span><br/> | <span data-ttu-id="83562-145">0, если агент задач отключен, или 1, если агент задач включен.</span><span class="sxs-lookup"><span data-stu-id="83562-145">0 if the task agent is disabled or 1 if the task agent is enabled.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="83562-146">Можно зарегистрировать более одного агента задач, но будет использоваться только один агент задачи.</span><span class="sxs-lookup"><span data-stu-id="83562-146">More than one task agent can be registered, but only one task agent will be used.</span></span> <span data-ttu-id="83562-147">Если включен более одного агента задач, будет использоваться только первый найденный агент.</span><span class="sxs-lookup"><span data-stu-id="83562-147">If more than one task agent is enabled, only the first one found will be used.</span></span>

 

<span data-ttu-id="83562-148">Хотя этот интерфейс поддерживается в операционных системах, указанных в приведенных ниже требованиях, он будет использоваться только в том случае, если виртуальная машина размещена на Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="83562-148">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="83562-149">Требования</span><span class="sxs-lookup"><span data-stu-id="83562-149">Requirements</span></span>



| <span data-ttu-id="83562-150">Требование</span><span class="sxs-lookup"><span data-stu-id="83562-150">Requirement</span></span> | <span data-ttu-id="83562-151">Значение</span><span class="sxs-lookup"><span data-stu-id="83562-151">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="83562-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83562-152">Minimum supported client</span></span><br/> | <span data-ttu-id="83562-153">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="83562-153">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="83562-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83562-154">Minimum supported server</span></span><br/> | <span data-ttu-id="83562-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83562-155">Windows Server 2008 R2</span></span><br/> |



 

