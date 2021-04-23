---
title: Сообщение TTM_GETBUBBLESIZE (Коммктрл. h)
description: Возвращает ширину и высоту элемента управления ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Элементы управления Windows для TTM_GETBUBBLESIZE сообщений
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135946"
---
# <a name="ttm_getbubblesize-message"></a><span data-ttu-id="102c0-104">\_Сообщение ТТМ жетбубблесизе</span><span class="sxs-lookup"><span data-stu-id="102c0-104">TTM\_GETBUBBLESIZE message</span></span>

<span data-ttu-id="102c0-105">Возвращает ширину и высоту элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="102c0-105">Returns the width and height of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="102c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="102c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102c0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="102c0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="102c0-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="102c0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="102c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="102c0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="102c0-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ToolTip.</span><span class="sxs-lookup"><span data-stu-id="102c0-110">Pointer to the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102c0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="102c0-111">Return value</span></span>

<span data-ttu-id="102c0-112">Возвращает ширину подсказки в нижнем слове и высоту в высоком слове в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="102c0-112">Returns the width of the tooltip in the low word and the height in the high word if successful.</span></span> <span data-ttu-id="102c0-113">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="102c0-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="102c0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="102c0-114">Remarks</span></span>

<span data-ttu-id="102c0-115">Если \_ Флаги TTF Track и TTF \_ заданы в элементе **Уфлагс** структуры подсказки [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , это сообщение можно использовать для точного размещения подсказки.</span><span class="sxs-lookup"><span data-stu-id="102c0-115">If the TTF\_TRACK and TTF\_ABSOLUTE flags are set in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, this message can be used to help position the tooltip accurately.</span></span>

## <a name="requirements"></a><span data-ttu-id="102c0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="102c0-116">Requirements</span></span>



| <span data-ttu-id="102c0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="102c0-117">Requirement</span></span> | <span data-ttu-id="102c0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="102c0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="102c0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="102c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="102c0-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="102c0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="102c0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="102c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="102c0-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="102c0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="102c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="102c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="102c0-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="102c0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





