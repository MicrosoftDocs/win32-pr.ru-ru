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
# <a name="tf_lbi_-constants"></a>TF \_ ЛБИ \_ \* константы

Константы ** \_ tf \_ \* ЛБИ* _ используются с методом [итфлангбаритемсинк:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) , чтобы указать, какие элементы языковой панели изменились.



| Константа/значение                                                                                                                                                                                                                                                                  | Описание                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <dt>_ * TF \_ \_Значок ЛБИ * *</dt> <dt>0x00000001</dt> </dl>                                                        | Значок элемента изменился. Языковая панель вызывает [итфлангбаритембуттон::](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) GetResponse в ответ на это уведомление.<br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <dt>**Tf \_ ЛБИ \_ Text**</dt> <dt>0x00000002</dt> </dl>                                                        | Изменился текст кнопки или растрового элемента кнопки. Языковая панель вызывает [итфлангбаритембуттон:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) или [Итфлангбаритембитмапбуттон:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext)в зависимости от того, какой из них подходит в ответ на это уведомление.<br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <dt>**Tf \_ \_Подсказка ЛБИ**</dt> <dt>0x00000004</dt> </dl>                                               | Текст подсказки для элемента изменился. Языковая панель вызывает [итфлангбаритем:: жеттултипстринг](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) в ответ на это уведомление.<br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <dt>**Tf \_ \_Точечный рисунок ЛБИ**</dt> <dt>0x00000008</dt> </dl>                                                  | Битовая карта точечного рисунка или элемента кнопки точечного рисунка изменилась. Языковая панель вызывает [итфлангбаритембитмап::D равбитмап](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) или [Итфлангбаритембитмапбуттон::D равбитмап](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), в зависимости от того, какой из них подходит в ответ на это уведомление.<br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <dt>**Tf \_ ЛБИное \_ всплывающее сообщение**</dt> <dt>0x00000010</dt> </dl>                                               | Информация для элемента с подсказкой изменена. Языковая панель вызывает [итфлангбаритембаллун:: жетбаллунинфо](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) в ответ на это уведомление.<br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <dt>**Tf \_ \_Состояние ЛБИ**</dt> <dt>0x00010000</dt> </dl>                                                  | Состояние элемента изменилось. Языковая панель вызывает [итфлангбаритем::](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) GetResponse в ответ на это уведомление.<br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <dt>**Tf \_ ЛБИ \_ бмпалл**</dt> <dt>tf \_ ЛБИ \_ Bitmap \| tf \_ ЛБИ \_ TOOLTIP</dt> </dl>                          | Объединяет \_ \_ БИТОВУЮ карту TF ЛБИ и \_ \_ подсказку TF ЛБИ.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <dt>**Tf \_ ЛБИ \_ бмпбтналл**</dt> <dt>tf \_ ЛБИ \_ точечный рисунок \| tf \_ ЛБИ \_ Text \| tf \_ ЛБИ \_ TOOLTIP</dt> </dl> | Объединяет \_ \_ БИТОВУЮ карту TF ЛБИ, TF \_ ЛБИ \_ Text и TF \_ ЛБИ \_ TOOLTIP.<br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <dt>**Tf \_ ЛБИ \_ бтналл**</dt> <dt>tf \_ ЛБИ \_ Icon \| tf \_ ЛБИ \_ Text \| tf \_ ЛБИ \_ TOOLTIP</dt> </dl>            | Объединяет \_ значок TF ЛБИ \_ , TF \_ ЛБИ \_ Text и TF \_ ЛБИ \_ TOOLTIP.<br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                       |
| Header<br/>                   | <dl> <dt>Ктфутб. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ктфутб. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Итфлангбаритемсинк:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





