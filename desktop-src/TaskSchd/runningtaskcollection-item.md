---
title: Руннингтаскколлектион. Item, свойство
description: Для сценария возвращает указанную задачу из коллекции.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- планировщик задач свойства элемента
- Свойство Item планировщик задач, объект Руннингтаскколлектион
- Планировщик задач объекта Руннингтаскколлектион, свойство Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136546"
---
# <a name="runningtaskcollectionitem-property"></a><span data-ttu-id="f70cd-106">Руннингтаскколлектион. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="f70cd-106">RunningTaskCollection.Item property</span></span>

<span data-ttu-id="f70cd-107">Для сценария возвращает указанную задачу из коллекции.</span><span class="sxs-lookup"><span data-stu-id="f70cd-107">For scripting, gets the specified task from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70cd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f70cd-108">Syntax</span></span>


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a><span data-ttu-id="f70cd-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f70cd-109">Property value</span></span>

<span data-ttu-id="f70cd-110">Объект [**руннингтаск**](runningtask.md) , содержащий запрошенный контекст.</span><span class="sxs-lookup"><span data-stu-id="f70cd-110">A [**RunningTask**](runningtask.md) object that contains the requested context.</span></span>

## <a name="remarks"></a><span data-ttu-id="f70cd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f70cd-111">Remarks</span></span>

<span data-ttu-id="f70cd-112">Коллекции основаны на 1.</span><span class="sxs-lookup"><span data-stu-id="f70cd-112">Collections are 1-based.</span></span> <span data-ttu-id="f70cd-113">Иными словами, индекс первого элемента в коллекции равен 1.</span><span class="sxs-lookup"><span data-stu-id="f70cd-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70cd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f70cd-114">Requirements</span></span>



| <span data-ttu-id="f70cd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f70cd-115">Requirement</span></span> | <span data-ttu-id="f70cd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f70cd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f70cd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f70cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f70cd-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f70cd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f70cd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f70cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f70cd-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f70cd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f70cd-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f70cd-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f70cd-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f70cd-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f70cd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f70cd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f70cd-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f70cd-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70cd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f70cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70cd-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f70cd-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





