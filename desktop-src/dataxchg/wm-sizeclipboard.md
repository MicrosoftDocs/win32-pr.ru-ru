---
title: Сообщение WM_SIZECLIPBOARD (Winuser. h)
description: Посылается в буфер обмена владельцем окном средства просмотра буфера обмена, когда буфер обмена содержит данные в \_ формате CF овнердисплай, а размер клиентской области средства просмотра буфера обмена изменился.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- Обмен данными с сообщениями WM_SIZECLIPBOARD
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802548"
---
# <a name="wm_sizeclipboard-message"></a><span data-ttu-id="b769d-104">\_Сообщение СИЗЕКЛИПБОАРД WM</span><span class="sxs-lookup"><span data-stu-id="b769d-104">WM\_SIZECLIPBOARD message</span></span>

<span data-ttu-id="b769d-105">Посылается в буфер обмена владельцем окном средства просмотра буфера обмена, когда буфер обмена содержит данные в формате [**CF \_ овнердисплай**](standard-clipboard-formats.md) , а размер клиентской области средства просмотра буфера обмена изменился.</span><span class="sxs-lookup"><span data-stu-id="b769d-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area has changed size.</span></span>


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a><span data-ttu-id="b769d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b769d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b769d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b769d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b769d-108">Маркер окна средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="b769d-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="b769d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b769d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b769d-110">Маркер объекта глобальной памяти, который содержит структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b769d-110">A handle to a global memory object that contains a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="b769d-111">Структура указывает новые размеры клиентской области средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="b769d-111">The structure specifies the new dimensions of the clipboard viewer's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b769d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b769d-112">Return value</span></span>

<span data-ttu-id="b769d-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="b769d-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b769d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b769d-114">Remarks</span></span>

<span data-ttu-id="b769d-115">Когда окно средства просмотра буфера обмена собирается к уничтожению или изменению размера, сообщение **WM \_ сизеклипбоард** отправляется с пустым прямоугольником (0, 0, 0, 0) в качестве нового размера.</span><span class="sxs-lookup"><span data-stu-id="b769d-115">When the clipboard viewer window is about to be destroyed or resized, a **WM\_SIZECLIPBOARD** message is sent with a null rectangle (0, 0, 0, 0) as the new size.</span></span> <span data-ttu-id="b769d-116">Это позволяет владельцу буфера обмена освобождать ресурсы, отображаемые на экране.</span><span class="sxs-lookup"><span data-stu-id="b769d-116">This permits the clipboard owner to free its display resources.</span></span>

<span data-ttu-id="b769d-117">Владелец буфера обмена должен использовать функцию [**глобаллокк**](/windows/desktop/api/winbase/nf-winbase-globallock) для блокировки объекта памяти, содержащего [**Rect**](/previous-versions//dd162897(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b769d-117">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory object that contains [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span> <span data-ttu-id="b769d-118">Перед возвращением владелец буфера обмена должен разблокировать объект с помощью функции [**глобалунлокк**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="b769d-118">Before returning, the clipboard owner must unlock the object by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b769d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b769d-119">Requirements</span></span>



| <span data-ttu-id="b769d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b769d-120">Requirement</span></span> | <span data-ttu-id="b769d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b769d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b769d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b769d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b769d-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b769d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b769d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b769d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b769d-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b769d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b769d-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b769d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b769d-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b769d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b769d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b769d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b769d-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b769d-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b769d-130">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="b769d-130">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

