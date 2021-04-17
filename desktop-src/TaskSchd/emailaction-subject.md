---
title: Емаилактион. subject, свойство
description: Для создания скриптов Возвращает или задает тему сообщения электронной почты.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Свойство Subject планировщик задач
- Свойство Subject планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673121"
---
# <a name="emailactionsubject-property"></a><span data-ttu-id="d3c3f-106">Емаилактион. subject, свойство</span><span class="sxs-lookup"><span data-stu-id="d3c3f-106">EmailAction.Subject property</span></span>

<span data-ttu-id="d3c3f-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-107">\[This object is no longer supported.</span></span> <span data-ttu-id="d3c3f-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="d3c3f-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="d3c3f-109">Для создания скриптов Возвращает или задает тему сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-109">For scripting, gets or sets the subject of the email message.</span></span>

<span data-ttu-id="d3c3f-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c3f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3c3f-111">Syntax</span></span>


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a><span data-ttu-id="d3c3f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d3c3f-112">Property value</span></span>

<span data-ttu-id="d3c3f-113">Тема сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-113">The subject of the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c3f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3c3f-114">Remarks</span></span>

<span data-ttu-id="d3c3f-115">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="d3c3f-116">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="d3c3f-117">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="d3c3f-118">Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="d3c3f-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c3f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d3c3f-119">Requirements</span></span>



| <span data-ttu-id="d3c3f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d3c3f-120">Requirement</span></span> | <span data-ttu-id="d3c3f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d3c3f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c3f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3c3f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c3f-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3c3f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d3c3f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3c3f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c3f-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3c3f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3c3f-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d3c3f-126">End of client support</span></span><br/>    | <span data-ttu-id="d3c3f-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3c3f-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="d3c3f-128">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d3c3f-128">End of server support</span></span><br/>    | <span data-ttu-id="d3c3f-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3c3f-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d3c3f-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d3c3f-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3c3f-131"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d3c3f-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d3c3f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c3f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c3f-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c3f-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c3f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3c3f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c3f-135">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="d3c3f-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="d3c3f-136">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d3c3f-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

