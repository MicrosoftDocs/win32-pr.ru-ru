---
title: Сообщение ACM_STOP (Коммктрл. h)
description: Останавливает воспроизведение фрагмента AVI в элементе управления Animation. Это сообщение можно отправить явным образом или с помощью \_ макроса анимации.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- Элементы управления Windows для ACM_STOP сообщений
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135371"
---
# <a name="acm_stop-message"></a><span data-ttu-id="c020e-105">Сообщение о фатальной ошибке ACM \_</span><span class="sxs-lookup"><span data-stu-id="c020e-105">ACM\_STOP message</span></span>

<span data-ttu-id="c020e-106">Останавливает воспроизведение фрагмента AVI в элементе управления Animation.</span><span class="sxs-lookup"><span data-stu-id="c020e-106">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="c020e-107">Это сообщение можно отправить явным образом или с помощью макроса [**анимации \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .</span><span class="sxs-lookup"><span data-stu-id="c020e-107">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c020e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c020e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c020e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c020e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c020e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c020e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c020e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c020e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c020e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c020e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c020e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c020e-113">Return value</span></span>

<span data-ttu-id="c020e-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c020e-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c020e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c020e-115">Requirements</span></span>



| <span data-ttu-id="c020e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c020e-116">Requirement</span></span> | <span data-ttu-id="c020e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c020e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c020e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c020e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c020e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c020e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c020e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c020e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c020e-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c020e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c020e-122">Header</span><span class="sxs-lookup"><span data-stu-id="c020e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c020e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c020e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





