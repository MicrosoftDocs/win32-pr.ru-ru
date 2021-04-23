---
title: Сообщение WM_DWMCOLORIZATIONCOLORCHANGED (Winuser. h)
description: Информирует все окна верхнего уровня о том, что цвет цветов изменился.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- Сообщение WM_DWMCOLORIZATIONCOLORCHANGED диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136074"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a><span data-ttu-id="38e90-104">\_Сообщение ДВМКОЛОРИЗАТИОНКОЛОРЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="38e90-104">WM\_DWMCOLORIZATIONCOLORCHANGED message</span></span>

<span data-ttu-id="38e90-105">Информирует все окна верхнего уровня о том, что цвет цветов изменился.</span><span class="sxs-lookup"><span data-stu-id="38e90-105">Informs all top-level windows that the colorization color has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="38e90-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38e90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38e90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38e90-108">Указывает новый цвет раскраски.</span><span class="sxs-lookup"><span data-stu-id="38e90-108">Specifies the new colorization color.</span></span> <span data-ttu-id="38e90-109">Цветовой формат — 0xAARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="38e90-109">The color format is 0xAARRGGBB.</span></span>

</dd> <dt>

<span data-ttu-id="38e90-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38e90-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38e90-111">Указывает, смешивается ли новый цвет с непрозрачностью.</span><span class="sxs-lookup"><span data-stu-id="38e90-111">Specifies whether the new color is blended with opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38e90-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38e90-112">Return value</span></span>

<span data-ttu-id="38e90-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="38e90-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e90-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38e90-114">Remarks</span></span>

<span data-ttu-id="38e90-115">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="38e90-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="38e90-116">[**Двмжетколоризатионколор**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) используется для определения текущего значения цвета.</span><span class="sxs-lookup"><span data-stu-id="38e90-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) is used to determine the current color value.</span></span>

## <a name="requirements"></a><span data-ttu-id="38e90-117">Требования</span><span class="sxs-lookup"><span data-stu-id="38e90-117">Requirements</span></span>



| <span data-ttu-id="38e90-118">Требование</span><span class="sxs-lookup"><span data-stu-id="38e90-118">Requirement</span></span> | <span data-ttu-id="38e90-119">Значение</span><span class="sxs-lookup"><span data-stu-id="38e90-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="38e90-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38e90-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38e90-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38e90-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="38e90-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38e90-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38e90-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38e90-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="38e90-124">Header</span><span class="sxs-lookup"><span data-stu-id="38e90-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38e90-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="38e90-125"><dt>Winuser.h</dt></span></span> </dl> |



 

