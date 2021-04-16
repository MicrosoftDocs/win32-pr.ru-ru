---
title: Сообщение WM_COMPAREITEM (Winuser. h)
description: Отправляется, чтобы определить относительное расположение нового элемента в отсортированном списке рисуемого владельцем поля со списком или списка.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- Элементы управления Windows для WM_COMPAREITEM сообщений
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489006"
---
# <a name="wm_compareitem-message"></a><span data-ttu-id="b778d-104">\_Сообщение КОМПАРЕИТЕМ WM</span><span class="sxs-lookup"><span data-stu-id="b778d-104">WM\_COMPAREITEM message</span></span>

<span data-ttu-id="b778d-105">Отправляется, чтобы определить относительное расположение нового элемента в отсортированном списке рисуемого владельцем поля со списком или списка.</span><span class="sxs-lookup"><span data-stu-id="b778d-105">Sent to determine the relative position of a new item in the sorted list of an owner-drawn combo box or list box.</span></span> <span data-ttu-id="b778d-106">Каждый раз, когда приложение добавляет новый элемент, система отправляет это сообщение владельцу поля со списком или списка, созданного с помощью параметра [**CBS \_ Sort**](combo-box-styles.md) или [**фунтов \_ сортировки**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b778d-106">Whenever the application adds a new item, the system sends this message to the owner of a combo box or list box created with the [**CBS\_SORT**](combo-box-styles.md) or [**LBS\_SORT**](list-box-styles.md) style.</span></span>


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b778d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b778d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b778d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b778d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b778d-109">Указывает идентификатор элемента управления, который отправил сообщение **WM \_ компареитем** .</span><span class="sxs-lookup"><span data-stu-id="b778d-109">Specifies the identifier of the control that sent the **WM\_COMPAREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="b778d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b778d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b778d-111">Указатель на структуру [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) , которая содержит идентификаторы и данные, предоставляемые приложением, для двух элементов в поле со списком или в списке.</span><span class="sxs-lookup"><span data-stu-id="b778d-111">Pointer to a [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure that contains the identifiers and application-supplied data for two items in the combo or list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b778d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b778d-112">Return value</span></span>

<span data-ttu-id="b778d-113">Возвращаемое значение указывает относительное расположение двух элементов.</span><span class="sxs-lookup"><span data-stu-id="b778d-113">The return value indicates the relative position of the two items.</span></span> <span data-ttu-id="b778d-114">Это может быть любое из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b778d-114">It may be any of the values shown in the following table.</span></span>



| <span data-ttu-id="b778d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b778d-115">Return code</span></span>                                                                          | <span data-ttu-id="b778d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b778d-116">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="b778d-117"><dt>**Значение**</dt></span><span class="sxs-lookup"><span data-stu-id="b778d-117"><dt>**Value**</dt></span></span> </dl> | <span data-ttu-id="b778d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b778d-118">Meaning</span></span><br/>                                           |
| <dl> <span data-ttu-id="b778d-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="b778d-119"><dt>**-1**</dt></span></span> </dl>    | <span data-ttu-id="b778d-120">Элемент 1 предшествует элементу 2 в отсортированном порядке.</span><span class="sxs-lookup"><span data-stu-id="b778d-120">Item 1 precedes item 2 in the sorted order.</span></span><br/>       |
| <dl> <span data-ttu-id="b778d-121"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="b778d-121"><dt>**0**</dt></span></span> </dl>     | <span data-ttu-id="b778d-122">Элементы 1 и 2 эквивалентны в порядке сортировки.</span><span class="sxs-lookup"><span data-stu-id="b778d-122">Items 1 and 2 are equivalent in the sorted order.</span></span><br/> |
| <dl> <span data-ttu-id="b778d-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b778d-123"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="b778d-124">Элемент 1 соответствует элементу 2 в отсортированном порядке.</span><span class="sxs-lookup"><span data-stu-id="b778d-124">Item 1 follows item 2 in the sorted order.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="b778d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b778d-125">Remarks</span></span>

<span data-ttu-id="b778d-126">Когда владелец рисуемого владельцем поля со списком или списка получает это сообщение, владелец возвращает значение, указывающее, какие из элементов, указанных структурой [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) , будут отображаться перед другой.</span><span class="sxs-lookup"><span data-stu-id="b778d-126">When the owner of an owner-drawn combo box or list box receives this message, the owner returns a value indicating which of the items specified by the [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure will appear before the other.</span></span> <span data-ttu-id="b778d-127">Как правило, система отправляет это сообщение несколько раз до тех пор, пока оно не определит точную позицию для нового элемента.</span><span class="sxs-lookup"><span data-stu-id="b778d-127">Typically, the system sends this message several times until it determines the exact position for the new item.</span></span>

<span data-ttu-id="b778d-128">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к **логическому** типу и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="b778d-128">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="b778d-129">\_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b778d-129">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b778d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="b778d-130">Requirements</span></span>



| <span data-ttu-id="b778d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="b778d-131">Requirement</span></span> | <span data-ttu-id="b778d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b778d-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b778d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b778d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b778d-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b778d-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b778d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b778d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b778d-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b778d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b778d-137">Header</span><span class="sxs-lookup"><span data-stu-id="b778d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b778d-138"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b778d-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b778d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b778d-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="b778d-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b778d-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b778d-141">**COMPAREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="b778d-141">**COMPAREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

<span data-ttu-id="b778d-142">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b778d-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b778d-143">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="b778d-143">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

