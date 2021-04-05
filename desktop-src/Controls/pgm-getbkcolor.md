---
title: Сообщение PGM_GETBKCOLOR (Коммктрл. h)
description: Возвращает текущий цвет фона для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетбкколор пейджера.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- Элементы управления Windows для PGM_GETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803046"
---
# <a name="pgm_getbkcolor-message"></a><span data-ttu-id="747bb-105">\_Сообщение ЖЕТБККОЛОР PGM</span><span class="sxs-lookup"><span data-stu-id="747bb-105">PGM\_GETBKCOLOR message</span></span>

<span data-ttu-id="747bb-106">Возвращает текущий цвет фона для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="747bb-106">Retrieves the current background color for the pager control.</span></span> <span data-ttu-id="747bb-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетбкколор пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="747bb-107">You can send this message explicitly or use the [**Pager\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="747bb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="747bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747bb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="747bb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="747bb-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="747bb-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="747bb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="747bb-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="747bb-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="747bb-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747bb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="747bb-113">Return value</span></span>

<span data-ttu-id="747bb-114">Возвращает значение **COLORREF** , содержащее текущий цвет фона.</span><span class="sxs-lookup"><span data-stu-id="747bb-114">Returns a **COLORREF** value that contains the current background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="747bb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="747bb-115">Remarks</span></span>

<span data-ttu-id="747bb-116">По умолчанию элемент управления страничный навигатор будет использовать цвет значка системной кнопки в качестве цвета фона.</span><span class="sxs-lookup"><span data-stu-id="747bb-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="747bb-117">Это тот же цвет, который можно извлечь, вызвав [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) с \_ бтнфаце Color.</span><span class="sxs-lookup"><span data-stu-id="747bb-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="747bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="747bb-118">Requirements</span></span>



| <span data-ttu-id="747bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="747bb-119">Requirement</span></span> | <span data-ttu-id="747bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="747bb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="747bb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="747bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="747bb-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="747bb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="747bb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="747bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="747bb-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="747bb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="747bb-125">Header</span><span class="sxs-lookup"><span data-stu-id="747bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="747bb-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="747bb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

