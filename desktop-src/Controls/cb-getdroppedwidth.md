---
title: Сообщение CB_GETDROPPEDWIDTH (Winuser. h)
description: Возвращает минимально допустимую ширину (в пикселях) поля со списком в \_ раскрывающемся списке или \_ стиле DROPDOWNLIST.
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- Элементы управления Windows для CB_GETDROPPEDWIDTH сообщений
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071622"
---
# <a name="cb_getdroppedwidth-message"></a><span data-ttu-id="a74c4-104">\_Сообщение ЖЕТДРОППЕДВИДС CB</span><span class="sxs-lookup"><span data-stu-id="a74c4-104">CB\_GETDROPPEDWIDTH message</span></span>

<span data-ttu-id="a74c4-105">Возвращает минимально допустимую ширину (в пикселях) поля со списком в [**\_ раскрывающемся**](combo-box-styles.md) списке или стиле [**\_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a74c4-105">Gets the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="a74c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a74c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a74c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a74c4-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a74c4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a74c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a74c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a74c4-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a74c4-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a74c4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a74c4-111">Return value</span></span>

<span data-ttu-id="a74c4-112">Если сообщение прошло удачно, возвращаемое значение будет шириной в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a74c4-112">If the message succeeds, the return value is the width, in pixels.</span></span>

<span data-ttu-id="a74c4-113">Если сообщение не выполняется, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="a74c4-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="a74c4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a74c4-114">Remarks</span></span>

<span data-ttu-id="a74c4-115">По умолчанию минимальная допустимая ширина раскрывающегося списка равна нулю.</span><span class="sxs-lookup"><span data-stu-id="a74c4-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="a74c4-116">Ширина списка является либо минимальной допустимой шириной, либо шириной поля со списком, в зависимости от того, какое значение больше.</span><span class="sxs-lookup"><span data-stu-id="a74c4-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="a74c4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a74c4-117">Requirements</span></span>



| <span data-ttu-id="a74c4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a74c4-118">Requirement</span></span> | <span data-ttu-id="a74c4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a74c4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a74c4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a74c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a74c4-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a74c4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a74c4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a74c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a74c4-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a74c4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a74c4-124">Header</span><span class="sxs-lookup"><span data-stu-id="a74c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a74c4-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a74c4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74c4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a74c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74c4-127">**\_СЕТДРОППЕДВИДС CB**</span><span class="sxs-lookup"><span data-stu-id="a74c4-127">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
</dt> </dl>

 

 





