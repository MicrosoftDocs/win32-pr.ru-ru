---
title: Сообщение LVM_SCROLL (Коммктрл. h)
description: Прокручивает содержимое элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса прокрутки ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- Элементы управления Windows для LVM_SCROLL сообщений
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491451"
---
# <a name="lvm_scroll-message"></a><span data-ttu-id="0d9c0-105">LVM \_ прокрутить сообщение</span><span class="sxs-lookup"><span data-stu-id="0d9c0-105">LVM\_SCROLL message</span></span>

<span data-ttu-id="0d9c0-106">Прокручивает содержимое элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="0d9c0-106">Scrolls the content of a list-view control.</span></span> <span data-ttu-id="0d9c0-107">Это сообщение можно отправить явно или с помощью макроса [**\_ прокрутки ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .</span><span class="sxs-lookup"><span data-stu-id="0d9c0-107">You can send this message explicitly or by using the [**ListView\_Scroll**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d9c0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d9c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d9c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d9c0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d9c0-110">Значение типа **int** , указывающее величину горизонтальной прокрутки (в пикселях) относительно текущей точки содержимого представления списка.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-110">Value of type **int** that specifies the amount of horizontal scrolling, in pixels, relative to the current position of the list view content.</span></span> <span data-ttu-id="0d9c0-111">Если элемент управления "представление списка" находится в представлении списка, это значение округляется до ближайшего числа пикселей, образующих целый столбец.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-111">If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column.</span></span>

</dd> <dt>

<span data-ttu-id="0d9c0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d9c0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d9c0-113">Значение типа **int** , указывающее величину вертикальной прокрутки (в пикселях) относительно текущей позицией содержимого представления списка.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-113">Value of type **int** that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d9c0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d9c0-114">Return value</span></span>

<span data-ttu-id="0d9c0-115">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-115">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d9c0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d9c0-116">Remarks</span></span>

<span data-ttu-id="0d9c0-117">Если элемент управления "представление списка" находится в представлении отчета, элемент управления можно прокручивать по вертикали только в пределах целых линий.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-117">When the list-view control is in report view, the control can only be scrolled vertically in whole line increments.</span></span> <span data-ttu-id="0d9c0-118">Таким образом, параметр *lParam* округляется до ближайшего числа пикселей, образующих весь инкремент строки.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-118">Therefore, the *lParam* parameter will be rounded to the nearest number of pixels that form a whole line increment.</span></span> <span data-ttu-id="0d9c0-119">Например, если высота строки составляет 16 пикселей, а для *lParam* передается 8, то список будет прокручиваться на 16 пикселей (1 строка).</span><span class="sxs-lookup"><span data-stu-id="0d9c0-119">For example, if the height of a line is 16 pixels and 8 is passed for *lParam*, the list will be scrolled by 16 pixels (1 line).</span></span> <span data-ttu-id="0d9c0-120">Если для *lParam* передается 7, список будет прокручиваться на 0 пикселей (0 строк).</span><span class="sxs-lookup"><span data-stu-id="0d9c0-120">If 7 is passed for *lParam*, the list will be scrolled 0 pixels (0 lines).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9c0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0d9c0-121">Requirements</span></span>



| <span data-ttu-id="0d9c0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0d9c0-122">Requirement</span></span> | <span data-ttu-id="0d9c0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0d9c0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9c0-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d9c0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9c0-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d9c0-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d9c0-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d9c0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9c0-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d9c0-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d9c0-128">Header</span><span class="sxs-lookup"><span data-stu-id="0d9c0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d9c0-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d9c0-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





