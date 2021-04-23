---
title: Сообщение WM_CTLCOLORLISTBOX (Winuser. h)
description: Отправляется в родительское окно списка до того, как система выводит список. Выполнив ответ на это сообщение, родительское окно может задать цвета текста и фона списка с помощью указанного маркера контекста устройства вывода.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- Элементы управления Windows для WM_CTLCOLORLISTBOX сообщений
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135782"
---
# <a name="wm_ctlcolorlistbox-message"></a><span data-ttu-id="42f86-105">\_Сообщение КТЛКОЛОРЛИСТБОКС WM</span><span class="sxs-lookup"><span data-stu-id="42f86-105">WM\_CTLCOLORLISTBOX message</span></span>

<span data-ttu-id="42f86-106">Отправляется в родительское окно списка до того, как система выводит список.</span><span class="sxs-lookup"><span data-stu-id="42f86-106">Sent to the parent window of a list box before the system draws the list box.</span></span> <span data-ttu-id="42f86-107">Выполнив ответ на это сообщение, родительское окно может задать цвета текста и фона списка с помощью указанного маркера контекста устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="42f86-107">By responding to this message, the parent window can set the text and background colors of the list box by using the specified display device context handle.</span></span>


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="42f86-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="42f86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f86-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42f86-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42f86-110">Обрабатывайте контекст устройства для списка.</span><span class="sxs-lookup"><span data-stu-id="42f86-110">Handle to the device context for the list box.</span></span>

</dd> <dt>

<span data-ttu-id="42f86-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42f86-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42f86-112">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="42f86-112">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f86-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42f86-113">Return value</span></span>

<span data-ttu-id="42f86-114">Если приложение обрабатывает это сообщение, оно должно возвращать маркер кисти.</span><span class="sxs-lookup"><span data-stu-id="42f86-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="42f86-115">Система использует кисть для рисования фона списка.</span><span class="sxs-lookup"><span data-stu-id="42f86-115">The system uses the brush to paint the background of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="42f86-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42f86-116">Remarks</span></span>

<span data-ttu-id="42f86-117">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для списка.</span><span class="sxs-lookup"><span data-stu-id="42f86-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the list box.</span></span>

<span data-ttu-id="42f86-118">Сообщение **WM \_ ктлколорлистбокс** никогда не передается между потоками.</span><span class="sxs-lookup"><span data-stu-id="42f86-118">The **WM\_CTLCOLORLISTBOX** message is never sent between threads.</span></span> <span data-ttu-id="42f86-119">Он отправляется только в пределах одного потока.</span><span class="sxs-lookup"><span data-stu-id="42f86-119">It is sent only within one thread.</span></span>

<span data-ttu-id="42f86-120">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу **int \_ ptr** и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="42f86-120">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="42f86-121">Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42f86-121">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="42f86-122">Значение **\_ мсгресулт DWL** , заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="42f86-122">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f86-123">Требования</span><span class="sxs-lookup"><span data-stu-id="42f86-123">Requirements</span></span>



| <span data-ttu-id="42f86-124">Требование</span><span class="sxs-lookup"><span data-stu-id="42f86-124">Requirement</span></span> | <span data-ttu-id="42f86-125">Значение</span><span class="sxs-lookup"><span data-stu-id="42f86-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f86-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42f86-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42f86-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42f86-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42f86-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42f86-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42f86-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42f86-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42f86-130">Header</span><span class="sxs-lookup"><span data-stu-id="42f86-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f86-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42f86-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f86-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42f86-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="42f86-133">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="42f86-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="42f86-134">**реализепалетте**</span><span class="sxs-lookup"><span data-stu-id="42f86-134">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="42f86-135">**селектпалетте**</span><span class="sxs-lookup"><span data-stu-id="42f86-135">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="42f86-136">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="42f86-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

