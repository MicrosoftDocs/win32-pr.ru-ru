---
title: Код уведомления RBN_CHEVRONPUSHED (Коммктрл. h)
description: Посылается элементом управления "Главная панель" при нажатии шеврона. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071604"
---
# <a name="rbn_chevronpushed-notification-code"></a><span data-ttu-id="e9fe5-105">\_Код уведомления РБН чевронпушед</span><span class="sxs-lookup"><span data-stu-id="e9fe5-105">RBN\_CHEVRONPUSHED notification code</span></span>

<span data-ttu-id="e9fe5-106">Посылается элементом управления "Главная панель" при нажатии шеврона.</span><span class="sxs-lookup"><span data-stu-id="e9fe5-106">Sent by a rebar control when a chevron is pushed.</span></span> <span data-ttu-id="e9fe5-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e9fe5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e9fe5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9fe5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9fe5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9fe5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9fe5-110">Указатель на структуру [**нмребарчеврон**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) полосы.</span><span class="sxs-lookup"><span data-stu-id="e9fe5-110">Pointer to the band's [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9fe5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9fe5-111">Return value</span></span>

<span data-ttu-id="e9fe5-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="e9fe5-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9fe5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9fe5-113">Remarks</span></span>

<span data-ttu-id="e9fe5-114">Когда приложение получает этот код уведомления, оно отвечает за отображение всплывающего меню с элементами для каждого скрытого инструмента.</span><span class="sxs-lookup"><span data-stu-id="e9fe5-114">When an application receives this notification code, it is responsible for displaying a popup menu with items for each hidden tool.</span></span> <span data-ttu-id="e9fe5-115">Используйте элемент **RC** структуры [**нмребарчеврон**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) , чтобы найти правильную точку для всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="e9fe5-115">Use the **rc** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure to find the correct position for the popup menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9fe5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e9fe5-116">Requirements</span></span>



| <span data-ttu-id="e9fe5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e9fe5-117">Requirement</span></span> | <span data-ttu-id="e9fe5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e9fe5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9fe5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9fe5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e9fe5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9fe5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9fe5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9fe5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e9fe5-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9fe5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9fe5-123">Header</span><span class="sxs-lookup"><span data-stu-id="e9fe5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9fe5-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9fe5-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





