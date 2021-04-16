---
title: Объект Комхандлерактион
description: Объект скрипта, представляющий действие, которое вызывает обработчик.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Планировщик задач действий обработчика COM, объект
- планировщик задач объекта Комхандлерактион
- Планировщик задач объекта Комхандлерактион, описание
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488937"
---
# <a name="comhandleraction-object"></a><span data-ttu-id="b5020-106">Объект Комхандлерактион</span><span class="sxs-lookup"><span data-stu-id="b5020-106">ComHandlerAction object</span></span>

<span data-ttu-id="b5020-107">Объект скрипта, представляющий действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="b5020-107">Scripting object that represents an action that fires a handler.</span></span>

## <a name="members"></a><span data-ttu-id="b5020-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="b5020-108">Members</span></span>

<span data-ttu-id="b5020-109">Объект **комхандлерактион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b5020-109">The **ComHandlerAction** object has these types of members:</span></span>

-   [<span data-ttu-id="b5020-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b5020-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5020-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b5020-111">Properties</span></span>

<span data-ttu-id="b5020-112">Объект **комхандлерактион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b5020-112">The **ComHandlerAction** object has these properties.</span></span>



| <span data-ttu-id="b5020-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="b5020-113">Property</span></span>                                               | <span data-ttu-id="b5020-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b5020-114">Access type</span></span>           | <span data-ttu-id="b5020-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b5020-115">Description</span></span>                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5020-116">**Класса**</span><span class="sxs-lookup"><span data-stu-id="b5020-116">**ClassId**</span></span>](comhandleraction-classid.md)<br/> | <span data-ttu-id="b5020-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="b5020-117">Read/write</span></span><br/> | <span data-ttu-id="b5020-118">Возвращает или задает идентификатор класса обработчика.</span><span class="sxs-lookup"><span data-stu-id="b5020-118">Gets or sets the identifier of the handler class.</span></span><br/>                                              |
| [<span data-ttu-id="b5020-119">**Data**</span><span class="sxs-lookup"><span data-stu-id="b5020-119">**Data**</span></span>](comhandleraction-data.md)<br/>       | <span data-ttu-id="b5020-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="b5020-120">Read/write</span></span><br/> | <span data-ttu-id="b5020-121">Возвращает или задает дополнительные данные, связанные с обработчиком.</span><span class="sxs-lookup"><span data-stu-id="b5020-121">Gets or sets additional data that is associated with the handler.</span></span><br/>                              |
| [<span data-ttu-id="b5020-122">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="b5020-122">**Id**</span></span>](action-id.md)<br/>                     | <span data-ttu-id="b5020-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="b5020-123">Read/write</span></span><br/> | <span data-ttu-id="b5020-124">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b5020-124">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b5020-125">Возвращает или задает идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="b5020-125">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="b5020-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b5020-126">**Type**</span></span>](action-type.md)<br/>                 | <span data-ttu-id="b5020-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5020-127">Read-only</span></span><br/>  | <span data-ttu-id="b5020-128">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b5020-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b5020-129">Возвращает тип действия.</span><span class="sxs-lookup"><span data-stu-id="b5020-129">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="b5020-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5020-130">Remarks</span></span>

<span data-ttu-id="b5020-131">Обработчики COM должны реализовывать интерфейс [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) для планировщик задач для запуска и завершения обработчика.</span><span class="sxs-lookup"><span data-stu-id="b5020-131">COM handlers must implement the [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) interface for the Task Scheduler to start and stop the handler.</span></span> <span data-ttu-id="b5020-132">В свою очередь, обработчик COM использует методы объекта [**таскхандлерстатус**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) для передачи состояния обратно в планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="b5020-132">In turn, the COM handler uses the methods of the [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) object to communicate the status back to the Task Scheduler.</span></span>

<span data-ttu-id="b5020-133">При чтении или записи XML действие обработчика COM задается в элементе [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="b5020-133">When reading or writing XML, a COM handler action is specified in the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5020-134">Требования</span><span class="sxs-lookup"><span data-stu-id="b5020-134">Requirements</span></span>



| <span data-ttu-id="b5020-135">Требование</span><span class="sxs-lookup"><span data-stu-id="b5020-135">Requirement</span></span> | <span data-ttu-id="b5020-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b5020-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5020-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5020-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b5020-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5020-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b5020-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5020-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b5020-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5020-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5020-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b5020-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5020-142"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5020-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5020-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b5020-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5020-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5020-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5020-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5020-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5020-146">**таскхандлерстатус**</span><span class="sxs-lookup"><span data-stu-id="b5020-146">**TaskHandlerStatus**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[<span data-ttu-id="b5020-147">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="b5020-147">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="b5020-148">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="b5020-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





