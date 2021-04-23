---
title: Сообщение PGM_RECALCSIZE (Коммктрл. h)
description: Заставляет элемент управления страничного навигатора повторно вычислить размер автономного окна. Отправка этого сообщения приведет к \_ отправке уведомления ПГН калксизе. Это сообщение можно отправить явным образом или использовать \_ макрос Рекалксизе пейджера.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- Элементы управления Windows для PGM_RECALCSIZE сообщений
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490203"
---
# <a name="pgm_recalcsize-message"></a><span data-ttu-id="d36c2-106">\_Сообщение РЕКАЛКСИЗЕ PGM</span><span class="sxs-lookup"><span data-stu-id="d36c2-106">PGM\_RECALCSIZE message</span></span>

<span data-ttu-id="d36c2-107">Заставляет элемент управления страничного навигатора повторно вычислить размер автономного окна.</span><span class="sxs-lookup"><span data-stu-id="d36c2-107">Forces the pager control to recalculate the size of the contained window.</span></span> <span data-ttu-id="d36c2-108">Отправка этого сообщения приведет к отправке уведомления [ПГН \_ калксизе](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="d36c2-108">Sending this message will result in a [PGN\_CALCSIZE](pgn-calcsize.md) notification being sent.</span></span> <span data-ttu-id="d36c2-109">Это сообщение можно отправить явным образом или использовать макрос [**\_ рекалксизе пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .</span><span class="sxs-lookup"><span data-stu-id="d36c2-109">You can send this message explicitly or use the [**Pager\_RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d36c2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d36c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d36c2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d36c2-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d36c2-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d36c2-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d36c2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d36c2-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d36c2-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d36c2-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d36c2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d36c2-115">Return value</span></span>

<span data-ttu-id="d36c2-116">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="d36c2-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d36c2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d36c2-117">Requirements</span></span>



| <span data-ttu-id="d36c2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d36c2-118">Requirement</span></span> | <span data-ttu-id="d36c2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d36c2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d36c2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d36c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d36c2-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d36c2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d36c2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d36c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d36c2-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d36c2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d36c2-124">Header</span><span class="sxs-lookup"><span data-stu-id="d36c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d36c2-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d36c2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





