---
title: Сообщение LVM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса InsertItem ListView.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- Элементы управления Windows для LVM_INSERTITEM сообщений
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654645"
---
# <a name="lvm_insertitem-message"></a><span data-ttu-id="22f09-105">\_Сообщение LVM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="22f09-105">LVM\_INSERTITEM message</span></span>

<span data-ttu-id="22f09-106">Вставляет новый элемент в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="22f09-106">Inserts a new item in a list-view control.</span></span> <span data-ttu-id="22f09-107">Это сообщение можно отправить явно или с помощью макроса [**\_ InsertItem ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="22f09-107">You can send this message explicitly or by using the [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="22f09-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="22f09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22f09-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22f09-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="22f09-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="22f09-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="22f09-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22f09-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22f09-112">Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , указывающую атрибуты элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="22f09-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the attributes of the list-view item.</span></span> <span data-ttu-id="22f09-113">Используйте элемент **Член iItem** , чтобы указать Отсчитываемый от нуля индекс, по которому следует вставить новый элемент.</span><span class="sxs-lookup"><span data-stu-id="22f09-113">Use the **iItem** member to specify the zero-based index at which the new item should be inserted.</span></span> <span data-ttu-id="22f09-114">Если это значение больше числа элементов, которые в настоящее время содержатся в ListView, новый элемент будет добавлен в конец списка и назначен правильному индексу.</span><span class="sxs-lookup"><span data-stu-id="22f09-114">If this value is greater than the number of items currently contained by the listview, the new item will be appended to the end of the list and assigned the correct index.</span></span> <span data-ttu-id="22f09-115">Проверьте возвращаемое значение сообщения, чтобы определить фактический индекс, назначенный элементу.</span><span class="sxs-lookup"><span data-stu-id="22f09-115">Examine the message's return value to determine the actual index assigned to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22f09-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22f09-116">Return value</span></span>

<span data-ttu-id="22f09-117">Возвращает индекс нового элемента, если он выполнен успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="22f09-117">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="22f09-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22f09-118">Remarks</span></span>

<span data-ttu-id="22f09-119">Нельзя использовать [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) или **LVM \_ InsertItem** для вставки подэлементов.</span><span class="sxs-lookup"><span data-stu-id="22f09-119">You cannot use [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) or **LVM\_INSERTITEM** to insert subitems.</span></span> <span data-ttu-id="22f09-120">Элемент **iSubItem** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="22f09-120">The **iSubItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure must be zero.</span></span> <span data-ttu-id="22f09-121">Сведения о настройке подэлементов см. в разделе [**LVM \_ сетитем**](lvm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="22f09-121">See [**LVM\_SETITEM**](lvm-setitem.md) for information on setting subitems.</span></span>

<span data-ttu-id="22f09-122">Если для элемента управления "представление списка" установлен стиль [**LVS \_ ex \_**](extended-list-view-styles.md) , любое значение, помещенное в битах 12 – 15 элемента **State** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="22f09-122">If a list-view control has the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style set, any value placed in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure will be ignored.</span></span> <span data-ttu-id="22f09-123">При добавлении элемента с этим набором стилей всегда будет задано непроверенное состояние.</span><span class="sxs-lookup"><span data-stu-id="22f09-123">When an item is added with this style set, it will always be set to the unchecked state.</span></span>

<span data-ttu-id="22f09-124">Если элемент управления "представление списка" имеет стиль окна [**LVS \_ Сортасцендинг**](list-view-window-styles.md) или [**LVS \_ сортдесцендинг**](list-view-window-styles.md) , сообщение **LVM \_ INSERTITEM** будет неудачным, если попытаться вставить элемент с LPSTR \_ тексткаллбакк в качестве значения для его элемента **псзтекст** .</span><span class="sxs-lookup"><span data-stu-id="22f09-124">If a list-view control has either the [**LVS\_SORTASCENDING**](list-view-window-styles.md) or [**LVS\_SORTDESCENDING**](list-view-window-styles.md) window style, an **LVM\_INSERTITEM** message will fail if you try to insert an item that has LPSTR\_TEXTCALLBACK as the value for its **pszText** member.</span></span>

<span data-ttu-id="22f09-125">Сообщение **LVM \_ INSERTITEM** будет вставлять новый элемент в надлежащей позиции в порядке сортировки, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="22f09-125">The **LVM\_INSERTITEM** message will insert the new item in the proper position in the sort order if the following conditions hold:</span></span>

-   <span data-ttu-id="22f09-126">Вы используете один из \_ стилей LVS сорткскскс.</span><span class="sxs-lookup"><span data-stu-id="22f09-126">You are using one of the LVS\_SORTXXX styles.</span></span>
-   <span data-ttu-id="22f09-127">Вы не используете стиль [**\_ овнердрав LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="22f09-127">You are not using the [**LVS\_OWNERDRAW**](list-view-window-styles.md) style.</span></span>
-   <span data-ttu-id="22f09-128">Элемент **псзтекст** структуры, на который указывает **питем** , не имеет значение LPSTR \_ тексткаллбакк.</span><span class="sxs-lookup"><span data-stu-id="22f09-128">The **pszText** member of the structure pointed to by **pitem** is not set to LPSTR\_TEXTCALLBACK.</span></span>

<span data-ttu-id="22f09-129">Если структура [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) не содержит лвиф \_ GROUPID в члене **Mask** , значение элемента **играупид** — I \_ граупидкаллбакк по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22f09-129">If the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure does not contain LVIF\_GROUPID in the **mask** member, the value of the **iGroupId** member is I\_GROUPIDCALLBACK by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="22f09-130">Требования</span><span class="sxs-lookup"><span data-stu-id="22f09-130">Requirements</span></span>



| <span data-ttu-id="22f09-131">Требование</span><span class="sxs-lookup"><span data-stu-id="22f09-131">Requirement</span></span> | <span data-ttu-id="22f09-132">Значение</span><span class="sxs-lookup"><span data-stu-id="22f09-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22f09-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22f09-133">Minimum supported client</span></span><br/> | <span data-ttu-id="22f09-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22f09-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22f09-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22f09-135">Minimum supported server</span></span><br/> | <span data-ttu-id="22f09-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22f09-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22f09-137">Header</span><span class="sxs-lookup"><span data-stu-id="22f09-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="22f09-138"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="22f09-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="22f09-139">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="22f09-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="22f09-140">**LVM \_ ИНСЕРТИТЕМВ** (Юникод) и **LVM \_ инсертитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="22f09-140">**LVM\_INSERTITEMW** (Unicode) and **LVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





