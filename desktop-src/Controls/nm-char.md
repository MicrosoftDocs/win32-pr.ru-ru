---
title: Код уведомления NM_CHAR (Коммктрл. h)
description: '\_Код уведомления NM char отправляется элементом управления при обработке клавиши знака. Этот код уведомления отправляется в виде \_ сообщения WM notify.'
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654726"
---
# <a name="nm_char-notification-code"></a><span data-ttu-id="8db6e-105">\_Код уведомления "NM char"</span><span class="sxs-lookup"><span data-stu-id="8db6e-105">NM\_CHAR notification code</span></span>

<span data-ttu-id="8db6e-106">\_Код уведомления NM char отправляется элементом управления при обработке клавиши знака.</span><span class="sxs-lookup"><span data-stu-id="8db6e-106">The NM\_CHAR notification code is sent by a control when a character key is processed.</span></span> <span data-ttu-id="8db6e-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8db6e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8db6e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8db6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8db6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8db6e-110">Указатель на структуру [**нмчар**](/windows/win32/api/commctrl/ns-commctrl-nmchar) , которая содержит дополнительные сведения о символе, вызвавшем код уведомления.</span><span class="sxs-lookup"><span data-stu-id="8db6e-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db6e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8db6e-111">Return value</span></span>

<span data-ttu-id="8db6e-112">Возвращаемое значение игнорируется большинством элементов управления.</span><span class="sxs-lookup"><span data-stu-id="8db6e-112">The return value is ignored by most controls.</span></span> <span data-ttu-id="8db6e-113">Дополнительные сведения см. в документации по отдельным элементам управления.</span><span class="sxs-lookup"><span data-stu-id="8db6e-113">For more information, see the documentation for the individual controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db6e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8db6e-114">Requirements</span></span>



| <span data-ttu-id="8db6e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8db6e-115">Requirement</span></span> | <span data-ttu-id="8db6e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8db6e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8db6e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8db6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8db6e-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8db6e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8db6e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8db6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8db6e-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8db6e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8db6e-121">Header</span><span class="sxs-lookup"><span data-stu-id="8db6e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8db6e-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db6e-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db6e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8db6e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db6e-124">NM \_ char (панель инструментов)</span><span class="sxs-lookup"><span data-stu-id="8db6e-124">NM\_CHAR (toolbar)</span></span>](nm-char-toolbar.md)
</dt> </dl>

 

 





