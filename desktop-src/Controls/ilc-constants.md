---
title: Флаги создания списка изображений (Шлобж. h)
description: Набор битовых флагов, указывающих тип создаваемого списка изображений. Этот параметр может быть сочетанием следующих значений, но может включать только одно из \_ значений цвета ILC. Используется для \_ инициализации ImageList Create и IImageList2.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490209"
---
# <a name="image-list-creation-flags"></a>Флаги создания списка изображений

Набор битовых флагов, указывающих тип создаваемого списка изображений. Этот параметр может быть сочетанием следующих значений, но может включать только одно из \_ значений цвета ILC. Используется в [**ImageList \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) и [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).



| Константа/значение                                                                                                                                                                                                                                     | Описание                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ Маска**</dt> <dt>0x00000001</dt> </dl>                                     | Использовать маску. Список изображений содержит два точечных рисунка, один из которых является монохромным точечным рисунком, используемым в качестве маски. Если это значение не включено, список изображений содержит только одно растровое изображение.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_ ЦВЕТ**</dt> <dt>0x00000000</dt> </dl>                                  | Используйте поведение по умолчанию, если не задан ни один из других \_ флагов ILC колоркс. Как правило, значение по умолчанию — ILC \_ COLOR4, но для старых видеодрайверов значение по умолчанию — ILC \_ колорддб.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_ КОЛОРДДБ**</dt> <dt>0x000000FE</dt> </dl>                         | Используйте зависимый от устройства точечный рисунок.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt> </dl>                               | Используйте 4-разрядный (16-цветный) раздел DIB (BMP) в качестве точечного рисунка для списка изображений.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt> </dl>                               | Используйте 8-разрядный раздел DIB. Цвета, используемые для таблицы цветов, имеют те же цвета, что и палитра полутонов.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | Используйте 16-разрядный (32/64k-цветной) раздел DIB.<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | Используйте 24-разрядный раздел DIB.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | Используйте 32-разрядный раздел DIB.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ ПАЛИТРа**</dt> <dt>0x00000800</dt> </dl>                            | Не реализован.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_ ЗЕРКАЛЬный**</dt> <dt>0x00002000</dt> </dl>                               | Зеркальное отображение содержащихся значков, если процесс зеркально отражен<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_ ПЕРИТЕММИРРОР**</dt> <dt>0x00008000</dt> </dl>          | Приводит к тому, что код зеркального отображения зеркально отражает каждый элемент при вставке набора изображений, а не на всю полосу.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_ ОРИГИНАЛСИЗЕ**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista и более поздние версии.** Список ImageList должен принимать меньшее значение, чем установленные изображения, и применять исходный размер на основе добавленного образа.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_ ХИГХКУАЛИТИСКАЛЕ**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista и более поздние версии.** Зарезервировано.<br/>                                                                                                                                            |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 





