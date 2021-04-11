---
title: Емаилактион. ReplyTo, свойство
description: Для создания скриптов Возвращает или задает адрес электронной почты, на который вы хотите ответить.
ms.assetid: 2b267e6e-c0c9-42ca-bc4a-cc18af5bcb9c
keywords:
- ReplyTo, свойство планировщик задач
- Свойство ReplyTo планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство ReplyTo
topic_type:
- apiref
api_name:
- EmailAction.ReplyTo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7ed1fd84245e4d938d329f0e9773271efec45b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892081"
---
# <a name="emailactionreplyto-property"></a><span data-ttu-id="a62f6-106">Емаилактион. ReplyTo, свойство</span><span class="sxs-lookup"><span data-stu-id="a62f6-106">EmailAction.ReplyTo property</span></span>

<span data-ttu-id="a62f6-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a62f6-107">\[This object is no longer supported.</span></span> <span data-ttu-id="a62f6-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="a62f6-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="a62f6-109">Для создания скриптов Возвращает или задает адрес электронной почты, на который вы хотите ответить.</span><span class="sxs-lookup"><span data-stu-id="a62f6-109">For scripting, gets or sets the email address that you want to reply to.</span></span>

<span data-ttu-id="a62f6-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a62f6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62f6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a62f6-111">Syntax</span></span>


```VB
EmailAction.ReplyTo As String
```



## <a name="property-value"></a><span data-ttu-id="a62f6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a62f6-112">Property value</span></span>

<span data-ttu-id="a62f6-113">Адрес электронной почты, на который вы хотите ответить.</span><span class="sxs-lookup"><span data-stu-id="a62f6-113">The email address that you want to reply to.</span></span>

## <a name="requirements"></a><span data-ttu-id="a62f6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a62f6-114">Requirements</span></span>



| <span data-ttu-id="a62f6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a62f6-115">Requirement</span></span> | <span data-ttu-id="a62f6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a62f6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a62f6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a62f6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a62f6-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a62f6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a62f6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a62f6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a62f6-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a62f6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a62f6-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a62f6-121">End of client support</span></span><br/>    | <span data-ttu-id="a62f6-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a62f6-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="a62f6-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a62f6-123">End of server support</span></span><br/>    | <span data-ttu-id="a62f6-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a62f6-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a62f6-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a62f6-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="a62f6-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a62f6-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a62f6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a62f6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a62f6-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a62f6-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a62f6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a62f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62f6-130">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="a62f6-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="a62f6-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a62f6-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

