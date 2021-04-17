---
title: Сообщение WM_PAINTCLIPBOARD (Winuser. h)
description: Посылается владельцу буфера обмена в окне средства просмотра буфера обмена, если в буфере обмена содержатся данные в \_ формате CF овнердисплай, а клиентская область окна просмотра буфера обмена нуждается в перерисовки.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- Обмен данными с сообщениями WM_PAINTCLIPBOARD
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661873"
---
# <a name="wm_paintclipboard-message"></a><span data-ttu-id="f7e52-104">\_Сообщение ПАИНТКЛИПБОАРД WM</span><span class="sxs-lookup"><span data-stu-id="f7e52-104">WM\_PAINTCLIPBOARD message</span></span>

<span data-ttu-id="f7e52-105">Посылается владельцу буфера обмена в окне средства просмотра буфера обмена, если в буфере обмена содержатся данные в формате [**CF \_ овнердисплай**](standard-clipboard-formats.md) , а клиентская область окна просмотра буфера обмена нуждается в перерисовки.</span><span class="sxs-lookup"><span data-stu-id="f7e52-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area needs repainting.</span></span>


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a><span data-ttu-id="f7e52-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7e52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e52-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7e52-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7e52-108">Маркер окна средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="f7e52-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="f7e52-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7e52-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7e52-110">Маркер объекта глобальной памяти, который содержит структуру [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="f7e52-110">A handle to a global memory object that contains a [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="f7e52-111">Структура определяет часть клиентской области для рисования.</span><span class="sxs-lookup"><span data-stu-id="f7e52-111">The structure defines the part of the client area to paint.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7e52-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7e52-112">Return value</span></span>

<span data-ttu-id="f7e52-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="f7e52-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e52-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7e52-114">Remarks</span></span>

<span data-ttu-id="f7e52-115">Чтобы определить, требуется ли перерисовка всей клиентской области или только ее части, владелец буфера обмена должен сравнить размеры области рисования, заданной в элементе **члене rcpaint структуры** элемента [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) , с измерениями, заданными в последнем сообщении [**WM \_ сизеклипбоард**](wm-sizeclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="f7e52-115">To determine whether the entire client area or just a portion of it needs repainting, the clipboard owner must compare the dimensions of the drawing area given in the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) to the dimensions given in the most recent [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span>

<span data-ttu-id="f7e52-116">Владелец буфера обмена должен использовать функцию [**глобаллокк**](/windows/desktop/api/winbase/nf-winbase-globallock) для блокировки памяти, содержащей структуру [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="f7e52-116">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory that contains the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="f7e52-117">Перед возвращением владелец буфера обмена должен разблокировать эту память с помощью функции [**глобалунлокк**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="f7e52-117">Before returning, the clipboard owner must unlock that memory by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e52-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f7e52-118">Requirements</span></span>



| <span data-ttu-id="f7e52-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f7e52-119">Requirement</span></span> | <span data-ttu-id="f7e52-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f7e52-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e52-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7e52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e52-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f7e52-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f7e52-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7e52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e52-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f7e52-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7e52-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f7e52-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7e52-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7e52-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e52-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7e52-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7e52-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f7e52-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7e52-129">**WM \_ сизеклипбоард**</span><span class="sxs-lookup"><span data-stu-id="f7e52-129">**WM\_SIZECLIPBOARD**</span></span>](wm-sizeclipboard.md)
</dt> <dt>

<span data-ttu-id="f7e52-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f7e52-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f7e52-131">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="f7e52-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

