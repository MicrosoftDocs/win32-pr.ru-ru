---
title: Сообщение TB_SETPADDING (Коммктрл. h)
description: Задает заполнение для элемента управления ToolBar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Элементы управления Windows для TB_SETPADDING сообщений
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137279"
---
# <a name="tb_setpadding-message"></a><span data-ttu-id="383e0-104">\_Сообщение СЕТПАДДИНГ ТБ</span><span class="sxs-lookup"><span data-stu-id="383e0-104">TB\_SETPADDING message</span></span>

<span data-ttu-id="383e0-105">Задает заполнение для элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="383e0-105">Sets the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="383e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="383e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="383e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="383e0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="383e0-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="383e0-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="383e0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="383e0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="383e0-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает горизонтальное заполнение в пикселях.</span><span class="sxs-lookup"><span data-stu-id="383e0-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the horizontal padding, in pixels.</span></span> <span data-ttu-id="383e0-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает вертикальное заполнение в пикселях.</span><span class="sxs-lookup"><span data-stu-id="383e0-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="383e0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="383e0-112">Return value</span></span>

<span data-ttu-id="383e0-113">Возвращает значение **типа DWORD** , содержащее предыдущее горизонтальное заполнение в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) и предыдущее вертикальное заполнение в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(в пикселях).</span><span class="sxs-lookup"><span data-stu-id="383e0-113">Returns a **DWORD** value that contains the previous horizontal padding in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous vertical padding in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="383e0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="383e0-114">Remarks</span></span>

<span data-ttu-id="383e0-115">Значения заполнения используются для создания пустой области между границей кнопки и изображением кнопки и (или) текстом.</span><span class="sxs-lookup"><span data-stu-id="383e0-115">The padding values are used to create a blank area between the edge of the button and the button's image and/or text.</span></span> <span data-ttu-id="383e0-116">Где и как фактически применяется внутреннее заполнение, зависит от типа кнопки и наличия изображения.</span><span class="sxs-lookup"><span data-stu-id="383e0-116">Where and how much padding is actually applied depends on the type of the button and whether it has an image.</span></span> <span data-ttu-id="383e0-117">Отступ по горизонтали применяется как справа, так и слева от кнопки, а вертикальное заполнение применяется как к верхней, так и к нижней части кнопки.</span><span class="sxs-lookup"><span data-stu-id="383e0-117">The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button.</span></span> <span data-ttu-id="383e0-118">Заполнение применяется только к кнопкам, имеющим стиль [**\_ AUTOSIZE тбстиле**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="383e0-118">Padding is only applied to buttons that have the [**TBSTYLE\_AUTOSIZE**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="383e0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="383e0-119">Requirements</span></span>



| <span data-ttu-id="383e0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="383e0-120">Requirement</span></span> | <span data-ttu-id="383e0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="383e0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="383e0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="383e0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="383e0-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="383e0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="383e0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="383e0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="383e0-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="383e0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="383e0-126">Header</span><span class="sxs-lookup"><span data-stu-id="383e0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="383e0-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="383e0-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="383e0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="383e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383e0-129">**\_отбивка по ТБ**</span><span class="sxs-lookup"><span data-stu-id="383e0-129">**TB\_GETPADDING**</span></span>](tb-getpadding.md)
</dt> </dl>

 

