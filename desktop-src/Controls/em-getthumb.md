---
title: Сообщение EM_GETTHUMB (Winuser. h)
description: Возвращает расположение бегунка (Thumb) в вертикальной полосе прокрутки для многострочного элемента управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- Элементы управления Windows для EM_GETTHUMB сообщений
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136854"
---
# <a name="em_getthumb-message"></a><span data-ttu-id="fee6b-105">\_Сообщение EM</span><span class="sxs-lookup"><span data-stu-id="fee6b-105">EM\_GETTHUMB message</span></span>

<span data-ttu-id="fee6b-106">Возвращает расположение бегунка (Thumb) в вертикальной полосе прокрутки для многострочного элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="fee6b-106">Gets the position of the scroll box (thumb) in the vertical scroll bar of a multiline edit control.</span></span> <span data-ttu-id="fee6b-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fee6b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fee6b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fee6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee6b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fee6b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fee6b-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fee6b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fee6b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fee6b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fee6b-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fee6b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee6b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fee6b-113">Return value</span></span>

<span data-ttu-id="fee6b-114">Возвращаемое значение является положением ползунка.</span><span class="sxs-lookup"><span data-stu-id="fee6b-114">The return value is the position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee6b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fee6b-115">Remarks</span></span>

<span data-ttu-id="fee6b-116">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 2,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="fee6b-116">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="fee6b-117">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fee6b-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fee6b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fee6b-118">Requirements</span></span>



| <span data-ttu-id="fee6b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fee6b-119">Requirement</span></span> | <span data-ttu-id="fee6b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fee6b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fee6b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fee6b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fee6b-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fee6b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fee6b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fee6b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fee6b-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fee6b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fee6b-125">Header</span><span class="sxs-lookup"><span data-stu-id="fee6b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee6b-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fee6b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





