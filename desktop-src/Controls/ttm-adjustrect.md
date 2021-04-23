---
title: Сообщение TTM_ADJUSTRECT (Коммктрл. h)
description: Вычисляет текстовый прямоугольник элемента управления ToolTip от прямоугольника окна или прямоугольника окна подсказки, необходимого для вывода указанного текстового прямоугольника.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- Элементы управления Windows для TTM_ADJUSTRECT сообщений
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988679"
---
# <a name="ttm_adjustrect-message"></a><span data-ttu-id="4aab0-104">\_Сообщение ТТМ аджустрект</span><span class="sxs-lookup"><span data-stu-id="4aab0-104">TTM\_ADJUSTRECT message</span></span>

<span data-ttu-id="4aab0-105">Вычисляет текстовый прямоугольник элемента управления ToolTip от прямоугольника окна или прямоугольника окна подсказки, необходимого для вывода указанного текстового прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4aab0-105">Calculates a tooltip control's text display rectangle from its window rectangle, or the tooltip window rectangle needed to display a specified text display rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="4aab0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4aab0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aab0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4aab0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aab0-108">Значение, указывающее выполняемую операцию.</span><span class="sxs-lookup"><span data-stu-id="4aab0-108">Value that specifies which operation to perform.</span></span> <span data-ttu-id="4aab0-109">Если **значение — true**, параметр *lParam* используется для указания прямоугольника текста и получает соответствующий прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="4aab0-109">If **TRUE**, *lParam* is used to specify a text-display rectangle and it receives the corresponding window rectangle.</span></span> <span data-ttu-id="4aab0-110">Если **значение равно false**, то параметр *lParam* используется для указания прямоугольника окна и получает соответствующий прямоугольник для вывода текста.</span><span class="sxs-lookup"><span data-stu-id="4aab0-110">If **FALSE**, *lParam* is used to specify a window rectangle and it receives the corresponding text display rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="4aab0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4aab0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aab0-112">Структура **Rect** для хранения окна всплывающей подсказки или прямоугольника для вывода текста.</span><span class="sxs-lookup"><span data-stu-id="4aab0-112">**RECT** structure to hold either a tooltip window rectangle or a text display rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aab0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4aab0-113">Return value</span></span>

<span data-ttu-id="4aab0-114">Функция возвращает ненулевое значение, если прямоугольник успешно скорректирован, и возвращает нуль при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="4aab0-114">Returns a nonzero value if the rectangle is successfully adjusted, and returns zero if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aab0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aab0-115">Remarks</span></span>

<span data-ttu-id="4aab0-116">Это сообщение особенно полезно, если необходимо использовать элемент управления ToolTip для вывода полного текста строки, которая обычно усекается.</span><span class="sxs-lookup"><span data-stu-id="4aab0-116">This message is particularly useful when you want to use a tooltip control to display the full text of a string that is usually truncated.</span></span> <span data-ttu-id="4aab0-117">Он обычно используется с элементами управления ListView и TreeView.</span><span class="sxs-lookup"><span data-stu-id="4aab0-117">It is commonly used with listview and treeview controls.</span></span> <span data-ttu-id="4aab0-118">Обычно это сообщение отправляется в ответ на [ТТН \_ Отображение](ttn-show.md) кода уведомления, чтобы можно было правильно разместить элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="4aab0-118">You typically send this message in response to a [TTN\_SHOW](ttn-show.md) notification code so that you can position the tooltip control properly.</span></span>

