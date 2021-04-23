---
title: Код уведомления NM_NCHITTEST (Коммктрл. h)
description: Посылается элементом управления "Главная панель", когда элемент управления получает \_ сообщение WM нчиттест. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8af39fd792ecb9aeb463957f49f5722737e6ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654525"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="de273-105">\_Код уведомления нчиттест (NM)</span><span class="sxs-lookup"><span data-stu-id="de273-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="de273-106">Посылается элементом управления "Главная панель", когда элемент управления получает сообщение [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="de273-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="de273-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="de273-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="de273-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="de273-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de273-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de273-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de273-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="de273-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="de273-111">Элемент *PT* содержит координаты мыши для сообщения проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="de273-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de273-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de273-112">Return value</span></span>

<span data-ttu-id="de273-113">Если не указано иное, возвращайте нуль, чтобы разрешить элементу управления выполнять обработку сообщения проверки попадания по умолчанию, или вернуть одно из значений НТ, \* задокументированных в [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) , чтобы переопределить обработку проверки попадания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="de273-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="de273-114">Требования</span><span class="sxs-lookup"><span data-stu-id="de273-114">Requirements</span></span>



| <span data-ttu-id="de273-115">Требование</span><span class="sxs-lookup"><span data-stu-id="de273-115">Requirement</span></span> | <span data-ttu-id="de273-116">Значение</span><span class="sxs-lookup"><span data-stu-id="de273-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de273-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de273-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de273-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de273-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de273-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de273-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de273-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="de273-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de273-121">Header</span><span class="sxs-lookup"><span data-stu-id="de273-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de273-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="de273-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

