---
title: Сообщение CB_GETMINVISIBLE (Коммктрл. h)
description: Возвращает минимальное число видимых элементов в раскрывающемся списке поля со списком.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Элементы управления Windows для CB_GETMINVISIBLE сообщений
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891918"
---
# <a name="cb_getminvisible-message"></a><span data-ttu-id="00f44-104">\_Сообщение ЖЕТМИНВИСИБЛЕ CB</span><span class="sxs-lookup"><span data-stu-id="00f44-104">CB\_GETMINVISIBLE message</span></span>

<span data-ttu-id="00f44-105">Возвращает минимальное число видимых элементов в раскрывающемся списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="00f44-105">Gets the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="00f44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00f44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00f44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00f44-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00f44-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="00f44-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="00f44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00f44-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00f44-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="00f44-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00f44-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00f44-111">Return value</span></span>

<span data-ttu-id="00f44-112">Возвращаемое значение — это минимальное число видимых элементов.</span><span class="sxs-lookup"><span data-stu-id="00f44-112">The return value is the minimum number of visible items.</span></span>

## <a name="remarks"></a><span data-ttu-id="00f44-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00f44-113">Remarks</span></span>

<span data-ttu-id="00f44-114">Если число элементов в раскрывающемся списке больше минимального, в поле со списком используется полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="00f44-114">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span>

<span data-ttu-id="00f44-115">Это сообщение пропускается, если элемент управления "поле со списком" имеет стиль [**CBS \_ ноинтегралхеигхт**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="00f44-115">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="00f44-116">Чтобы использовать **CB \_ жетминвисибле**, приложение должно указать comctl32.dll версии 6 в манифесте.</span><span class="sxs-lookup"><span data-stu-id="00f44-116">To use **CB\_GETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="00f44-117">Дополнительные сведения см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="00f44-117">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00f44-118">Требования</span><span class="sxs-lookup"><span data-stu-id="00f44-118">Requirements</span></span>



| <span data-ttu-id="00f44-119">Требование</span><span class="sxs-lookup"><span data-stu-id="00f44-119">Requirement</span></span> | <span data-ttu-id="00f44-120">Значение</span><span class="sxs-lookup"><span data-stu-id="00f44-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00f44-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00f44-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00f44-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00f44-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00f44-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00f44-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00f44-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00f44-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00f44-125">Header</span><span class="sxs-lookup"><span data-stu-id="00f44-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f44-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f44-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00f44-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00f44-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="00f44-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="00f44-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="00f44-129">**\_СЕТМИНВИСИБЛЕ CB**</span><span class="sxs-lookup"><span data-stu-id="00f44-129">**CB\_SETMINVISIBLE**</span></span>](cb-setminvisible.md)
</dt> <dt>

[<span data-ttu-id="00f44-130">**Поле со списком \_ жетминвисибле**</span><span class="sxs-lookup"><span data-stu-id="00f44-130">**ComboBox\_GetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





