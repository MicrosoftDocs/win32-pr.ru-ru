---
title: Таскфолдер. Делететаск, метод
description: Для создания скриптов удаляет задачу из папки.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- планировщик задач метода Делететаск
- Планировщик задач метода Делететаск, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, метод Делететаск
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802782"
---
# <a name="taskfolderdeletetask-method"></a><span data-ttu-id="f87fd-106">Таскфолдер. Делететаск, метод</span><span class="sxs-lookup"><span data-stu-id="f87fd-106">TaskFolder.DeleteTask method</span></span>

<span data-ttu-id="f87fd-107">Для создания скриптов удаляет задачу из папки.</span><span class="sxs-lookup"><span data-stu-id="f87fd-107">For scripting, deletes a task from the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="f87fd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f87fd-108">Syntax</span></span>


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="f87fd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f87fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f87fd-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f87fd-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f87fd-111">Имя задачи, указанной при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="f87fd-111">The name of the task that is specified when the task was registered.</span></span> <span data-ttu-id="f87fd-112">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="f87fd-112">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="f87fd-113">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="f87fd-113">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="f87fd-114">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f87fd-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f87fd-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f87fd-115">Not supported.</span></span> <span data-ttu-id="f87fd-116">Значение равно 0</span><span class="sxs-lookup"><span data-stu-id="f87fd-116">Value is 0</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f87fd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f87fd-117">Return value</span></span>

<span data-ttu-id="f87fd-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f87fd-118">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87fd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f87fd-119">Requirements</span></span>



| <span data-ttu-id="f87fd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f87fd-120">Requirement</span></span> | <span data-ttu-id="f87fd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f87fd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f87fd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f87fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f87fd-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f87fd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f87fd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f87fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f87fd-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f87fd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f87fd-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f87fd-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="f87fd-127"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f87fd-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f87fd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f87fd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f87fd-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f87fd-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87fd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f87fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87fd-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f87fd-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





