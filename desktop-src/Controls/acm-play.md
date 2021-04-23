---
title: Сообщение ACM_PLAY (Коммктрл. h)
description: Воспроизводит ролик AVI в элементе управления Animation. Элемент управления воспроизводит клип в фоновом режиме, в то время как поток продолжит выполнение. Это сообщение можно отправить явно или с помощью \_ макроса анимировать Play.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- Элементы управления Windows для ACM_PLAY сообщений
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489651"
---
# <a name="acm_play-message"></a><span data-ttu-id="bdf06-106">ACM \_ воспроизведение сообщения</span><span class="sxs-lookup"><span data-stu-id="bdf06-106">ACM\_PLAY message</span></span>

<span data-ttu-id="bdf06-107">Воспроизводит ролик AVI в элементе управления Animation.</span><span class="sxs-lookup"><span data-stu-id="bdf06-107">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="bdf06-108">Элемент управления воспроизводит клип в фоновом режиме, в то время как поток продолжит выполнение.</span><span class="sxs-lookup"><span data-stu-id="bdf06-108">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="bdf06-109">Это сообщение можно отправить явно или с помощью макроса [**анимировать \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .</span><span class="sxs-lookup"><span data-stu-id="bdf06-109">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdf06-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdf06-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf06-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdf06-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdf06-112">Значение **uint** , указывающее количество повторов воспроизведения фрагмента AVI.</span><span class="sxs-lookup"><span data-stu-id="bdf06-112">A **UINT** that specifies the number of times to replay the AVI clip.</span></span> <span data-ttu-id="bdf06-113">Значение-1 означает воспроизведение клипа в течение неограниченного времени.</span><span class="sxs-lookup"><span data-stu-id="bdf06-113">A value of -1 means replay the clip indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="bdf06-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdf06-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdf06-115">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это Отсчитываемый от нуля индекс кадра, с которого начинается воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="bdf06-115">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the zero-based index of the frame where playing begins.</span></span> <span data-ttu-id="bdf06-116">Значение должно быть меньше 65 536.</span><span class="sxs-lookup"><span data-stu-id="bdf06-116">The value must be less than 65,536.</span></span> <span data-ttu-id="bdf06-117">Нулевое значение означает, что начинается с первого кадра в ролике AVI.</span><span class="sxs-lookup"><span data-stu-id="bdf06-117">A value of zero means begin with the first frame in the AVI clip.</span></span>

<span data-ttu-id="bdf06-118">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это Отсчитываемый от нуля индекс кадра, в котором завершается воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="bdf06-118">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the zero-based index of the frame where playing ends.</span></span> <span data-ttu-id="bdf06-119">Значение должно быть меньше 65 536.</span><span class="sxs-lookup"><span data-stu-id="bdf06-119">The value must be less than 65,536.</span></span> <span data-ttu-id="bdf06-120">Значение-1 означает, что заканчивается последним кадром в ролике AVI.</span><span class="sxs-lookup"><span data-stu-id="bdf06-120">A value of -1 means end with the last frame in the AVI clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf06-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdf06-121">Return value</span></span>

<span data-ttu-id="bdf06-122">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="bdf06-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf06-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdf06-123">Remarks</span></span>

<span data-ttu-id="bdf06-124">С помощью [**анимации можно \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) направить элемент управления анимации для показа определенного кадра клипа AVI.</span><span class="sxs-lookup"><span data-stu-id="bdf06-124">You can use [**Animate\_Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) to direct the animation control to display a particular frame of the AVI clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf06-125">Требования</span><span class="sxs-lookup"><span data-stu-id="bdf06-125">Requirements</span></span>



| <span data-ttu-id="bdf06-126">Требование</span><span class="sxs-lookup"><span data-stu-id="bdf06-126">Requirement</span></span> | <span data-ttu-id="bdf06-127">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf06-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf06-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdf06-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf06-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdf06-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdf06-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdf06-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf06-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bdf06-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdf06-132">Header</span><span class="sxs-lookup"><span data-stu-id="bdf06-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf06-133"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf06-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

