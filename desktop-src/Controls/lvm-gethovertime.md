---
title: Сообщение LVM_GETHOVERTIME (Коммктрл. h)
description: Возвращает количество времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран. Это сообщение можно отправить явным образом или использовать \_ макрос Жесовертиме ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- Элементы управления Windows для LVM_GETHOVERTIME сообщений
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491466"
---
# <a name="lvm_gethovertime-message"></a><span data-ttu-id="6f4f1-105">\_Сообщение LVM жесовертиме</span><span class="sxs-lookup"><span data-stu-id="6f4f1-105">LVM\_GETHOVERTIME message</span></span>

<span data-ttu-id="6f4f1-106">Возвращает количество времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-106">Retrieves the amount of time that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="6f4f1-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жесовертиме ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .</span><span class="sxs-lookup"><span data-stu-id="6f4f1-107">You can send this message explicitly or use the [**ListView\_GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f4f1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f4f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f4f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f4f1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f4f1-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f4f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f4f1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6f4f1-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f4f1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f4f1-113">Return value</span></span>

<span data-ttu-id="6f4f1-114">Возвращает количество времени в миллисекундах, в течение которого курсор мыши должен навестися над элементом, прежде чем он будет выбран.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-114">Returns the amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="6f4f1-115">Если возвращаемое значение равно (**DWORD**)-1, то по умолчанию используется время наведения.</span><span class="sxs-lookup"><span data-stu-id="6f4f1-115">If the return value is (**DWORD**)-1, then the hover time is the default hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f4f1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f4f1-116">Remarks</span></span>

<span data-ttu-id="6f4f1-117">Время наведения на себя влияет только на элементы управления "представление списка", которые имеют расширенный стиль представления списка [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md), [**LVS \_ ex \_ онекликкактивате**](extended-list-view-styles.md)или [**LVS \_ ex \_ твокликкактивате**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6f4f1-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4f1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6f4f1-118">Requirements</span></span>



| <span data-ttu-id="6f4f1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6f4f1-119">Requirement</span></span> | <span data-ttu-id="6f4f1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6f4f1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4f1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f4f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4f1-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f4f1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f4f1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f4f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4f1-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6f4f1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f4f1-125">Header</span><span class="sxs-lookup"><span data-stu-id="6f4f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f4f1-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f4f1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





