---
title: Principal.Id, свойство
description: Для создания скриптов Возвращает или задает идентификатор участника.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Свойство ID планировщик задач
- Свойство ID планировщик задач, объект Principal
- Объект Principal планировщик задач, свойство ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415884"
---
# <a name="principalid-property"></a><span data-ttu-id="514c4-106">Principal.Id, свойство</span><span class="sxs-lookup"><span data-stu-id="514c4-106">Principal.Id property</span></span>

<span data-ttu-id="514c4-107">Для создания скриптов Возвращает или задает идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="514c4-107">For scripting, gets or sets the identifier of the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="514c4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="514c4-108">Syntax</span></span>


```VB
Principal.Id As String
```



## <a name="property-value"></a><span data-ttu-id="514c4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="514c4-109">Property value</span></span>

<span data-ttu-id="514c4-110">Идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="514c4-110">The identifier of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="514c4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="514c4-111">Remarks</span></span>

<span data-ttu-id="514c4-112">Этот идентификатор также используется при указании свойства [**ActionCollection. Context**](actioncollection-context.md) .</span><span class="sxs-lookup"><span data-stu-id="514c4-112">This identifier is also used when specifying the [**ActionCollection.Context**](actioncollection-context.md) property.</span></span>

<span data-ttu-id="514c4-113">При чтении или записи XML для задачи идентификатор участника указывается в атрибуте ID элемента [**Principal**](taskschedulerschema-principal-principaltype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="514c4-113">When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="514c4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="514c4-114">Requirements</span></span>



| <span data-ttu-id="514c4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="514c4-115">Requirement</span></span> | <span data-ttu-id="514c4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="514c4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="514c4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="514c4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="514c4-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="514c4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="514c4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="514c4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="514c4-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="514c4-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="514c4-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="514c4-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="514c4-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="514c4-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="514c4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="514c4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="514c4-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="514c4-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514c4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="514c4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514c4-126">**ActionCollection. Context**</span><span class="sxs-lookup"><span data-stu-id="514c4-126">**ActionCollection.Context**</span></span>](actioncollection-context.md)
</dt> <dt>

[<span data-ttu-id="514c4-127">**Основного**</span><span class="sxs-lookup"><span data-stu-id="514c4-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="514c4-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="514c4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