<span data-ttu-id="4aab0-119">Прямоугольник окна подсказки немного больше, чем прямоугольник, в котором отображается текст подсказки.</span><span class="sxs-lookup"><span data-stu-id="4aab0-119">The tooltip window rectangle is somewhat larger than the text display rectangle that bounds the tooltip string.</span></span> <span data-ttu-id="4aab0-120">Начало координат окна также смещается вверх и влево от источника отображаемого прямоугольника текста.</span><span class="sxs-lookup"><span data-stu-id="4aab0-120">The window origin is also offset up and to the left from the origin of the text display rectangle.</span></span> <span data-ttu-id="4aab0-121">Чтобы разместить прямоугольник текста, необходимо вычислить соответствующий прямоугольник окна и использовать этот прямоугольник для размещения подсказки.</span><span class="sxs-lookup"><span data-stu-id="4aab0-121">To position the text display rectangle, you must calculate the corresponding window rectangle and use that rectangle to position the tooltip.</span></span> <span data-ttu-id="4aab0-122">**ТТМ \_ АДЖУСТРЕКТ** обрабатывает это вычисление.</span><span class="sxs-lookup"><span data-stu-id="4aab0-122">**TTM\_ADJUSTRECT** handles this calculation for you.</span></span>

<span data-ttu-id="4aab0-123">Если для параметра *wParam* задано **значение true**, то **ТТМ \_ аджустрект** принимает размер и расположение требуемого текста всплывающей подсказки и передает обратно размер и расположение окна подсказки, необходимого для вывода текста в указанном положении.</span><span class="sxs-lookup"><span data-stu-id="4aab0-123">If you set *wParam* to **TRUE**, **TTM\_ADJUSTRECT** takes the size and position of the desired tooltip text display rectangle, and passes back the size and position of the tooltip window needed to display the text in the specified position.</span></span> <span data-ttu-id="4aab0-124">Если для параметра *wParam* задано значение **false**, можно указать прямоугольник окна подсказки, а **ТТМ \_ аджустрект** будет возвращать размер и расположение текстового прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4aab0-124">If you set *wParam* to **FALSE**, you can specify a tooltip window rectangle and **TTM\_ADJUSTRECT** will return the size and position of its text rectangle.</span></span>

<span data-ttu-id="4aab0-125">В следующем фрагменте кода показано использование сообщения **ТТМ \_ аджустрект** для размещения элемента управления ToolTip для вывода полного текста строки элемента управления вместо усеченной строки.</span><span class="sxs-lookup"><span data-stu-id="4aab0-125">The following code fragment illustrates the use of the **TTM\_ADJUSTRECT** message to position a tooltip control to display the full text of a control's string in place of a truncated string.</span></span> <span data-ttu-id="4aab0-126">Определяемая приложением функция **жетмитемрект** Возвращает текстовый прямоугольник, который потребуется для вывода текста подсказки непосредственно над усеченной строкой.</span><span class="sxs-lookup"><span data-stu-id="4aab0-126">The application-defined **GetMyItemRect** function returns the text rectangle that will be needed to display the tooltip text directly over the truncated string.</span></span> <span data-ttu-id="4aab0-127">Сведения о реализации этой функции будут зависеть от конкретного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4aab0-127">The details of how this function is implemented will depend on the particular control.</span></span> <span data-ttu-id="4aab0-128">**ТТМ \_ АДЖУСТРЕКТ** используется для отправки этого текстового прямоугольника в элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="4aab0-128">**TTM\_ADJUSTRECT** is used to send this text rectangle to the tooltip control.</span></span> <span data-ttu-id="4aab0-129">Он возвращает прямоугольник соответствующего размера и позиционирования окна, который затем используется для позиционирования окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="4aab0-129">It returns an appropriately sized and positioned window rectangle that is then used to position the tooltip window.</span></span>


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a><span data-ttu-id="4aab0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="4aab0-130">Requirements</span></span>



| <span data-ttu-id="4aab0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4aab0-131">Requirement</span></span> | <span data-ttu-id="4aab0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4aab0-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4aab0-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4aab0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4aab0-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4aab0-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4aab0-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4aab0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4aab0-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4aab0-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4aab0-137">Header</span><span class="sxs-lookup"><span data-stu-id="4aab0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aab0-138"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aab0-138"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





