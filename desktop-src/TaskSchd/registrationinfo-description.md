---
title: Регистратионинфо. Description, свойство
description: Для создания скриптов Возвращает или задает описание задачи.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- планировщик задач Свойства описания
- Свойство Description планировщик задач, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c79b60fe6a96493c52011e5bd731679b3fee1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414697"
---
# <a name="registrationinfodescription-property"></a><span data-ttu-id="77610-106">Регистратионинфо. Description, свойство</span><span class="sxs-lookup"><span data-stu-id="77610-106">RegistrationInfo.Description property</span></span>

<span data-ttu-id="77610-107">Для создания скриптов Возвращает или задает описание задачи.</span><span class="sxs-lookup"><span data-stu-id="77610-107">For scripting, gets or sets the description of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="77610-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77610-108">Syntax</span></span>


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a><span data-ttu-id="77610-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="77610-109">Property value</span></span>

<span data-ttu-id="77610-110">Описание задачи.</span><span class="sxs-lookup"><span data-stu-id="77610-110">The description of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="77610-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77610-111">Remarks</span></span>

<span data-ttu-id="77610-112">При чтении или записи XML для задачи описание задачи указывается с помощью элемента [**Description**](taskschedulerschema-description-registrationinfotype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="77610-112">When reading or writing XML for a task, the description of the task is specified using the [**Description**](taskschedulerschema-description-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="77610-113">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="77610-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="77610-114">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="77610-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="77610-115">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="77610-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="77610-116">Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="77610-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="77610-117">Требования</span><span class="sxs-lookup"><span data-stu-id="77610-117">Requirements</span></span>



| <span data-ttu-id="77610-118">Требование</span><span class="sxs-lookup"><span data-stu-id="77610-118">Requirement</span></span> | <span data-ttu-id="77610-119">Значение</span><span class="sxs-lookup"><span data-stu-id="77610-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77610-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77610-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77610-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77610-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77610-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77610-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77610-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77610-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77610-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="77610-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="77610-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="77610-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="77610-126">DLL</span><span class="sxs-lookup"><span data-stu-id="77610-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77610-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77610-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77610-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77610-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77610-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="77610-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





