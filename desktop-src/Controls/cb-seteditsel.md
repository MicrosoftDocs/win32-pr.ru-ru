---
title: Сообщение CB_SETEDITSEL (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТЕДИТСЕЛ CB для выбора символов в элементе управления "поле ввода" поля со списком.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- Элементы управления Windows для CB_SETEDITSEL сообщений
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490524"
---
# <a name="cb_seteditsel-message"></a><span data-ttu-id="b4320-104">\_Сообщение СЕТЕДИТСЕЛ CB</span><span class="sxs-lookup"><span data-stu-id="b4320-104">CB\_SETEDITSEL message</span></span>

<span data-ttu-id="b4320-105">Приложение отправляет сообщение **\_ сетедитсел CB** для выбора символов в элементе управления "поле ввода" поля со списком.</span><span class="sxs-lookup"><span data-stu-id="b4320-105">An application sends a **CB\_SETEDITSEL** message to select characters in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4320-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4320-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4320-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4320-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b4320-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b4320-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4320-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4320-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) параметра *lParam* указывает начальную точку.</span><span class="sxs-lookup"><span data-stu-id="b4320-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* specifies the starting position.</span></span> <span data-ttu-id="b4320-111">Если **ловорд** имеет значение-1, то выбор, если он есть, будет удален.</span><span class="sxs-lookup"><span data-stu-id="b4320-111">If the **LOWORD** is -1, the selection, if any, is removed.</span></span>

<span data-ttu-id="b4320-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) параметра *lParam* задает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="b4320-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of *lParam* specifies the ending position.</span></span> <span data-ttu-id="b4320-113">Если **HIWORD** имеет значение-1, то выбирается весь текст из начальной позиции к последнему символу в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="b4320-113">If the **HIWORD** is -1, all text from the starting position to the last character in the edit control is selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4320-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4320-114">Return value</span></span>

<span data-ttu-id="b4320-115">Если сообщение прошло удачно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="b4320-115">If the message succeeds, the return value is **TRUE**.</span></span> <span data-ttu-id="b4320-116">Если сообщение отправляется в поле со списком с помощью стиля [**\_ DROPDOWNLIST**](combo-box-styles.md) , то это значение — CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="b4320-116">If the message is sent to a combo box with the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4320-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4320-117">Remarks</span></span>

<span data-ttu-id="b4320-118">Позиции отсчитываются от нуля.</span><span class="sxs-lookup"><span data-stu-id="b4320-118">The positions are zero-based.</span></span> <span data-ttu-id="b4320-119">Первый символ элемента управления "поле ввода" находится в нулевой позиции.</span><span class="sxs-lookup"><span data-stu-id="b4320-119">The first character of the edit control is in the zero position.</span></span> <span data-ttu-id="b4320-120">Первый символ после последнего выбранного символа находится в конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="b4320-120">The first character after the last selected character is in the ending position.</span></span> <span data-ttu-id="b4320-121">Например, чтобы выбрать первые четыре символа элемента управления "поле ввода", используйте начальную точку 0 и конечную точку 4.</span><span class="sxs-lookup"><span data-stu-id="b4320-121">For example, to select the first four characters of the edit control, use a starting position of 0 and an ending position of 4.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4320-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b4320-122">Requirements</span></span>



| <span data-ttu-id="b4320-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b4320-123">Requirement</span></span> | <span data-ttu-id="b4320-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b4320-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4320-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4320-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b4320-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4320-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4320-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4320-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b4320-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4320-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4320-129">Header</span><span class="sxs-lookup"><span data-stu-id="b4320-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4320-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4320-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4320-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4320-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4320-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b4320-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b4320-133">**\_ЖЕТЕДИТСЕЛ CB**</span><span class="sxs-lookup"><span data-stu-id="b4320-133">**CB\_GETEDITSEL**</span></span>](cb-geteditsel.md)
</dt> <dt>

<span data-ttu-id="b4320-134">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b4320-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b4320-135">**макелпарам**</span><span class="sxs-lookup"><span data-stu-id="b4320-135">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

