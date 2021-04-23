---
title: Ексекактион. Arguments, свойство
description: Для создания скриптов Возвращает или задает аргументы, связанные с операцией командной строки.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Свойство Arguments планировщик задач
- Свойство Arguments планировщик задач, объект Ексекактион
- Планировщик задач объекта Ексекактион, свойство Arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988424"
---
# <a name="execactionarguments-property"></a><span data-ttu-id="aa078-106">Ексекактион. Arguments, свойство</span><span class="sxs-lookup"><span data-stu-id="aa078-106">ExecAction.Arguments property</span></span>

<span data-ttu-id="aa078-107">Для создания скриптов Возвращает или задает аргументы, связанные с операцией командной строки.</span><span class="sxs-lookup"><span data-stu-id="aa078-107">For scripting, gets or sets the arguments associated with the command-line operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa078-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa078-108">Syntax</span></span>


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a><span data-ttu-id="aa078-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aa078-109">Property value</span></span>

<span data-ttu-id="aa078-110">Аргументы, необходимые для операции командной строки.</span><span class="sxs-lookup"><span data-stu-id="aa078-110">The arguments that are needed by the command-line operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa078-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa078-111">Remarks</span></span>

<span data-ttu-id="aa078-112">При чтении или записи XML аргументы операции командной строки задаются в элементе [**arguments**](taskschedulerschema-arguments-exectype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="aa078-112">When reading or writing XML, the command-line operation arguments are specified in the [**Arguments**](taskschedulerschema-arguments-exectype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa078-113">Требования</span><span class="sxs-lookup"><span data-stu-id="aa078-113">Requirements</span></span>



| <span data-ttu-id="aa078-114">Требование</span><span class="sxs-lookup"><span data-stu-id="aa078-114">Requirement</span></span> | <span data-ttu-id="aa078-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aa078-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa078-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa078-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa078-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa078-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa078-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa078-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa078-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa078-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa078-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="aa078-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa078-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa078-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa078-122">DLL</span><span class="sxs-lookup"><span data-stu-id="aa078-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa078-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa078-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa078-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa078-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa078-125">**ексекактион**</span><span class="sxs-lookup"><span data-stu-id="aa078-125">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="aa078-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="aa078-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





