---
title: Сообщение LVM_SETITEMTEXT (Коммктрл. h)
description: Изменяет текст элемента представления списка или подэлемента. Это сообщение можно отправить явно или с помощью \_ макроса Сетитемтекст ListView.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- Элементы управления Windows для LVM_SETITEMTEXT сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892017"
---
# <a name="lvm_setitemtext-message"></a><span data-ttu-id="99f92-105">\_Сообщение LVM сетитемтекст</span><span class="sxs-lookup"><span data-stu-id="99f92-105">LVM\_SETITEMTEXT message</span></span>

<span data-ttu-id="99f92-106">Изменяет текст элемента представления списка или подэлемента.</span><span class="sxs-lookup"><span data-stu-id="99f92-106">Changes the text of a list-view item or subitem.</span></span> <span data-ttu-id="99f92-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетитемтекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .</span><span class="sxs-lookup"><span data-stu-id="99f92-107">You can send this message explicitly or by using the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="99f92-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="99f92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99f92-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99f92-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99f92-110">Отсчитываемый от нуля индекс элемента списка представления.</span><span class="sxs-lookup"><span data-stu-id="99f92-110">Zero-based index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="99f92-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99f92-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99f92-112">Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="99f92-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="99f92-113">Элемент **iSubItem** является индексом подэлемента или может быть равен нулю, чтобы задать метку элемента.</span><span class="sxs-lookup"><span data-stu-id="99f92-113">The **iSubItem** member is the index of the subitem, or it can be zero to set the item label.</span></span> <span data-ttu-id="99f92-114">Элемент **псзтекст** является адресом строки, завершающейся нулем, содержащей новый текст. Он также может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="99f92-114">The **pszText** member is the address of a null-terminated string containing the new text; it can also be **NULL**.</span></span> <span data-ttu-id="99f92-115">Элемент **псзтекст** также может быть LPSTR \_ тексткаллбакк для указания элемента обратного вызова, для которого в родительском окне сохраняется текст.</span><span class="sxs-lookup"><span data-stu-id="99f92-115">The **pszText** member can also be LPSTR\_TEXTCALLBACK to indicate a callback item for which the parent window stores the text.</span></span> <span data-ttu-id="99f92-116">В этом случае элемент управления "представление списка" отправляет родительский код уведомления [**ЛВН \_ жетдиспинфо**](lvn-getdispinfo.md) , когда он нуждается в тексте.</span><span class="sxs-lookup"><span data-stu-id="99f92-116">In this case, the list-view control sends the parent an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code when it needs the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99f92-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99f92-117">Return value</span></span>

<span data-ttu-id="99f92-118">Если сообщение отправляется явным образом, оно возвращает **true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="99f92-118">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f92-119">Требования</span><span class="sxs-lookup"><span data-stu-id="99f92-119">Requirements</span></span>



| <span data-ttu-id="99f92-120">Требование</span><span class="sxs-lookup"><span data-stu-id="99f92-120">Requirement</span></span> | <span data-ttu-id="99f92-121">Значение</span><span class="sxs-lookup"><span data-stu-id="99f92-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99f92-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99f92-122">Minimum supported client</span></span><br/> | <span data-ttu-id="99f92-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99f92-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99f92-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99f92-124">Minimum supported server</span></span><br/> | <span data-ttu-id="99f92-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99f92-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99f92-126">Header</span><span class="sxs-lookup"><span data-stu-id="99f92-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="99f92-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="99f92-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="99f92-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="99f92-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="99f92-129">**LVM \_ СЕТИТЕМТЕКСТВ** (Юникод) и **LVM \_ сетитемтекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="99f92-129">**LVM\_SETITEMTEXTW** (Unicode) and **LVM\_SETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





