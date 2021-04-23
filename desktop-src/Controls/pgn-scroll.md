---
title: Код уведомления PGN_SCROLL (Коммктрл. h)
description: Сообщает родительскому окну элемента управления страничного навигатора о том, что автономное окно будет прокручиваться. Это уведомление отправляется в виде \_ сообщения WM notify.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135706"
---
# <a name="pgn_scroll-notification-code"></a><span data-ttu-id="2f788-105">\_Код уведомления прокрутки ПГН</span><span class="sxs-lookup"><span data-stu-id="2f788-105">PGN\_SCROLL notification code</span></span>

<span data-ttu-id="2f788-106">Сообщает родительскому окну элемента управления страничного навигатора о том, что автономное окно будет прокручиваться.</span><span class="sxs-lookup"><span data-stu-id="2f788-106">Notifies a pager control's parent window that the contained window is about to be scrolled.</span></span> <span data-ttu-id="2f788-107">Это уведомление отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2f788-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2f788-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f788-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f788-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f788-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f788-110">Указатель на структуру [**нмпгскролл**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) , которая содержит и получает сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="2f788-110">Pointer to an [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="2f788-111">Элемент **идир** этой структуры указывает направление прокрутки.</span><span class="sxs-lookup"><span data-stu-id="2f788-111">The **iDir** member of this structure indicates the direction of the scroll.</span></span> <span data-ttu-id="2f788-112">Элементы **Икспос** и **ийпос** содержат горизонтальное и вертикальное расположение вложенного окна до прокрутки.</span><span class="sxs-lookup"><span data-stu-id="2f788-112">The **iXpos** and **iYpos** members contain the horizontal and vertical position of the contained window prior to the scroll.</span></span> <span data-ttu-id="2f788-113">Элемент **искролл** содержит разностную сумму прокрутки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f788-113">The **iScroll** member contains the default scroll delta amount.</span></span> <span data-ttu-id="2f788-114">При необходимости можно изменить этот элемент на другую величину прокрутки.</span><span class="sxs-lookup"><span data-stu-id="2f788-114">You can modify this member to a different scroll amount if desired.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f788-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f788-115">Return value</span></span>

<span data-ttu-id="2f788-116">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2f788-116">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f788-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2f788-117">Requirements</span></span>



| <span data-ttu-id="2f788-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2f788-118">Requirement</span></span> | <span data-ttu-id="2f788-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2f788-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f788-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f788-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f788-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f788-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f788-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f788-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f788-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f788-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f788-124">Header</span><span class="sxs-lookup"><span data-stu-id="2f788-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f788-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f788-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





