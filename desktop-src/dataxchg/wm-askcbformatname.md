---
title: Сообщение WM_ASKCBFORMATNAME (Winuser. h)
description: Отправляется в окно просмотра владельцу буфера обмена для запроса имени \_ формата буфера обмена CF овнердисплай.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- Обмен данными с сообщениями WM_ASKCBFORMATNAME
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135486"
---
# <a name="wm_askcbformatname-message"></a><span data-ttu-id="725b4-104">\_Сообщение АСККБФОРМАТНАМЕ WM</span><span class="sxs-lookup"><span data-stu-id="725b4-104">WM\_ASKCBFORMATNAME message</span></span>

<span data-ttu-id="725b4-105">Отправляется в окно просмотра владельцу буфера обмена для запроса имени формата буфера обмена [**CF \_ овнердисплай**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="725b4-105">Sent to the clipboard owner by a clipboard viewer window to request the name of a [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) clipboard format.</span></span>

<span data-ttu-id="725b4-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="725b4-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a><span data-ttu-id="725b4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="725b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="725b4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="725b4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="725b4-109">Размер (в символах) буфера, на который указывает параметр *lParam* .</span><span class="sxs-lookup"><span data-stu-id="725b4-109">The size, in characters, of the buffer pointed to by the *lParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="725b4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="725b4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="725b4-111">Указатель на буфер, который должен получить имя формата буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="725b4-111">A pointer to the buffer that is to receive the clipboard format name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="725b4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="725b4-112">Return value</span></span>

<span data-ttu-id="725b4-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="725b4-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="725b4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="725b4-114">Remarks</span></span>

<span data-ttu-id="725b4-115">В ответ на это сообщение владелец буфера обмена должен скопировать имя формата, отображаемого владельцем, в указанный буфер, не превышающий размер буфера, указанный параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="725b4-115">In response to this message, the clipboard owner should copy the name of the owner-display format to the specified buffer, not exceeding the buffer size specified by the *wParam* parameter.</span></span>

<span data-ttu-id="725b4-116">Окно просмотра буфера обмена отправляет это сообщение владельцу буфера обмена, чтобы определить имя формата [**CF \_ овнердисплай**](standard-clipboard-formats.md) , например, чтобы инициализировать список доступных форматов.</span><span class="sxs-lookup"><span data-stu-id="725b4-116">A clipboard viewer window sends this message to the clipboard owner to determine the name of the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format   for example, to initialize a menu listing available formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="725b4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="725b4-117">Requirements</span></span>



| <span data-ttu-id="725b4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="725b4-118">Requirement</span></span> | <span data-ttu-id="725b4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="725b4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="725b4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="725b4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="725b4-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="725b4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="725b4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="725b4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="725b4-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="725b4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="725b4-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="725b4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="725b4-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="725b4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725b4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="725b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725b4-127">Общие сведения о буфере обмена</span><span class="sxs-lookup"><span data-stu-id="725b4-127">Clipboard Overview</span></span>](clipboard.md)
</dt> </dl>

 

