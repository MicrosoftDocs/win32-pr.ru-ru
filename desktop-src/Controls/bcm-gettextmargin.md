---
title: Сообщение BCM_GETTEXTMARGIN (Коммктрл. h)
description: Возвращает поля, используемые для рисования текста в элементе управления "Кнопка". Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки жеттекстмаргин.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- Элементы управления Windows для BCM_GETTEXTMARGIN сообщений
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988556"
---
# <a name="bcm_gettextmargin-message"></a><span data-ttu-id="c072c-105">\_Сообщение ЖЕТТЕКСТМАРГИН BCM</span><span class="sxs-lookup"><span data-stu-id="c072c-105">BCM\_GETTEXTMARGIN message</span></span>

<span data-ttu-id="c072c-106">Возвращает поля, используемые для рисования текста в элементе управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="c072c-106">Gets the margins used to draw text in a button control.</span></span> <span data-ttu-id="c072c-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ жеттекстмаргин**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) .</span><span class="sxs-lookup"><span data-stu-id="c072c-107">You can send this message explicitly or use the [**Button\_GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c072c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c072c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c072c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c072c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c072c-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c072c-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c072c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c072c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c072c-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую поля, используемые для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="c072c-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c072c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c072c-113">Return value</span></span>

<span data-ttu-id="c072c-114">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="c072c-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="c072c-115">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c072c-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c072c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c072c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c072c-117">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="c072c-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c072c-118">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c072c-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c072c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c072c-119">Requirements</span></span>



| <span data-ttu-id="c072c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c072c-120">Requirement</span></span> | <span data-ttu-id="c072c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c072c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c072c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c072c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c072c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c072c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c072c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c072c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c072c-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c072c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c072c-126">Header</span><span class="sxs-lookup"><span data-stu-id="c072c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c072c-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c072c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

