---
title: Сообщение TB_SETBUTTONWIDTH (Коммктрл. h)
description: Задает минимальную и максимальную ширину кнопок в элементе управления ToolBar.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Элементы управления Windows для TB_SETBUTTONWIDTH сообщений
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135951"
---
# <a name="tb_setbuttonwidth-message"></a><span data-ttu-id="9cae3-104">\_Сообщение СЕТБУТТОНВИДС ТБ</span><span class="sxs-lookup"><span data-stu-id="9cae3-104">TB\_SETBUTTONWIDTH message</span></span>

<span data-ttu-id="9cae3-105">Задает минимальную и максимальную ширину кнопок в элементе управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="9cae3-105">Sets the minimum and maximum button widths in the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9cae3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cae3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cae3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cae3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cae3-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9cae3-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9cae3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cae3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cae3-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает минимальную ширину кнопки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9cae3-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum button width, in pixels.</span></span> <span data-ttu-id="9cae3-111">Кнопки панели инструментов никогда не будут более узкими, чем это значение.</span><span class="sxs-lookup"><span data-stu-id="9cae3-111">Toolbar buttons will never be narrower than this value.</span></span>

<span data-ttu-id="9cae3-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает максимальную ширину кнопки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9cae3-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum button width, in pixels.</span></span> <span data-ttu-id="9cae3-113">Если текст кнопки слишком широк, элемент управления отображает его с помощью точек многоточия.</span><span class="sxs-lookup"><span data-stu-id="9cae3-113">If button text is too wide, the control displays it with ellipsis points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cae3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cae3-114">Return value</span></span>

<span data-ttu-id="9cae3-115">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9cae3-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cae3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cae3-116">Remarks</span></span>

<span data-ttu-id="9cae3-117">Используйте **ТБ \_ сетбуттонвидс** , чтобы задать максимальную и минимальную допустимую ширину для кнопок перед их добавлением.</span><span class="sxs-lookup"><span data-stu-id="9cae3-117">Use **TB\_SETBUTTONWIDTH** to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="9cae3-118">Чтобы задать фактический размер кнопок, используйте [**\_ сетбуттонсизе ТБ**](tb-setbuttonsize.md) .</span><span class="sxs-lookup"><span data-stu-id="9cae3-118">Use [**TB\_SETBUTTONSIZE**](tb-setbuttonsize.md) to set the actual size of buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cae3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9cae3-119">Requirements</span></span>



| <span data-ttu-id="9cae3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9cae3-120">Requirement</span></span> | <span data-ttu-id="9cae3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9cae3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cae3-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cae3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9cae3-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cae3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9cae3-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cae3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9cae3-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cae3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cae3-126">Header</span><span class="sxs-lookup"><span data-stu-id="9cae3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cae3-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cae3-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

