---
title: Константы TF_LBI_STATUS_ (Ктфутб. h)
description: '\_ \_ Константа TF ЛБИ Status \_ \ указывает состояние элемента языковой панели. Эти значения используются с методом Итфлангбаритемного состояния.'
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803341"
---
# <a name="tf_lbi_status_-constants"></a>\_ \_ \_ \* Константы состояния TF ЛБИ

Константа ** \_ tf \_ ЛБИ \_ \* Status* _ указывает состояние элемента языковой панели. Эти значения используются с методом [итфлангбаритем:: with Status](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .



| Константа/значение                                                                                                                                                                                                                                                       | Описание                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>_ * TF \_ \_ \_ Скрытое состояние ЛБИ * *</dt> <dt>0x00000001</dt> </dl>                 | Элемент скрыт. Этот стиль игнорируется, если элемент не содержит \_ стиль ХИДДЕНСТАТУСКОНТРОЛ TF ЛБИ \_ Style \_ .<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**Tf \_ \_Состояние ЛБИ \_ disabled**</dt> <dt>0x00000002</dt> </dl>           | Элемент отключен.<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**Tf \_ ЛБИ \_ состояние \_ БТН \_ переключено**</dt> <dt>0x00010000</dt> </dl> | Элемент находится в переключенном или нажатом состоянии. Этот стиль игнорируется, если элемент не содержит \_ \_ \_ стиль переключателя TF ЛБИ Style БТН \_ .<br/> |



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

[Итфлангбаритем::/Status](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





