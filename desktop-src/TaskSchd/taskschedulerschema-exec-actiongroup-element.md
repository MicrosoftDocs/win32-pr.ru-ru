---
title: Exec (actionGroup), элемент
description: Указывает действие, выполняющее операцию командной строки.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Элемент Exec планировщик задач
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674557"
---
# <a name="exec-actiongroup-element"></a><span data-ttu-id="7b00e-104">Exec (actionGroup), элемент</span><span class="sxs-lookup"><span data-stu-id="7b00e-104">Exec (actionGroup) Element</span></span>

<span data-ttu-id="7b00e-105">Указывает действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="7b00e-105">Specifies an action that executes a command-line operation.</span></span>

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

<span data-ttu-id="7b00e-106">Элемент **exec** определяется [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="7b00e-106">The **Exec** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="7b00e-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="7b00e-107">Parent element</span></span>



| <span data-ttu-id="7b00e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="7b00e-108">Element</span></span>                                                         | <span data-ttu-id="7b00e-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="7b00e-109">Derived from</span></span>                                                       | <span data-ttu-id="7b00e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7b00e-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="7b00e-111">**Действия**</span><span class="sxs-lookup"><span data-stu-id="7b00e-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="7b00e-112">**актионстипе**</span><span class="sxs-lookup"><span data-stu-id="7b00e-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="7b00e-113">Содержит действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="7b00e-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="7b00e-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7b00e-114">Child elements</span></span>



| <span data-ttu-id="7b00e-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="7b00e-115">Element</span></span>                                                                           | <span data-ttu-id="7b00e-116">Тип</span><span class="sxs-lookup"><span data-stu-id="7b00e-116">Type</span></span>       | <span data-ttu-id="7b00e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7b00e-117">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b00e-118">**Аргументы**</span><span class="sxs-lookup"><span data-stu-id="7b00e-118">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="7b00e-119">**string**</span><span class="sxs-lookup"><span data-stu-id="7b00e-119">**string**</span></span> | <span data-ttu-id="7b00e-120">Задает аргументы, связанные с операцией командной строки.</span><span class="sxs-lookup"><span data-stu-id="7b00e-120">Specifies the arguments associated with the command-line operation.</span></span><br/>                               |
| [<span data-ttu-id="7b00e-121">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="7b00e-121">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | <span data-ttu-id="7b00e-122">**string**</span><span class="sxs-lookup"><span data-stu-id="7b00e-122">**string**</span></span> | <span data-ttu-id="7b00e-123">Указывает исполняемый файл или документ для запуска.</span><span class="sxs-lookup"><span data-stu-id="7b00e-123">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="7b00e-124">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="7b00e-124">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | <span data-ttu-id="7b00e-125">строка</span><span class="sxs-lookup"><span data-stu-id="7b00e-125">string</span></span>     | <span data-ttu-id="7b00e-126">Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.</span><span class="sxs-lookup"><span data-stu-id="7b00e-126">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="7b00e-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b00e-127">Attributes</span></span>



| <span data-ttu-id="7b00e-128">Имя</span><span class="sxs-lookup"><span data-stu-id="7b00e-128">Name</span></span> | <span data-ttu-id="7b00e-129">Тип</span><span class="sxs-lookup"><span data-stu-id="7b00e-129">Type</span></span>       | <span data-ttu-id="7b00e-130">Описание</span><span class="sxs-lookup"><span data-stu-id="7b00e-130">Description</span></span>                                                    |
|------|------------|----------------------------------------------------------------|
| <span data-ttu-id="7b00e-131">идентификатор</span><span class="sxs-lookup"><span data-stu-id="7b00e-131">id</span></span>   | <span data-ttu-id="7b00e-132">**string**</span><span class="sxs-lookup"><span data-stu-id="7b00e-132">**string**</span></span> | <span data-ttu-id="7b00e-133">Идентификатор действия, выполняемого задачей.</span><span class="sxs-lookup"><span data-stu-id="7b00e-133">The identifier of the action performed by the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7b00e-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b00e-134">Remarks</span></span>

<span data-ttu-id="7b00e-135">Перечисленные выше дочерние элементы определяются сложным типом [**ексектипе**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7b00e-135">The child elements listed above are defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

<span data-ttu-id="7b00e-136">Для разработки скриптов действие выполнения определяется объектом [**ексекактион**](execaction.md) .</span><span class="sxs-lookup"><span data-stu-id="7b00e-136">For script development, an execution action is defined by the [**ExecAction**](execaction.md) object.</span></span>

<span data-ttu-id="7b00e-137">Для разработки на C++ действие выполнения определяется интерфейсом [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .</span><span class="sxs-lookup"><span data-stu-id="7b00e-137">For C++ development, an execution action is defined by the [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) interface.</span></span>

<span data-ttu-id="7b00e-138">Если переменные среды используются в [**команде**](taskschedulerschema-command-exectype-element.md), [**аргументах**](taskschedulerschema-arguments-exectype-element.md)или элементах [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , значения переменных среды кэшируются и используются при запуске Taskeng.exe (обработчик задач).</span><span class="sxs-lookup"><span data-stu-id="7b00e-138">If environment variables are used in the [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md), or [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) elements, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="7b00e-139">Изменения переменных среды, происходящих после запуска обработчика задач, не будут использоваться обработчиком задач.</span><span class="sxs-lookup"><span data-stu-id="7b00e-139">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

## <a name="examples"></a><span data-ttu-id="7b00e-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="7b00e-140">Examples</span></span>

<span data-ttu-id="7b00e-141">Полный пример XML-кода для задачи, использующей триггер события, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="7b00e-141">For a complete example of the XML for a task that uses an event trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b00e-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7b00e-142">Requirements</span></span>



| <span data-ttu-id="7b00e-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7b00e-143">Requirement</span></span> | <span data-ttu-id="7b00e-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7b00e-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b00e-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b00e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7b00e-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b00e-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b00e-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b00e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7b00e-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b00e-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b00e-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b00e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b00e-150">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="7b00e-150">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





