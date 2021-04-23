---
title: RegistrationInfo.Doc, свойство ументатион
description: Для создания скриптов Возвращает или задает любую дополнительную документацию для задачи.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- планировщик задач свойств документации
- Свойство документации планировщик задач, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство Documentation
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135058"
---
# <a name="registrationinfodocumentation-property"></a><span data-ttu-id="e895e-106">RegistrationInfo.Doc, свойство ументатион</span><span class="sxs-lookup"><span data-stu-id="e895e-106">RegistrationInfo.Documentation property</span></span>

<span data-ttu-id="e895e-107">Для создания скриптов Возвращает или задает любую дополнительную документацию для задачи.</span><span class="sxs-lookup"><span data-stu-id="e895e-107">For scripting, gets or sets any additional documentation for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="e895e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e895e-108">Syntax</span></span>


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a><span data-ttu-id="e895e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e895e-109">Property value</span></span>

<span data-ttu-id="e895e-110">Любая дополнительная документация, связанная с задачей.</span><span class="sxs-lookup"><span data-stu-id="e895e-110">Any additional documentation that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="e895e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e895e-111">Remarks</span></span>

<span data-ttu-id="e895e-112">При чтении или записи XML для задачи дополнительная документация для задачи указывается с помощью элемента [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="e895e-112">When reading or writing XML for a task, the additional documentation for the task is specified using the [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="e895e-113">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="e895e-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="e895e-114">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="e895e-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="e895e-115">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="e895e-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="e895e-116">Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="e895e-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e895e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e895e-117">Requirements</span></span>



| <span data-ttu-id="e895e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e895e-118">Requirement</span></span> | <span data-ttu-id="e895e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e895e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e895e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e895e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e895e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e895e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e895e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e895e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e895e-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e895e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e895e-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e895e-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e895e-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e895e-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e895e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e895e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e895e-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e895e-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e895e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e895e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e895e-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e895e-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





