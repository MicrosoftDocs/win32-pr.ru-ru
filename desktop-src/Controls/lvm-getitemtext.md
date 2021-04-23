---
title: Сообщение LVM_GETITEMTEXT (Коммктрл. h)
description: Извлекает текст элемента представления списка или подэлемента. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемтекст ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Элементы управления Windows для LVM_GETITEMTEXT сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137114"
---
# <a name="lvm_getitemtext-message"></a><span data-ttu-id="4a725-105">\_Сообщение LVM жетитемтекст</span><span class="sxs-lookup"><span data-stu-id="4a725-105">LVM\_GETITEMTEXT message</span></span>

<span data-ttu-id="4a725-106">Извлекает текст элемента представления списка или подэлемента.</span><span class="sxs-lookup"><span data-stu-id="4a725-106">Retrieves the text of a list-view item or subitem.</span></span> <span data-ttu-id="4a725-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемтекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="4a725-107">You can send this message explicitly or by using the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a725-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a725-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a725-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a725-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a725-110">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="4a725-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="4a725-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a725-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a725-112">Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="4a725-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="4a725-113">Чтобы получить текст элемента, задайте для **iSubItem** значение 0.</span><span class="sxs-lookup"><span data-stu-id="4a725-113">To retrieve the item text, set **iSubItem** to zero.</span></span> <span data-ttu-id="4a725-114">Чтобы получить текст подэлемента, установите **iSubItem** в качестве индекса подэлемента.</span><span class="sxs-lookup"><span data-stu-id="4a725-114">To retrieve the text of a subitem, set **iSubItem** to the subitem's index.</span></span> <span data-ttu-id="4a725-115">Элемент **псзтекст** указывает на буфер, который получает текст.</span><span class="sxs-lookup"><span data-stu-id="4a725-115">The **pszText** member points to a buffer that receives the text.</span></span> <span data-ttu-id="4a725-116">Элемент **кчтекстмакс** указывает количество символов в буфере.</span><span class="sxs-lookup"><span data-stu-id="4a725-116">The **cchTextMax** member specifies the number of characters in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a725-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a725-117">Return value</span></span>

<span data-ttu-id="4a725-118">Если сообщение отправляется явным образом, оно возвращает число символов в элементе **псзтекст** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="4a725-118">If you send this message explicitly, it returns the number of characters in the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a725-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a725-119">Remarks</span></span>

<span data-ttu-id="4a725-120">Это сообщение можно также отправить, вызвав макрос [**\_ жетитемтекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="4a725-120">You can also send this message by calling the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span> <span data-ttu-id="4a725-121">Однако этот макрос не возвращает длину строки.</span><span class="sxs-lookup"><span data-stu-id="4a725-121">However, this macro does not return the string length.</span></span>

<span data-ttu-id="4a725-122">**LVM \_ ЖЕТИТЕМТЕКСТ** не поддерживается в стиле [**LVS \_ овнердата**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4a725-122">**LVM\_GETITEMTEXT** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a725-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4a725-123">Requirements</span></span>



| <span data-ttu-id="4a725-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4a725-124">Requirement</span></span> | <span data-ttu-id="4a725-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4a725-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a725-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a725-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4a725-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a725-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a725-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a725-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4a725-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a725-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a725-130">Header</span><span class="sxs-lookup"><span data-stu-id="4a725-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a725-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a725-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4a725-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4a725-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4a725-133">**LVM \_ ЖЕТИТЕМТЕКСТВ** (Юникод) и **LVM \_ жетитемтекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4a725-133">**LVM\_GETITEMTEXTW** (Unicode) and **LVM\_GETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





