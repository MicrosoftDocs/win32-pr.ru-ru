---
title: Сообщение TB_ADDBUTTONS (Коммктрл. h)
description: Добавляет одну или несколько кнопок на панель инструментов.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- Элементы управления Windows для TB_ADDBUTTONS сообщений
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989441"
---
# <a name="tb_addbuttons-message"></a><span data-ttu-id="4c38f-104">\_Сообщение АДДБУТТОНС ТБ</span><span class="sxs-lookup"><span data-stu-id="4c38f-104">TB\_ADDBUTTONS message</span></span>

<span data-ttu-id="4c38f-105">Добавляет одну или несколько кнопок на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="4c38f-105">Adds one or more buttons to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c38f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c38f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c38f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c38f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c38f-108">Число добавляемых кнопок.</span><span class="sxs-lookup"><span data-stu-id="4c38f-108">Number of buttons to add.</span></span>

</dd> <dt>

<span data-ttu-id="4c38f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c38f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c38f-110">Указатель на массив структур [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , содержащих сведения о добавляемых кнопках.</span><span class="sxs-lookup"><span data-stu-id="4c38f-110">Pointer to an array of [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures that contain information about the buttons to add.</span></span> <span data-ttu-id="4c38f-111">Число элементов в массиве должно совпадать с кнопками, заданными параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="4c38f-111">There must be the same number of elements in the array as buttons specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c38f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c38f-112">Return value</span></span>

<span data-ttu-id="4c38f-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4c38f-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c38f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c38f-114">Remarks</span></span>

<span data-ttu-id="4c38f-115">Если панель инструментов была создана с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , перед отправкой **\_ аддбуттонс ТБ** необходимо отправить на панель инструментов сообщение [**\_ буттонструктсизе**](tb-buttonstructsize.md) ТБ.</span><span class="sxs-lookup"><span data-stu-id="4c38f-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBUTTONS**.</span></span>

<span data-ttu-id="4c38f-116">Сведения о назначении точечных рисунков кнопкам панели инструментов из одного или нескольких списков изображений см. в статье [**ТБ \_ сетимажелист**](tb-setimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="4c38f-116">See [**TB\_SETIMAGELIST**](tb-setimagelist.md) for a discussion of how to assign bitmaps to toolbar buttons from one or more image lists.</span></span>

## <a name="examples"></a><span data-ttu-id="4c38f-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="4c38f-117">Examples</span></span>

<span data-ttu-id="4c38f-118">В следующем примере кода на панель инструментов добавляются три кнопки с использованием стандартного системного точечного рисунка для кнопок просмотра.</span><span class="sxs-lookup"><span data-stu-id="4c38f-118">The following example code adds three buttons to a toolbar, using the standard system bitmap for view buttons.</span></span> <span data-ttu-id="4c38f-119">Сообщение [**\_ Аддбитмап в ТБ**](tb-addbitmap.md) возвращает индекс первого изображения кнопки в списке изображений.</span><span class="sxs-lookup"><span data-stu-id="4c38f-119">The [**TB\_ADDBITMAP**](tb-addbitmap.md) message returns the index of the first button image within the image list.</span></span> <span data-ttu-id="4c38f-120">Отдельные образы определяются по смещению от этого значения.</span><span class="sxs-lookup"><span data-stu-id="4c38f-120">Individual images are identified by their offsets from that value.</span></span>


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a><span data-ttu-id="4c38f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4c38f-121">Requirements</span></span>



| <span data-ttu-id="4c38f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4c38f-122">Requirement</span></span> | <span data-ttu-id="4c38f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4c38f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c38f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c38f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4c38f-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c38f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c38f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c38f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4c38f-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c38f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c38f-128">Header</span><span class="sxs-lookup"><span data-stu-id="4c38f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c38f-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c38f-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4c38f-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4c38f-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4c38f-131">**ТБ \_ АДДБУТТОНСВ** (Юникод) и **ТБ \_ аддбуттонса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4c38f-131">**TB\_ADDBUTTONSW** (Unicode) and **TB\_ADDBUTTONSA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4c38f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c38f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c38f-133">**Значения индекса изображения стандартной кнопки панели инструментов**</span><span class="sxs-lookup"><span data-stu-id="4c38f-133">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

