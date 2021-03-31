---
title: TaskService. Хигхестверсион, свойство
description: Для сценариев указывает самую новую версию планировщик задач, поддерживаемую компьютером.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- планировщик задач свойства Хигхестверсион
- Планировщик задач свойства Хигхестверсион, объект TaskService
- Планировщик задач объекта TaskService, свойство Хигхестверсион
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803952"
---
# <a name="taskservicehighestversion-property"></a><span data-ttu-id="dce57-106">TaskService. Хигхестверсион, свойство</span><span class="sxs-lookup"><span data-stu-id="dce57-106">TaskService.HighestVersion property</span></span>

<span data-ttu-id="dce57-107">Для сценариев указывает самую новую версию планировщик задач, поддерживаемую компьютером.</span><span class="sxs-lookup"><span data-stu-id="dce57-107">For scripting, indicates the highest version of Task Scheduler that a computer supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce57-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dce57-108">Syntax</span></span>


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a><span data-ttu-id="dce57-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dce57-109">Property value</span></span>

<span data-ttu-id="dce57-110">Самая высокая версия планировщик задач, поддерживаемая компьютером.</span><span class="sxs-lookup"><span data-stu-id="dce57-110">The highest version of Task Scheduler that a computer supports.</span></span> <span data-ttu-id="dce57-111">Самая высокая версия — это значение, разделенное на MajorVersion/MinorVersion на 16-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="dce57-111">The highest version is a value that is split into MajorVersion/MinorVersion on the 16-bit boundary.</span></span> <span data-ttu-id="dce57-112">Служба планировщик задач возвращает значение 1 для основной версии и 2 для дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="dce57-112">The Task Scheduler service returns 1 for the major version and 2 for the minor version.</span></span> <span data-ttu-id="dce57-113">Используйте функцию [CLng](/previous-versions//ck4c5842(v=vs.85)) для получения целочисленного значения свойства.</span><span class="sxs-lookup"><span data-stu-id="dce57-113">Use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the integer value of the property.</span></span>

## <a name="examples"></a><span data-ttu-id="dce57-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="dce57-114">Examples</span></span>

<span data-ttu-id="dce57-115">В следующем коде показано, как использовать функцию [CLng](/previous-versions//ck4c5842(v=vs.85)) для получения значения свойства **хигхестверсион** .</span><span class="sxs-lookup"><span data-stu-id="dce57-115">The following code shows how to use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the value of the **HighestVersion** property.</span></span>


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a><span data-ttu-id="dce57-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dce57-116">Requirements</span></span>



| <span data-ttu-id="dce57-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dce57-117">Requirement</span></span> | <span data-ttu-id="dce57-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dce57-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce57-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dce57-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dce57-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dce57-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dce57-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dce57-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dce57-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dce57-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dce57-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dce57-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="dce57-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dce57-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dce57-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dce57-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dce57-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dce57-126"><dt>Taskschd.dll</dt></span></span> </dl> |



 

