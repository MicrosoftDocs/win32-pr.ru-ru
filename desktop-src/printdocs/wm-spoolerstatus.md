---
description: Сообщение WM \_ спулерстатус отправляется из диспетчера печати при добавлении или удалении задания из очереди диспетчера печати.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Сообщение WM_SPOOLERSTATUS (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156647"
---
# <a name="wm_spoolerstatus-message"></a><span data-ttu-id="fd63b-103">\_Сообщение СПУЛЕРСТАТУС WM</span><span class="sxs-lookup"><span data-stu-id="fd63b-103">WM\_SPOOLERSTATUS message</span></span>

<span data-ttu-id="fd63b-104">Сообщение **WM \_ спулерстатус** отправляется из диспетчера печати при добавлении или удалении задания из очереди диспетчера печати.</span><span class="sxs-lookup"><span data-stu-id="fd63b-104">The **WM\_SPOOLERSTATUS** message is sent from Print Manager whenever a job is added to or removed from the Print Manager queue.</span></span>

<span data-ttu-id="fd63b-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fd63b-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="fd63b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd63b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd63b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd63b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd63b-108">Флаг JOBSTATUS запроса на вытягивание \_ .</span><span class="sxs-lookup"><span data-stu-id="fd63b-108">The PR\_JOBSTATUS flag.</span></span>

</dd> <dt>

<span data-ttu-id="fd63b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd63b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd63b-110">Слово нижнего порядка указывает количество заданий, остающихся в очереди диспетчера печати.</span><span class="sxs-lookup"><span data-stu-id="fd63b-110">The low-order word specifies the number of jobs remaining in the Print Manager queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd63b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd63b-111">Return value</span></span>

<span data-ttu-id="fd63b-112">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="fd63b-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd63b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd63b-113">Remarks</span></span>

<span data-ttu-id="fd63b-114">Это сообщение предназначено только для информационных целей.</span><span class="sxs-lookup"><span data-stu-id="fd63b-114">This message is for informational purposes only.</span></span> <span data-ttu-id="fd63b-115">Это сообщение является Советом и не имеет гарантированной семантики доставки.</span><span class="sxs-lookup"><span data-stu-id="fd63b-115">This message is advisory and does not have guaranteed delivery semantics.</span></span> <span data-ttu-id="fd63b-116">Приложения не должны рассчитывать на то, что они получат \_ сообщение WM спулерстатус для каждого изменения в состоянии диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="fd63b-116">Applications should not assume that they will receive a WM\_SPOOLERSTATUS message for every change in spooler status.</span></span>

<span data-ttu-id="fd63b-117">Сообщение WM \_ спулерстатус не поддерживается после Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd63b-117">The WM\_SPOOLERSTATUS message is not supported after Windows XP.</span></span> <span data-ttu-id="fd63b-118">Чтобы получать уведомления об изменениях состояния очереди печати, можно использовать [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) и [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="fd63b-118">To be notified of changes to the print queue status, you can use [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) and [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd63b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fd63b-119">Requirements</span></span>



| <span data-ttu-id="fd63b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fd63b-120">Requirement</span></span> | <span data-ttu-id="fd63b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fd63b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd63b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd63b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd63b-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fd63b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fd63b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd63b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd63b-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fd63b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fd63b-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fd63b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd63b-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd63b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd63b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd63b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd63b-129">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="fd63b-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fd63b-130">Сообщения API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="fd63b-130">Print Spooler API Messages</span></span>](printing-and-print-spooler-messages.md)
</dt> <dt>

[<span data-ttu-id="fd63b-131">**финдфирстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="fd63b-131">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="fd63b-132">**финднекстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="fd63b-132">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

