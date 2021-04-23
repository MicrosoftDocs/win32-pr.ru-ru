---
title: Сообщение TTM_DELTOOL (Коммктрл. h)
description: Удаляет инструмент из элемента управления ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- Элементы управления Windows для TTM_DELTOOL сообщений
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654506"
---
# <a name="ttm_deltool-message"></a><span data-ttu-id="5259e-104">\_Сообщение ТТМ делтул</span><span class="sxs-lookup"><span data-stu-id="5259e-104">TTM\_DELTOOL message</span></span>

<span data-ttu-id="5259e-105">Удаляет инструмент из элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="5259e-105">Removes a tool from a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5259e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5259e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5259e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5259e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5259e-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5259e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5259e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5259e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5259e-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5259e-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="5259e-111">Элементы **HWND** и **uId** определяют средство, которое необходимо удалить, а член **кбсизе** должен задавать размер структуры.</span><span class="sxs-lookup"><span data-stu-id="5259e-111">The **hwnd** and **uId** members identify the tool to remove, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="5259e-112">Все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="5259e-112">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5259e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5259e-113">Return value</span></span>

<span data-ttu-id="5259e-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="5259e-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5259e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5259e-115">Requirements</span></span>



| <span data-ttu-id="5259e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5259e-116">Requirement</span></span> | <span data-ttu-id="5259e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5259e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5259e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5259e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5259e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5259e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5259e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5259e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5259e-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5259e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5259e-122">Header</span><span class="sxs-lookup"><span data-stu-id="5259e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5259e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5259e-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5259e-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5259e-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5259e-125">**ТТМ \_ ДЕЛТУЛВ** (Юникод) и **ТТМ \_ делтула** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5259e-125">**TTM\_DELTOOLW** (Unicode) and **TTM\_DELTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="5259e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5259e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5259e-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5259e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5259e-128">**ТТМ \_ аддтул**</span><span class="sxs-lookup"><span data-stu-id="5259e-128">**TTM\_ADDTOOL**</span></span>](ttm-addtool.md)
</dt> <dt>

<span data-ttu-id="5259e-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5259e-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5259e-130">Сведения об элементах управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="5259e-130">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





