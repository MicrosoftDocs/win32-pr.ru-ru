---
title: Сообщение HDM_GETOVERFLOWRECT (Коммктрл. h)
description: Возвращает ограничивающий прямоугольник кнопки переполнения, если в \_ элементе управления "заголовок" задан стиль переполнения HDS, а кнопка переполнения является видимой. Отправляйте это сообщение явным образом или с помощью \_ макроса Жетоверфловрект заголовка.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- Элементы управления Windows для HDM_GETOVERFLOWRECT сообщений
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534505"
---
# <a name="hdm_getoverflowrect-message"></a><span data-ttu-id="38091-105">\_Сообщение ЖЕТОВЕРФЛОВРЕКТ HDM</span><span class="sxs-lookup"><span data-stu-id="38091-105">HDM\_GETOVERFLOWRECT message</span></span>

<span data-ttu-id="38091-106">Возвращает ограничивающий прямоугольник кнопки переполнения, если в элементе управления "заголовок" задан стиль [**\_ переполнения HDS**](header-control-styles.md) , а кнопка переполнения является видимой.</span><span class="sxs-lookup"><span data-stu-id="38091-106">Gets the bounding rectangle of the overflow button when the [**HDS\_OVERFLOW**](header-control-styles.md) style is set on the header control and the overflow button is visible.</span></span> <span data-ttu-id="38091-107">Отправляйте это сообщение явным образом или с помощью макроса [**\_ жетоверфловрект заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .</span><span class="sxs-lookup"><span data-stu-id="38091-107">Send this message explicitly or by using the [**Header\_GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="38091-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="38091-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38091-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38091-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38091-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38091-110">Not used.</span></span> <span data-ttu-id="38091-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="38091-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="38091-112">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38091-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38091-113">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для получения сведений о ограничивающем прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="38091-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="38091-114">Отправитель сообщения отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="38091-114">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="38091-115">Координаты, возвращаемые в структуре **Rect** , выражаются в виде экранных координат.</span><span class="sxs-lookup"><span data-stu-id="38091-115">The coordinates returned in the **RECT** structure are expressed as screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38091-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38091-116">Return value</span></span>

<span data-ttu-id="38091-117">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="38091-117">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="38091-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38091-118">Remarks</span></span>

<span data-ttu-id="38091-119">Элемент управления "заголовок" должен иметь Style **ХДФ \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="38091-119">The header control must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="38091-120">Требования</span><span class="sxs-lookup"><span data-stu-id="38091-120">Requirements</span></span>



| <span data-ttu-id="38091-121">Требование</span><span class="sxs-lookup"><span data-stu-id="38091-121">Requirement</span></span> | <span data-ttu-id="38091-122">Значение</span><span class="sxs-lookup"><span data-stu-id="38091-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38091-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38091-123">Minimum supported client</span></span><br/> | <span data-ttu-id="38091-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38091-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38091-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38091-125">Minimum supported server</span></span><br/> | <span data-ttu-id="38091-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38091-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38091-127">Header</span><span class="sxs-lookup"><span data-stu-id="38091-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="38091-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="38091-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38091-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38091-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38091-130">Сведения об элементах управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="38091-130">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

