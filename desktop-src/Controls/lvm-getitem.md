---
title: Сообщение LVM_GETITEM (Коммктрл. h)
description: Извлекает некоторые или все атрибуты элемента представления списка. Это сообщение можно отправить явным образом или с помощью \_ макроса элемента ListView.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- Элементы управления Windows для LVM_GETITEM сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803395"
---
# <a name="lvm_getitem-message"></a><span data-ttu-id="4a033-105">\_Сообщение LVM</span><span class="sxs-lookup"><span data-stu-id="4a033-105">LVM\_GETITEM message</span></span>

<span data-ttu-id="4a033-106">Извлекает некоторые или все атрибуты элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="4a033-106">Retrieves some or all of a list-view item's attributes.</span></span> <span data-ttu-id="4a033-107">Это сообщение можно отправить явным образом или с помощью макроса [**\_ элемента ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="4a033-107">You can send this message explicitly or by using the [**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a033-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a033-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a033-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a033-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4a033-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4a033-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4a033-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a033-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a033-112">Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , указывающую сведения для извлечения и получения сведений об элементе List-View.</span><span class="sxs-lookup"><span data-stu-id="4a033-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the information to retrieve and receives information about the list-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a033-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a033-113">Return value</span></span>

<span data-ttu-id="4a033-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4a033-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a033-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a033-115">Remarks</span></span>

<span data-ttu-id="4a033-116">При отправке сообщения **LVM- \_ Item** элементы **Член iItem** и **iSubItem** определяют элемент или подэлемент для получения сведений, а элемент **Mask** указывает, какие атрибуты следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="4a033-116">When the **LVM\_GETITEM** message is sent, the **iItem** and **iSubItem** members identify the item or subitem to retrieve information about and the **mask** member specifies which attributes to retrieve.</span></span> <span data-ttu-id="4a033-117">Список возможных значений см. в описании структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="4a033-117">For a list of possible values, see the description of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

<span data-ttu-id="4a033-118">Если в элементе \_ **Mask** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) задан флаг Лвиф Text, то элемент **псзтекст** должен указывать на допустимый буфер, а элемент **кчтекстмакс** должен быть установлен в значение, равное количеству символов в этом буфере.</span><span class="sxs-lookup"><span data-stu-id="4a033-118">If the LVIF\_TEXT flag is set in the **mask** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span> <span data-ttu-id="4a033-119">В приложениях не следует рассчитывать, что текст обязательно будет помещен в указанный буфер.</span><span class="sxs-lookup"><span data-stu-id="4a033-119">Applications should not assume that the text will necessarily be placed in the specified buffer.</span></span> <span data-ttu-id="4a033-120">Вместо этого элемент управления может изменить элемент **псзтекст** структуры, чтобы он указывал на новый текст, а не поместить его в буфер.</span><span class="sxs-lookup"><span data-stu-id="4a033-120">The control may instead change the **pszText** member of the structure to point to the new text, rather than place it in the buffer.</span></span>

<span data-ttu-id="4a033-121">Если элемент **маски** задает \_ значение состояния лвиф, то элемент **статемаск** должен указывать извлекаемые биты состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="4a033-121">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member must specify the item state bits to retrieve.</span></span> <span data-ttu-id="4a033-122">В выходных данных элемент **State** содержит значения заданных битов состояния.</span><span class="sxs-lookup"><span data-stu-id="4a033-122">On output, the **state** member contains the values of the specified state bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a033-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4a033-123">Requirements</span></span>



| <span data-ttu-id="4a033-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4a033-124">Requirement</span></span> | <span data-ttu-id="4a033-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4a033-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a033-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a033-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4a033-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a033-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a033-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a033-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4a033-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a033-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a033-130">Header</span><span class="sxs-lookup"><span data-stu-id="4a033-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a033-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a033-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4a033-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4a033-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4a033-133">**LVM \_ ЖЕТИТЕМВ** (Юникод) и **LVM- \_ элемент** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4a033-133">**LVM\_GETITEMW** (Unicode) and **LVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





