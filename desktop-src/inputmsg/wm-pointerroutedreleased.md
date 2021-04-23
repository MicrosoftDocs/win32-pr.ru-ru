---
title: Сообщение WM_POINTERROUTEDRELEASED
description: Посылается всем процессам (настроенным для межпроцессных цепочек через Аддконтентвискросспроцессчаининг, которые в настоящее время не обрабатывают ввод указателя) при получении сообщения WM_POINTERUP в текущем процессе.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415560"
---
# <a name="wm_pointerroutedreleased-message"></a><span data-ttu-id="0c62f-104">Сообщение WM_POINTERROUTEDRELEASED</span><span class="sxs-lookup"><span data-stu-id="0c62f-104">WM_POINTERROUTEDRELEASED message</span></span>

<span data-ttu-id="0c62f-105">Посылается всем процессам (настроенным для межпроцессных цепочек через [**аддконтентвискросспроцессчаининг**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) , которые в настоящее время не обрабатывают ввод указателя) при получении сообщения [**WM_POINTERUP**](wm-pointerup.md) в текущем процессе.</span><span class="sxs-lookup"><span data-stu-id="0c62f-105">Sent to all processes (configured for cross-process chaining through [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [**WM_POINTERUP**](wm-pointerup.md) message is received on the current process.</span></span>


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a><span data-ttu-id="0c62f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c62f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c62f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c62f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c62f-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0c62f-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="0c62f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c62f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c62f-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0c62f-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c62f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c62f-111">Return value</span></span>

<span data-ttu-id="0c62f-112">NULL</span><span class="sxs-lookup"><span data-stu-id="0c62f-112">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="0c62f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0c62f-113">Requirements</span></span>



| <span data-ttu-id="0c62f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0c62f-114">Requirement</span></span> | <span data-ttu-id="0c62f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0c62f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c62f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c62f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c62f-117">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0c62f-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c62f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c62f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c62f-119">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="0c62f-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c62f-120">Header</span><span class="sxs-lookup"><span data-stu-id="0c62f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c62f-121"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c62f-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c62f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c62f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c62f-123">Сообщения</span><span class="sxs-lookup"><span data-stu-id="0c62f-123">Messages</span></span>](messages.md)
</dt> </dl>

 

