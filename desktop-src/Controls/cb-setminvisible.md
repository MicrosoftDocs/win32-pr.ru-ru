---
title: Сообщение CB_SETMINVISIBLE (Коммктрл. h)
description: Приложение отправляет \_ сообщение СЕТМИНВИСИБЛЕ CB, чтобы задать минимальное количество видимых элементов в раскрывающемся списке поля со списком.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- Элементы управления Windows для CB_SETMINVISIBLE сообщений
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135219"
---
# <a name="cb_setminvisible-message"></a><span data-ttu-id="e949b-104">\_Сообщение СЕТМИНВИСИБЛЕ CB</span><span class="sxs-lookup"><span data-stu-id="e949b-104">CB\_SETMINVISIBLE message</span></span>

<span data-ttu-id="e949b-105">Приложение отправляет сообщение **\_ сетминвисибле CB** , чтобы задать минимальное количество видимых элементов в раскрывающемся списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e949b-105">An application sends a **CB\_SETMINVISIBLE** message to set the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e949b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e949b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e949b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e949b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e949b-108">Указывает минимальное число видимых элементов.</span><span class="sxs-lookup"><span data-stu-id="e949b-108">Specifies the minimum number of visible items.</span></span>

</dd> <dt>

<span data-ttu-id="e949b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e949b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e949b-110">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e949b-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e949b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e949b-111">Return value</span></span>

<span data-ttu-id="e949b-112">Если сообщение прошло успешно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e949b-112">If the message is successful, the return value is **TRUE**.</span></span> <span data-ttu-id="e949b-113">В противном случае возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="e949b-113">Otherwise the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e949b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e949b-114">Remarks</span></span>

<span data-ttu-id="e949b-115">Если число элементов в раскрывающемся списке больше минимального, в поле со списком используется полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e949b-115">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span> <span data-ttu-id="e949b-116">По умолчанию 30 — минимальное число видимых элементов.</span><span class="sxs-lookup"><span data-stu-id="e949b-116">By default, 30 is the minimum number of visible items.</span></span>

<span data-ttu-id="e949b-117">Это сообщение пропускается, если элемент управления "поле со списком" имеет стиль [**CBS \_ ноинтегралхеигхт**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="e949b-117">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="e949b-118">Чтобы использовать **CB \_ сетминвисибле**, приложение должно указать comctl32.dll версии 6 в манифесте.</span><span class="sxs-lookup"><span data-stu-id="e949b-118">To use **CB\_SETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="e949b-119">Дополнительные сведения см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e949b-119">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e949b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e949b-120">Requirements</span></span>



| <span data-ttu-id="e949b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e949b-121">Requirement</span></span> | <span data-ttu-id="e949b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e949b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e949b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e949b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e949b-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e949b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e949b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e949b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e949b-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e949b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e949b-127">Header</span><span class="sxs-lookup"><span data-stu-id="e949b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e949b-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e949b-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e949b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e949b-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e949b-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e949b-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e949b-131">**\_ЖЕТМИНВИСИБЛЕ CB**</span><span class="sxs-lookup"><span data-stu-id="e949b-131">**CB\_GETMINVISIBLE**</span></span>](cb-getminvisible.md)
</dt> <dt>

[<span data-ttu-id="e949b-132">**Поле со списком \_ сетминвисибле**</span><span class="sxs-lookup"><span data-stu-id="e949b-132">**ComboBox\_SetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





