---
title: Емаилактион. BCC, свойство
description: Для создания скриптов Возвращает или задает адрес электронной почты или адреса, которые нужно отправить в сообщении электронной почты.
ms.assetid: ab340cd7-d6ce-4dce-8474-fdbbc02bd65b
keywords:
- планировщик задач свойства скрытой копии
- Свойство скрытой копии планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство BCC
topic_type:
- apiref
api_name:
- EmailAction.Bcc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bded5e88c236123832956ce42413352348ea535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681908"
---
# <a name="emailactionbcc-property"></a><span data-ttu-id="54cf6-106">Емаилактион. BCC, свойство</span><span class="sxs-lookup"><span data-stu-id="54cf6-106">EmailAction.Bcc property</span></span>

<span data-ttu-id="54cf6-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="54cf6-107">\[This object is no longer supported.</span></span> <span data-ttu-id="54cf6-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="54cf6-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="54cf6-109">Для создания скриптов Возвращает или задает адрес электронной почты или адреса, которые нужно отправить в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="54cf6-109">For scripting, gets or sets the email address or addresses that you want to Bcc in the email message.</span></span>

<span data-ttu-id="54cf6-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="54cf6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="54cf6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54cf6-111">Syntax</span></span>


```VB
EmailAction.Bcc As String
```



## <a name="property-value"></a><span data-ttu-id="54cf6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="54cf6-112">Property value</span></span>

<span data-ttu-id="54cf6-113">Адрес электронной почты или адреса, которые нужно отправить в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="54cf6-113">The email address or addresses that you want to Bcc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cf6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="54cf6-114">Requirements</span></span>



| <span data-ttu-id="54cf6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="54cf6-115">Requirement</span></span> | <span data-ttu-id="54cf6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="54cf6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54cf6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54cf6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54cf6-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54cf6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="54cf6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54cf6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54cf6-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54cf6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54cf6-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="54cf6-121">End of client support</span></span><br/>    | <span data-ttu-id="54cf6-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54cf6-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="54cf6-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="54cf6-123">End of server support</span></span><br/>    | <span data-ttu-id="54cf6-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54cf6-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="54cf6-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="54cf6-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="54cf6-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54cf6-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54cf6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="54cf6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54cf6-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54cf6-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54cf6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54cf6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cf6-130">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="54cf6-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="54cf6-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="54cf6-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

