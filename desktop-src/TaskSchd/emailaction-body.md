---
title: Емаилактион. Body, свойство
description: Для сценариев Возвращает или задает текст сообщения электронной почты, содержащего сообщение электронной почты.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Свойство Body планировщик задач
- Свойство Body планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672687"
---
# <a name="emailactionbody-property"></a><span data-ttu-id="dc956-106">Емаилактион. Body, свойство</span><span class="sxs-lookup"><span data-stu-id="dc956-106">EmailAction.Body property</span></span>

<span data-ttu-id="dc956-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc956-107">\[This object is no longer supported.</span></span> <span data-ttu-id="dc956-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="dc956-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="dc956-109">Для сценариев Возвращает или задает текст сообщения электронной почты, содержащего сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="dc956-109">For scripting, gets or sets the body of the email that contains the email message.</span></span>

<span data-ttu-id="dc956-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dc956-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc956-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc956-111">Syntax</span></span>


```VB
EmailAction.Body As String
```



## <a name="property-value"></a><span data-ttu-id="dc956-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dc956-112">Property value</span></span>

<span data-ttu-id="dc956-113">Текст сообщения электронной почты, содержащего сообщение.</span><span class="sxs-lookup"><span data-stu-id="dc956-113">The body of the email that contains the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc956-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc956-114">Remarks</span></span>

<span data-ttu-id="dc956-115">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="dc956-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="dc956-116">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="dc956-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="dc956-117">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="dc956-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="dc956-118">Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="dc956-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc956-119">Требования</span><span class="sxs-lookup"><span data-stu-id="dc956-119">Requirements</span></span>



| <span data-ttu-id="dc956-120">Требование</span><span class="sxs-lookup"><span data-stu-id="dc956-120">Requirement</span></span> | <span data-ttu-id="dc956-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dc956-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc956-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc956-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc956-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc956-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dc956-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc956-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc956-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc956-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc956-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dc956-126">End of client support</span></span><br/>    | <span data-ttu-id="dc956-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dc956-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="dc956-128">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="dc956-128">End of server support</span></span><br/>    | <span data-ttu-id="dc956-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc956-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="dc956-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dc956-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc956-131"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc956-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc956-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dc956-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc956-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc956-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc956-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc956-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc956-135">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="dc956-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="dc956-136">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="dc956-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

