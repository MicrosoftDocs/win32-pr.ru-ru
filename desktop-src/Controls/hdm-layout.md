---
title: Сообщение HDM_LAYOUT (Коммктрл. h)
description: Извлекает сведения, используемые для задания размера и расположения элемента управления заголовка в пределах целевого прямоугольника родительского окна. Это сообщение можно отправить явным образом или использовать \_ макрос макета заголовка.
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- Элементы управления Windows для HDM_LAYOUT сообщений
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071654"
---
# <a name="hdm_layout-message"></a><span data-ttu-id="54819-105">\_Сообщение макета HDM</span><span class="sxs-lookup"><span data-stu-id="54819-105">HDM\_LAYOUT message</span></span>

<span data-ttu-id="54819-106">Извлекает сведения, используемые для задания размера и расположения элемента управления заголовка в пределах целевого прямоугольника родительского окна.</span><span class="sxs-lookup"><span data-stu-id="54819-106">Retrieves information used to set the size and position of the header control within the target rectangle of the parent window.</span></span> <span data-ttu-id="54819-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ макета заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .</span><span class="sxs-lookup"><span data-stu-id="54819-107">You can send this message explicitly or use the [**Header\_Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="54819-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="54819-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54819-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54819-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="54819-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="54819-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="54819-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54819-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54819-112">Указатель на структуру [**хдлайаут**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) .</span><span class="sxs-lookup"><span data-stu-id="54819-112">A pointer to an [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) structure.</span></span> <span data-ttu-id="54819-113">Элемент **PRC** указывает координаты прямоугольника, а элемент **пвпос** получает размер и расположение элемента управления заголовка внутри прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="54819-113">The **prc** member specifies the coordinates of a rectangle, and the **pwpos** member receives the size and position for the header control within the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54819-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54819-114">Return value</span></span>

<span data-ttu-id="54819-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="54819-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="54819-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54819-116">Remarks</span></span>

<span data-ttu-id="54819-117">Элемент **пвпос** структуры *lParam* получает значения size и Position, подходящие для позиционирования элемента управления вдоль верхней границы заданного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="54819-117">The **pwpos** member of the *lParam* structure receives size and position values appropriate for positioning the control along the top of the specified rectangle.</span></span> <span data-ttu-id="54819-118">Значение Height представляет собой сумму высоты горизонтальных границ элемента управления и среднюю высоту символов в шрифте, выделенном в контексте устройства элемента управления.</span><span class="sxs-lookup"><span data-stu-id="54819-118">The height value is the sum of the heights of the control's horizontal borders and the average height of characters in the font currently selected into the control's device context.</span></span>

<span data-ttu-id="54819-119">Чтобы использовать **\_ Макет HDM** для установки начального размера и расположения элемента управления "заголовок", установите начальное состояние видимости элемента управления, чтобы оно было скрыто.</span><span class="sxs-lookup"><span data-stu-id="54819-119">To use **HDM\_LAYOUT** to set the initial size and position of a header control, set the initial visibility state of the control so that it is hidden.</span></span> <span data-ttu-id="54819-120">После отправки **\_ макета HDM** для получения значений размера и расположения используйте функцию [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) , чтобы задать новый размер, положение и состояние видимости.</span><span class="sxs-lookup"><span data-stu-id="54819-120">After sending **HDM\_LAYOUT** to retrieve the size and position values, use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to set the new size, position, and visibility state.</span></span>

## <a name="requirements"></a><span data-ttu-id="54819-121">Требования</span><span class="sxs-lookup"><span data-stu-id="54819-121">Requirements</span></span>



| <span data-ttu-id="54819-122">Требование</span><span class="sxs-lookup"><span data-stu-id="54819-122">Requirement</span></span> | <span data-ttu-id="54819-123">Значение</span><span class="sxs-lookup"><span data-stu-id="54819-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54819-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54819-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54819-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54819-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54819-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54819-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54819-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54819-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54819-128">Header</span><span class="sxs-lookup"><span data-stu-id="54819-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="54819-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="54819-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

