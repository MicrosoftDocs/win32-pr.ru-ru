---
title: Сообщение PGM_SETBORDER (Коммктрл. h)
description: Задает текущий размер границы для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Сетбордер пейджера.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- Элементы управления Windows для PGM_SETBORDER сообщений
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071520"
---
# <a name="pgm_setborder-message"></a><span data-ttu-id="8cff1-105">\_Сообщение СЕТБОРДЕР PGM</span><span class="sxs-lookup"><span data-stu-id="8cff1-105">PGM\_SETBORDER message</span></span>

<span data-ttu-id="8cff1-106">Задает текущий размер границы для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="8cff1-106">Sets the current border size for the pager control.</span></span> <span data-ttu-id="8cff1-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетбордер пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .</span><span class="sxs-lookup"><span data-stu-id="8cff1-107">You can send this message explicitly or use the [**Pager\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cff1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cff1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cff1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8cff1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8cff1-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8cff1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8cff1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cff1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cff1-112">Новый размер границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="8cff1-112">New size of the border, in pixels.</span></span> <span data-ttu-id="8cff1-113">Это значение не должно быть больше, чем кнопка страничного навигатора, или меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="8cff1-113">This value should not be larger than the pager button or less than zero.</span></span> <span data-ttu-id="8cff1-114">Если значение *lParam* слишком велико, граница будет иметь тот же размер, что и кнопка.</span><span class="sxs-lookup"><span data-stu-id="8cff1-114">If *lParam* is too large, the border will be drawn the same size as the button.</span></span> <span data-ttu-id="8cff1-115">Если параметр *lParam* имеет отрицательное значение, то размер границы будет обнулен.</span><span class="sxs-lookup"><span data-stu-id="8cff1-115">If *lParam* is negative, the border size will be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cff1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cff1-116">Return value</span></span>

<span data-ttu-id="8cff1-117">Возвращает значение типа INT, которое содержит предыдущий размер границы (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="8cff1-117">Returns an INT value that contains the previous border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cff1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8cff1-118">Requirements</span></span>



| <span data-ttu-id="8cff1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8cff1-119">Requirement</span></span> | <span data-ttu-id="8cff1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cff1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cff1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8cff1-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cff1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cff1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cff1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8cff1-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cff1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cff1-125">Header</span><span class="sxs-lookup"><span data-stu-id="8cff1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cff1-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cff1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





