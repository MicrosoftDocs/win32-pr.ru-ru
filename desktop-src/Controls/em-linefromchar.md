---
title: Сообщение EM_LINEFROMCHAR (Winuser. h)
description: Возвращает индекс строки, содержащей указанный индекс символа в многострочном элементе управления Edit.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Элементы управления Windows для EM_LINEFROMCHAR сообщений
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135607"
---
# <a name="em_linefromchar-message"></a><span data-ttu-id="a187e-104">\_Сообщение ЛИНЕФРОМЧАР EM</span><span class="sxs-lookup"><span data-stu-id="a187e-104">EM\_LINEFROMCHAR message</span></span>

<span data-ttu-id="a187e-105">Возвращает индекс строки, содержащей указанный индекс символа в многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="a187e-105">Gets the index of the line that contains the specified character index in a multiline edit control.</span></span> <span data-ttu-id="a187e-106">Индекс символа — это Отсчитываемый от нуля индекс символа, начиная с начала элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a187e-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="a187e-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a187e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a187e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a187e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a187e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a187e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a187e-110">Индекс символа, содержащегося в строке, номер которой должен быть получен.</span><span class="sxs-lookup"><span data-stu-id="a187e-110">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="a187e-111">Если этот параметр имеет значение-1, **EM \_ линефромчар** получает номер строки текущей строки (строка, содержащая курсор) или, если имеется выделенный фрагмент, номер строки, содержащей начало выделения.</span><span class="sxs-lookup"><span data-stu-id="a187e-111">If this parameter is -1, **EM\_LINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="a187e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a187e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a187e-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a187e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a187e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a187e-114">Return value</span></span>

<span data-ttu-id="a187e-115">Возвращаемое значение — номер строки, начинающейся с нуля, с индексом символа, указанным параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a187e-115">The return value is the zero-based line number of the line containing the character index specified by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="a187e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a187e-116">Remarks</span></span>

<span data-ttu-id="a187e-117">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a187e-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a187e-118">Если индекс символа больше 64 000, используйте сообщение [**EM \_ екслинефромчар**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="a187e-118">If the character index is greater than 64,000, use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span> <span data-ttu-id="a187e-119">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a187e-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a187e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a187e-120">Requirements</span></span>



| <span data-ttu-id="a187e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a187e-121">Requirement</span></span> | <span data-ttu-id="a187e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a187e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a187e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a187e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a187e-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a187e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a187e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a187e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a187e-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a187e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a187e-127">Header</span><span class="sxs-lookup"><span data-stu-id="a187e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a187e-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a187e-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a187e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a187e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a187e-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a187e-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a187e-131">**EM \_ екслинефромчар**</span><span class="sxs-lookup"><span data-stu-id="a187e-131">**EM\_EXLINEFROMCHAR**</span></span>](em-exlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="a187e-132">**EM \_ линеиндекс**</span><span class="sxs-lookup"><span data-stu-id="a187e-132">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





