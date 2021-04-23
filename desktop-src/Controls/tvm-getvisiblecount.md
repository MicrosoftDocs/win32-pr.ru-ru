---
title: Сообщение TVM_GETVISIBLECOUNT (Коммктрл. h)
description: Получает количество элементов, которые могут быть полностью видны в клиентском окне элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Жетвисиблекаунт TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- Элементы управления Windows для TVM_GETVISIBLECOUNT сообщений
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988366"
---
# <a name="tvm_getvisiblecount-message"></a><span data-ttu-id="a57dd-105">\_Сообщение TVM жетвисиблекаунт</span><span class="sxs-lookup"><span data-stu-id="a57dd-105">TVM\_GETVISIBLECOUNT message</span></span>

<span data-ttu-id="a57dd-106">Получает количество элементов, которые могут быть полностью видны в клиентском окне элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="a57dd-106">Obtains the number of items that can be fully visible in the client window of a tree-view control.</span></span> <span data-ttu-id="a57dd-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетвисиблекаунт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .</span><span class="sxs-lookup"><span data-stu-id="a57dd-107">You can send this message explicitly or by using the [**TreeView\_GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a57dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a57dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a57dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a57dd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a57dd-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a57dd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a57dd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a57dd-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a57dd-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a57dd-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a57dd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a57dd-113">Return value</span></span>

<span data-ttu-id="a57dd-114">Возвращает число элементов, которые могут быть полностью видны в клиентском окне элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="a57dd-114">Returns the number of items that can be fully visible in the client window of the tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a57dd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a57dd-115">Remarks</span></span>

<span data-ttu-id="a57dd-116">Количество элементов, которые могут быть полностью видимыми, может быть больше числа элементов в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="a57dd-116">The number of items that can be fully visible may be greater than the number of items in the control.</span></span> <span data-ttu-id="a57dd-117">Элемент управления вычисляет это значение, разделив высоту клиентского окна по высоте элемента.</span><span class="sxs-lookup"><span data-stu-id="a57dd-117">The control calculates this value by dividing the height of the client window by the height of an item.</span></span>

<span data-ttu-id="a57dd-118">Обратите внимание, что возвращаемое значение — это количество элементов, которые могут быть *полностью* видимы.</span><span class="sxs-lookup"><span data-stu-id="a57dd-118">Note that the return value is the number of items that can be *fully* visible.</span></span> <span data-ttu-id="a57dd-119">Если вы видите все 20 элементов и часть одного элемента, возвращаемое значение равно 20.</span><span class="sxs-lookup"><span data-stu-id="a57dd-119">If you can see all of 20 items and part of one more item, the return value is 20.</span></span>

## <a name="requirements"></a><span data-ttu-id="a57dd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a57dd-120">Requirements</span></span>



| <span data-ttu-id="a57dd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a57dd-121">Requirement</span></span> | <span data-ttu-id="a57dd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a57dd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a57dd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a57dd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a57dd-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a57dd-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a57dd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a57dd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a57dd-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a57dd-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a57dd-127">Header</span><span class="sxs-lookup"><span data-stu-id="a57dd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a57dd-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a57dd-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





