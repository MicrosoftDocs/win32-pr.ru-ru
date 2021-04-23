---
title: Сообщение CB_GETDROPPEDCONTROLRECT (Winuser. h)
description: Приложение отправляет \_ сообщение ЖЕТДРОППЕДКОНТРОЛРЕКТ CB для получения экранных координат поля со списком в состоянии его отклонения.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- Элементы управления Windows для CB_GETDROPPEDCONTROLRECT сообщений
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491226"
---
# <a name="cb_getdroppedcontrolrect-message"></a><span data-ttu-id="db66b-104">\_Сообщение ЖЕТДРОППЕДКОНТРОЛРЕКТ CB</span><span class="sxs-lookup"><span data-stu-id="db66b-104">CB\_GETDROPPEDCONTROLRECT message</span></span>

<span data-ttu-id="db66b-105">Приложение отправляет сообщение **\_ жетдроппедконтролрект CB** для получения экранных координат поля со списком в состоянии его отклонения.</span><span class="sxs-lookup"><span data-stu-id="db66b-105">An application sends a **CB\_GETDROPPEDCONTROLRECT** message to retrieve the screen coordinates of a combo box in its dropped-down state.</span></span>

## <a name="parameters"></a><span data-ttu-id="db66b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db66b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db66b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db66b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db66b-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="db66b-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="db66b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db66b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db66b-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает координаты поля со списком в его удаленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="db66b-110">A pointer to the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the coordinates of the combo box in its dropped-down state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db66b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db66b-111">Return value</span></span>

<span data-ttu-id="db66b-112">Если сообщение прошло удачно, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="db66b-112">If the message succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="db66b-113">Если сообщение не выполняется, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="db66b-113">If the message fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="db66b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="db66b-114">Requirements</span></span>



| <span data-ttu-id="db66b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="db66b-115">Requirement</span></span> | <span data-ttu-id="db66b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="db66b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db66b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db66b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db66b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db66b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db66b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db66b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db66b-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db66b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db66b-121">Header</span><span class="sxs-lookup"><span data-stu-id="db66b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="db66b-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db66b-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db66b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db66b-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="db66b-124">[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db66b-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

