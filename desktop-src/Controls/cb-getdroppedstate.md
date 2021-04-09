---
title: Сообщение CB_GETDROPPEDSTATE (Winuser. h)
description: Определяет, раскрывается ли список поля со списком.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- Элементы управления Windows для CB_GETDROPPEDSTATE сообщений
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072038"
---
# <a name="cb_getdroppedstate-message"></a><span data-ttu-id="f5b40-104">\_Сообщение ЖЕТДРОППЕДСТАТЕ CB</span><span class="sxs-lookup"><span data-stu-id="f5b40-104">CB\_GETDROPPEDSTATE message</span></span>

<span data-ttu-id="f5b40-105">Определяет, раскрывается ли список поля со списком.</span><span class="sxs-lookup"><span data-stu-id="f5b40-105">Determines whether the list box of a combo box is dropped down.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5b40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5b40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b40-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5b40-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b40-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f5b40-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f5b40-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5b40-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b40-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f5b40-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b40-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5b40-111">Return value</span></span>

<span data-ttu-id="f5b40-112">Если список является видимым, возвращается значение **true**. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="f5b40-112">If the list box is visible, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b40-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f5b40-113">Requirements</span></span>



| <span data-ttu-id="f5b40-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f5b40-114">Requirement</span></span> | <span data-ttu-id="f5b40-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f5b40-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b40-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5b40-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b40-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5b40-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f5b40-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5b40-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b40-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5b40-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5b40-120">Header</span><span class="sxs-lookup"><span data-stu-id="f5b40-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5b40-121"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5b40-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b40-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5b40-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b40-123">**\_ШОВДРОПДОВН CB**</span><span class="sxs-lookup"><span data-stu-id="f5b40-123">**CB\_SHOWDROPDOWN**</span></span>](cb-showdropdown.md)
</dt> </dl>

 

 





