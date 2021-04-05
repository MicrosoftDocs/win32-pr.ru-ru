---
title: Сообщение WM_POINTERROUTEDAWAY
description: Происходит в процессе получения входных данных при наведении указателя мыши на другой процесс. Аддконтентвискросспроцессчаининг).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- WM_POINTERROUTEDAWAY сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071791"
---
# <a name="wm_pointerroutedaway-message"></a><span data-ttu-id="10a25-104">Сообщение WM_POINTERROUTEDAWAY</span><span class="sxs-lookup"><span data-stu-id="10a25-104">WM_POINTERROUTEDAWAY message</span></span>

<span data-ttu-id="10a25-105">Происходит в процессе получения входных данных при наведении указателя мыши на другой процесс.</span><span class="sxs-lookup"><span data-stu-id="10a25-105">Occurs on the process receiving input when the pointer input is routed to another process.</span></span>

<span data-ttu-id="10a25-106">Посылается при переходе указателя с одного процесса на другой в содержимом, настроенном для цепочек между процессами ([**аддконтентвискросспроцессчаининг**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="10a25-106">Sent when pointer input transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="10a25-107">Это сообщение отправляется процессу, который в данный момент получает входные указатели.</span><span class="sxs-lookup"><span data-stu-id="10a25-107">This message is sent to the process currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a><span data-ttu-id="10a25-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10a25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10a25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10a25-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="10a25-110">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="10a25-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10a25-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10a25-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="10a25-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10a25-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10a25-113">Return value</span></span>

<span data-ttu-id="10a25-114">NULL</span><span class="sxs-lookup"><span data-stu-id="10a25-114">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="10a25-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10a25-115">Remarks</span></span>

<span data-ttu-id="10a25-116">Это сообщение не отправляется ни с [**WM_POINTERUP**](wm-pointerup.md) сообщением, ни с сообщением [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="10a25-116">This message is not sent with either a [**WM_POINTERUP**](wm-pointerup.md) message or a [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a25-117">Требования</span><span class="sxs-lookup"><span data-stu-id="10a25-117">Requirements</span></span>



| <span data-ttu-id="10a25-118">Требование</span><span class="sxs-lookup"><span data-stu-id="10a25-118">Requirement</span></span> | <span data-ttu-id="10a25-119">Значение</span><span class="sxs-lookup"><span data-stu-id="10a25-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a25-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10a25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10a25-121">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="10a25-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="10a25-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10a25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10a25-123">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="10a25-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10a25-124">Header</span><span class="sxs-lookup"><span data-stu-id="10a25-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10a25-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10a25-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10a25-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10a25-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a25-127">Сообщения</span><span class="sxs-lookup"><span data-stu-id="10a25-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="10a25-128">**WM_POINTERROUTEDTO**</span><span class="sxs-lookup"><span data-stu-id="10a25-128">**WM_POINTERROUTEDTO**</span></span>](wm-pointerroutedto.md)
</dt> </dl>

 

