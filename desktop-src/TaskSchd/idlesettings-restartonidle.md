---
title: Идлесеттингс. Рестартонидле, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, перезапускается ли задача, когда компьютер циклически переключается в состояние простоя.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- планировщик задач свойства Рестартонидле
- Планировщик задач свойства Рестартонидле, объект Идлесеттингс
- Планировщик задач объекта Идлесеттингс, свойство Рестартонидле
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681906"
---
# <a name="idlesettingsrestartonidle-property"></a><span data-ttu-id="d8334-106">Идлесеттингс. Рестартонидле, свойство</span><span class="sxs-lookup"><span data-stu-id="d8334-106">IdleSettings.RestartOnIdle property</span></span>

<span data-ttu-id="d8334-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, перезапускается ли задача, когда компьютер циклически переключается в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="d8334-107">For scripting, gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8334-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8334-108">Syntax</span></span>


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d8334-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d8334-109">Property value</span></span>

<span data-ttu-id="d8334-110">Логическое значение, указывающее, должна ли задача перезапускаться, когда компьютер циклически перейдет в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="d8334-110">A Boolean value that indicates whether the task must be restarted when the computer cycles into an idle condition more than once.</span></span> <span data-ttu-id="d8334-111">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="d8334-111">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8334-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8334-112">Remarks</span></span>

<span data-ttu-id="d8334-113">Это свойство используется только в том случае, если свойство [**идлесеттингс. стопонидлинд**](idlesettings-stoponidleend.md) имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="d8334-113">This property is only used if the [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) property is set to True.</span></span>

<span data-ttu-id="d8334-114">При чтении или записи XML для задачи этот параметр указывается в элементе [**рестартонидле**](taskschedulerschema-restartonidle-idlesettingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d8334-114">When reading or writing XML for a task, this setting is specified in the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8334-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d8334-115">Requirements</span></span>



| <span data-ttu-id="d8334-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d8334-116">Requirement</span></span> | <span data-ttu-id="d8334-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d8334-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8334-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8334-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d8334-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8334-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d8334-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8334-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d8334-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8334-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8334-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d8334-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8334-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d8334-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d8334-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d8334-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8334-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8334-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8334-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8334-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8334-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d8334-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d8334-128">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="d8334-128">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





