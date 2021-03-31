---
title: Сообщение TCM_SETCURFOCUS (Коммктрл. h)
description: Устанавливает фокус на указанную вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сеткурфокус.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- Элементы управления Windows для TCM_SETCURFOCUS сообщений
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988684"
---
# <a name="tcm_setcurfocus-message"></a><span data-ttu-id="eac05-105">\_Сообщение СЕТКУРФОКУС TCM</span><span class="sxs-lookup"><span data-stu-id="eac05-105">TCM\_SETCURFOCUS message</span></span>

<span data-ttu-id="eac05-106">Устанавливает фокус на указанную вкладку в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="eac05-106">Sets the focus to a specified tab in a tab control.</span></span> <span data-ttu-id="eac05-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сеткурфокус**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="eac05-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eac05-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eac05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eac05-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eac05-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eac05-110">Индекс вкладки, получающей фокус.</span><span class="sxs-lookup"><span data-stu-id="eac05-110">Index of the tab that gets the focus.</span></span>

</dd> <dt>

<span data-ttu-id="eac05-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eac05-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eac05-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="eac05-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eac05-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eac05-113">Return value</span></span>

<span data-ttu-id="eac05-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="eac05-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eac05-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eac05-115">Remarks</span></span>

<span data-ttu-id="eac05-116">Если элемент управления "Вкладка" имеет стиль [**\_ кнопок TCS**](tab-control-styles.md) (режим кнопки), вкладка с фокусом может отличаться от выбранной вкладки. Например, если выбрана вкладка, пользователь может нажать клавиши со стрелками, чтобы установить фокус на другую вкладку, не изменяя выбранную вкладку. В режиме кнопки **TCM \_ сеткурфокус** устанавливает фокус ввода на кнопку, связанную с указанной вкладкой, но не изменяет выбранную вкладку.</span><span class="sxs-lookup"><span data-stu-id="eac05-116">If the tab control has the [**TCS\_BUTTONS**](tab-control-styles.md) style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, **TCM\_SETCURFOCUS** sets the input focus to the button associated with the specified tab, but it does not change the selected tab.</span></span>

<span data-ttu-id="eac05-117">Если в элементе управления "Вкладка" отсутствует [**стиль \_ кнопок TCS**](tab-control-styles.md) , изменение фокуса также приведет к изменению выбранной вкладки. В этом случае элемент управления "Вкладка" отправляет коды уведомлений [ТКН \_ Селчангинг](tcn-selchanging.md) и [ТКН \_ селчанже](tcn-selchange.md) в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="eac05-117">If the tab control does not have the [**TCS\_BUTTONS**](tab-control-styles.md) style, changing the focus also changes the selected tab. In this case, the tab control sends the [TCN\_SELCHANGING](tcn-selchanging.md) and [TCN\_SELCHANGE](tcn-selchange.md) notification codes to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac05-118">Требования</span><span class="sxs-lookup"><span data-stu-id="eac05-118">Requirements</span></span>



| <span data-ttu-id="eac05-119">Требование</span><span class="sxs-lookup"><span data-stu-id="eac05-119">Requirement</span></span> | <span data-ttu-id="eac05-120">Значение</span><span class="sxs-lookup"><span data-stu-id="eac05-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eac05-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eac05-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eac05-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eac05-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eac05-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eac05-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eac05-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eac05-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eac05-125">Header</span><span class="sxs-lookup"><span data-stu-id="eac05-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eac05-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="eac05-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac05-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eac05-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac05-128">**\_ЖЕТКУРФОКУС TCM**</span><span class="sxs-lookup"><span data-stu-id="eac05-128">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
</dt> </dl>

 

 





