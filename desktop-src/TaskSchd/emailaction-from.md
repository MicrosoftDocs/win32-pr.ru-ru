---
title: Емаилактион. from, свойство
description: Для создания скриптов Возвращает или задает адрес электронной почты, по которому нужно отправить электронное письмо.
ms.assetid: befe6900-6fbe-4ba2-aeda-271b770e971a
keywords:
- Из свойства планировщик задач
- Из свойства планировщик задач, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство From
topic_type:
- apiref
api_name:
- EmailAction.From
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d91b132e8d56caba1a21768e4aacfdda855fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136190"
---
# <a name="emailactionfrom-property"></a><span data-ttu-id="3f47a-106">Емаилактион. from, свойство</span><span class="sxs-lookup"><span data-stu-id="3f47a-106">EmailAction.From property</span></span>

<span data-ttu-id="3f47a-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3f47a-107">\[This object is no longer supported.</span></span> <span data-ttu-id="3f47a-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="3f47a-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="3f47a-109">Для создания скриптов Возвращает или задает адрес электронной почты, по которому нужно отправить электронное письмо.</span><span class="sxs-lookup"><span data-stu-id="3f47a-109">For scripting, gets or sets the email address that you want to send the email from.</span></span>

<span data-ttu-id="3f47a-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3f47a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f47a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f47a-111">Syntax</span></span>


```VB
EmailAction.From As String
```



## <a name="property-value"></a><span data-ttu-id="3f47a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3f47a-112">Property value</span></span>

<span data-ttu-id="3f47a-113">Адрес электронной почты, с которого вы хотите отправить электронное письмо.</span><span class="sxs-lookup"><span data-stu-id="3f47a-113">The email address that you want to send the email from.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f47a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3f47a-114">Requirements</span></span>



| <span data-ttu-id="3f47a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3f47a-115">Requirement</span></span> | <span data-ttu-id="3f47a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3f47a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f47a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f47a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3f47a-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f47a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f47a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f47a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3f47a-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f47a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f47a-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3f47a-121">End of client support</span></span><br/>    | <span data-ttu-id="3f47a-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f47a-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="3f47a-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3f47a-123">End of server support</span></span><br/>    | <span data-ttu-id="3f47a-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f47a-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3f47a-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3f47a-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f47a-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f47a-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f47a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3f47a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f47a-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f47a-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f47a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f47a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f47a-130">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="3f47a-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="3f47a-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="3f47a-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

