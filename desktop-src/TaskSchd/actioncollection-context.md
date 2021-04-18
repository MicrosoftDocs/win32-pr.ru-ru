---
title: ActionCollection. Context, свойство
description: Для создания скриптов Возвращает или задает идентификатор участника для задачи.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- планировщик задач свойства контекста
- Свойство Context планировщик задач, объект ActionCollection
- Планировщик задач объекта ActionCollection, свойство Context
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681994"
---
# <a name="actioncollectioncontext-property"></a><span data-ttu-id="a833d-106">ActionCollection. Context, свойство</span><span class="sxs-lookup"><span data-stu-id="a833d-106">ActionCollection.Context property</span></span>

<span data-ttu-id="a833d-107">Для создания скриптов Возвращает или задает идентификатор участника для задачи.</span><span class="sxs-lookup"><span data-stu-id="a833d-107">For scripting, gets or sets the identifier of the principal for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="a833d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a833d-108">Syntax</span></span>


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a><span data-ttu-id="a833d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a833d-109">Property value</span></span>

<span data-ttu-id="a833d-110">Идентификатор участника для задачи.</span><span class="sxs-lookup"><span data-stu-id="a833d-110">The identifier of the principal for the task.</span></span> <span data-ttu-id="a833d-111">Указанный здесь идентификатор должен соответствовать идентификатору, указанному в свойстве ID интерфейса IPrincipal, определяющего участника.</span><span class="sxs-lookup"><span data-stu-id="a833d-111">The identifier that is specified here must match the identifier that is specified in the Id property of the IPrincipal interface that defines the principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="a833d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a833d-112">Requirements</span></span>



| <span data-ttu-id="a833d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a833d-113">Requirement</span></span> | <span data-ttu-id="a833d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a833d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a833d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a833d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a833d-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a833d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a833d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a833d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a833d-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a833d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a833d-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a833d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="a833d-120"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a833d-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a833d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a833d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a833d-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a833d-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a833d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a833d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a833d-124">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a833d-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="a833d-125">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="a833d-125">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





