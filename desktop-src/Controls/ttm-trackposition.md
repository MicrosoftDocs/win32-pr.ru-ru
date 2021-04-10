---
title: Сообщение TTM_TRACKPOSITION (Коммктрл. h)
description: Задает расположение подсказки для отслеживания.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Элементы управления Windows для TTM_TRACKPOSITION сообщений
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071775"
---
# <a name="ttm_trackposition-message"></a><span data-ttu-id="3b306-104">\_Сообщение ТТМ траккпоситион</span><span class="sxs-lookup"><span data-stu-id="3b306-104">TTM\_TRACKPOSITION message</span></span>

<span data-ttu-id="3b306-105">Задает расположение подсказки для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="3b306-105">Sets the position of a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b306-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b306-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b306-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b306-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3b306-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3b306-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b306-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b306-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Указывает координату x точки, в которой будет отображаться подсказка отслеживания, в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="3b306-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span> <span data-ttu-id="3b306-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Указывает координату y точки, в которой будет отображаться подсказка отслеживания, в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="3b306-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b306-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b306-112">Return value</span></span>

<span data-ttu-id="3b306-113">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="3b306-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b306-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b306-114">Remarks</span></span>

<span data-ttu-id="3b306-115">Элемент управления ToolTip выбирает, где отображать окно подсказки в соответствии с координатами, предоставленными этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="3b306-115">The tooltip control chooses where to display the tooltip window based on the coordinates you provide with this message.</span></span> <span data-ttu-id="3b306-116">В результате окно подсказки появится рядом с инструментом, которому оно соответствует.</span><span class="sxs-lookup"><span data-stu-id="3b306-116">This causes the tooltip window to appear beside the tool to which it corresponds.</span></span> <span data-ttu-id="3b306-117">Чтобы окна подсказки отображались по конкретным координатам, включите флаг "TTF \_ Absolute" в элемент **Уфлагс** структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) при добавлении средства.</span><span class="sxs-lookup"><span data-stu-id="3b306-117">To have tooltip windows displayed at specific coordinates, include the TTF\_ABSOLUTE flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when adding the tool.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b306-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3b306-118">Requirements</span></span>



| <span data-ttu-id="3b306-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3b306-119">Requirement</span></span> | <span data-ttu-id="3b306-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3b306-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b306-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b306-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b306-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b306-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b306-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b306-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b306-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b306-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b306-125">Header</span><span class="sxs-lookup"><span data-stu-id="3b306-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b306-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b306-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b306-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b306-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b306-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3b306-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b306-129">**ТТМ \_ траккактивате**</span><span class="sxs-lookup"><span data-stu-id="3b306-129">**TTM\_TRACKACTIVATE**</span></span>](ttm-trackactivate.md)
</dt> <dt>

<span data-ttu-id="3b306-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3b306-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3b306-131">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="3b306-131">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

