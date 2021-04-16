---
title: Руннингтаск. Енгинепид, свойство
description: Для сценариев возвращает идентификатор процесса для подсистемы (процесса), выполняющей задачу.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- планировщик задач свойства Енгинепид
- Планировщик задач свойства Енгинепид, объект Руннингтаск
- Планировщик задач объекта Руннингтаск, свойство Енгинепид
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672736"
---
# <a name="runningtaskenginepid-property"></a><span data-ttu-id="bd61f-106">Руннингтаск. Енгинепид, свойство</span><span class="sxs-lookup"><span data-stu-id="bd61f-106">RunningTask.EnginePID property</span></span>

<span data-ttu-id="bd61f-107">Для сценариев возвращает идентификатор процесса для подсистемы (процесса), выполняющей задачу.</span><span class="sxs-lookup"><span data-stu-id="bd61f-107">For scripting, gets the process ID for the engine (process) which is running the task.</span></span>

<span data-ttu-id="bd61f-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bd61f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd61f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd61f-109">Syntax</span></span>


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a><span data-ttu-id="bd61f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bd61f-110">Property value</span></span>

<span data-ttu-id="bd61f-111">Идентификатор процесса для подсистемы, в которой выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="bd61f-111">The process ID for the engine which is running the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd61f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd61f-112">Remarks</span></span>

<span data-ttu-id="bd61f-113">Идентификатор процесса, возвращаемый этим свойством, не может быть добавлен непосредственно в строку.</span><span class="sxs-lookup"><span data-stu-id="bd61f-113">The process ID returned by this property cannot be appended directly to a string.</span></span> <span data-ttu-id="bd61f-114">Возвращаемое значение должно быть преобразовано в целочисленное значение первым путем вызова функции [CInt](/previous-versions//fctcwhw9(v=vs.85)) возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="bd61f-114">The returned value needs to be converted to an integer value first by calling the [CInt](/previous-versions//fctcwhw9(v=vs.85)) function on the returned value.</span></span>


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a><span data-ttu-id="bd61f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bd61f-115">Requirements</span></span>



| <span data-ttu-id="bd61f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bd61f-116">Requirement</span></span> | <span data-ttu-id="bd61f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bd61f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd61f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd61f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd61f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd61f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bd61f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd61f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd61f-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd61f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd61f-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bd61f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd61f-123"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd61f-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd61f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bd61f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd61f-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd61f-125"><dt>Taskschd.dll</dt></span></span> </dl> |



 

