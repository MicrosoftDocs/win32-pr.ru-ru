---
title: Емаилактион. Хеадерфиелдс, свойство
description: Для создания скриптов Возвращает или задает сведения о заголовке электронного письма, которое необходимо отправить.
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- планировщик задач свойства Хеадерфиелдс
- Планировщик задач свойства Хеадерфиелдс, объект Емаилактион
- Планировщик задач объекта Емаилактион, свойство Хеадерфиелдс
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cfb963879e47e51e1096d2559fe4e72c6b2543
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892082"
---
# <a name="emailactionheaderfields-property"></a><span data-ttu-id="28175-106">Емаилактион. Хеадерфиелдс, свойство</span><span class="sxs-lookup"><span data-stu-id="28175-106">EmailAction.HeaderFields property</span></span>

<span data-ttu-id="28175-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="28175-107">\[This object is no longer supported.</span></span> <span data-ttu-id="28175-108">Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.\]</span><span class="sxs-lookup"><span data-stu-id="28175-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="28175-109">Для создания скриптов Возвращает или задает сведения о заголовке электронного письма, которое необходимо отправить.</span><span class="sxs-lookup"><span data-stu-id="28175-109">For scripting, gets or sets the header information in the email you want to send.</span></span>

<span data-ttu-id="28175-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="28175-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="28175-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28175-111">Syntax</span></span>


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a><span data-ttu-id="28175-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="28175-112">Property value</span></span>

<span data-ttu-id="28175-113">Сведения заголовка в сообщении электронной почты, которое необходимо отправить.</span><span class="sxs-lookup"><span data-stu-id="28175-113">The header information in the email you want to send.</span></span>

## <a name="requirements"></a><span data-ttu-id="28175-114">Требования</span><span class="sxs-lookup"><span data-stu-id="28175-114">Requirements</span></span>



| <span data-ttu-id="28175-115">Требование</span><span class="sxs-lookup"><span data-stu-id="28175-115">Requirement</span></span> | <span data-ttu-id="28175-116">Значение</span><span class="sxs-lookup"><span data-stu-id="28175-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28175-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28175-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28175-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28175-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="28175-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28175-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28175-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28175-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28175-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="28175-121">End of client support</span></span><br/>    | <span data-ttu-id="28175-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28175-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="28175-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="28175-123">End of server support</span></span><br/>    | <span data-ttu-id="28175-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28175-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="28175-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="28175-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="28175-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="28175-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="28175-127">DLL</span><span class="sxs-lookup"><span data-stu-id="28175-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28175-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28175-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28175-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28175-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28175-130">**емаилактион**</span><span class="sxs-lookup"><span data-stu-id="28175-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="28175-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="28175-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

