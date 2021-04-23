---
title: Сообщение WM_DELETEITEM (Winuser. h)
description: Посылается владельцу списка или поля со списком при удалении списка или поля со списком, а также при удалении элементов с помощью \_ сообщения делетестринг, балансировки нагрузки \_ РЕСЕТКОНТЕНТ, CB \_ делетестринг или CB \_ ресетконтент.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- Элементы управления Windows для WM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490365"
---
# <a name="wm_deleteitem-message"></a><span data-ttu-id="b51ef-104">\_Сообщение DELETEITEM WM</span><span class="sxs-lookup"><span data-stu-id="b51ef-104">WM\_DELETEITEM message</span></span>

<span data-ttu-id="b51ef-105">Посылается владельцу списка или поля со списком при удалении списка или поля со списком, а также при удалении элементов с помощью сообщения [**\_ делетестринг**](lb-deletestring.md), [**балансировки нагрузки \_ Ресетконтент**](lb-resetcontent.md), [**CB \_ делетестринг**](cb-deletestring.md)или [**CB \_ ресетконтент**](cb-resetcontent.md) .</span><span class="sxs-lookup"><span data-stu-id="b51ef-105">Sent to the owner of a list box or combo box when the list box or combo box is destroyed or when items are removed by the [**LB\_DELETESTRING**](lb-deletestring.md), [**LB\_RESETCONTENT**](lb-resetcontent.md), [**CB\_DELETESTRING**](cb-deletestring.md), or [**CB\_RESETCONTENT**](cb-resetcontent.md) message.</span></span> <span data-ttu-id="b51ef-106">Система отправляет сообщение **WM \_ DELETEITEM** для каждого удаленного элемента.</span><span class="sxs-lookup"><span data-stu-id="b51ef-106">The system sends a **WM\_DELETEITEM** message for each deleted item.</span></span> <span data-ttu-id="b51ef-107">Система отправляет сообщение **WM \_ DELETEITEM** для любого удаленного поля списка или элемента поля со списком с ненулевыми данными элемента.</span><span class="sxs-lookup"><span data-stu-id="b51ef-107">The system sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b51ef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b51ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b51ef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b51ef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b51ef-110">Указывает идентификатор элемента управления, который отправил сообщение **WM \_ DELETEITEM** .</span><span class="sxs-lookup"><span data-stu-id="b51ef-110">Specifies the identifier of the control that sent the **WM\_DELETEITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="b51ef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b51ef-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b51ef-112">Указатель на структуру [**делетеитемструкт**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) , содержащую сведения об элементе, удаленном из списка.</span><span class="sxs-lookup"><span data-stu-id="b51ef-112">Pointer to a [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) structure that contains information about the item deleted from a list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b51ef-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b51ef-113">Return value</span></span>

<span data-ttu-id="b51ef-114">Приложение должно возвращать **значение true** , если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="b51ef-114">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b51ef-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b51ef-115">Remarks</span></span>

<span data-ttu-id="b51ef-116">Microsoft Windows NT и более поздние версии: Windows отправляет сообщение **WM \_ DELETEITEM** только для элементов, удаленных из списка, нарисованного владельцем (с помощью стиля [**фунта \_ овнердравфиксед**](list-box-styles.md) или [**фунта \_ овнердраввариабле**](list-box-styles.md) ) или поля со списком, рисуемого владельцем (с помощью [**CBS \_ овнердравфиксед**](combo-box-styles.md) или типа [**CBS \_ овнердраввариабле**](combo-box-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="b51ef-116">Microsoft Windows NT and later: Windows sends a **WM\_DELETEITEM** message only for items deleted from an owner-drawn list box (with the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) or [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style) or owner-drawn combo box (with the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style).</span></span>

<span data-ttu-id="b51ef-117">Windows 95: Windows отправляет сообщение **WM \_ DELETEITEM** для любого удаленного поля списка или элемента поля со списком с ненулевыми данными элемента.</span><span class="sxs-lookup"><span data-stu-id="b51ef-117">Windows 95: Windows sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b51ef-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b51ef-118">Requirements</span></span>



| <span data-ttu-id="b51ef-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b51ef-119">Requirement</span></span> | <span data-ttu-id="b51ef-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b51ef-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b51ef-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b51ef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b51ef-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b51ef-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b51ef-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b51ef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b51ef-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b51ef-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b51ef-125">Header</span><span class="sxs-lookup"><span data-stu-id="b51ef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b51ef-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b51ef-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b51ef-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b51ef-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b51ef-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b51ef-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b51ef-129">**\_ДЕЛЕТЕСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="b51ef-129">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="b51ef-130">**\_РЕСЕТКОНТЕНТ CB**</span><span class="sxs-lookup"><span data-stu-id="b51ef-130">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="b51ef-131">**делетеитемструкт**</span><span class="sxs-lookup"><span data-stu-id="b51ef-131">**DELETEITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[<span data-ttu-id="b51ef-132">**делетестринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="b51ef-132">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="b51ef-133">**ресетконтент балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="b51ef-133">**LB\_RESETCONTENT**</span></span>](lb-resetcontent.md)
</dt> </dl>

 

 





