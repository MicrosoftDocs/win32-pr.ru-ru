---
title: Сообщение LVM_GETFOOTERRECT (Коммктрл. h)
description: Извлекает координаты нижнего колонтитула для элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеррект ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- Элементы управления Windows для LVM_GETFOOTERRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135127"
---
# <a name="lvm_getfooterrect-message"></a><span data-ttu-id="cc7c8-105">\_Сообщение LVM жетфутеррект</span><span class="sxs-lookup"><span data-stu-id="cc7c8-105">LVM\_GETFOOTERRECT message</span></span>

<span data-ttu-id="cc7c8-106">Извлекает координаты нижнего колонтитула для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="cc7c8-106">Retrieves the coordinates of the footer for a list-view control.</span></span> <span data-ttu-id="cc7c8-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеррект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .</span><span class="sxs-lookup"><span data-stu-id="cc7c8-107">Send this message explicitly or by using the [**ListView\_GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc7c8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc7c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc7c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc7c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc7c8-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-110">Not used.</span></span> <span data-ttu-id="cc7c8-111">Должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="cc7c8-112">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc7c8-113">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для получения координат.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="cc7c8-114">Вызывающий процесс отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-114">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="cc7c8-115">Полученные координаты выражаются как клиентские координаты.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-115">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc7c8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc7c8-116">Return value</span></span>

<span data-ttu-id="cc7c8-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cc7c8-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc7c8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cc7c8-118">Requirements</span></span>



| <span data-ttu-id="cc7c8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cc7c8-119">Requirement</span></span> | <span data-ttu-id="cc7c8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cc7c8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7c8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc7c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc7c8-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc7c8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc7c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc7c8-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc7c8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc7c8-125">Header</span><span class="sxs-lookup"><span data-stu-id="cc7c8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc7c8-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc7c8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

