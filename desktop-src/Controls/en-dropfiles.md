---
title: Код уведомления EN_DROPFILES (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что пользователь пытается удалить файлы в элемент управления. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify при получении сообщения WM \_ дропфилес.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489285"
---
# <a name="en_dropfiles-notification-code"></a><span data-ttu-id="f538c-105">\_Код уведомления EN дропфилес</span><span class="sxs-lookup"><span data-stu-id="f538c-105">EN\_DROPFILES notification code</span></span>

<span data-ttu-id="f538c-106">Сообщает родительскому окну элемента управления Rich Edit, что пользователь пытается удалить файлы в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="f538c-106">Notifies a rich edit control parent window that the user is attempting to drop files into the control.</span></span> <span data-ttu-id="f538c-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) при получении сообщения [**WM \_ дропфилес**](/windows/desktop/shell/wm-dropfiles) .</span><span class="sxs-lookup"><span data-stu-id="f538c-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message when it receives the [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) message.</span></span>


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f538c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f538c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f538c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f538c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f538c-110">Структура [**ендропфилес**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) , которая получает сведения о пропущенных файлах.</span><span class="sxs-lookup"><span data-stu-id="f538c-110">An [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure that receives dropped files information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f538c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f538c-111">Return value</span></span>

<span data-ttu-id="f538c-112">Чтобы разрешить операцию Drop, возвращайте ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f538c-112">Return a nonzero value to allow the drop operation.</span></span>

<span data-ttu-id="f538c-113">Возвращает ноль, чтобы пропустить операцию Drop.</span><span class="sxs-lookup"><span data-stu-id="f538c-113">Return zero to ignore the drop operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f538c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f538c-114">Remarks</span></span>

<span data-ttu-id="f538c-115">Чтобы элемент управления "поле ввода" получал сообщения [**WM \_ дропфилес**](/windows/desktop/shell/wm-dropfiles) , родительское окно должно зарегистрировать элемент управления как цель перетаскивания с помощью функции [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) .</span><span class="sxs-lookup"><span data-stu-id="f538c-115">For a rich edit control to receive [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) messages, the parent window must register the control as a drop target by using the [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) function.</span></span> <span data-ttu-id="f538c-116">Элемент управления не регистрирует сам себя.</span><span class="sxs-lookup"><span data-stu-id="f538c-116">The control does not register itself.</span></span>

<span data-ttu-id="f538c-117">Чтобы получить \_ коды уведомлений EN дропфилес, укажите [**енм \_ дропфилес**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f538c-117">To receive EN\_DROPFILES notification codes, specify [**ENM\_DROPFILES**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f538c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f538c-118">Requirements</span></span>



| <span data-ttu-id="f538c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f538c-119">Requirement</span></span> | <span data-ttu-id="f538c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f538c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f538c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f538c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f538c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f538c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f538c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f538c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f538c-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f538c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f538c-125">Header</span><span class="sxs-lookup"><span data-stu-id="f538c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f538c-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f538c-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f538c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f538c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f538c-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f538c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f538c-129">**ендропфилес**</span><span class="sxs-lookup"><span data-stu-id="f538c-129">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

