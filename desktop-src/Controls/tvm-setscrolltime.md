---
title: Сообщение TVM_SETSCROLLTIME (Коммктрл. h)
description: Задает максимальное время прокрутки для элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Сетскроллтиме TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- Элементы управления Windows для TVM_SETSCROLLTIME сообщений
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654539"
---
# <a name="tvm_setscrolltime-message"></a><span data-ttu-id="0feb4-105">\_Сообщение TVM сетскроллтиме</span><span class="sxs-lookup"><span data-stu-id="0feb4-105">TVM\_SETSCROLLTIME message</span></span>

<span data-ttu-id="0feb4-106">Задает максимальное время прокрутки для элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="0feb4-106">Sets the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="0feb4-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетскроллтиме TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="0feb4-107">You can send this message explicitly or by using the [**TreeView\_SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0feb4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0feb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0feb4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0feb4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0feb4-110">Новое максимальное время прокрутки в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="0feb4-110">New maximum scroll time, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="0feb4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0feb4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0feb4-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0feb4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0feb4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0feb4-113">Return value</span></span>

<span data-ttu-id="0feb4-114">Возвращает предыдущее максимальное время прокрутки в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="0feb4-114">Returns the previous maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="0feb4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0feb4-115">Remarks</span></span>

<span data-ttu-id="0feb4-116">Максимальное время прокрутки — это наибольшее количество времени, которое может занять операция прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0feb4-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="0feb4-117">Прокрутка будет скорректирована таким образом, что прокрутка будет выполняться в пределах максимального времени прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0feb4-117">Scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="0feb4-118">Операция прокрутки может занять меньше времени, чем максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="0feb4-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="0feb4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0feb4-119">Requirements</span></span>



| <span data-ttu-id="0feb4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0feb4-120">Requirement</span></span> | <span data-ttu-id="0feb4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0feb4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0feb4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0feb4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0feb4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0feb4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0feb4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0feb4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0feb4-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0feb4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0feb4-126">Header</span><span class="sxs-lookup"><span data-stu-id="0feb4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0feb4-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0feb4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0feb4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0feb4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0feb4-129">**TVM \_ жетскроллтиме**</span><span class="sxs-lookup"><span data-stu-id="0feb4-129">**TVM\_GETSCROLLTIME**</span></span>](tvm-getscrolltime.md)
</dt> </dl>

 

 





