---
title: Емаилактион. Server, свойство
description: Для создания скриптов Возвращает или задает имя SMTP-сервера, который используется для отправки электронной почты.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- планировщик задач свойств сервера
- Свойство сервера планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство сервера
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340770"
---
# <a name="emailactionserver-property"></a><span data-ttu-id="e361e-106">Емаилактион. Server, свойство</span><span class="sxs-lookup"><span data-stu-id="e361e-106">EmailAction.Server property</span></span>

<span data-ttu-id="e361e-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e361e-107">\[This object is no longer supported.</span></span> <span data-ttu-id="e361e-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="e361e-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="e361e-109">Для создания скриптов Возвращает или задает имя SMTP-сервера, который используется для отправки электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e361e-109">For scripting, gets or sets the name of the SMTP server that you use to send email from.</span></span>

<span data-ttu-id="e361e-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e361e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e361e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e361e-111">Syntax</span></span>


```VB
EmailAction.Server As String
```



## <a name="property-value"></a><span data-ttu-id="e361e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e361e-112">Property value</span></span>

<span data-ttu-id="e361e-113">Имя сервера, который используется для отправки электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e361e-113">The name of the server that you use to send email from.</span></span>

## <a name="remarks"></a><span data-ttu-id="e361e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e361e-114">Remarks</span></span>

<span data-ttu-id="e361e-115">Убедитесь, что SMTP-сервер, который отправляет сообщение, правильно настроен.</span><span class="sxs-lookup"><span data-stu-id="e361e-115">Make sure the SMTP server that sends the email is setup correctly.</span></span> <span data-ttu-id="e361e-116">Электронная почта отправляется с использованием проверки подлинности NTLM для SMTP-серверов Windows. Это означает, что учетные данные безопасности, используемые для выполнения задачи, также должны иметь права доступа на SMTP-сервере для отправки сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e361e-116">E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message.</span></span> <span data-ttu-id="e361e-117">Если SMTP-сервер является сервером, отличным от Windows, то сообщение электронной почты будет отправлено, если сервер разрешает анонимный доступ.</span><span class="sxs-lookup"><span data-stu-id="e361e-117">If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.</span></span> <span data-ttu-id="e361e-118">Сведения о настройке SMTP-сервера см. в разделе [Настройка SMTP-](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)сервера, а сведения об управлении параметрами SMTP-сервера см. в разделе [Администрирование SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="e361e-118">For information about setting up the SMTP server, see [SMTP Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true), and for information about managing SMTP server settings, see [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e361e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e361e-119">Requirements</span></span>



| <span data-ttu-id="e361e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e361e-120">Requirement</span></span> | <span data-ttu-id="e361e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e361e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e361e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e361e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e361e-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e361e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e361e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e361e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e361e-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e361e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e361e-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e361e-126">End of client support</span></span><br/>    | <span data-ttu-id="e361e-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e361e-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e361e-128">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e361e-128">End of server support</span></span><br/>    | <span data-ttu-id="e361e-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e361e-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e361e-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e361e-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="e361e-131"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e361e-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e361e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e361e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e361e-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e361e-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e361e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e361e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e361e-135">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="e361e-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="e361e-136">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e361e-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

