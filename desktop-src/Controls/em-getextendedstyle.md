---
title: Сообщение EM_GETEXTENDEDSTYLE (Коммктрл. h)
description: Возвращает расширенный стиль для элемента управления "поле ввода". Отправьте это сообщение явным образом или с помощью \_ макроса Edit жетекстендедстиле.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Элементы управления Windows для EM_GETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491814"
---
# <a name="em_getextendedstyle-message-commctrlh"></a><span data-ttu-id="cd91d-105">Сообщение EM_GETEXTENDEDSTYLE (Коммктрл. h)</span><span class="sxs-lookup"><span data-stu-id="cd91d-105">EM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="cd91d-106">Возвращает расширенный стиль для элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="cd91d-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="cd91d-107">Отправьте это сообщение явным образом или с помощью макроса [**Edit \_ жетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="cd91d-107">Send this message explicitly or by using the [**Edit\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd91d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd91d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd91d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd91d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cd91d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cd91d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cd91d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd91d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cd91d-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cd91d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd91d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd91d-113">Return value</span></span>

<span data-ttu-id="cd91d-114">Возвращает значение расширенного стиля. Дополнительные сведения о стилях см. в разделе [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="cd91d-114">Returns the value of extended style.For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd91d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd91d-115">Remarks</span></span>

<span data-ttu-id="cd91d-116">Расширенные стили для элемента управления "поле ввода" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="cd91d-116">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd91d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cd91d-117">Requirements</span></span>



| <span data-ttu-id="cd91d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cd91d-118">Requirement</span></span> | <span data-ttu-id="cd91d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cd91d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd91d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd91d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd91d-121">\[Только для настольных приложений Windows 10 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="cd91d-121">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cd91d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd91d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd91d-123">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="cd91d-123">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd91d-124">Header</span><span class="sxs-lookup"><span data-stu-id="cd91d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd91d-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd91d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

