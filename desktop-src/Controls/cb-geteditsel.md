---
title: Сообщение CB_GETEDITSEL (Winuser. h)
description: Возвращает начальные и конечные позиции символов текущего выделения в элементе управления "поле ввода" поля со списком.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- Элементы управления Windows для CB_GETEDITSEL сообщений
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071621"
---
# <a name="cb_geteditsel-message"></a><span data-ttu-id="6dc82-104">\_Сообщение ЖЕТЕДИТСЕЛ CB</span><span class="sxs-lookup"><span data-stu-id="6dc82-104">CB\_GETEDITSEL message</span></span>

<span data-ttu-id="6dc82-105">Возвращает начальные и конечные позиции символов текущего выделения в элементе управления "поле ввода" поля со списком.</span><span class="sxs-lookup"><span data-stu-id="6dc82-105">Gets the starting and ending character positions of the current selection in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6dc82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6dc82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dc82-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6dc82-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dc82-108">Указатель на значение **DWORD** , получающее начальную точку выделения.</span><span class="sxs-lookup"><span data-stu-id="6dc82-108">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="6dc82-109">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6dc82-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6dc82-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6dc82-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dc82-111">Указатель на значение **DWORD** , которое получает конечную точку выделения.</span><span class="sxs-lookup"><span data-stu-id="6dc82-111">A pointer to a **DWORD** value that receives the ending position of the selection.</span></span> <span data-ttu-id="6dc82-112">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6dc82-112">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dc82-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6dc82-113">Return value</span></span>

<span data-ttu-id="6dc82-114">Возвращаемое значение — это отсчитываемое от нуля значение **типа DWORD** с начальной позицией выбора в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) и с конечной позицией первого символа после последнего выбранного символа в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6dc82-114">The return value is a zero-based **DWORD** value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and with the ending position of the first character after the last selected character in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="6dc82-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="6dc82-115">Examples</span></span>

<span data-ttu-id="6dc82-116">В следующем примере кода показаны два способа получения текущего диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="6dc82-116">The following code example shows two ways of retrieving the current selection range.</span></span>


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a><span data-ttu-id="6dc82-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6dc82-117">Requirements</span></span>



| <span data-ttu-id="6dc82-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6dc82-118">Requirement</span></span> | <span data-ttu-id="6dc82-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6dc82-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc82-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6dc82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc82-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6dc82-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6dc82-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6dc82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc82-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6dc82-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6dc82-124">Header</span><span class="sxs-lookup"><span data-stu-id="6dc82-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dc82-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dc82-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dc82-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6dc82-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6dc82-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6dc82-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6dc82-128">**\_СЕТЕДИТСЕЛ CB**</span><span class="sxs-lookup"><span data-stu-id="6dc82-128">**CB\_SETEDITSEL**</span></span>](cb-seteditsel.md)
</dt> <dt>

<span data-ttu-id="6dc82-129">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="6dc82-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6dc82-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6dc82-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6dc82-131">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6dc82-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

