---
description: '\_Событие устройства ДБТ пользователяопределенные определяет определяемое пользователем событие.'
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Событие DBT_USERDEFINED (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072447"
---
# <a name="dbt_userdefined-event"></a><span data-ttu-id="f3639-103">\_Событие ДБТ пользователяопределенные</span><span class="sxs-lookup"><span data-stu-id="f3639-103">DBT\_USERDEFINED event</span></span>

<span data-ttu-id="f3639-104">\_Событие устройства ДБТ пользователяопределенные определяет определяемое пользователем событие.</span><span class="sxs-lookup"><span data-stu-id="f3639-104">The DBT\_USERDEFINED device event identifies a user-defined event.</span></span>

<span data-ttu-id="f3639-105">Для вещания этого события устройства вызовите функцию [**броадкастсистеммессаже**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) с сообщением [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="f3639-105">To broadcast this device event, call the [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) function with the [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="f3639-106">Присвойте параметру *wParam* значение ДБТ \_ Пользователяопределенные и задайте *lParam* , как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="f3639-106">Set *wParam* to DBT\_USERDEFINED and set *lParam* as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="f3639-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3639-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3639-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f3639-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f3639-109">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="f3639-109">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="f3639-110">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="f3639-110">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f3639-111">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="f3639-111">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f3639-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3639-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3639-113">Задайте для параметра значение ДБТ \_ пользователяопределенные.</span><span class="sxs-lookup"><span data-stu-id="f3639-113">Set to DBT\_USERDEFINED.</span></span>

</dd> <dt>

<span data-ttu-id="f3639-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3639-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3639-115">Указатель на структуру [**\_ \_ \_ пользователяопределенные для разработки**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) , которая описывает выполняемую пользователем трансляцию.</span><span class="sxs-lookup"><span data-stu-id="f3639-115">A pointer to a [**\_DEV\_BROADCAST\_USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) structure which describes the user-defined broadcast in progress.</span></span> <span data-ttu-id="f3639-116">Член **дбуд \_ szName** содержит имя определяемого пользователем сообщения, за которым следуют все определяемые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="f3639-116">The **dbud\_szName** member contains the name of the user-defined message, followed by any user-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3639-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3639-117">Return value</span></span>

<span data-ttu-id="f3639-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f3639-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3639-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f3639-119">Requirements</span></span>



| <span data-ttu-id="f3639-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f3639-120">Requirement</span></span> | <span data-ttu-id="f3639-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f3639-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3639-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3639-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3639-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3639-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="f3639-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3639-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3639-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3639-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f3639-126">Header</span><span class="sxs-lookup"><span data-stu-id="f3639-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3639-127"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3639-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3639-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3639-129">События устройства</span><span class="sxs-lookup"><span data-stu-id="f3639-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="f3639-130">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="f3639-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="f3639-131">**\_\_пользователяопределенныеная рассылка dev \_**</span><span class="sxs-lookup"><span data-stu-id="f3639-131">**\_DEV\_BROADCAST\_USERDEFINED**</span></span>](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[<span data-ttu-id="f3639-132">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="f3639-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> <dt>

[<span data-ttu-id="f3639-133">**броадкастсистеммессаже**</span><span class="sxs-lookup"><span data-stu-id="f3639-133">**BroadcastSystemMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

