---
title: Сообщение CB_SETDROPPEDWIDTH (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТДРОППЕДВИДС CB, чтобы задать минимальную допустимую ширину (в пикселях) поля со списком, используя \_ раскрывающийся список CBS или \_ стиль DROPDOWNLIST.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- Элементы управления Windows для CB_SETDROPPEDWIDTH сообщений
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891913"
---
# <a name="cb_setdroppedwidth-message"></a><span data-ttu-id="af5a5-104">\_Сообщение СЕТДРОППЕДВИДС CB</span><span class="sxs-lookup"><span data-stu-id="af5a5-104">CB\_SETDROPPEDWIDTH message</span></span>

<span data-ttu-id="af5a5-105">Приложение отправляет сообщение **\_ сетдроппедвидс CB** , чтобы задать минимальную допустимую ширину (в пикселях) поля со списком, используя [**\_ раскрывающийся список CBS**](combo-box-styles.md) или стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="af5a5-105">An application sends the **CB\_SETDROPPEDWIDTH** message to set the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="af5a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af5a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af5a5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af5a5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af5a5-108">Минимальная допустимая ширина окна списка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="af5a5-108">The minimum allowable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="af5a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af5a5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af5a5-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="af5a5-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af5a5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af5a5-111">Return value</span></span>

<span data-ttu-id="af5a5-112">Если сообщение прошло успешно, возвращаемое значение является новой шириной списка.</span><span class="sxs-lookup"><span data-stu-id="af5a5-112">If the message is successful, The return value is the new width of the list box.</span></span>

<span data-ttu-id="af5a5-113">Если сообщение не выполняется, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="af5a5-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="af5a5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af5a5-114">Remarks</span></span>

<span data-ttu-id="af5a5-115">По умолчанию минимальная допустимая ширина раскрывающегося списка равна нулю.</span><span class="sxs-lookup"><span data-stu-id="af5a5-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="af5a5-116">Ширина списка является либо минимальной допустимой шириной, либо шириной поля со списком, в зависимости от того, какое значение больше.</span><span class="sxs-lookup"><span data-stu-id="af5a5-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5a5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="af5a5-117">Requirements</span></span>



| <span data-ttu-id="af5a5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="af5a5-118">Requirement</span></span> | <span data-ttu-id="af5a5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="af5a5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af5a5-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af5a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af5a5-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af5a5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="af5a5-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af5a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af5a5-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af5a5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="af5a5-124">Header</span><span class="sxs-lookup"><span data-stu-id="af5a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="af5a5-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af5a5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af5a5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af5a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5a5-127">**\_ЖЕТДРОППЕДВИДС CB**</span><span class="sxs-lookup"><span data-stu-id="af5a5-127">**CB\_GETDROPPEDWIDTH**</span></span>](cb-getdroppedwidth.md)
</dt> </dl>

 

 





