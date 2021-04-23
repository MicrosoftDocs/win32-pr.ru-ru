---
title: Сообщение CB_SETCURSEL (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТКУРСЕЛ CB, чтобы выбрать строку в списке поля со списком.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- Элементы управления Windows для CB_SETCURSEL сообщений
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071607"
---
# <a name="cb_setcursel-message"></a><span data-ttu-id="52d46-104">\_Сообщение СЕТКУРСЕЛ CB</span><span class="sxs-lookup"><span data-stu-id="52d46-104">CB\_SETCURSEL message</span></span>

<span data-ttu-id="52d46-105">Приложение отправляет сообщение **\_ сеткурсел CB** , чтобы выбрать строку в списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="52d46-105">An application sends a **CB\_SETCURSEL** message to select a string in the list of a combo box.</span></span> <span data-ttu-id="52d46-106">При необходимости список Прокручивает строку в представление.</span><span class="sxs-lookup"><span data-stu-id="52d46-106">If necessary, the list scrolls the string into view.</span></span> <span data-ttu-id="52d46-107">Текст в элементе управления "поле со списком" изменяется в соответствии с новым выделением, и все предыдущие выделения в списке удаляются.</span><span class="sxs-lookup"><span data-stu-id="52d46-107">The text in the edit control of the combo box changes to reflect the new selection, and any previous selection in the list is removed.</span></span>

## <a name="parameters"></a><span data-ttu-id="52d46-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52d46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d46-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52d46-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52d46-110">Указывает отсчитываемый от нуля индекс строки для выбора.</span><span class="sxs-lookup"><span data-stu-id="52d46-110">Specifies the zero-based index of the string to select.</span></span> <span data-ttu-id="52d46-111">Если этот параметр имеет значение-1, все текущие выделенные элементы списка удаляются, а элемент управления "поле ввода" удаляется.</span><span class="sxs-lookup"><span data-stu-id="52d46-111">If this parameter is -1, any current selection in the list is removed and the edit control is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="52d46-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52d46-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52d46-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="52d46-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d46-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52d46-114">Return value</span></span>

<span data-ttu-id="52d46-115">Если сообщение прошло успешно, возвращается значение индекса выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="52d46-115">If the message is successful, the return value is the index of the item selected.</span></span> <span data-ttu-id="52d46-116">Если параметр *wParam* больше числа элементов в списке или параметр *wParam* равен-1, возвращается значение CB \_ Err, а выделение снимается.</span><span class="sxs-lookup"><span data-stu-id="52d46-116">If *wParam* is greater than the number of items in the list or if *wParam* is -1, the return value is CB\_ERR and the selection is cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d46-117">Требования</span><span class="sxs-lookup"><span data-stu-id="52d46-117">Requirements</span></span>



| <span data-ttu-id="52d46-118">Требование</span><span class="sxs-lookup"><span data-stu-id="52d46-118">Requirement</span></span> | <span data-ttu-id="52d46-119">Значение</span><span class="sxs-lookup"><span data-stu-id="52d46-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52d46-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52d46-120">Minimum supported client</span></span><br/> | <span data-ttu-id="52d46-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52d46-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52d46-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52d46-122">Minimum supported server</span></span><br/> | <span data-ttu-id="52d46-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52d46-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52d46-124">Header</span><span class="sxs-lookup"><span data-stu-id="52d46-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d46-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52d46-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d46-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52d46-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="52d46-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="52d46-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52d46-128">**\_FINDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="52d46-128">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="52d46-129">**CB \_**</span><span class="sxs-lookup"><span data-stu-id="52d46-129">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="52d46-130">**\_СЕЛЕКТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="52d46-130">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> </dl>

 

 





