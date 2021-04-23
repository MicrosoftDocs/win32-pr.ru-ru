---
title: Сообщение BCM_SETSPLITINFO (Коммктрл. h)
description: Задает сведения для элемента управления "разворачивающаяся кнопка". Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки сетсплитинфо.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- Элементы управления Windows для BCM_SETSPLITINFO сообщений
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654527"
---
# <a name="bcm_setsplitinfo-message"></a><span data-ttu-id="aa913-105">\_Сообщение СЕТСПЛИТИНФО BCM</span><span class="sxs-lookup"><span data-stu-id="aa913-105">BCM\_SETSPLITINFO message</span></span>

<span data-ttu-id="aa913-106">Задает сведения для элемента управления "разворачивающаяся кнопка".</span><span class="sxs-lookup"><span data-stu-id="aa913-106">Sets information for a split button control.</span></span> <span data-ttu-id="aa913-107">Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ сетсплитинфо**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) .</span><span class="sxs-lookup"><span data-stu-id="aa913-107">Send this message explicitly or by using the [**Button\_SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa913-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa913-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa913-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa913-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa913-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="aa913-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aa913-111">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa913-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa913-112">Указатель на структуру [**\_ сплитинфо кнопки**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) , содержащую сведения о разворачивающейся кнопке.</span><span class="sxs-lookup"><span data-stu-id="aa913-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure containing information about the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa913-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa913-113">Return value</span></span>

<span data-ttu-id="aa913-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="aa913-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa913-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa913-115">Remarks</span></span>

<span data-ttu-id="aa913-116">Это сообщение используется только с стилями кнопки " [**BS \_**](button-styles.md) " и " [**BS \_ дефсплитбуттон**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="aa913-116">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa913-117">Требования</span><span class="sxs-lookup"><span data-stu-id="aa913-117">Requirements</span></span>



| <span data-ttu-id="aa913-118">Требование</span><span class="sxs-lookup"><span data-stu-id="aa913-118">Requirement</span></span> | <span data-ttu-id="aa913-119">Значение</span><span class="sxs-lookup"><span data-stu-id="aa913-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa913-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa913-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa913-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa913-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa913-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa913-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa913-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa913-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa913-124">Header</span><span class="sxs-lookup"><span data-stu-id="aa913-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa913-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa913-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa913-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa913-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa913-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="aa913-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa913-128">Стили кнопок</span><span class="sxs-lookup"><span data-stu-id="aa913-128">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="aa913-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="aa913-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aa913-130">Типы кнопок</span><span class="sxs-lookup"><span data-stu-id="aa913-130">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





