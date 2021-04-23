---
title: Сообщение WM_POINTERROUTEDTO
description: Отправляется при текущем вводе указателя для существующего идентификатора указателя, переходит от одного процесса к другому через содержимое, настроенное для межпроцессных цепочек (Аддконтентвискросспроцессчаининг).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415285"
---
# <a name="wm_pointerroutedto-message"></a><span data-ttu-id="94c9d-104">Сообщение WM_POINTERROUTEDTO</span><span class="sxs-lookup"><span data-stu-id="94c9d-104">WM_POINTERROUTEDTO message</span></span>

<span data-ttu-id="94c9d-105">Отправляется при текущем вводе указателя для существующего идентификатора указателя, переходит от одного процесса к другому через содержимое, настроенное для межпроцессных цепочек ([**аддконтентвискросспроцессчаининг**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="94c9d-105">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="94c9d-106">Это сообщение отправляется в процесс, не принимающий входные данные указателя.</span><span class="sxs-lookup"><span data-stu-id="94c9d-106">This message is sent to the process not currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a><span data-ttu-id="94c9d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="94c9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94c9d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94c9d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94c9d-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="94c9d-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="94c9d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94c9d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94c9d-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="94c9d-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94c9d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94c9d-112">Return value</span></span>

<span data-ttu-id="94c9d-113">NULL</span><span class="sxs-lookup"><span data-stu-id="94c9d-113">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="94c9d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94c9d-114">Remarks</span></span>

<span data-ttu-id="94c9d-115">Это сообщение не отправляется при публикации [**WM_POINTERDOWN**](wm-pointerdown.md) сообщения для нового идентификатора указателя в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="94c9d-115">This message is not sent when a [**WM_POINTERDOWN**](wm-pointerdown.md) message is posted for a new pointer ID on a different process.</span></span>

<span data-ttu-id="94c9d-116">[**WM_POINTERDOWN**](wm-pointerdown.md) сообщение не отправляется, если сначала будет отправлено **WM_POINTERROUTEDTO** сообщение.</span><span class="sxs-lookup"><span data-stu-id="94c9d-116">A [**WM_POINTERDOWN**](wm-pointerdown.md) message is not sent if a **WM_POINTERROUTEDTO** message is posted first.</span></span>

## <a name="requirements"></a><span data-ttu-id="94c9d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="94c9d-117">Requirements</span></span>



| <span data-ttu-id="94c9d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="94c9d-118">Requirement</span></span> | <span data-ttu-id="94c9d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="94c9d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94c9d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94c9d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="94c9d-121">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="94c9d-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94c9d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94c9d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="94c9d-123">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="94c9d-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94c9d-124">Header</span><span class="sxs-lookup"><span data-stu-id="94c9d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="94c9d-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94c9d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94c9d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94c9d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c9d-127">Сообщения</span><span class="sxs-lookup"><span data-stu-id="94c9d-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="94c9d-128">**WM_POINTERROUTEDAWAY**</span><span class="sxs-lookup"><span data-stu-id="94c9d-128">**WM_POINTERROUTEDAWAY**</span></span>](wm-pointerroutedaway.md)
</dt> </dl>

 

