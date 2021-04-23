---
title: Сообщение LVN_ENDSCROLL (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", когда заканчивается операция прокрутки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- Элементы управления Windows для LVN_ENDSCROLL сообщений
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892830"
---
# <a name="lvn_endscroll-message"></a><span data-ttu-id="fb083-105">\_Сообщение ЛВН ендскролл</span><span class="sxs-lookup"><span data-stu-id="fb083-105">LVN\_ENDSCROLL message</span></span>

<span data-ttu-id="fb083-106">Сообщает родительскому окну элемента управления "представление списка", когда заканчивается операция прокрутки.</span><span class="sxs-lookup"><span data-stu-id="fb083-106">Notifies a list-view control's parent window when a scrolling operation ends.</span></span> <span data-ttu-id="fb083-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fb083-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fb083-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb083-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb083-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb083-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb083-110">Указатель на структуру [**нмлвскролл**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) , содержащую горизонтальную или вертикальную позицию, где заканчивается операция прокрутки.</span><span class="sxs-lookup"><span data-stu-id="fb083-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation ends.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb083-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb083-111">Return value</span></span>

<span data-ttu-id="fb083-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="fb083-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb083-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb083-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb083-114">Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="fb083-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="fb083-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fb083-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb083-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fb083-116">Requirements</span></span>



| <span data-ttu-id="fb083-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fb083-117">Requirement</span></span> | <span data-ttu-id="fb083-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fb083-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb083-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb083-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fb083-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb083-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb083-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb083-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fb083-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb083-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb083-123">Header</span><span class="sxs-lookup"><span data-stu-id="fb083-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb083-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb083-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





