---
title: Сообщение HDM_SETHOTDIVIDER (Коммктрл. h)
description: Изменяет цвет разделителя между элементами заголовка, чтобы указать место назначения для внешней операции перетаскивания. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сесотдивидер.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- Элементы управления Windows для HDM_SETHOTDIVIDER сообщений
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135786"
---
# <a name="hdm_sethotdivider-message"></a><span data-ttu-id="784b0-105">\_Сообщение СЕСОТДИВИДЕР HDM</span><span class="sxs-lookup"><span data-stu-id="784b0-105">HDM\_SETHOTDIVIDER message</span></span>

<span data-ttu-id="784b0-106">Изменяет цвет разделителя между элементами заголовка, чтобы указать место назначения для внешней операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="784b0-106">Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation.</span></span> <span data-ttu-id="784b0-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сесотдивидер**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .</span><span class="sxs-lookup"><span data-stu-id="784b0-107">You can send this message explicitly or use the [**Header\_SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="784b0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="784b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="784b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="784b0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="784b0-110">Тип значения, представленного параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="784b0-110">The type of value represented by *lParam*.</span></span> <span data-ttu-id="784b0-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="784b0-111">This value can be one of the following:</span></span>



| <span data-ttu-id="784b0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="784b0-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="784b0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="784b0-113">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="784b0-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="784b0-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="784b0-115">Указывает, что *lParam* содержит клиентские координаты указателя.</span><span class="sxs-lookup"><span data-stu-id="784b0-115">Indicates that *lParam* holds the client coordinates of the pointer.</span></span><br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="784b0-116"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="784b0-116"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="784b0-117">Указывает, что *lParam* содержит значение индекса разделителя.</span><span class="sxs-lookup"><span data-stu-id="784b0-117">Indicates that *lParam* holds a divider index value.</span></span><br/>                 |



 

</dd> <dt>

<span data-ttu-id="784b0-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="784b0-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="784b0-119">Значение, содержащееся в параметре *lParam* , интерпретируется в зависимости от значения параметра *wParam*.</span><span class="sxs-lookup"><span data-stu-id="784b0-119">A value held in *lParam* is interpreted depending on the value of *wParam*.</span></span>

<span data-ttu-id="784b0-120">Если параметр *wParam* имеет **значение true**, то параметр *lParam* представляет координаты x и y указателя.</span><span class="sxs-lookup"><span data-stu-id="784b0-120">If *wParam* is **TRUE**, *lParam* represents the x- and y-coordinates of the pointer.</span></span> <span data-ttu-id="784b0-121">Координата x находится в нижнем слове, а координата y — в верхнем слове.</span><span class="sxs-lookup"><span data-stu-id="784b0-121">The x-coordinate is in the low word, and the y-coordinate is in the high word.</span></span> <span data-ttu-id="784b0-122">Когда элемент управления "заголовок" получает сообщение, он выделяет соответствующий разделитель на основе координат *lParam* .</span><span class="sxs-lookup"><span data-stu-id="784b0-122">When the header control receives the message, it highlights the appropriate divider based on the *lParam* coordinates.</span></span>

<span data-ttu-id="784b0-123">Если параметр *wParam* имеет **значение false**, то параметр *lParam* представляет целочисленный индекс выделенного разделителя.</span><span class="sxs-lookup"><span data-stu-id="784b0-123">If *wParam* is **FALSE**, *lParam* represents the integer index of the divider to be highlighted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="784b0-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="784b0-124">Return value</span></span>

<span data-ttu-id="784b0-125">Возвращает значение, равное индексу разделителя, выделенного элементом управления.</span><span class="sxs-lookup"><span data-stu-id="784b0-125">Returns a value equal to the index of the divider that the control highlighted.</span></span>

## <a name="remarks"></a><span data-ttu-id="784b0-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="784b0-126">Remarks</span></span>

<span data-ttu-id="784b0-127">Это сообщение создает действие, которое автоматически создается элементом управления "заголовок", если он имеет стиль [**HDS \_ DRAGDROP**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="784b0-127">This message creates an effect that a header control automatically produces when it has the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="784b0-128">Сообщение **\_ сесотдивидер HDM** предназначено для использования, когда владелец элемента управления обрабатывает операции перетаскивания вручную.</span><span class="sxs-lookup"><span data-stu-id="784b0-128">The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.</span></span>

## <a name="requirements"></a><span data-ttu-id="784b0-129">Требования</span><span class="sxs-lookup"><span data-stu-id="784b0-129">Requirements</span></span>



| <span data-ttu-id="784b0-130">Требование</span><span class="sxs-lookup"><span data-stu-id="784b0-130">Requirement</span></span> | <span data-ttu-id="784b0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="784b0-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="784b0-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="784b0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="784b0-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="784b0-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="784b0-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="784b0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="784b0-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="784b0-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="784b0-136">Header</span><span class="sxs-lookup"><span data-stu-id="784b0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="784b0-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="784b0-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





