---
title: Сообщение CB_SHOWDROPDOWN (Winuser. h)
description: Приложение отправляет \_ сообщение ШОВДРОПДОВН CB для отображения или скрытия списка поля со списком, имеющего \_ раскрывающийся список CBS или \_ стиль DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Элементы управления Windows для CB_SHOWDROPDOWN сообщений
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137182"
---
# <a name="cb_showdropdown-message"></a><span data-ttu-id="5fc29-104">\_Сообщение ШОВДРОПДОВН CB</span><span class="sxs-lookup"><span data-stu-id="5fc29-104">CB\_SHOWDROPDOWN message</span></span>

<span data-ttu-id="5fc29-105">Приложение отправляет сообщение **\_ шовдропдовн CB** для отображения или скрытия списка поля со списком, имеющего [**\_ раскрывающийся список CBS**](combo-box-styles.md) или стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5fc29-105">An application sends a **CB\_SHOWDROPDOWN** message to show or hide the list box of a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fc29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fc29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fc29-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc29-108">**Логическое** значение, указывающее, должен ли раскрывающийся список отображаться или скрываться.</span><span class="sxs-lookup"><span data-stu-id="5fc29-108">A **BOOL** that specifies whether the drop-down list box is to be shown or hidden.</span></span> <span data-ttu-id="5fc29-109">Значение **true** показывает список; значение **false** скрывает его.</span><span class="sxs-lookup"><span data-stu-id="5fc29-109">A value of **TRUE** shows the list box; a value of **FALSE** hides it.</span></span>

</dd> <dt>

<span data-ttu-id="5fc29-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fc29-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc29-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="5fc29-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc29-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fc29-112">Return value</span></span>

<span data-ttu-id="5fc29-113">Возвращаемое значение всегда равно **true**.</span><span class="sxs-lookup"><span data-stu-id="5fc29-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc29-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fc29-114">Remarks</span></span>

<span data-ttu-id="5fc29-115">Это сообщение не влияет на поле со списком, созданное с [**помощью \_ простого стиля CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5fc29-115">This message has no effect on a combo box created with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc29-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5fc29-116">Requirements</span></span>



| <span data-ttu-id="5fc29-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5fc29-117">Requirement</span></span> | <span data-ttu-id="5fc29-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5fc29-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc29-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fc29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc29-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fc29-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5fc29-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fc29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc29-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5fc29-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5fc29-123">Header</span><span class="sxs-lookup"><span data-stu-id="5fc29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc29-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc29-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc29-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fc29-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc29-126">**\_ЖЕТДРОППЕДСТАТЕ CB**</span><span class="sxs-lookup"><span data-stu-id="5fc29-126">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
</dt> </dl>

 

 





