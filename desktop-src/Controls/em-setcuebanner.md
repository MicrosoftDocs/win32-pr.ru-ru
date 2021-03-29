---
title: Сообщение EM_SETCUEBANNER (Коммктрл. h)
description: Задает текстовую подсказку или подсказку, отображаемую элементом управления "поле ввода" для запроса сведений о пользователе.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Элементы управления Windows для EM_SETCUEBANNER сообщений
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492468"
---
# <a name="em_setcuebanner-message"></a><span data-ttu-id="92ad5-104">\_Сообщение СЕТКУЕБАННЕР EM</span><span class="sxs-lookup"><span data-stu-id="92ad5-104">EM\_SETCUEBANNER message</span></span>

<span data-ttu-id="92ad5-105">Задает текстовую подсказку или подсказку, отображаемую элементом управления "поле ввода" для запроса сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="92ad5-105">Sets the textual cue, or tip, that is displayed by the edit control to prompt the user for information.</span></span>

## <a name="parameters"></a><span data-ttu-id="92ad5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92ad5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92ad5-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92ad5-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92ad5-108">**Значение true** , если баннер подсказки должен отображаться даже в том случае, если элемент управления "поле ввода" имеет фокус; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="92ad5-108">**TRUE** if the cue banner should show even when the edit control has focus; otherwise, **FALSE**.</span></span> <span data-ttu-id="92ad5-109">**False** — это поведение по умолчанию, которое закрывается при щелчке элемента управления пользователем.</span><span class="sxs-lookup"><span data-stu-id="92ad5-109">**FALSE** is the default behavior the cue banner disappears when the user clicks in the control.</span></span>

</dd> <dt>

<span data-ttu-id="92ad5-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92ad5-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92ad5-111">Указатель на строку в Юникоде, содержащую текст, отображаемый как текстовая подсказка.</span><span class="sxs-lookup"><span data-stu-id="92ad5-111">A pointer to a Unicode string that contains the text to display as the textual cue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92ad5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92ad5-112">Return value</span></span>

<span data-ttu-id="92ad5-113">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="92ad5-113">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="92ad5-114">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="92ad5-114">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="92ad5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92ad5-115">Remarks</span></span>

<span data-ttu-id="92ad5-116">В элементе управления "поле ввода", используемом для начала поиска, может отображаться текст "введите Поиск здесь" в виде текстового подсказки.</span><span class="sxs-lookup"><span data-stu-id="92ad5-116">An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue.</span></span> <span data-ttu-id="92ad5-117">Когда пользователь щелкает текст, текст исчезает, и пользователь может ввести.</span><span class="sxs-lookup"><span data-stu-id="92ad5-117">When the user clicks the text, the text goes away and the user can type.</span></span>

<span data-ttu-id="92ad5-118">Нельзя задать заголовок подсказки в многострочном элементе управления Edit или в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="92ad5-118">You cannot set a cue banner on a multiline edit control or on a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="92ad5-119">Чтобы использовать этот API, необходимо предоставить манифест, задающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="92ad5-119">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="92ad5-120">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="92ad5-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92ad5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="92ad5-121">Requirements</span></span>



| <span data-ttu-id="92ad5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="92ad5-122">Requirement</span></span> | <span data-ttu-id="92ad5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="92ad5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92ad5-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92ad5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="92ad5-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92ad5-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92ad5-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92ad5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="92ad5-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92ad5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92ad5-128">Header</span><span class="sxs-lookup"><span data-stu-id="92ad5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="92ad5-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="92ad5-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92ad5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92ad5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ad5-131">**Изменить \_ сеткуебаннертекст**</span><span class="sxs-lookup"><span data-stu-id="92ad5-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





