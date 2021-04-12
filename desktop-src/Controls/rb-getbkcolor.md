---
title: Сообщение RB_GETBKCOLOR (Коммктрл. h)
description: Возвращает цвет фона элемента управления главной панели по умолчанию.
ms.assetid: be90d1ce-a1f8-446d-ae64-001f7174ab05
keywords:
- Элементы управления Windows для RB_GETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- RB_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0c6f2348dfa54dc02ddc40658fd1289885ff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491766"
---
# <a name="rb_getbkcolor-message"></a><span data-ttu-id="fe0a3-104">\_Сообщение ЖЕТБККОЛОР RB</span><span class="sxs-lookup"><span data-stu-id="fe0a3-104">RB\_GETBKCOLOR message</span></span>

<span data-ttu-id="fe0a3-105">Возвращает цвет фона элемента управления главной панели по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fe0a3-105">Retrieves a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe0a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe0a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe0a3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe0a3-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fe0a3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe0a3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe0a3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fe0a3-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fe0a3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe0a3-111">Return value</span></span>

<span data-ttu-id="fe0a3-112">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее текущий цвет фона по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fe0a3-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represent the current default background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0a3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="fe0a3-113">Requirements</span></span>



| <span data-ttu-id="fe0a3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="fe0a3-114">Requirement</span></span> | <span data-ttu-id="fe0a3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fe0a3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0a3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe0a3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0a3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe0a3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe0a3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe0a3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0a3-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe0a3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe0a3-120">Header</span><span class="sxs-lookup"><span data-stu-id="fe0a3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0a3-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a3-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0a3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe0a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0a3-123">**\_СЕТБККОЛОР RB**</span><span class="sxs-lookup"><span data-stu-id="fe0a3-123">**RB\_SETBKCOLOR**</span></span>](rb-setbkcolor.md)
</dt> </dl>

 

