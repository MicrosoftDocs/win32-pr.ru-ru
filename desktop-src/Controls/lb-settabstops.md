---
title: Сообщение LB_SETTABSTOPS (Winuser. h)
description: Задает позиции табуляции в поле со списком.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- Элементы управления Windows для LB_SETTABSTOPS сообщений
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892457"
---
# <a name="lb_settabstops-message"></a><span data-ttu-id="1d3a6-104">Сообщение сеттабстопс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="1d3a6-104">LB\_SETTABSTOPS message</span></span>

<span data-ttu-id="1d3a6-105">Задает позиции табуляции в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-105">Sets the tab-stop positions in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d3a6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d3a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d3a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d3a6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d3a6-108">Указывает количество единиц табуляции.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-108">Specifies the number of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="1d3a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d3a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d3a6-110">Указатель на первый элемент массива целых чисел, содержащий позиции табуляции.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-110">Pointer to the first member of an array of integers containing the tab stops.</span></span> <span data-ttu-id="1d3a6-111">Целые числа представляют число кварталов средней ширины символов для шрифта, выбранного в списке.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-111">The integers represent the number of quarters of the average character width for the font that is selected into the list box.</span></span> <span data-ttu-id="1d3a6-112">Например, позиция табуляции 4 помещается в 1,0 единиц знака, а позиция табуляции, равной 6, помещается по 1,5 среднему числу единиц символов.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-112">For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units.</span></span> <span data-ttu-id="1d3a6-113">Однако если список является частью диалогового окна, то целые числа находятся в единицах шаблона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-113">However, if the list box is part of a dialog box, the integers are in dialog template units.</span></span> <span data-ttu-id="1d3a6-114">Позиции табуляции должны быть отсортированы в возрастающем порядке. обратные вкладки не допускаются.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-114">The tab stops must be sorted in ascending order; backward tabs are not allowed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d3a6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d3a6-115">Return value</span></span>

<span data-ttu-id="1d3a6-116">Если заданы все указанные вкладки, возвращаемое значение равно **true**; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-116">If all the specified tabs are set, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d3a6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d3a6-117">Remarks</span></span>

<span data-ttu-id="1d3a6-118">Чтобы ответить на сообщение **\_ Сеттабстопса балансировки нагрузки** , список должен быть создан с помощью стиля [**фунта \_ усетабстопс**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1d3a6-118">To respond to the **LB\_SETTABSTOPS** message, the list box must have been created with the [**LBS\_USETABSTOPS**](list-box-styles.md) style.</span></span>

<span data-ttu-id="1d3a6-119">Если параметр *wParam* равен 0, а *lParam* имеет **значение NULL**, то позиция табуляции по умолчанию равна двум единицам диалогового шаблона.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-119">If *wParam* is 0 and *lParam* is **NULL**, the default tab stop is two dialog template units.</span></span> <span data-ttu-id="1d3a6-120">Если параметр *wParam* равен 1, то в списке будут находиться позиции табуляции, разделенные расстоянием, заданным параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-120">If *wParam* is 1, the list box will have tab stops separated by the distance specified by *lParam*.</span></span>

<span data-ttu-id="1d3a6-121">Если *lParam* указывает на больше одного значения, для каждого значения в *lParam* будет задана позиция табуляции до числа, указанного параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-121">If *lParam* points to more than a single value, a tab stop will be set for each value in *lParam*, up to the number specified by *wParam*.</span></span>

<span data-ttu-id="1d3a6-122">Значения, заданные параметром *lParam* , находятся в шаблонах диалоговых окон, которые являются аппаратно-независимыми устройствами, используемыми в шаблонах диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-122">The values specified by *lParam* are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="1d3a6-123">Чтобы преобразовать измерения из шаблона диалогового окна в единицы экрана (в пикселях), используйте функцию [**мапдиалогрект**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="1d3a6-123">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="1d3a6-124">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): буфер, на который указывает *lParam* , должен находиться в памяти, доступной для записи, несмотря на то, что сообщение не изменяет массив.</span><span class="sxs-lookup"><span data-stu-id="1d3a6-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The buffer pointed to by *lParam* must reside in writable memory, even though the message does not modify the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d3a6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1d3a6-125">Requirements</span></span>



| <span data-ttu-id="1d3a6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1d3a6-126">Requirement</span></span> | <span data-ttu-id="1d3a6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1d3a6-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3a6-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d3a6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3a6-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d3a6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d3a6-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d3a6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3a6-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d3a6-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d3a6-132">Header</span><span class="sxs-lookup"><span data-stu-id="1d3a6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d3a6-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d3a6-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d3a6-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d3a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3a6-135">**мапдиалогрект**</span><span class="sxs-lookup"><span data-stu-id="1d3a6-135">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

