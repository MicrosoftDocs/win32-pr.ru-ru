---
title: Сообщение WM_MEASUREITEM (Winuser. h)
description: Отправляется в окно владельца поля со списком, списка, элемента управления "список-представление" или пункта меню при создании элемента управления или меню.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- Элементы управления Windows для WM_MEASUREITEM сообщений
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892229"
---
# <a name="wm_measureitem-message"></a><span data-ttu-id="5dee7-104">\_Сообщение МЕАСУРЕИТЕМ WM</span><span class="sxs-lookup"><span data-stu-id="5dee7-104">WM\_MEASUREITEM message</span></span>

<span data-ttu-id="5dee7-105">Отправляется в окно владельца поля со списком, списка, элемента управления "список-представление" или пункта меню при создании элемента управления или меню.</span><span class="sxs-lookup"><span data-stu-id="5dee7-105">Sent to the owner window of a combo box, list box, list-view control, or menu item when the control or menu is created.</span></span>

<span data-ttu-id="5dee7-106">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5dee7-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5dee7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dee7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dee7-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dee7-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dee7-109">Содержит значение элемента **ктлид** структуры [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , на которое указывает параметр *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5dee7-109">Contains the value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="5dee7-110">Это значение определяет элемент управления, который отправил сообщение **WM \_ меасуреитем** .</span><span class="sxs-lookup"><span data-stu-id="5dee7-110">This value identifies the control that sent the **WM\_MEASUREITEM** message.</span></span> <span data-ttu-id="5dee7-111">Если значение равно нулю, сообщение было отправлено меню.</span><span class="sxs-lookup"><span data-stu-id="5dee7-111">If the value is zero, the message was sent by a menu.</span></span> <span data-ttu-id="5dee7-112">Если значение не равно нулю, сообщение было отправлено полем со списком или списком.</span><span class="sxs-lookup"><span data-stu-id="5dee7-112">If the value is nonzero, the message was sent by a combo box or by a list box.</span></span> <span data-ttu-id="5dee7-113">Если значение не равно нулю, а значение элемента **ItemId** в **меасуреитемструкт** , на которое указывает *lParam* , равно (UINT) 1, сообщение было отправлено комбинированным полем ввода.</span><span class="sxs-lookup"><span data-stu-id="5dee7-113">If the value is nonzero, and the value of the **itemID** member of the **MEASUREITEMSTRUCT** pointed to by *lParam* is (UINT)  1, the message was sent by a combo edit field.</span></span>

</dd> <dt>

<span data-ttu-id="5dee7-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dee7-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dee7-115">Указатель на структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , содержащую Размеры рисуемого владельцем элемента управления или пункта меню.</span><span class="sxs-lookup"><span data-stu-id="5dee7-115">Pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dee7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dee7-116">Return value</span></span>

<span data-ttu-id="5dee7-117">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="5dee7-117">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dee7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dee7-118">Remarks</span></span>

<span data-ttu-id="5dee7-119">Когда окно владельца получает сообщение **WM \_ меасуреитем** , владелец заполняет структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , на которую указывает параметр *lParam* сообщения, и возвращает значение; это значение указывает систему измерений элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5dee7-119">When the owner window receives the **WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span> <span data-ttu-id="5dee7-120">Если список или поле со списком создается с помощью стиля [**фунта \_ Овнердраввариабле**](list-box-styles.md) или [**CBS \_ овнердраввариабле**](combo-box-styles.md) , это сообщение отправляется владельцу для каждого элемента в элементе управления; в противном случае это сообщение отправляется один раз.</span><span class="sxs-lookup"><span data-stu-id="5dee7-120">If a list box or combo box is created with the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, this message is sent to the owner for each item in the control; otherwise, this message is sent once.</span></span>

<span data-ttu-id="5dee7-121">Система отправляет сообщение **WM \_ меасуреитем** в окно владельца полей со списком и списков, созданных с помощью стиля овнердравфиксед перед отправкой сообщения [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="5dee7-121">The system sends the **WM\_MEASUREITEM** message to the owner window of combo boxes and list boxes created with the OWNERDRAWFIXED style before sending the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="5dee7-122">В результате, когда владелец получает это сообщение, система еще не определила высоту и ширину шрифта, используемого в элементе управления. вызовы функций и вычисления, которым требуются эти значения, должны выполняться в основной функции приложения или библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5dee7-122">As a result, when the owner receives this message, the system has not yet determined the height and width of the font used in the control; function calls and calculations requiring these values should occur in the main function of the application or library.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dee7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5dee7-123">Requirements</span></span>



| <span data-ttu-id="5dee7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5dee7-124">Requirement</span></span> | <span data-ttu-id="5dee7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5dee7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dee7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dee7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5dee7-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5dee7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5dee7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dee7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5dee7-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5dee7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5dee7-130">Header</span><span class="sxs-lookup"><span data-stu-id="5dee7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dee7-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dee7-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dee7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dee7-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="5dee7-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5dee7-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5dee7-134">**меасуреитемструкт**</span><span class="sxs-lookup"><span data-stu-id="5dee7-134">**MEASUREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

<span data-ttu-id="5dee7-135">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="5dee7-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5dee7-136">**WM \_ инитдиалог**</span><span class="sxs-lookup"><span data-stu-id="5dee7-136">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

