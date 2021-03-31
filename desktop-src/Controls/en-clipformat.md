---
title: Код уведомления EN_CLIPFORMAT (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что вставка выполнялась с определенным форматом буфера обмена. Безоконный элемент управления "поле ввода" отправляет это уведомление с помощью метода Ткснотифи Итекссост.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988481"
---
# <a name="en_clipformat-notification-code"></a><span data-ttu-id="9ec21-105">\_Код уведомления EN клипформат</span><span class="sxs-lookup"><span data-stu-id="9ec21-105">EN\_CLIPFORMAT notification code</span></span>

<span data-ttu-id="9ec21-106">Сообщает родительскому окну элемента управления Rich Edit, что вставка выполнялась с определенным форматом буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="9ec21-106">Notifies a rich edit control's parent window that a paste occurred with a particular clipboard format.</span></span> <span data-ttu-id="9ec21-107">Безоконный элемент управления "поле ввода" не отправляет это уведомление с помощью метода [**итекссост:: ткснотифи**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="9ec21-107">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span>


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9ec21-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ec21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ec21-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ec21-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ec21-110">ИДЕНТИФИКАТОР окна, полученный путем вызова функции [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) со \_ значением идентификатора ГВЛ.</span><span class="sxs-lookup"><span data-stu-id="9ec21-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="9ec21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ec21-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ec21-112">Указатель на структуру [**клипбоардформат**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) , содержащую сведения о формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="9ec21-112">A pointer to a [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) structure that contains information about the clipboard format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ec21-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ec21-113">Return value</span></span>

<span data-ttu-id="9ec21-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9ec21-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ec21-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ec21-115">Remarks</span></span>

<span data-ttu-id="9ec21-116">Чтобы получить \_ коды уведомлений EN клипформат, укажите [**енм \_ клипформат**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="9ec21-116">To receive EN\_CLIPFORMAT notification codes, specify [**ENM\_CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec21-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9ec21-117">Requirements</span></span>



| <span data-ttu-id="9ec21-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9ec21-118">Requirement</span></span> | <span data-ttu-id="9ec21-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9ec21-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec21-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ec21-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec21-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9ec21-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9ec21-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ec21-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec21-123">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9ec21-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ec21-124">Header</span><span class="sxs-lookup"><span data-stu-id="9ec21-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ec21-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ec21-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec21-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ec21-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec21-127">**клипбоардформат**</span><span class="sxs-lookup"><span data-stu-id="9ec21-127">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

