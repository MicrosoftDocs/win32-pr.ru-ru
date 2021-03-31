---
title: Объект Нетворксеттингс
description: Для сценариев предоставляет параметры, которые служба планировщик задач использует для получения сетевого профиля.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- планировщик задач объекта Нетворксеттингс
- Планировщик задач объекта Нетворксеттингс, описание
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491094"
---
# <a name="networksettings-object"></a><span data-ttu-id="8b73f-105">Объект Нетворксеттингс</span><span class="sxs-lookup"><span data-stu-id="8b73f-105">NetworkSettings object</span></span>

<span data-ttu-id="8b73f-106">Для сценариев предоставляет параметры, которые служба планировщик задач использует для получения сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="8b73f-106">For scripting, provides the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

## <a name="members"></a><span data-ttu-id="8b73f-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="8b73f-107">Members</span></span>

<span data-ttu-id="8b73f-108">Объект **нетворксеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8b73f-108">The **NetworkSettings** object has these types of members:</span></span>

-   [<span data-ttu-id="8b73f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b73f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b73f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b73f-110">Properties</span></span>

<span data-ttu-id="8b73f-111">Объект **нетворксеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8b73f-111">The **NetworkSettings** object has these properties.</span></span>



| <span data-ttu-id="8b73f-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="8b73f-112">Property</span></span>                                        | <span data-ttu-id="8b73f-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="8b73f-113">Access type</span></span>           | <span data-ttu-id="8b73f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8b73f-114">Description</span></span>                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b73f-115">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="8b73f-115">**Id**</span></span>](networksettings-id.md)<br/>     | <span data-ttu-id="8b73f-116">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="8b73f-116">Read/write</span></span><br/> | <span data-ttu-id="8b73f-117">Возвращает или задает значение идентификатора GUID, определяющее сетевой профиль.</span><span class="sxs-lookup"><span data-stu-id="8b73f-117">Gets or sets a GUID value that identifies a network profile.</span></span><br/>                        |
| [<span data-ttu-id="8b73f-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8b73f-118">**Name**</span></span>](networksettings-name.md)<br/> | <span data-ttu-id="8b73f-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="8b73f-119">Read/write</span></span><br/> | <span data-ttu-id="8b73f-120">Возвращает или задает имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="8b73f-120">Gets or sets the name of a network profile.</span></span> <span data-ttu-id="8b73f-121">Имя используется в целях показа.</span><span class="sxs-lookup"><span data-stu-id="8b73f-121">The name is used for display purposes.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b73f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b73f-122">Remarks</span></span>

<span data-ttu-id="8b73f-123">При чтении или записи собственного XML-кода для задачи параметры сети задаются с помощью элемента [**нетворксеттингс**](taskschedulerschema-networksettings-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="8b73f-123">When reading or writing your own XML for a task, network settings are specified using the [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b73f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8b73f-124">Requirements</span></span>



| <span data-ttu-id="8b73f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8b73f-125">Requirement</span></span> | <span data-ttu-id="8b73f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8b73f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b73f-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b73f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8b73f-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b73f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8b73f-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b73f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8b73f-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b73f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b73f-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8b73f-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b73f-132"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b73f-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b73f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8b73f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b73f-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b73f-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b73f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b73f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b73f-136">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="8b73f-136">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="8b73f-137">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="8b73f-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





