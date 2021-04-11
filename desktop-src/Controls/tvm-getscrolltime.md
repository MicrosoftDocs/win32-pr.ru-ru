---
title: Сообщение TVM_GETSCROLLTIME (Коммктрл. h)
description: Возвращает максимальное время прокрутки для элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Жетскроллтиме TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- Элементы управления Windows для TVM_GETSCROLLTIME сообщений
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135443"
---
# <a name="tvm_getscrolltime-message"></a><span data-ttu-id="548e6-105">\_Сообщение TVM жетскроллтиме</span><span class="sxs-lookup"><span data-stu-id="548e6-105">TVM\_GETSCROLLTIME message</span></span>

<span data-ttu-id="548e6-106">Возвращает максимальное время прокрутки для элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="548e6-106">Retrieves the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="548e6-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетскроллтиме TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="548e6-107">You can send this message explicitly or by using the [**TreeView\_GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="548e6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="548e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="548e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="548e6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="548e6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="548e6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="548e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="548e6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="548e6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="548e6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="548e6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="548e6-113">Return value</span></span>

<span data-ttu-id="548e6-114">Возвращает максимальное время прокрутки в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="548e6-114">Returns the maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="548e6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="548e6-115">Remarks</span></span>

<span data-ttu-id="548e6-116">Максимальное время прокрутки — это наибольшее количество времени, которое может занять операция прокрутки.</span><span class="sxs-lookup"><span data-stu-id="548e6-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="548e6-117">Прокрутка будет скорректирована таким образом, что прокрутка будет выполняться в пределах максимального времени прокрутки.</span><span class="sxs-lookup"><span data-stu-id="548e6-117">The scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="548e6-118">Операция прокрутки может занять меньше времени, чем максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="548e6-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="548e6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="548e6-119">Requirements</span></span>



| <span data-ttu-id="548e6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="548e6-120">Requirement</span></span> | <span data-ttu-id="548e6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="548e6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="548e6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="548e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="548e6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="548e6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="548e6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="548e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="548e6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="548e6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="548e6-126">Header</span><span class="sxs-lookup"><span data-stu-id="548e6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="548e6-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="548e6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548e6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="548e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548e6-129">**TVM \_ сетскроллтиме**</span><span class="sxs-lookup"><span data-stu-id="548e6-129">**TVM\_SETSCROLLTIME**</span></span>](tvm-setscrolltime.md)
</dt> </dl>

 

 





