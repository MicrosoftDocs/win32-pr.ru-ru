---
title: Сообщение TCM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Задает расширенные стили, которые будет использовать элемент управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетекстендедстиле.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- Элементы управления Windows для TCM_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071646"
---
# <a name="tcm_setextendedstyle-message"></a><span data-ttu-id="a49a6-105">\_Сообщение СЕТЕКСТЕНДЕДСТИЛЕ TCM</span><span class="sxs-lookup"><span data-stu-id="a49a6-105">TCM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="a49a6-106">Задает расширенные стили, которые будет использовать элемент управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="a49a6-106">Sets the extended styles that the tab control will use.</span></span> <span data-ttu-id="a49a6-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="a49a6-107">You can send this message explicitly or by using the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a49a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a49a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a49a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a49a6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a49a6-110">Значение **типа DWORD** , указывающее, какие стили в *lParam* должны быть затронуты.</span><span class="sxs-lookup"><span data-stu-id="a49a6-110">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="a49a6-111">Будут изменены только расширенные стили в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a49a6-111">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="a49a6-112">Все остальные стили будут поддерживаться по мере их возникновения.</span><span class="sxs-lookup"><span data-stu-id="a49a6-112">All other styles will be maintained as they are.</span></span> <span data-ttu-id="a49a6-113">Если этот параметр равен нулю, будут затронуты все стили в *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a49a6-113">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="a49a6-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a49a6-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a49a6-115">Значение, указывающее стили расширенного элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="a49a6-115">Value specifying the extended tab control styles.</span></span> <span data-ttu-id="a49a6-116">Это значение представляет собой сочетание [расширенных стилей](tab-control-extended-styles.md)элемента управления Tab.</span><span class="sxs-lookup"><span data-stu-id="a49a6-116">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a49a6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a49a6-117">Return value</span></span>

<span data-ttu-id="a49a6-118">Возвращает значение **типа DWORD** , содержащее предыдущий элемент управления Tab расширенные стили.</span><span class="sxs-lookup"><span data-stu-id="a49a6-118">Returns a **DWORD** value that contains the previous tab control extended styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="a49a6-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a49a6-119">Remarks</span></span>

<span data-ttu-id="a49a6-120">Параметр *wParam* позволяет изменять один или несколько расширенных стилей без предварительного получения существующих стилей.</span><span class="sxs-lookup"><span data-stu-id="a49a6-120">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="a49a6-121">Например, если передать [**TCS \_ ex \_ флатсепараторс**](tab-control-extended-styles.md) для *wParam* и 0 для *lParam*, то стиль **TCS \_ ex \_ флатсепараторс** будет сброшен, но все остальные стили останутся прежними.</span><span class="sxs-lookup"><span data-stu-id="a49a6-121">For example, if you pass [**TCS\_EX\_FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **TCS\_EX\_FLATSEPARATORS** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="a49a6-122">В целях обратной совместимости макрос [**табктрл \_ сетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) не был обновлен для использования *двексмаск*.</span><span class="sxs-lookup"><span data-stu-id="a49a6-122">For backward compatibility reasons, the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro has not been updated to use *dwExMask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a49a6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a49a6-123">Requirements</span></span>



| <span data-ttu-id="a49a6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a49a6-124">Requirement</span></span> | <span data-ttu-id="a49a6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a49a6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a49a6-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a49a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a49a6-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a49a6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a49a6-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a49a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a49a6-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a49a6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a49a6-130">Header</span><span class="sxs-lookup"><span data-stu-id="a49a6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a49a6-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a49a6-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a49a6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a49a6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49a6-133">**\_ЖЕТЕКСТЕНДЕДСТИЛЕ TCM**</span><span class="sxs-lookup"><span data-stu-id="a49a6-133">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
</dt> </dl>

 

 





