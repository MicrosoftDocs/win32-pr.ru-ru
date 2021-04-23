---
title: Сообщение TTM_ADDTOOL (Коммктрл. h)
description: Регистрирует инструмент с помощью элемента управления ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Элементы управления Windows для TTM_ADDTOOL сообщений
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654507"
---
# <a name="ttm_addtool-message"></a><span data-ttu-id="1e080-104">\_Сообщение ТТМ аддтул</span><span class="sxs-lookup"><span data-stu-id="1e080-104">TTM\_ADDTOOL message</span></span>

<span data-ttu-id="1e080-105">Регистрирует инструмент с помощью элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="1e080-105">Registers a tool with a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e080-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e080-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e080-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e080-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1e080-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1e080-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1e080-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e080-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e080-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , содержащую сведения, необходимые элементу управления ToolTip для показа текста для инструмента.</span><span class="sxs-lookup"><span data-stu-id="1e080-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure containing information that the tooltip control needs to display text for the tool.</span></span> <span data-ttu-id="1e080-111">Перед отправкой этого сообщения необходимо заполнить элемент **кбсизе** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="1e080-111">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e080-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e080-112">Return value</span></span>

<span data-ttu-id="1e080-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1e080-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e080-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1e080-114">Requirements</span></span>



| <span data-ttu-id="1e080-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1e080-115">Requirement</span></span> | <span data-ttu-id="1e080-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1e080-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e080-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e080-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1e080-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e080-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e080-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e080-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1e080-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e080-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e080-121">Header</span><span class="sxs-lookup"><span data-stu-id="1e080-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e080-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e080-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1e080-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="1e080-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1e080-124">**ТТМ \_ АДДТУЛВ** (Юникод) и **ТТМ \_ аддтула** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1e080-124">**TTM\_ADDTOOLW** (Unicode) and **TTM\_ADDTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="1e080-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e080-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e080-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1e080-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e080-127">**ТТМ \_ делтул**</span><span class="sxs-lookup"><span data-stu-id="1e080-127">**TTM\_DELTOOL**</span></span>](ttm-deltool.md)
</dt> <dt>

<span data-ttu-id="1e080-128">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1e080-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e080-129">Сведения об элементах управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="1e080-129">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





