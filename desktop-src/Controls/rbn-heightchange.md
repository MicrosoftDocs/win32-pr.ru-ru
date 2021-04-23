---
title: Код уведомления RBN_HEIGHTCHANGE (Коммктрл. h)
description: Посылается элементом управления главной панели при изменении его высоты. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988593"
---
# <a name="rbn_heightchange-notification-code"></a><span data-ttu-id="20ab0-105">\_Код уведомления РБН хеигхтчанже</span><span class="sxs-lookup"><span data-stu-id="20ab0-105">RBN\_HEIGHTCHANGE notification code</span></span>

<span data-ttu-id="20ab0-106">Посылается элементом управления главной панели при изменении его высоты.</span><span class="sxs-lookup"><span data-stu-id="20ab0-106">Sent by a rebar control when its height has changed.</span></span> <span data-ttu-id="20ab0-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="20ab0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="20ab0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="20ab0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ab0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20ab0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20ab0-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="20ab0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ab0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20ab0-111">Return value</span></span>

<span data-ttu-id="20ab0-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="20ab0-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="20ab0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20ab0-113">Remarks</span></span>

<span data-ttu-id="20ab0-114">Элементы управления главной панели, использующие стиль по [**\_ вертикали**](common-control-styles.md) , отправляют этот код уведомления при изменении их ширины.</span><span class="sxs-lookup"><span data-stu-id="20ab0-114">Rebar controls that use the [**CCS\_VERT**](common-control-styles.md) style send this notification code when their width changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ab0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="20ab0-115">Requirements</span></span>



| <span data-ttu-id="20ab0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="20ab0-116">Requirement</span></span> | <span data-ttu-id="20ab0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="20ab0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20ab0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20ab0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20ab0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20ab0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20ab0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20ab0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20ab0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20ab0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20ab0-122">Header</span><span class="sxs-lookup"><span data-stu-id="20ab0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20ab0-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ab0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





