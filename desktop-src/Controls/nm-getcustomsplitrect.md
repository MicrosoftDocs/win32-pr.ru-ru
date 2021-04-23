---
title: Код уведомления NM_GETCUSTOMSPLITRECT (Коммктрл. h)
description: Отправляется элементом управления "Кнопка" в родительский элемент, чтобы получить измерения для двух прямоугольников разворачивающейся кнопки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135114"
---
# <a name="nm_getcustomsplitrect-notification-code"></a><span data-ttu-id="9ffe2-105">\_Код уведомления жеткустомсплитрект (NM)</span><span class="sxs-lookup"><span data-stu-id="9ffe2-105">NM\_GETCUSTOMSPLITRECT notification code</span></span>

<span data-ttu-id="9ffe2-106">Отправляется элементом управления "Кнопка" в родительский элемент, чтобы получить измерения для двух прямоугольников разворачивающейся кнопки.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-106">Sent by a button control to its parent to get measurements for the two rectangles of the split button.</span></span> <span data-ttu-id="9ffe2-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9ffe2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9ffe2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ffe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ffe2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ffe2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ffe2-110">Указатель на [**нмкустомсплитректинфо**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) для получения сведений об ограничивающих прямоугольниках.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-110">A pointer to an [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) to receive bounding rectangles information.</span></span> <span data-ttu-id="9ffe2-111">Структура **нмкустомсплитректинфо** отправляется с кодом уведомления как запрос для родителя, чтобы предоставить измерения для прямоугольников разворачивающейся кнопки.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-111">The **NMCUSTOMSPLITRECTINFO** structure is sent with the notification code as a request for the parent to provide measurements for the rectangles of the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ffe2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ffe2-112">Return value</span></span>

<span data-ttu-id="9ffe2-113">Возвращайте [**кдрф \_ скипдефаулт**](cdrf-constants.md) , чтобы указать элементу управления "Кнопка" использовать значения, возвращаемые в структуре [**нмкустомсплитректинфо**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; в противном случае возвратите [**кдрф \_ додефаулт**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9ffe2-113">Return [**CDRF\_SKIPDEFAULT**](cdrf-constants.md) to tell the button control to use the values returned in the [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) structure; otherwise, return [**CDRF\_DODEFAULT**](cdrf-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ffe2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ffe2-114">Remarks</span></span>

<span data-ttu-id="9ffe2-115">Этот код уведомления отправляется элементом управления "Кнопка" перед его прорисовкой.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-115">This notification code is sent by a button control before it is drawn.</span></span> <span data-ttu-id="9ffe2-116">Кнопка должна иметь тип [**\_ SPLITBUTTON**](button-styles.md) или [**BS \_ дефсплитбуттон**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="9ffe2-116">The button must be of style [**BS\_SPLITBUTTON**](button-styles.md) or [**BS\_DEFSPLITBUTTON**](button-styles.md).</span></span> <span data-ttu-id="9ffe2-117">Если прямоугольники, возвращаемые элементу управления в *lParam* , недопустимы, они игнорируются.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-117">If the rectangles returned to the control in *lParam* are not valid, they are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ffe2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9ffe2-118">Requirements</span></span>



| <span data-ttu-id="9ffe2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9ffe2-119">Requirement</span></span> | <span data-ttu-id="9ffe2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9ffe2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffe2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ffe2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffe2-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ffe2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ffe2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ffe2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffe2-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ffe2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ffe2-125">Header</span><span class="sxs-lookup"><span data-stu-id="9ffe2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ffe2-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ffe2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





