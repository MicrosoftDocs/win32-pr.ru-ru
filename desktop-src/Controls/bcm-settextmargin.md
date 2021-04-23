---
title: Сообщение BCM_SETTEXTMARGIN (Коммктрл. h)
description: '\_Сообщение СЕТТЕКСТМАРГИН BCM задает поля для рисования текста в элементе управления "Кнопка".'
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- Элементы управления Windows для BCM_SETTEXTMARGIN сообщений
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490551"
---
# <a name="bcm_settextmargin-message"></a><span data-ttu-id="5d82c-104">\_Сообщение СЕТТЕКСТМАРГИН BCM</span><span class="sxs-lookup"><span data-stu-id="5d82c-104">BCM\_SETTEXTMARGIN message</span></span>

<span data-ttu-id="5d82c-105">Сообщение **\_ сеттекстмаргин BCM** задает поля для рисования текста в элементе управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="5d82c-105">The **BCM\_SETTEXTMARGIN** message sets the margins for drawing text in a button control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d82c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d82c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d82c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d82c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d82c-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5d82c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5d82c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d82c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d82c-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую поля, используемые для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="5d82c-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d82c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d82c-111">Return value</span></span>

<span data-ttu-id="5d82c-112">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="5d82c-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="5d82c-113">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5d82c-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d82c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d82c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d82c-115">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="5d82c-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5d82c-116">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5d82c-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d82c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5d82c-117">Requirements</span></span>



| <span data-ttu-id="5d82c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5d82c-118">Requirement</span></span> | <span data-ttu-id="5d82c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5d82c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d82c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d82c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d82c-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d82c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d82c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d82c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d82c-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d82c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d82c-124">Header</span><span class="sxs-lookup"><span data-stu-id="5d82c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d82c-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d82c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d82c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d82c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d82c-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5d82c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d82c-128">**Кнопка " \_ сеттекстмаргин"**</span><span class="sxs-lookup"><span data-stu-id="5d82c-128">**Button\_SetTextMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

<span data-ttu-id="5d82c-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5d82c-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5d82c-130">Кнопки</span><span class="sxs-lookup"><span data-stu-id="5d82c-130">Buttons</span></span>](buttons.md)
</dt> </dl>

 

