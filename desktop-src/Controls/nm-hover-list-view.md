---
title: Код уведомления NM_HOVER (представление списка) (Коммктрл. h)
description: Посылается элементом управления "представление списка" при наведении указателя мыши на элемент. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- Элементы управления Windows для кода уведомления NM_HOVER (представление списка)
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891429"
---
# <a name="nm_hover-list-view-notification-code"></a><span data-ttu-id="7351d-105">\_Код уведомления для наведения в NM (представление списка)</span><span class="sxs-lookup"><span data-stu-id="7351d-105">NM\_HOVER (list view) notification code</span></span>

<span data-ttu-id="7351d-106">Посылается элементом управления "представление списка" при наведении указателя мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="7351d-106">Sent by a list-view control when the mouse hovers over an item.</span></span> <span data-ttu-id="7351d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7351d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7351d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7351d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7351d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7351d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7351d-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="7351d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7351d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7351d-111">Return value</span></span>

<span data-ttu-id="7351d-112">Возвращает ноль, чтобы позволить представлению списка обрабатывать указатель мыши в обычном режиме или ненулевой, чтобы предотвратить обработку наведения.</span><span class="sxs-lookup"><span data-stu-id="7351d-112">Return zero to allow the list view to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7351d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7351d-113">Requirements</span></span>



| <span data-ttu-id="7351d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7351d-114">Requirement</span></span> | <span data-ttu-id="7351d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7351d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7351d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7351d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7351d-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7351d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7351d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7351d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7351d-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7351d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7351d-120">Header</span><span class="sxs-lookup"><span data-stu-id="7351d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7351d-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7351d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





