---
title: Код уведомления TDN_TIMER (Коммктрл. h)
description: Отправляется диалоговым окном задачи примерно каждые 200 миллисекунд.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654697"
---
# <a name="tdn_timer-notification-code"></a><span data-ttu-id="d05c0-104">\_Код уведомления о таймере ТДН</span><span class="sxs-lookup"><span data-stu-id="d05c0-104">TDN\_TIMER notification code</span></span>

<span data-ttu-id="d05c0-105">Отправляется диалоговым окном задачи примерно каждые 200 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="d05c0-105">Sent by a task dialog approximately every 200 milliseconds.</span></span> <span data-ttu-id="d05c0-106">Этот код уведомления отправляется, если \_ флаг таймера обратного вызова TDF \_ задан в элементе **dwFlags** структуры [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , переданной в функцию [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="d05c0-106">This notification code is sent when the TDF\_CALLBACK\_TIMER flag has been set in the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that was passed to the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="d05c0-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода **таскдиалогиндирект** .</span><span class="sxs-lookup"><span data-stu-id="d05c0-107">This notification code is received only through the task dialog callback function, which can be registered using the **TaskDialogIndirect** method.</span></span>


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="d05c0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d05c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d05c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d05c0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d05c0-110">Значение **типа DWORD** , указывающее количество миллисекунд, прошедших с момента создания диалогового окна или возвращенного этим кодом уведомления **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="d05c0-110">A **DWORD** that specifies the number of milliseconds since the dialog was created or this notification code returned **S\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d05c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d05c0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d05c0-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d05c0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d05c0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d05c0-113">Return value</span></span>

<span data-ttu-id="d05c0-114">Чтобы сбросить значение TickCount, приложение должно вернуть **\_ значение false**. в противном случае значение TickCount продолжит расти.</span><span class="sxs-lookup"><span data-stu-id="d05c0-114">To reset the tickcount, the application must return **S\_FALSE**, otherwise the tickcount will continue to increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="d05c0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d05c0-115">Requirements</span></span>



| <span data-ttu-id="d05c0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d05c0-116">Requirement</span></span> | <span data-ttu-id="d05c0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d05c0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d05c0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d05c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d05c0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d05c0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d05c0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d05c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d05c0-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d05c0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d05c0-122">Header</span><span class="sxs-lookup"><span data-stu-id="d05c0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d05c0-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d05c0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





