---
description: Посылается всем окнам верхнего уровня, когда система обнаруживает более 12,5% системного времени в течение 30 – 60-секундного интервала, который тратится на сжатие памяти. Это означает, что недостаточно памяти системы.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Сообщение WM_COMPACTING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702579"
---
# <a name="wm_compacting-message"></a><span data-ttu-id="41bcd-104">\_Сообщение о сжатии WM</span><span class="sxs-lookup"><span data-stu-id="41bcd-104">WM\_COMPACTING message</span></span>

<span data-ttu-id="41bcd-105">Посылается всем окнам верхнего уровня, когда система обнаруживает более 12,5% системного времени в течение 30 – 60-секундного интервала, который тратится на сжатие памяти.</span><span class="sxs-lookup"><span data-stu-id="41bcd-105">Sent to all top-level windows when the system detects more than 12.5 percent of system time over a 30- to 60-second interval is being spent compacting memory.</span></span> <span data-ttu-id="41bcd-106">Это означает, что недостаточно памяти системы.</span><span class="sxs-lookup"><span data-stu-id="41bcd-106">This indicates that system memory is low.</span></span>

<span data-ttu-id="41bcd-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="41bcd-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="41bcd-108">Это сообщение предоставляется только для обеспечения совместимости с 16-разрядными приложениями на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="41bcd-108">This message is provided only for compatibility with 16-bit Windows-based applications.</span></span>

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a><span data-ttu-id="41bcd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="41bcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41bcd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41bcd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41bcd-111">Отношение времени центрального процессора (ЦП), которое в данный момент затрачено системной сжатой памятью, к времени ЦП, затраченному системой на выполнение других операций.</span><span class="sxs-lookup"><span data-stu-id="41bcd-111">The ratio of central processing unit (CPU) time currently spent by the system compacting memory to CPU time currently spent by the system performing other operations.</span></span> <span data-ttu-id="41bcd-112">Например, 0x8000 представляет 50% времени ЦП, затраченного на сжатие памяти.</span><span class="sxs-lookup"><span data-stu-id="41bcd-112">For example, 0x8000 represents 50 percent of CPU time spent compacting memory.</span></span>

</dd> <dt>

<span data-ttu-id="41bcd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41bcd-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41bcd-114">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="41bcd-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41bcd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41bcd-115">Return value</span></span>

<span data-ttu-id="41bcd-116">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="41bcd-116">Type: **LRESULT**</span></span>

<span data-ttu-id="41bcd-117">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="41bcd-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="41bcd-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41bcd-118">Remarks</span></span>

<span data-ttu-id="41bcd-119">Когда приложение получает это сообщение, оно должно освободить максимально возможный объем памяти, принимая во внимание текущий уровень активности приложения и общее число приложений, выполняющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="41bcd-119">When an application receives this message, it should free as much memory as possible, taking into account the current level of activity of the application and the total number of applications running on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="41bcd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="41bcd-120">Requirements</span></span>



| <span data-ttu-id="41bcd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="41bcd-121">Requirement</span></span> | <span data-ttu-id="41bcd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="41bcd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41bcd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41bcd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41bcd-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41bcd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41bcd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41bcd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41bcd-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41bcd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41bcd-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="41bcd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="41bcd-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41bcd-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41bcd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41bcd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41bcd-130">Обзор Windows</span><span class="sxs-lookup"><span data-stu-id="41bcd-130">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
