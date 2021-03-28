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
# <a name="mp_popupflags-constants"></a>\_Константы ПОПУПФЛАГС MP

Представляет параметры, доступные при отображении всплывающего меню.



| Константа/значение                                                                                                                                                                                                                               | Описание                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**МППФ \_ SETFOCUS**</dt> <dt>0x00000001</dt> </dl>                | Подайте всплывающему меню фокус.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**МППФ \_ ИНИТИАЛСЕЛЕКТ**</dt> <dt>0x00000002</dt> </dl> | Выберите первый элемент во всплывающем меню.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**МППФ \_ Неанимированное**</dt> свойство <dt>0x00000004</dt> </dl>             | Не используйте системные анимации по умолчанию, например, при отображении меню.<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**МППФ \_ КЛАВИАТУРА**</dt> <dt>0x00000010</dt> </dl>                | Активируйте меню с помощью сочетания клавиш.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**МППФ \_ Изменить расположение**</dt> <dt>0x00000020</dt> </dl>          | Отображение полосы в другом положении в зависимости от изменений в меню.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**МППФ \_ ФОРЦЕЗОРДЕР**</dt> <dt>0x00000040</dt> </dl>       | Зарезервировано. Не используется.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**МППФ \_ ФИНАЛСЕЛЕКТ**</dt> <dt>0x00000080</dt> </dl>       | Выберите последний элемент в меню.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**МППФ \_ Выровняйте \_ левые**</dt> <dt>0x02000000</dt> </dl>         | **Windows Vista или более поздней версии**: Выровняйте всплывающее меню слева от области, указанной в параметре *прцексклуде* [**Итраккшеллмену::P опуп**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) или [**именупопуп::P опуп**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup). Это выравнивание по умолчанию.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**МППФ \_ Выровняйте \_ справа**</dt> <dt>0x04000000</dt> </dl>      | **Windows Vista или более поздней версии**: Выровняйте всплывающее меню справа от области, указанной в параметре *прцексклуде* [**Итраккшеллмену::P опуп**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) или [**именупопуп::P опуп**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**МППФ \_ Лучшие**</dt> <dt>0x20000000</dt> </dl>                               | Расположите всплывающее меню над начальной точкой, указанной в параметре *PPT* [**итраккшеллмену::P опуп**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) или [**именупопуп::P опуп**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**МППФ \_ LEFT**</dt> <dt>0x40000000</dt> </dl>                            | Расположите всплывающее меню слева от начальной точки.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**МППФ \_ RIGHT**</dt> <dt>0x60000000</dt> </dl>                         | Расположите всплывающее меню справа от начальной точки.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**МППФ \_ BOTTOM**</dt> <dt>(int) 0x80000000</dt> </dl>                 | Расположите всплывающее меню под начальной точкой.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**МППФ \_ \_Маска POS**</dt> <dt>(int) 0xE0000000</dt> </dl>          | Маска расположения меню.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Примечания

Эти константы определены в файле shobjidl. h, начиная с Windows XP с пакетом обновления 1 (SP1) и Windows Server 2003

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Именупопуп::P опуп**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**Итраккшеллмену::P опуп**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




