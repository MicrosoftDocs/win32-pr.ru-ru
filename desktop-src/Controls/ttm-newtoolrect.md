---
title: Сообщение TTM_NEWTOOLRECT (Коммктрл. h)
description: Задает новый ограничивающий прямоугольник для инструмента.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- Элементы управления Windows для TTM_NEWTOOLRECT сообщений
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490671"
---
# <a name="ttm_newtoolrect-message"></a><span data-ttu-id="469a0-104">\_Сообщение ТТМ невтулрект</span><span class="sxs-lookup"><span data-stu-id="469a0-104">TTM\_NEWTOOLRECT message</span></span>

<span data-ttu-id="469a0-105">Задает новый ограничивающий прямоугольник для инструмента.</span><span class="sxs-lookup"><span data-stu-id="469a0-105">Sets a new bounding rectangle for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="469a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="469a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="469a0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="469a0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="469a0-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="469a0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="469a0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="469a0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="469a0-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="469a0-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="469a0-111">Элементы **HWND** и **uId** определяют инструмент, а член **Rect** задает новый ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="469a0-111">The **hwnd** and **uId** members identify a tool, and the **rect** member specifies the new bounding rectangle.</span></span> <span data-ttu-id="469a0-112">Перед отправкой этого сообщения необходимо заполнить элемент **кбсизе** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="469a0-112">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="469a0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="469a0-113">Return value</span></span>

<span data-ttu-id="469a0-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="469a0-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="469a0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="469a0-115">Requirements</span></span>



| <span data-ttu-id="469a0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="469a0-116">Requirement</span></span> | <span data-ttu-id="469a0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="469a0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="469a0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="469a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="469a0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="469a0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="469a0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="469a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="469a0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="469a0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="469a0-122">Header</span><span class="sxs-lookup"><span data-stu-id="469a0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="469a0-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="469a0-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="469a0-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="469a0-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="469a0-125">**ТТМ \_ НЕВТУЛРЕКТВ** (Юникод) и **ТТМ \_ невтулректа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="469a0-125">**TTM\_NEWTOOLRECTW** (Unicode) and **TTM\_NEWTOOLRECTA** (ANSI)</span></span><br/>           |



 

 





