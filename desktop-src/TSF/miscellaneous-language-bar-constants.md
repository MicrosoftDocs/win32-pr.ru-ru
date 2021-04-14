---
title: Различные константы языковой панели (Ктфутб. h)
description: Различные константы языковой панели задают определенные свойства языковых панелей.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415985"
---
# <a name="miscellaneous-language-bar-constants"></a>Различные константы языковой панели

Различные константы языковой панели задают определенные свойства языковых панелей.



| Константа/значение                                                                                                                                                                                                                                               | Описание                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <dt>**Tf \_ ДТЛБИ \_ усепрофилеикон**</dt> <dt>0x00000001</dt> </dl> | Элемент языковой панели системы должен отображать значок, указанный для профиля языка. Используется в методах [итфсистемдевицетипелангбаритем:: жетиконмоде](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) и [Итфсистемдевицетипелангбаритем:: сетиконмоде](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) .<br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <dt>**Tf \_ ИНВАЛИДМЕНУИТЕМ**</dt> <dt>(UINT) (-1)</dt> </dl>                 | Не используется.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <dt>**Tf \_ ЛБИ \_ бмпф \_ по вертикали**</dt> <dt>0x00000001</dt> </dl>         | Не используется.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <dt>**Tf \_ ЛБИ \_ DESC \_ maxlen**</dt> <dt>32</dt> </dl>                       | Длина в WCHAR символах для члена структуры [tf \_ Лангбаритеминфо. сздескриптион](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).<br/>                                                                                                                                                                                                 |



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

[Итфсистемдевицетипелангбаритем:: Жетиконмоде](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[Итфсистемдевицетипелангбаритем:: Сетиконмоде](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[TF \_ лангбаритеминфо](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





