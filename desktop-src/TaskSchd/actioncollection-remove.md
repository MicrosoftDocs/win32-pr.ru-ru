---
title: ActionCollection. Remove, метод
description: Для сценариев удаляет указанное действие из коллекции.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Удалить метод планировщик задач
- Метод Remove планировщик задач, объект ActionCollection
- Планировщик задач объекта ActionCollection, метод Remove
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802998"
---
# <a name="actioncollectionremove-method"></a><span data-ttu-id="b70ca-106">ActionCollection. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="b70ca-106">ActionCollection.Remove method</span></span>

<span data-ttu-id="b70ca-107">Для сценариев удаляет указанное действие из коллекции.</span><span class="sxs-lookup"><span data-stu-id="b70ca-107">For scripting, removes the specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70ca-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b70ca-108">Syntax</span></span>


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="b70ca-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b70ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70ca-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b70ca-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70ca-111">Индекс удаляемого действия.</span><span class="sxs-lookup"><span data-stu-id="b70ca-111">The index of the action to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70ca-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b70ca-112">Return value</span></span>

<span data-ttu-id="b70ca-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b70ca-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b70ca-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b70ca-114">Remarks</span></span>

<span data-ttu-id="b70ca-115">При удалении элементов Обратите внимание, что индекс для первого элемента в коллекции равен 1, а индекс последнего элемента — значение свойства [**ActionCollection. Count**](actioncollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="b70ca-115">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**ActionCollection.Count**](actioncollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70ca-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b70ca-116">Requirements</span></span>



| <span data-ttu-id="b70ca-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b70ca-117">Requirement</span></span> | <span data-ttu-id="b70ca-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b70ca-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b70ca-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b70ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b70ca-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b70ca-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b70ca-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b70ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b70ca-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b70ca-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b70ca-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b70ca-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b70ca-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b70ca-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b70ca-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b70ca-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b70ca-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b70ca-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b70ca-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b70ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70ca-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="b70ca-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b70ca-129">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="b70ca-129">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





