---
title: Тригжерколлектион. Remove, метод
description: Для сценариев удаляет указанный триггер из коллекции триггеров, используемых задачей.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- триггеры планировщик задач, удаление
- Удалить метод планировщик задач
- Метод Remove планировщик задач, объект Тригжерколлектион
- Планировщик задач объекта Тригжерколлектион, метод Remove
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340610"
---
# <a name="triggercollectionremove-method"></a><span data-ttu-id="82805-107">Тригжерколлектион. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="82805-107">TriggerCollection.Remove method</span></span>

<span data-ttu-id="82805-108">Для сценариев удаляет указанный триггер из коллекции триггеров, используемых задачей.</span><span class="sxs-lookup"><span data-stu-id="82805-108">For scripting, removes the specified trigger from the collection of triggers used by the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="82805-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82805-109">Syntax</span></span>


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="82805-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="82805-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82805-111">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82805-111">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82805-112">Индекс удаляемого триггера.</span><span class="sxs-lookup"><span data-stu-id="82805-112">The index of the trigger to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82805-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82805-113">Return value</span></span>

<span data-ttu-id="82805-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="82805-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82805-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82805-115">Remarks</span></span>

<span data-ttu-id="82805-116">При удалении элементов Обратите внимание, что индекс для первого элемента в коллекции равен 1, а индекс последнего элемента — значение свойства [**тригжерколлектион. Count**](triggercollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="82805-116">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**TriggerCollection.Count**](triggercollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="82805-117">Требования</span><span class="sxs-lookup"><span data-stu-id="82805-117">Requirements</span></span>



| <span data-ttu-id="82805-118">Требование</span><span class="sxs-lookup"><span data-stu-id="82805-118">Requirement</span></span> | <span data-ttu-id="82805-119">Значение</span><span class="sxs-lookup"><span data-stu-id="82805-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82805-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82805-120">Minimum supported client</span></span><br/> | <span data-ttu-id="82805-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82805-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="82805-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82805-122">Minimum supported server</span></span><br/> | <span data-ttu-id="82805-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82805-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82805-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="82805-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="82805-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="82805-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="82805-126">DLL</span><span class="sxs-lookup"><span data-stu-id="82805-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82805-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82805-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82805-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82805-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82805-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="82805-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





