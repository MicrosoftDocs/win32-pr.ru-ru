---
title: Сообщение EM_SHOWSCROLLBAR (RichEdit. h)
description: Показывает или скрывает одну из полос прокрутки в главном окне элемента управления Rich Edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Элементы управления Windows для EM_SHOWSCROLLBAR сообщений
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988552"
---
# <a name="em_showscrollbar-message"></a><span data-ttu-id="ed1c7-104">\_Сообщение ШОВСКРОЛЛБАР EM</span><span class="sxs-lookup"><span data-stu-id="ed1c7-104">EM\_SHOWSCROLLBAR message</span></span>

<span data-ttu-id="ed1c7-105">Показывает или скрывает одну из полос прокрутки в главном окне элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-105">Shows or hides one of the scroll bars in the host window of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed1c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed1c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed1c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1c7-108">Определяет, какая полоса прокрутки должна отображаться: горизонтальная или вертикальная.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-108">Identifies which scroll bar to display: horizontal or vertical.</span></span> <span data-ttu-id="ed1c7-109">Этот параметр должен иметь **SB \_** или **SB \_ горизонтали**.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-109">This parameter must be **SB\_VERT** or **SB\_HORZ**.</span></span>

</dd> <dt>

<span data-ttu-id="ed1c7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed1c7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1c7-111">Указывает, показывать ли полосу прокрутки или скрывать ее.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-111">Specifies whether to show the scroll bar or hide it.</span></span> <span data-ttu-id="ed1c7-112">Укажите **значение true** , чтобы показать полосу прокрутки, и **false** , чтобы скрыть ее.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-112">Specify **TRUE** to show the scroll bar and **FALSE** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1c7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed1c7-113">Return value</span></span>

<span data-ttu-id="ed1c7-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed1c7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed1c7-115">Remarks</span></span>

<span data-ttu-id="ed1c7-116">Этот метод допустим только в том случае, если элемент управления находится в активном месте.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-116">This method is only valid when the control is in-place active.</span></span> <span data-ttu-id="ed1c7-117">Вызовы, выполняемые, пока элемент управления неактивен, могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ed1c7-117">Calls made while the control is inactive may fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1c7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ed1c7-118">Requirements</span></span>



| <span data-ttu-id="ed1c7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ed1c7-119">Requirement</span></span> | <span data-ttu-id="ed1c7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ed1c7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1c7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed1c7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1c7-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed1c7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed1c7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed1c7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1c7-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed1c7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed1c7-125">Header</span><span class="sxs-lookup"><span data-stu-id="ed1c7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed1c7-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c7-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1c7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed1c7-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed1c7-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ed1c7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed1c7-129">**EM \_ жетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="ed1c7-129">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> <dt>

[<span data-ttu-id="ed1c7-130">**EM \_ сетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="ed1c7-130">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

 





