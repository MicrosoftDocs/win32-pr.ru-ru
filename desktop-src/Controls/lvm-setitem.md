---
title: Сообщение LVM_SETITEM (Коммктрл. h)
description: Задает некоторые или все атрибуты элемента представления списка. Можно также отправить LVM \_ сетитем, чтобы задать текст подэлемента. Это сообщение можно отправить явно или с помощью \_ макроса Сетитем ListView.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- Элементы управления Windows для LVM_SETITEM сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071387"
---
# <a name="lvm_setitem-message"></a><span data-ttu-id="d0b3e-106">\_Сообщение LVM сетитем</span><span class="sxs-lookup"><span data-stu-id="d0b3e-106">LVM\_SETITEM message</span></span>

<span data-ttu-id="d0b3e-107">Задает некоторые или все атрибуты элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-107">Sets some or all of a list-view item's attributes.</span></span> <span data-ttu-id="d0b3e-108">Можно также отправить LVM \_ сетитем, чтобы задать текст подэлемента.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-108">You can also send LVM\_SETITEM to set the text of a subitem.</span></span> <span data-ttu-id="d0b3e-109">Это сообщение можно отправить явно или с помощью макроса [**\_ сетитем ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="d0b3e-109">You can send this message explicitly or by using the [**ListView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0b3e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0b3e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b3e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0b3e-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d0b3e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d0b3e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0b3e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b3e-114">Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , содержащую новые атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-114">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="d0b3e-115">Члены **Член iItem** и **iSubItem** определяют элемент или подэлемент, а элемент **Mask** указывает, какие атрибуты задаются.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-115">The **iItem** and **iSubItem** members identify the item or subitem, and the **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="d0b3e-116">Если элемент **Mask** задает \_ текстовое значение лвиф, то элемент **псзтекст** является адресом строки, завершающейся нулем, а элемент **кчтекстмакс** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-116">If the **mask** member specifies the LVIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span> <span data-ttu-id="d0b3e-117">Если элемент **Mask** задает \_ значение состояния лвиф, то элемент **статемаск** указывает, какие состояния элементов следует изменить, а элемент **State** содержит значения этих состояний.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-117">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member specifies which item states to change and the **state** member contains the values for those states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b3e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0b3e-118">Return value</span></span>

<span data-ttu-id="d0b3e-119">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-119">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b3e-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0b3e-120">Remarks</span></span>

<span data-ttu-id="d0b3e-121">Чтобы задать атрибуты элемента списка, установите для элемента **Член iItem** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) индекс элемента и установите для элемента **iSubItem** значение Zero.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-121">To set the attributes of a list-view item, set the **iItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the index of the item, and set the **iSubItem** member to zero.</span></span> <span data-ttu-id="d0b3e-122">Для элемента можно задать элементы **State**, **псзтекст**, **иимаже** и **lParam** структуры **лвитем** .</span><span class="sxs-lookup"><span data-stu-id="d0b3e-122">For an item, you can set the **state**, **pszText**, **iImage**, and **lParam** members of the **LVITEM** structure.</span></span>

<span data-ttu-id="d0b3e-123">Чтобы задать текст для подэлемента, задайте элементы **Член iItem** и **iSubItem** , чтобы указать конкретный подэлемент, и используйте элемент **псзтекст** для указания текста.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-123">To set the text of a subitem, set the **iItem** and **iSubItem** members to indicate the specific subitem, and use the **pszText** member to specify the text.</span></span> <span data-ttu-id="d0b3e-124">Кроме того, можно использовать макрос [**\_ сетитемтекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) для установки текста вложенного элемента.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-124">Alternatively, you can use the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro to set the text of a subitem.</span></span> <span data-ttu-id="d0b3e-125">Нельзя задать элементы **State** или **lParam** для подэлементов, так как они не имеют этих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-125">You cannot set the **state** or **lParam** members for subitems because subitems do not have these attributes.</span></span> <span data-ttu-id="d0b3e-126">В версии 4,70 и более поздних можно задать элемент **иимаже** для подэлементов.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-126">In version 4.70 and later, you can set the **iImage** member for subitems.</span></span> <span data-ttu-id="d0b3e-127">Изображение подэлемента будет отображаться, если элемент управления "представление списка" имеет расширенный стиль [**LVS \_ ex \_ субитемимажес**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b3e-127">The subitem image will be displayed if the list-view control has the [**LVS\_EX\_SUBITEMIMAGES**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="d0b3e-128">В предыдущих версиях изображение подэлемента будет пропущено.</span><span class="sxs-lookup"><span data-stu-id="d0b3e-128">Previous versions will ignore the subitem image.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b3e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d0b3e-129">Requirements</span></span>



| <span data-ttu-id="d0b3e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d0b3e-130">Requirement</span></span> | <span data-ttu-id="d0b3e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b3e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b3e-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0b3e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b3e-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0b3e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0b3e-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0b3e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b3e-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0b3e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0b3e-136">Header</span><span class="sxs-lookup"><span data-stu-id="d0b3e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0b3e-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b3e-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d0b3e-138">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d0b3e-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d0b3e-139">**LVM \_ СЕТИТЕМВ** (Юникод) и **LVM \_ сетитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d0b3e-139">**LVM\_SETITEMW** (Unicode) and **LVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





