---
title: Сообщение LVM_GETFOOTERITEMRECT (Коммктрл. h)
description: Возвращает координаты нижнего колонтитула для указанного элемента в элементе управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеритемрект ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- Элементы управления Windows для LVM_GETFOOTERITEMRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262181"
---
# <a name="lvm_getfooteritemrect-message"></a><span data-ttu-id="47c40-105">\_Сообщение LVM жетфутеритемрект</span><span class="sxs-lookup"><span data-stu-id="47c40-105">LVM\_GETFOOTERITEMRECT message</span></span>

<span data-ttu-id="47c40-106">Возвращает координаты нижнего колонтитула для указанного элемента в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="47c40-106">Gets the coordinates of a footer for a specified item in a list-view control.</span></span> <span data-ttu-id="47c40-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеритемрект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .</span><span class="sxs-lookup"><span data-stu-id="47c40-107">Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="47c40-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="47c40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c40-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47c40-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c40-110">Индекс элемента в элементе управления List-View.</span><span class="sxs-lookup"><span data-stu-id="47c40-110">The index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="47c40-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="47c40-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c40-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для получения координат.</span><span class="sxs-lookup"><span data-stu-id="47c40-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="47c40-113">Вызывающее приложение отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="47c40-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="47c40-114">Полученные координаты выражаются как клиентские координаты.</span><span class="sxs-lookup"><span data-stu-id="47c40-114">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c40-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47c40-115">Return value</span></span>

<span data-ttu-id="47c40-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="47c40-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c40-117">Требования</span><span class="sxs-lookup"><span data-stu-id="47c40-117">Requirements</span></span>



| <span data-ttu-id="47c40-118">Требование</span><span class="sxs-lookup"><span data-stu-id="47c40-118">Requirement</span></span> | <span data-ttu-id="47c40-119">Значение</span><span class="sxs-lookup"><span data-stu-id="47c40-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47c40-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47c40-120">Minimum supported client</span></span><br/> | <span data-ttu-id="47c40-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47c40-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47c40-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47c40-122">Minimum supported server</span></span><br/> | <span data-ttu-id="47c40-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47c40-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47c40-124">Header</span><span class="sxs-lookup"><span data-stu-id="47c40-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="47c40-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="47c40-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

