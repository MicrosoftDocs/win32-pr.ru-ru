---
title: Сообщение BCM_SETDROPDOWNSTATE (Коммктрл. h)
description: Задает раскрывающееся состояние для кнопки с \_ раскрывающимся списком Style тбстиле. Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки сетдропдовнстате.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- Элементы управления Windows для BCM_SETDROPDOWNSTATE сообщений
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135867"
---
# <a name="bcm_setdropdownstate-message"></a><span data-ttu-id="9fa28-105">\_Сообщение СЕТДРОПДОВНСТАТЕ BCM</span><span class="sxs-lookup"><span data-stu-id="9fa28-105">BCM\_SETDROPDOWNSTATE message</span></span>

<span data-ttu-id="9fa28-106">Задает раскрывающееся состояние для кнопки с [**\_ раскрывающимся списком Style тбстиле**](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="9fa28-106">Sets the drop down state for a button with style [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span> <span data-ttu-id="9fa28-107">Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ сетдропдовнстате**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .</span><span class="sxs-lookup"><span data-stu-id="9fa28-107">Send this message explicitly or by using the [**Button\_SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fa28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fa28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fa28-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fa28-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa28-110">**Логическое** **значение, истинное** для состояния BST \_ дропдовнпушед, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9fa28-110">A **BOOL** that is **TRUE** for state of BST\_DROPDOWNPUSHED, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="9fa28-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fa28-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fa28-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9fa28-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fa28-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fa28-113">Return value</span></span>

<span data-ttu-id="9fa28-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9fa28-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa28-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9fa28-115">Requirements</span></span>



| <span data-ttu-id="9fa28-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9fa28-116">Requirement</span></span> | <span data-ttu-id="9fa28-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9fa28-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa28-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fa28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa28-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fa28-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fa28-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fa28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa28-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fa28-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fa28-122">Header</span><span class="sxs-lookup"><span data-stu-id="9fa28-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fa28-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fa28-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa28-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fa28-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fa28-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9fa28-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9fa28-126">Стили кнопок</span><span class="sxs-lookup"><span data-stu-id="9fa28-126">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="9fa28-127">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9fa28-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9fa28-128">Типы кнопок</span><span class="sxs-lookup"><span data-stu-id="9fa28-128">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





