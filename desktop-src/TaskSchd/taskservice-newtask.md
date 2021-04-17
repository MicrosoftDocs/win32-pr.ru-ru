---
title: TaskService. @, метод
description: Для создания скриптов возвращает пустой объект определения задачи, который должен быть заполнен параметрами и свойствами, а затем зарегистрирован с помощью метода Таскфолдер. Регистертаскдефинитион.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- планировщик задач метода "в команде"
- Метод планировщик задач, объект TaskService
- Планировщик задач объекта TaskService, метод "в команде"
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682124"
---
# <a name="taskservicenewtask-method"></a><span data-ttu-id="3cf85-106">TaskService. @, метод</span><span class="sxs-lookup"><span data-stu-id="3cf85-106">TaskService.NewTask method</span></span>

<span data-ttu-id="3cf85-107">Для создания скриптов возвращает пустой объект определения задачи, который должен быть заполнен параметрами и свойствами, а затем зарегистрирован с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="3cf85-107">For scripting, returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf85-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cf85-108">Syntax</span></span>


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="3cf85-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cf85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf85-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cf85-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cf85-111">Этот параметр зарезервирован для будущего использования и должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="3cf85-111">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf85-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cf85-112">Return value</span></span>

<span data-ttu-id="3cf85-113">Определение задачи, в которой указаны все сведения, необходимые для создания новой задачи.</span><span class="sxs-lookup"><span data-stu-id="3cf85-113">The task definition that specifies all the information required to create a new task.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf85-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3cf85-114">Requirements</span></span>



| <span data-ttu-id="3cf85-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3cf85-115">Requirement</span></span> | <span data-ttu-id="3cf85-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3cf85-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf85-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cf85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf85-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3cf85-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3cf85-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cf85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf85-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3cf85-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3cf85-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3cf85-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="3cf85-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3cf85-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3cf85-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3cf85-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cf85-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cf85-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





