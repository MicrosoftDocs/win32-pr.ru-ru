---
description: Представляет параметры, доступные при отображении всплывающего меню.
title: Константы MP_POPUPFLAGS (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154930"
---
# <a name="mp_popupflags-constants"></a><span data-ttu-id="07462-103">\_Константы ПОПУПФЛАГС MP</span><span class="sxs-lookup"><span data-stu-id="07462-103">MP\_POPUPFLAGS constants</span></span>

<span data-ttu-id="07462-104">Представляет параметры, доступные при отображении всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="07462-104">Represent options available when displaying a pop-up menu.</span></span>



| <span data-ttu-id="07462-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="07462-105">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="07462-106">Описание</span><span class="sxs-lookup"><span data-stu-id="07462-106">Description</span></span>                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <span data-ttu-id="07462-107"><dt>**МППФ \_ SETFOCUS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="07462-107"><dt>**MPPF\_SETFOCUS**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="07462-108">Подайте всплывающему меню фокус.</span><span class="sxs-lookup"><span data-stu-id="07462-108">Give the pop-up menu the focus.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <span data-ttu-id="07462-109"><dt>**МППФ \_ ИНИТИАЛСЕЛЕКТ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="07462-109"><dt>**MPPF\_INITIALSELECT**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="07462-110">Выберите первый элемент во всплывающем меню.</span><span class="sxs-lookup"><span data-stu-id="07462-110">Select the first item in the pop-up menu.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <span data-ttu-id="07462-111"><dt>**МППФ \_ Неанимированное**</dt> свойство <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="07462-111"><dt>**MPPF\_NOANIMATE**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="07462-112">Не используйте системные анимации по умолчанию, например, при отображении меню.</span><span class="sxs-lookup"><span data-stu-id="07462-112">Do not use the default system animations, for example, fade-in, when displaying the menu.</span></span><br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <span data-ttu-id="07462-113"><dt>**МППФ \_ КЛАВИАТУРА**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="07462-113"><dt>**MPPF\_KEYBOARD**</dt> <dt>0x00000010</dt></span></span> </dl>                | <span data-ttu-id="07462-114">Активируйте меню с помощью сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="07462-114">Activate the menu by a keyboard shortcut.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <span data-ttu-id="07462-115"><dt>**МППФ \_ Изменить расположение**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="07462-115"><dt>**MPPF\_REPOSITION**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="07462-116">Отображение полосы в другом положении в зависимости от изменений в меню.</span><span class="sxs-lookup"><span data-stu-id="07462-116">Display the bar in a different position, based on changes to the menu.</span></span><br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <span data-ttu-id="07462-117"><dt>**МППФ \_ ФОРЦЕЗОРДЕР**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="07462-117"><dt>**MPPF\_FORCEZORDER**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="07462-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="07462-118">Reserved.</span></span> <span data-ttu-id="07462-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="07462-119">Do not use.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <span data-ttu-id="07462-120"><dt>**МППФ \_ ФИНАЛСЕЛЕКТ**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="07462-120"><dt>**MPPF\_FINALSELECT**</dt> <dt>0x00000080</dt></span></span> </dl>       | <span data-ttu-id="07462-121">Выберите последний элемент в меню.</span><span class="sxs-lookup"><span data-stu-id="07462-121">Select the last item in the menu.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <span data-ttu-id="07462-122"><dt>**МППФ \_ Выровняйте \_ левые**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="07462-122"><dt>**MPPF\_ALIGN\_LEFT**</dt> <dt>0x02000000</dt></span></span> </dl>         | <span data-ttu-id="07462-123">**Windows Vista или более поздней версии**: Выровняйте всплывающее меню слева от области, указанной в параметре *прцексклуде* [**Итраккшеллмену::P опуп**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) или [**именупопуп::P опуп**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="07462-123">**Windows Vista or later**: Align the pop-up menu to the left of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span> <span data-ttu-id="07462-124">Это выравнивание по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07462-124">This is the default alignment.</span></span><br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <span data-ttu-id="07462-125"><dt>**МППФ \_ Выровняйте \_ справа**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="07462-125"><dt>**MPPF\_ALIGN\_RIGHT**</dt> <dt>0x04000000</dt></span></span> </dl>      | <span data-ttu-id="07462-126">**Windows Vista или более поздней версии**: Выровняйте всплывающее меню справа от области, указанной в параметре *прцексклуде* [**Итраккшеллмену::P опуп**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) или [**именупопуп::P опуп**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="07462-126">**Windows Vista or later**: Align the pop-up menu to the right of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <span data-ttu-id="07462-127"><dt>**МППФ \_ Лучшие**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="07462-127"><dt>**MPPF\_TOP**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="07462-128">Расположите всплывающее меню над начальной точкой, указанной в параметре *PPT* [**итраккшеллмену::P опуп**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) или [**именупопуп::P опуп**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="07462-128">Position the pop-up menu above the initial point specified in the *ppt* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <span data-ttu-id="07462-129"><dt>**МППФ \_ LEFT**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="07462-129"><dt>**MPPF\_LEFT**</dt> <dt>0x40000000</dt></span></span> </dl>                            | <span data-ttu-id="07462-130">Расположите всплывающее меню слева от начальной точки.</span><span class="sxs-lookup"><span data-stu-id="07462-130">Position the pop-up menu to the left of the initial point.</span></span><br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <span data-ttu-id="07462-131"><dt>**МППФ \_ RIGHT**</dt> <dt>0x60000000</dt></span><span class="sxs-lookup"><span data-stu-id="07462-131"><dt>**MPPF\_RIGHT**</dt> <dt>0x60000000</dt></span></span> </dl>                         | <span data-ttu-id="07462-132">Расположите всплывающее меню справа от начальной точки.</span><span class="sxs-lookup"><span data-stu-id="07462-132">Position the pop-up menu to the right of the initial point.</span></span><br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <span data-ttu-id="07462-133"><dt>**МППФ \_ BOTTOM**</dt> <dt>(int) 0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="07462-133"><dt>**MPPF\_BOTTOM**</dt> <dt>(int)0x80000000</dt></span></span> </dl>                 | <span data-ttu-id="07462-134">Расположите всплывающее меню под начальной точкой.</span><span class="sxs-lookup"><span data-stu-id="07462-134">Position the pop-up menu below the initial point.</span></span><br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <span data-ttu-id="07462-135"><dt>**МППФ \_ \_Маска POS**</dt> <dt>(int) 0xE0000000</dt></span><span class="sxs-lookup"><span data-stu-id="07462-135"><dt>**MPPF\_POS\_MASK**</dt> <dt>(int)0xE0000000</dt></span></span> </dl>          | <span data-ttu-id="07462-136">Маска расположения меню.</span><span class="sxs-lookup"><span data-stu-id="07462-136">The menu position mask.</span></span><br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="07462-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="07462-137">Remarks</span></span>

<span data-ttu-id="07462-138">Эти константы определены в файле shobjidl. h, начиная с Windows XP с пакетом обновления 1 (SP1) и Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07462-138">These constants are defined in the Shobjidl.h file beginning in Windows XP Service Pack 1 (SP1) and Windows Server 2003</span></span>

## <a name="requirements"></a><span data-ttu-id="07462-139">Требования</span><span class="sxs-lookup"><span data-stu-id="07462-139">Requirements</span></span>



| <span data-ttu-id="07462-140">Требование</span><span class="sxs-lookup"><span data-stu-id="07462-140">Requirement</span></span> | <span data-ttu-id="07462-141">Значение</span><span class="sxs-lookup"><span data-stu-id="07462-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07462-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07462-142">Minimum supported client</span></span><br/> | <span data-ttu-id="07462-143">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="07462-143">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07462-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07462-144">Minimum supported server</span></span><br/> | <span data-ttu-id="07462-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07462-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07462-146">Header</span><span class="sxs-lookup"><span data-stu-id="07462-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="07462-147"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07462-147"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="07462-148">IDL</span><span class="sxs-lookup"><span data-stu-id="07462-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07462-149"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="07462-149"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07462-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07462-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07462-151">**Именупопуп::P опуп**</span><span class="sxs-lookup"><span data-stu-id="07462-151">**IMenuPopup::Popup**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[<span data-ttu-id="07462-152">**Итраккшеллмену::P опуп**</span><span class="sxs-lookup"><span data-stu-id="07462-152">**ITrackShellMenu::Popup**</span></span>](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




