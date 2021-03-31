---
title: Сообщение PGM_SETBKCOLOR (Коммктрл. h)
description: Задает текущий цвет фона для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Сетбкколор пейджера.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- Элементы управления Windows для PGM_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135714"
---
# <a name="pgm_setbkcolor-message"></a><span data-ttu-id="c3f78-105">\_Сообщение СЕТБККОЛОР PGM</span><span class="sxs-lookup"><span data-stu-id="c3f78-105">PGM\_SETBKCOLOR message</span></span>

<span data-ttu-id="c3f78-106">Задает текущий цвет фона для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="c3f78-106">Sets the current background color for the pager control.</span></span> <span data-ttu-id="c3f78-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетбкколор пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="c3f78-107">You can send this message explicitly or use the [**Pager\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3f78-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3f78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f78-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3f78-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c3f78-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c3f78-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c3f78-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3f78-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3f78-112">Значение **COLORREF** , содержащее новый цвет фона для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="c3f78-112">**COLORREF** value that contains the new background color of the pager control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f78-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3f78-113">Return value</span></span>

<span data-ttu-id="c3f78-114">Возвращает значение **COLORREF** , содержащее предыдущий цвет фона.</span><span class="sxs-lookup"><span data-stu-id="c3f78-114">Returns a **COLORREF** value that contains the previous background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f78-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3f78-115">Remarks</span></span>

<span data-ttu-id="c3f78-116">По умолчанию элемент управления страничный навигатор будет использовать цвет значка системной кнопки в качестве цвета фона.</span><span class="sxs-lookup"><span data-stu-id="c3f78-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="c3f78-117">Это тот же цвет, который можно извлечь, вызвав [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) с \_ бтнфаце Color.</span><span class="sxs-lookup"><span data-stu-id="c3f78-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f78-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c3f78-118">Requirements</span></span>



| <span data-ttu-id="c3f78-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c3f78-119">Requirement</span></span> | <span data-ttu-id="c3f78-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c3f78-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f78-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3f78-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f78-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3f78-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3f78-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3f78-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f78-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3f78-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3f78-125">Header</span><span class="sxs-lookup"><span data-stu-id="c3f78-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f78-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3f78-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

