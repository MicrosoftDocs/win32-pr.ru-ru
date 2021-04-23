---
title: Код уведомления NM_NCHITTEST (Главная панель) (Коммктрл. h)
description: Посылается элементом управления "Главная панель", когда элемент управления получает \_ сообщение WM нчиттест. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Элементы управления Windows для кода уведомления NM_NCHITTEST (Главная панель)
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
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136843"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="1add8-105">\_Код уведомления "NM нчиттест" (Главная панель)</span><span class="sxs-lookup"><span data-stu-id="1add8-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="1add8-106">Посылается элементом управления "Главная панель", когда элемент управления получает сообщение [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="1add8-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="1add8-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1add8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1add8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1add8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1add8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1add8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1add8-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="1add8-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="1add8-111">Элемент **двитемспек** содержит индекс диапазона, по которому произошло тестовое сообщение о нажатии, а элемент **PT** содержит координаты указателя мыши для тестового сообщения о нажатии.</span><span class="sxs-lookup"><span data-stu-id="1add8-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1add8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1add8-112">Return value</span></span>

<span data-ttu-id="1add8-113">Возвращает ноль, чтобы разрешить главной панели выполнять обработку сообщения проверки попадания по умолчанию или возвращать одно из значений НТ, \* задокументированных в [**\_ нчиттест WM**](/windows/desktop/inputdev/wm-nchittest) , для переопределения обработки проверки нажатия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1add8-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1add8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1add8-114">Requirements</span></span>



| <span data-ttu-id="1add8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1add8-115">Requirement</span></span> | <span data-ttu-id="1add8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1add8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1add8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1add8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1add8-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1add8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1add8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1add8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1add8-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1add8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1add8-121">Header</span><span class="sxs-lookup"><span data-stu-id="1add8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1add8-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1add8-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

