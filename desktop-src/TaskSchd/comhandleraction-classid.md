---
title: Комхандлерактион. ClassId, свойство
description: Для создания скриптов Возвращает или задает идентификатор класса обработчика.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Свойство ClassId планировщик задач
- Свойство ClassId планировщик задач, объект Комхандлерактион
- Планировщик задач объекта Комхандлерактион, свойство ClassId
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801799"
---
# <a name="comhandleractionclassid-property"></a><span data-ttu-id="e3452-106">Комхандлерактион. ClassId, свойство</span><span class="sxs-lookup"><span data-stu-id="e3452-106">ComHandlerAction.ClassId property</span></span>

<span data-ttu-id="e3452-107">Для создания скриптов Возвращает или задает идентификатор класса обработчика.</span><span class="sxs-lookup"><span data-stu-id="e3452-107">For scripting, gets or sets the identifier of the handler class.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3452-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3452-108">Syntax</span></span>


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a><span data-ttu-id="e3452-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e3452-109">Property value</span></span>

<span data-ttu-id="e3452-110">Идентификатор класса, определяющего запускаемый обработчик.</span><span class="sxs-lookup"><span data-stu-id="e3452-110">The identifier of the class that defines the handler to be fired.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3452-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3452-111">Remarks</span></span>

<span data-ttu-id="e3452-112">При чтении или записи XML класс обработчика COM указывается в элементе [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="e3452-112">When reading or writing XML, the class of a COM handler is specified in the [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3452-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e3452-113">Requirements</span></span>



| <span data-ttu-id="e3452-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e3452-114">Requirement</span></span> | <span data-ttu-id="e3452-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e3452-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3452-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3452-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3452-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3452-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e3452-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3452-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3452-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3452-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3452-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e3452-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3452-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e3452-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e3452-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e3452-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3452-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3452-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3452-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3452-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3452-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e3452-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e3452-126">**комхандлерактион**</span><span class="sxs-lookup"><span data-stu-id="e3452-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





