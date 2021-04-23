---
title: Тасксеттингс. Алловдемандстарт, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задачу можно запустить с помощью команды Run или контекстного меню.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- планировщик задач свойства Алловдемандстарт
- Планировщик задач свойства Алловдемандстарт, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Алловдемандстарт
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414965"
---
# <a name="tasksettingsallowdemandstart-property"></a><span data-ttu-id="cee92-106">Тасксеттингс. Алловдемандстарт, свойство</span><span class="sxs-lookup"><span data-stu-id="cee92-106">TaskSettings.AllowDemandStart property</span></span>

<span data-ttu-id="cee92-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что задачу можно запустить с помощью команды Run или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="cee92-107">For scripting, gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.</span></span>

<span data-ttu-id="cee92-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="cee92-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee92-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cee92-109">Syntax</span></span>


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a><span data-ttu-id="cee92-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cee92-110">Property value</span></span>

<span data-ttu-id="cee92-111">Если значение — true, задача может быть запущена с помощью команды Run или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="cee92-111">If True, the task can be run by using the Run command or the Context menu.</span></span> <span data-ttu-id="cee92-112">Если значение равно false, задача не может быть выполнена с помощью команды Run или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="cee92-112">If False, the task cannot be run using the Run command or the Context menu.</span></span> <span data-ttu-id="cee92-113">Значение по умолчанию равно True.</span><span class="sxs-lookup"><span data-stu-id="cee92-113">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="cee92-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cee92-114">Remarks</span></span>

<span data-ttu-id="cee92-115">Если для этого свойства задано значение true, задача может быть запущена независимо от того, когда триггеры запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="cee92-115">When this property is set to True, the task can be started independent of when any triggers start the task.</span></span>

<span data-ttu-id="cee92-116">При чтении или записи XML для задачи этот параметр указывается в элементе [алловстартондеманд](taskschedulerschema-allowstartondemand-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="cee92-116">When reading or writing XML for a task, this setting is specified in the [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee92-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cee92-117">Requirements</span></span>



| <span data-ttu-id="cee92-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cee92-118">Requirement</span></span> | <span data-ttu-id="cee92-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cee92-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cee92-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cee92-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cee92-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cee92-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cee92-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cee92-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cee92-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cee92-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cee92-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cee92-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="cee92-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cee92-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cee92-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cee92-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cee92-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cee92-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee92-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cee92-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee92-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="cee92-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





