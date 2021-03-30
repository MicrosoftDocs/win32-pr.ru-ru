---
title: Тригжерколлектион. Item, свойство
description: Для сценариев Возвращает указанный триггер из коллекции.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- планировщик задач свойства элемента
- Свойство Item планировщик задач, объект Тригжерколлектион
- Планировщик задач объекта Тригжерколлектион, свойство Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801732"
---
# <a name="triggercollectionitem-property"></a><span data-ttu-id="e2304-106">Тригжерколлектион. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="e2304-106">TriggerCollection.Item property</span></span>

<span data-ttu-id="e2304-107">Для сценариев Возвращает указанный триггер из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e2304-107">For scripting, gets the specified trigger from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2304-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2304-108">Syntax</span></span>


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a><span data-ttu-id="e2304-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e2304-109">Property value</span></span>

<span data-ttu-id="e2304-110">Объект [**триггера**](trigger.md) , представляющий запрошенный триггер.</span><span class="sxs-lookup"><span data-stu-id="e2304-110">A [**Trigger**](trigger.md) object that represents the requested trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2304-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2304-111">Remarks</span></span>

<span data-ttu-id="e2304-112">Коллекции основаны на 1.</span><span class="sxs-lookup"><span data-stu-id="e2304-112">Collections are 1-based.</span></span> <span data-ttu-id="e2304-113">Иными словами, индекс первого элемента в коллекции равен 1.</span><span class="sxs-lookup"><span data-stu-id="e2304-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2304-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e2304-114">Requirements</span></span>



| <span data-ttu-id="e2304-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e2304-115">Requirement</span></span> | <span data-ttu-id="e2304-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e2304-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2304-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2304-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2304-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2304-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e2304-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2304-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2304-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2304-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2304-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e2304-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2304-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2304-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2304-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e2304-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2304-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2304-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2304-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2304-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2304-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e2304-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





