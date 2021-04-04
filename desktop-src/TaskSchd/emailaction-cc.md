---
title: EmailAction.Cc, свойство
description: Для создания скриптов Возвращает или задает адрес электронной почты или адреса, которые нужно отправить в сообщении электронной почты.
ms.assetid: 4ad67064-3e6b-4666-a3ce-66e4dcc3f873
keywords:
- планировщик задач свойства CC
- Свойство CC планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство CC
topic_type:
- apiref
api_name:
- EmailAction.Cc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f05d7fbd1883aa38ba972eba1eb14767349357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802573"
---
# <a name="emailactioncc-property"></a><span data-ttu-id="aa8f7-106">EmailAction.Cc, свойство</span><span class="sxs-lookup"><span data-stu-id="aa8f7-106">EmailAction.Cc property</span></span>

<span data-ttu-id="aa8f7-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-107">\[This object is no longer supported.</span></span> <span data-ttu-id="aa8f7-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="aa8f7-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="aa8f7-109">Для создания скриптов Возвращает или задает адрес электронной почты или адреса, которые нужно отправить в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-109">For scripting, gets or sets the email address or addresses that you want to Cc in the email message.</span></span>

<span data-ttu-id="aa8f7-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa8f7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa8f7-111">Syntax</span></span>


```VB
EmailAction.Cc As String
```



## <a name="property-value"></a><span data-ttu-id="aa8f7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aa8f7-112">Property value</span></span>

<span data-ttu-id="aa8f7-113">Адрес электронной почты или адреса, которые вы хотите отправить в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-113">The email address or addresses that you want to Cc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8f7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aa8f7-114">Requirements</span></span>



| <span data-ttu-id="aa8f7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aa8f7-115">Requirement</span></span> | <span data-ttu-id="aa8f7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aa8f7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8f7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa8f7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8f7-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa8f7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa8f7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa8f7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8f7-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa8f7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa8f7-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="aa8f7-121">End of client support</span></span><br/>    | <span data-ttu-id="aa8f7-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa8f7-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="aa8f7-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="aa8f7-123">End of server support</span></span><br/>    | <span data-ttu-id="aa8f7-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa8f7-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="aa8f7-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="aa8f7-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa8f7-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa8f7-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa8f7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="aa8f7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa8f7-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa8f7-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa8f7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa8f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa8f7-130">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="aa8f7-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="aa8f7-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="aa8f7-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

