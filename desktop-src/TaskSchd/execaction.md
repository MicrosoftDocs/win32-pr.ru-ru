---
title: Объект Ексекактион
description: Объект скрипта, представляющий действие, выполняющее операцию командной строки.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- выполнение планировщик задач действий, интерфейс
- планировщик задач объекта Ексекактион
- Планировщик задач объекта Ексекактион, описание
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137239"
---
# <a name="execaction-object"></a><span data-ttu-id="f17ca-106">Объект Ексекактион</span><span class="sxs-lookup"><span data-stu-id="f17ca-106">ExecAction object</span></span>

<span data-ttu-id="f17ca-107">Объект скрипта, представляющий действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="f17ca-107">Scripting object that represents an action that executes a command-line operation.</span></span>

## <a name="members"></a><span data-ttu-id="f17ca-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="f17ca-108">Members</span></span>

<span data-ttu-id="f17ca-109">Объект **ексекактион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f17ca-109">The **ExecAction** object has these types of members:</span></span>

-   [<span data-ttu-id="f17ca-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f17ca-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f17ca-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f17ca-111">Properties</span></span>

<span data-ttu-id="f17ca-112">Объект **ексекактион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f17ca-112">The **ExecAction** object has these properties.</span></span>



| <span data-ttu-id="f17ca-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="f17ca-113">Property</span></span>                                                            | <span data-ttu-id="f17ca-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="f17ca-114">Access type</span></span>           | <span data-ttu-id="f17ca-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f17ca-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f17ca-116">**Аргументы**</span><span class="sxs-lookup"><span data-stu-id="f17ca-116">**Arguments**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | <span data-ttu-id="f17ca-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f17ca-117">Read/write</span></span><br/> | <span data-ttu-id="f17ca-118">Возвращает или задает аргументы, связанные с операцией командной строки.</span><span class="sxs-lookup"><span data-stu-id="f17ca-118">Gets or sets the arguments associated with the command-line operation.</span></span><br/>                                                 |
| [<span data-ttu-id="f17ca-119">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="f17ca-119">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | <span data-ttu-id="f17ca-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f17ca-120">Read/write</span></span><br/> | <span data-ttu-id="f17ca-121">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="f17ca-121">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="f17ca-122">Возвращает или задает идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="f17ca-122">Gets or sets the identifier of the action.</span></span><br/>                         |
| [<span data-ttu-id="f17ca-123">**Путь**</span><span class="sxs-lookup"><span data-stu-id="f17ca-123">**Path**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | <span data-ttu-id="f17ca-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f17ca-124">Read/write</span></span><br/> | <span data-ttu-id="f17ca-125">Возвращает или задает путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="f17ca-125">Gets or sets the path to an executable file.</span></span><br/>                                                                           |
| [<span data-ttu-id="f17ca-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f17ca-126">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | <span data-ttu-id="f17ca-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f17ca-127">Read-only</span></span><br/>  | <span data-ttu-id="f17ca-128">Наследуется от объекта [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="f17ca-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="f17ca-129">Возвращает тип действия.</span><span class="sxs-lookup"><span data-stu-id="f17ca-129">Gets the type of the action.</span></span><br/>                                       |
| [<span data-ttu-id="f17ca-130">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="f17ca-130">**WorkingDirectory**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | <span data-ttu-id="f17ca-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f17ca-131">Read/write</span></span><br/> | <span data-ttu-id="f17ca-132">Возвращает или задает каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="f17ca-132">Gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f17ca-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f17ca-133">Remarks</span></span>

<span data-ttu-id="f17ca-134">Если в свойствах [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)или [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) используются переменные среды, значения переменных среды кэшируются и используются при запуске Taskeng.exe (обработчик задач).</span><span class="sxs-lookup"><span data-stu-id="f17ca-134">If environment variables are used in the [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments), or [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="f17ca-135">Изменения переменных среды, происходящих после запуска обработчика задач, не будут использоваться обработчиком задач.</span><span class="sxs-lookup"><span data-stu-id="f17ca-135">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

<span data-ttu-id="f17ca-136">Это действие выполняет операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="f17ca-136">This action performs a command-line operation.</span></span> <span data-ttu-id="f17ca-137">Например, действие может выполнить сценарий или запустить исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="f17ca-137">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="f17ca-138">При чтении или записи XML действие выполнения указывается в элементе [**exec**](taskschedulerschema-exec-actiongroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="f17ca-138">When reading or writing XML, an execution action is specified in the [**Exec**](taskschedulerschema-exec-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="f17ca-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="f17ca-139">Examples</span></span>

<span data-ttu-id="f17ca-140">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="f17ca-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f17ca-141">Требования</span><span class="sxs-lookup"><span data-stu-id="f17ca-141">Requirements</span></span>



| <span data-ttu-id="f17ca-142">Требование</span><span class="sxs-lookup"><span data-stu-id="f17ca-142">Requirement</span></span> | <span data-ttu-id="f17ca-143">Значение</span><span class="sxs-lookup"><span data-stu-id="f17ca-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f17ca-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f17ca-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f17ca-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f17ca-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f17ca-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f17ca-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f17ca-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f17ca-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f17ca-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f17ca-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="f17ca-149"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f17ca-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f17ca-150">DLL</span><span class="sxs-lookup"><span data-stu-id="f17ca-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f17ca-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f17ca-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





