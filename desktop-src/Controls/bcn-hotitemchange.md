---
title: Код уведомления BCN_HOTITEMCHANGE (Коммктрл. h)
description: Уведомляет владельца элемента управления "Кнопка", что указатель мыши вводит или выходит за пределы клиентской области элемента управления "Кнопка". Элемент управления "Кнопка" отправляет этот код уведомления в виде сообщения WM \_ Notify.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071464"
---
# <a name="bcn_hotitemchange-notification-code"></a><span data-ttu-id="85d28-105">\_Код уведомления ХОТИТЕМЧАНЖЕ BCN</span><span class="sxs-lookup"><span data-stu-id="85d28-105">BCN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="85d28-106">Уведомляет владельца элемента управления "Кнопка", что указатель мыши вводит или выходит за пределы клиентской области элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="85d28-106">Notifies the button control owner that the mouse is entering or leaving the client area of the button control.</span></span> <span data-ttu-id="85d28-107">Элемент управления "Кнопка" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="85d28-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="85d28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85d28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85d28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85d28-110">Указатель на структуру [**нмбчотитем**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .</span><span class="sxs-lookup"><span data-stu-id="85d28-110">A pointer to a [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d28-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85d28-111">Return value</span></span>

<span data-ttu-id="85d28-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="85d28-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d28-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85d28-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="85d28-114">Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="85d28-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="85d28-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="85d28-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85d28-116">Требования</span><span class="sxs-lookup"><span data-stu-id="85d28-116">Requirements</span></span>



| <span data-ttu-id="85d28-117">Требование</span><span class="sxs-lookup"><span data-stu-id="85d28-117">Requirement</span></span> | <span data-ttu-id="85d28-118">Значение</span><span class="sxs-lookup"><span data-stu-id="85d28-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85d28-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85d28-119">Minimum supported client</span></span><br/> | <span data-ttu-id="85d28-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85d28-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85d28-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85d28-121">Minimum supported server</span></span><br/> | <span data-ttu-id="85d28-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85d28-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85d28-123">Header</span><span class="sxs-lookup"><span data-stu-id="85d28-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="85d28-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="85d28-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





