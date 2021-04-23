---
title: Константы TF_LBI_ (Ктфутб. h)
description: '\_ \_ Константы TF ЛБИ \ используются с методом Итфлангбаритемсинк OnUpdate для указания того, какие элементы языковой панели изменились.'
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681855"
---
# <a name="tf_lbi_-constants"></a><span data-ttu-id="15ad2-103">TF \_ ЛБИ \_ \* константы</span><span class="sxs-lookup"><span data-stu-id="15ad2-103">TF\_LBI\_\* Constants</span></span>

<span data-ttu-id="15ad2-104">Константы \*\* \_ tf \_ \* ЛБИ\* _ используются с методом [итфлангбаритемсинк:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) , чтобы указать, какие элементы языковой панели изменились.</span><span class="sxs-lookup"><span data-stu-id="15ad2-104">The \**TF\_LBI\_\** _ constants are used with the [ITfLangBarItemSink::OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) method to indicate which language bar items changed.</span></span>



| <span data-ttu-id="15ad2-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="15ad2-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="15ad2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="15ad2-106">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <span data-ttu-id="15ad2-107"><dt>_ \* TF \_ \_Значок ЛБИ \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-107"><dt>_\*TF\_LBI\_ICON\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                                        | <span data-ttu-id="15ad2-108">Значок элемента изменился.</span><span class="sxs-lookup"><span data-stu-id="15ad2-108">The icon of the item has changed.</span></span> <span data-ttu-id="15ad2-109">Языковая панель вызывает [итфлангбаритембуттон::](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) GetResponse в ответ на это уведомление.</span><span class="sxs-lookup"><span data-stu-id="15ad2-109">The language bar calls [ITfLangBarItemButton::GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in response to this notification.</span></span><br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <span data-ttu-id="15ad2-110"><dt>**Tf \_ ЛБИ \_ Text**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-110"><dt>**TF\_LBI\_TEXT**</dt> <dt>0x00000002</dt></span></span> </dl>                                                        | <span data-ttu-id="15ad2-111">Изменился текст кнопки или растрового элемента кнопки.</span><span class="sxs-lookup"><span data-stu-id="15ad2-111">The text of a button or bitmap button item has changed.</span></span> <span data-ttu-id="15ad2-112">Языковая панель вызывает [итфлангбаритембуттон:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) или [Итфлангбаритембитмапбуттон:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext)в зависимости от того, какой из них подходит в ответ на это уведомление.</span><span class="sxs-lookup"><span data-stu-id="15ad2-112">The language bar calls [ITfLangBarItemButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) or [ITfLangBarItemBitmapButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), whichever is appropriate, in response to this notification.</span></span><br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <span data-ttu-id="15ad2-113"><dt>**Tf \_ \_Подсказка ЛБИ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-113"><dt>**TF\_LBI\_TOOLTIP**</dt> <dt>0x00000004</dt></span></span> </dl>                                               | <span data-ttu-id="15ad2-114">Текст подсказки для элемента изменился.</span><span class="sxs-lookup"><span data-stu-id="15ad2-114">The tooltip text of the item changed.</span></span> <span data-ttu-id="15ad2-115">Языковая панель вызывает [итфлангбаритем:: жеттултипстринг](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) в ответ на это уведомление.</span><span class="sxs-lookup"><span data-stu-id="15ad2-115">The language bar calls [ITfLangBarItem::GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in response to this notification.</span></span><br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <span data-ttu-id="15ad2-116"><dt>**Tf \_ \_Точечный рисунок ЛБИ**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-116"><dt>**TF\_LBI\_BITMAP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                  | <span data-ttu-id="15ad2-117">Битовая карта точечного рисунка или элемента кнопки точечного рисунка изменилась.</span><span class="sxs-lookup"><span data-stu-id="15ad2-117">The bitmap of a bitmap or bitmap button item changed.</span></span> <span data-ttu-id="15ad2-118">Языковая панель вызывает [итфлангбаритембитмап::D равбитмап](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) или [Итфлангбаритембитмапбуттон::D равбитмап](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), в зависимости от того, какой из них подходит в ответ на это уведомление.</span><span class="sxs-lookup"><span data-stu-id="15ad2-118">The language bar calls [ITfLangBarItemBitmap::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) or [ITfLangBarItemBitmapButton::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), whichever is appropriate, in response to this notification.</span></span><br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <span data-ttu-id="15ad2-119"><dt>**Tf \_ ЛБИное \_ всплывающее сообщение**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-119"><dt>**TF\_LBI\_BALLOON**</dt> <dt>0x00000010</dt></span></span> </dl>                                               | <span data-ttu-id="15ad2-120">Информация для элемента с подсказкой изменена.</span><span class="sxs-lookup"><span data-stu-id="15ad2-120">The information for a balloon item changed.</span></span> <span data-ttu-id="15ad2-121">Языковая панель вызывает [итфлангбаритембаллун:: жетбаллунинфо](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) в ответ на это уведомление.</span><span class="sxs-lookup"><span data-stu-id="15ad2-121">The language bar calls [ITfLangBarItemBalloon::GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in response to this notification.</span></span><br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <span data-ttu-id="15ad2-122"><dt>**Tf \_ \_Состояние ЛБИ**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-122"><dt>**TF\_LBI\_STATUS**</dt> <dt>0x00010000</dt></span></span> </dl>                                                  | <span data-ttu-id="15ad2-123">Состояние элемента изменилось.</span><span class="sxs-lookup"><span data-stu-id="15ad2-123">The item status changed.</span></span> <span data-ttu-id="15ad2-124">Языковая панель вызывает [итфлангбаритем::](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) GetResponse в ответ на это уведомление.</span><span class="sxs-lookup"><span data-stu-id="15ad2-124">The language bar calls [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in response to this notification.</span></span><br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <span data-ttu-id="15ad2-125"><dt>**Tf \_ ЛБИ \_ бмпалл**</dt> <dt>tf \_ ЛБИ \_ Bitmap \| tf \_ ЛБИ \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-125"><dt>**TF\_LBI\_BMPALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>                          | <span data-ttu-id="15ad2-126">Объединяет \_ \_ БИТОВУЮ карту TF ЛБИ и \_ \_ подсказку TF ЛБИ.</span><span class="sxs-lookup"><span data-stu-id="15ad2-126">Combines TF\_LBI\_BITMAP and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <span data-ttu-id="15ad2-127"><dt>**Tf \_ ЛБИ \_ бмпбтналл**</dt> <dt>tf \_ ЛБИ \_ точечный рисунок \| tf \_ ЛБИ \_ Text \| tf \_ ЛБИ \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-127"><dt>**TF\_LBI\_BMPBTNALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl> | <span data-ttu-id="15ad2-128">Объединяет \_ \_ БИТОВУЮ карту TF ЛБИ, TF \_ ЛБИ \_ Text и TF \_ ЛБИ \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="15ad2-128">Combines TF\_LBI\_BITMAP, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <span data-ttu-id="15ad2-129"><dt>**Tf \_ ЛБИ \_ бтналл**</dt> <dt>tf \_ ЛБИ \_ Icon \| tf \_ ЛБИ \_ Text \| tf \_ ЛБИ \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-129"><dt>**TF\_LBI\_BTNALL**</dt> <dt>TF\_LBI\_ICON\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>            | <span data-ttu-id="15ad2-130">Объединяет \_ значок TF ЛБИ \_ , TF \_ ЛБИ \_ Text и TF \_ ЛБИ \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="15ad2-130">Combines TF\_LBI\_ICON, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="15ad2-131">Требования</span><span class="sxs-lookup"><span data-stu-id="15ad2-131">Requirements</span></span>



| <span data-ttu-id="15ad2-132">Требование</span><span class="sxs-lookup"><span data-stu-id="15ad2-132">Requirement</span></span> | <span data-ttu-id="15ad2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="15ad2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15ad2-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15ad2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="15ad2-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15ad2-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="15ad2-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15ad2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="15ad2-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15ad2-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15ad2-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="15ad2-138">Redistributable</span></span><br/>          | <span data-ttu-id="15ad2-139">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="15ad2-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="15ad2-140">Header</span><span class="sxs-lookup"><span data-stu-id="15ad2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ad2-141"><dt>Ктфутб. h</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-141"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="15ad2-142">IDL</span><span class="sxs-lookup"><span data-stu-id="15ad2-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15ad2-143"><dt>Ктфутб. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15ad2-143"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ad2-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15ad2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ad2-145">Итфлангбаритемсинк:: OnUpdate</span><span class="sxs-lookup"><span data-stu-id="15ad2-145">ITfLangBarItemSink::OnUpdate</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





