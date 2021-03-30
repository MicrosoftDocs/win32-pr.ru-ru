---
title: Регистратионинфо. Source, свойство
description: Для сценариев Возвращает или задает, откуда была создана задача. Например, задача может исходить из компонента, службы, приложения или пользователя.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- планировщик задач свойства источника
- Свойство Source планировщик задач, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802981"
---
# <a name="registrationinfosource-property"></a><span data-ttu-id="0df9c-107">Регистратионинфо. Source, свойство</span><span class="sxs-lookup"><span data-stu-id="0df9c-107">RegistrationInfo.Source property</span></span>

<span data-ttu-id="0df9c-108">Для сценариев Возвращает или задает, откуда была создана задача.</span><span class="sxs-lookup"><span data-stu-id="0df9c-108">For scripting, gets or sets where the task originated from.</span></span> <span data-ttu-id="0df9c-109">Например, задача может исходить из компонента, службы, приложения или пользователя.</span><span class="sxs-lookup"><span data-stu-id="0df9c-109">For example, a task may originate from a component, service, application, or user.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df9c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0df9c-110">Syntax</span></span>


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a><span data-ttu-id="0df9c-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0df9c-111">Property value</span></span>

<span data-ttu-id="0df9c-112">Источник задачи.</span><span class="sxs-lookup"><span data-stu-id="0df9c-112">Where the task originated from.</span></span> <span data-ttu-id="0df9c-113">Например, из компонента, службы, приложения или пользователя.</span><span class="sxs-lookup"><span data-stu-id="0df9c-113">For example, from a component, service, application, or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df9c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0df9c-114">Remarks</span></span>

<span data-ttu-id="0df9c-115">При чтении или записи XML для задачи сведения об источнике задачи задаются с помощью [**исходного**](taskschedulerschema-source-registrationinfotype-element.md) элемента схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0df9c-115">When reading or writing XML for a task, the task source information is specified using the [**Source**](taskschedulerschema-source-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="0df9c-116">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="0df9c-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="0df9c-117">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="0df9c-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="0df9c-118">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="0df9c-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="0df9c-119">Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="0df9c-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df9c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0df9c-120">Requirements</span></span>



| <span data-ttu-id="0df9c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0df9c-121">Requirement</span></span> | <span data-ttu-id="0df9c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0df9c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0df9c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0df9c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0df9c-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0df9c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0df9c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0df9c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0df9c-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0df9c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0df9c-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0df9c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="0df9c-128"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0df9c-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0df9c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0df9c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0df9c-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0df9c-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df9c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0df9c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df9c-132">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="0df9c-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





