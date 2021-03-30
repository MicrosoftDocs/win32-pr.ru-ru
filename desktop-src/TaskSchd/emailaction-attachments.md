---
title: Емаилактион. вложения, свойство
description: Для сценариев Возвращает или задает массив вложений, отправляемых с сообщением электронной почты.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- планировщик задач свойства вложения
- Свойство вложений планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство вложений
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802578"
---
# <a name="emailactionattachments-property"></a><span data-ttu-id="fbfe5-106">Емаилактион. вложения, свойство</span><span class="sxs-lookup"><span data-stu-id="fbfe5-106">EmailAction.Attachments property</span></span>

<span data-ttu-id="fbfe5-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-107">\[This object is no longer supported.</span></span> <span data-ttu-id="fbfe5-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="fbfe5-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="fbfe5-109">Для сценариев Возвращает или задает массив вложений, отправляемых с сообщением электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-109">For scripting, gets or sets an array of attachments that is sent with the email message.</span></span>

<span data-ttu-id="fbfe5-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbfe5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbfe5-111">Syntax</span></span>


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a><span data-ttu-id="fbfe5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fbfe5-112">Property value</span></span>

<span data-ttu-id="fbfe5-113">Массив вложений, отправляемых с сообщением электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-113">An array of attachments that is sent with the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbfe5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbfe5-114">Remarks</span></span>

<span data-ttu-id="fbfe5-115">В массиве вложений может быть не более восьми вложений.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-115">A maximum of eight attachments can be in the array of attachments.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbfe5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fbfe5-116">Requirements</span></span>



| <span data-ttu-id="fbfe5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fbfe5-117">Requirement</span></span> | <span data-ttu-id="fbfe5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfe5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbfe5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbfe5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fbfe5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbfe5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fbfe5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbfe5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fbfe5-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbfe5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbfe5-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fbfe5-123">End of client support</span></span><br/>    | <span data-ttu-id="fbfe5-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbfe5-124">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="fbfe5-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fbfe5-125">End of server support</span></span><br/>    | <span data-ttu-id="fbfe5-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbfe5-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="fbfe5-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fbfe5-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbfe5-128"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fbfe5-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fbfe5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fbfe5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbfe5-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbfe5-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbfe5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbfe5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbfe5-132">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="fbfe5-132">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="fbfe5-133">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fbfe5-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

