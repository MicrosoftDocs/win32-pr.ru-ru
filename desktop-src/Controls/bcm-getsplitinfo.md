---
title: Сообщение BCM_GETSPLITINFO (Коммктрл. h)
description: Возвращает сведения для элемента управления "кнопка разворачивающейся кнопки". Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки жетсплитинфо.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Элементы управления Windows для BCM_GETSPLITINFO сообщений
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988731"
---
# <a name="bcm_getsplitinfo-message"></a><span data-ttu-id="be820-105">\_Сообщение ЖЕТСПЛИТИНФО BCM</span><span class="sxs-lookup"><span data-stu-id="be820-105">BCM\_GETSPLITINFO message</span></span>

<span data-ttu-id="be820-106">Возвращает сведения для элемента управления "кнопка разворачивающейся кнопки".</span><span class="sxs-lookup"><span data-stu-id="be820-106">Gets information for a split button control.</span></span> <span data-ttu-id="be820-107">Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ жетсплитинфо**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) .</span><span class="sxs-lookup"><span data-stu-id="be820-107">Send this message explicitly or by using the [**Button\_GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="be820-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be820-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be820-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be820-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be820-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="be820-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="be820-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="be820-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be820-112">Указатель на структуру [**кнопки \_ сплитинфо**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) для получения сведений о кнопке.</span><span class="sxs-lookup"><span data-stu-id="be820-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure to receive information on the button.</span></span> <span data-ttu-id="be820-113">Вызывающий объект отвечает за выделение памяти для структуры.</span><span class="sxs-lookup"><span data-stu-id="be820-113">The caller is responsible for allocating the memory for the structure.</span></span> <span data-ttu-id="be820-114">Установите элемент **маски** этой структуры, чтобы определить, какие сведения следует получить.</span><span class="sxs-lookup"><span data-stu-id="be820-114">Set the **mask** member of this structure to determine what information to receive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be820-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be820-115">Return value</span></span>

<span data-ttu-id="be820-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="be820-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="be820-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be820-117">Remarks</span></span>

<span data-ttu-id="be820-118">Это сообщение используется только с стилями кнопки " [**BS \_**](button-styles.md) " и " [**BS \_ дефсплитбуттон**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="be820-118">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="be820-119">Требования</span><span class="sxs-lookup"><span data-stu-id="be820-119">Requirements</span></span>



| <span data-ttu-id="be820-120">Требование</span><span class="sxs-lookup"><span data-stu-id="be820-120">Requirement</span></span> | <span data-ttu-id="be820-121">Значение</span><span class="sxs-lookup"><span data-stu-id="be820-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be820-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be820-122">Minimum supported client</span></span><br/> | <span data-ttu-id="be820-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be820-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be820-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be820-124">Minimum supported server</span></span><br/> | <span data-ttu-id="be820-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be820-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be820-126">Header</span><span class="sxs-lookup"><span data-stu-id="be820-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="be820-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="be820-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be820-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be820-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="be820-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="be820-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be820-130">Стили кнопок</span><span class="sxs-lookup"><span data-stu-id="be820-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="be820-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="be820-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="be820-132">Типы кнопок</span><span class="sxs-lookup"><span data-stu-id="be820-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





