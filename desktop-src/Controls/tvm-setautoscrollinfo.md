---
title: Сообщение TVM_SETAUTOSCROLLINFO (Коммктрл. h)
description: Задает сведения, используемые для определения характеристик автоматической прокрутки. Это сообщение можно отправить явно или с помощью \_ макроса Сетаутоскроллинфо TreeView.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- Элементы управления Windows для TVM_SETAUTOSCROLLINFO сообщений
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654469"
---
# <a name="tvm_setautoscrollinfo-message"></a><span data-ttu-id="7e610-105">\_Сообщение TVM сетаутоскроллинфо</span><span class="sxs-lookup"><span data-stu-id="7e610-105">TVM\_SETAUTOSCROLLINFO message</span></span>

<span data-ttu-id="7e610-106">Задает сведения, используемые для определения характеристик автоматической прокрутки.</span><span class="sxs-lookup"><span data-stu-id="7e610-106">Sets information used to determine auto-scroll characteristics.</span></span> <span data-ttu-id="7e610-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетаутоскроллинфо TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="7e610-107">You can send this message explicitly or by using the [**TreeView\_SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e610-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e610-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e610-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e610-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e610-110">Указывает количество пикселей в секунду.</span><span class="sxs-lookup"><span data-stu-id="7e610-110">Specifies pixels per second.</span></span> <span data-ttu-id="7e610-111">Смещение для прокрутки делится на *wParam* , чтобы определить общую длительность автоматической прокрутки.</span><span class="sxs-lookup"><span data-stu-id="7e610-111">The offset to scroll is divided by the *wParam* to determine the total duration of the auto-scroll.</span></span>

</dd> <dt>

<span data-ttu-id="7e610-112">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e610-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e610-113">Задает интервал времени перерисовки.</span><span class="sxs-lookup"><span data-stu-id="7e610-113">Specifies the redraw time interval.</span></span> <span data-ttu-id="7e610-114">Перерисовка при каждом еласпед интервале, пока элемент не будет прокручивается в представление.</span><span class="sxs-lookup"><span data-stu-id="7e610-114">Redraw at every elasped interval, until the item is scrolled into view.</span></span> <span data-ttu-id="7e610-115">Заданному параметром *wParam*, выполняется вычисление расположения элемента и происходит перерисовка.</span><span class="sxs-lookup"><span data-stu-id="7e610-115">Given *wParam*, the location of the item is calculated and a repaint occurs.</span></span> <span data-ttu-id="7e610-116">Задайте это значение, чтобы создать плавную прокрутку.</span><span class="sxs-lookup"><span data-stu-id="7e610-116">Set this value to create smooth scrolling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e610-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e610-117">Return value</span></span>

<span data-ttu-id="7e610-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="7e610-118">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e610-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e610-119">Remarks</span></span>

<span data-ttu-id="7e610-120">Сведения о прокрутке используются для прокрутки невидимого элемента на представление.</span><span class="sxs-lookup"><span data-stu-id="7e610-120">Autoscroll information is used to scroll a nonvisible item into view.</span></span> <span data-ttu-id="7e610-121">Элемент управления должен иметь расширенный стиль [**телевизоры \_ \_ аутохскролл**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7e610-121">The control must have the [**TVS\_EX\_AUTOHSCROLL**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="7e610-122">Дополнительные сведения о расширенных стилях см. в разделе Tree-View Control Extended Styles.</span><span class="sxs-lookup"><span data-stu-id="7e610-122">For information on extended styles, see Tree-View Control Extended Styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e610-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7e610-123">Requirements</span></span>



| <span data-ttu-id="7e610-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7e610-124">Requirement</span></span> | <span data-ttu-id="7e610-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7e610-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e610-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e610-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7e610-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e610-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e610-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e610-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7e610-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7e610-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e610-130">Header</span><span class="sxs-lookup"><span data-stu-id="7e610-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e610-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e610-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





