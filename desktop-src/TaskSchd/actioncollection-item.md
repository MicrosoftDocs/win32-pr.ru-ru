---
title: ActionCollection. Item, свойство
description: Для скрипта возвращает указанное действие из коллекции.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- планировщик задач свойства элемента
- Свойство Item планировщик задач, объект ActionCollection
- Планировщик задач объекта ActionCollection, свойство Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415888"
---
# <a name="actioncollectionitem-property"></a><span data-ttu-id="18179-106">ActionCollection. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="18179-106">ActionCollection.Item property</span></span>

<span data-ttu-id="18179-107">Для скрипта возвращает указанное действие из коллекции.</span><span class="sxs-lookup"><span data-stu-id="18179-107">For scripting, gets a specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="18179-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18179-108">Syntax</span></span>


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a><span data-ttu-id="18179-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="18179-109">Property value</span></span>

<span data-ttu-id="18179-110">Объект [**Action**](action.md) , представляющий запрошенное действие.</span><span class="sxs-lookup"><span data-stu-id="18179-110">An [**Action**](action.md) object that represents the requested action.</span></span>

## <a name="remarks"></a><span data-ttu-id="18179-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18179-111">Remarks</span></span>

<span data-ttu-id="18179-112">Коллекции основаны на 1.</span><span class="sxs-lookup"><span data-stu-id="18179-112">Collections are 1-based.</span></span> <span data-ttu-id="18179-113">Иными словами, индекс первого элемента в коллекции равен 1.</span><span class="sxs-lookup"><span data-stu-id="18179-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="18179-114">Требования</span><span class="sxs-lookup"><span data-stu-id="18179-114">Requirements</span></span>



| <span data-ttu-id="18179-115">Требование</span><span class="sxs-lookup"><span data-stu-id="18179-115">Requirement</span></span> | <span data-ttu-id="18179-116">Значение</span><span class="sxs-lookup"><span data-stu-id="18179-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18179-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18179-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18179-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18179-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="18179-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18179-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18179-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18179-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18179-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="18179-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="18179-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="18179-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="18179-123">DLL</span><span class="sxs-lookup"><span data-stu-id="18179-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18179-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18179-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18179-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18179-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18179-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="18179-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="18179-127">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="18179-127">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





