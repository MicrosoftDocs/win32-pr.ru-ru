---
title: Код уведомления EN_OLEOPFAILED (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что при выполнении действия пользователя в объекте модели COM произошла ошибка. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892025"
---
# <a name="en_oleopfailed-notification-code"></a><span data-ttu-id="23c7d-105">\_Код уведомления EN олеопфаилед</span><span class="sxs-lookup"><span data-stu-id="23c7d-105">EN\_OLEOPFAILED notification code</span></span>

<span data-ttu-id="23c7d-106">Сообщает родительскому окну элемента управления Rich Edit, что при выполнении действия пользователя в объекте модели COM произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="23c7d-106">Notifies a rich edit control's parent window that a user action on a Component Object Model (COM) object has failed.</span></span> <span data-ttu-id="23c7d-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="23c7d-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="23c7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23c7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23c7d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23c7d-110">Структура [**енолеопфаилед**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) , содержащая сведения о сбое.</span><span class="sxs-lookup"><span data-stu-id="23c7d-110">An [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) structure that contains information about the failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23c7d-111">Return value</span></span>

<span data-ttu-id="23c7d-112">Этот код уведомления возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="23c7d-112">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c7d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23c7d-113">Remarks</span></span>

<span data-ttu-id="23c7d-114">Родительское окно всегда будет получать сообщение [**WM \_ Notify**](wm-notify.md) для этого события, оно не требует отправки маски уведомления с [**\_ SETEVENTMASK EM**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="23c7d-114">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23c7d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="23c7d-115">Requirements</span></span>



| <span data-ttu-id="23c7d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="23c7d-116">Requirement</span></span> | <span data-ttu-id="23c7d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="23c7d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23c7d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23c7d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23c7d-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23c7d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23c7d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23c7d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23c7d-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23c7d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23c7d-122">Header</span><span class="sxs-lookup"><span data-stu-id="23c7d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="23c7d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c7d-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c7d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23c7d-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="23c7d-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="23c7d-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="23c7d-126">**енолеопфаилед**</span><span class="sxs-lookup"><span data-stu-id="23c7d-126">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





