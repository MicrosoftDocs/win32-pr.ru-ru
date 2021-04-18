---
title: Константы TF_SFT_ (Ктфутб. h)
description: '\_ \_ Константы TF SFT \ определяют параметры вывода плавающей языковой панели.'
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681909"
---
# <a name="tf_sft_-constants"></a>TF \_ SFT \_ \* константы

Константы ** \_ tf \_ \* SFT* _. указывают параметры экрана плавающей языковой панели.



| Константа/значение                                                                                                                                                                                                                                                                    | Описание                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>_ * TF \_ SFT \_ шовнормал * *</dt> <dt>0x00000001</dt> </dl>                                        | Отображение языковой панели в виде плавающего окна. Эта константа не может быть объединена с помощью TF \_ SFT \_ Dock, TF \_ SFT \_ сворачивания, TF \_ SFT \_ Hidden или TF \_ SFT \_ дескбанд констант.<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**Tf \_ SFT \_ DOCKER**</dt> <dt>0x00000002</dt> </dl>                                                          | Закрепите языковую панель в отдельной области задач. Эта константа не может использоваться в сочетании с TF \_ SFT \_ ШОВНОРМАЛ, TF \_ SFT \_ сворачивания, TF \_ SFT \_ Hidden или TF \_ SFT \_ дескбанд константами. Доступно только в Windows XP.<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**Tf \_ SFT, \_ уменьшено до**</dt> <dt>0x00000004</dt> </dl>                                           | Отображение языковой панели в виде одного значка в области уведомлений. Эту константу нельзя сочетать с \_ \_ константами TF SFT ШОВНОРМАЛ, TF \_ SFT \_ DOCKER, TF \_ SFT \_ Hidden или TF \_ SFT \_ дескбанд. В Windows XP используйте \_ \_ вместо него TF SFT дескбанд.<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**Tf \_ \_Скрытые**</dt> <dt>0x00000008</dt> </dl>                                                    | Скрыть языковую панель. Эта константа не может быть объединена с TF \_ SFT \_ ШОВНОРМАЛ, TF \_ SFT \_ Dock, TF \_ SFT \_ сворачивания или TF \_ SFT \_ дескбанд константами.<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**Tf \_ \_НЕпрозрачное для SFT**</dt> <dt>0x00000010</dt> </dl>                            | Сделать языковую панель непрозрачной.<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**Tf \_ SFT \_ ловтранспаренци**</dt> <dt>0x00000020</dt> </dl>                         | Сделать языковую панель частично прозрачной. Доступно только в Windows 2000 или более поздней версии.<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**Tf \_ SFT \_ хигхтранспаренци**</dt> <dt>0x00000040</dt> </dl>                      | Сделать языковую панель сильно прозрачной. Доступно только в Windows 2000 или более поздней версии.<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**Tf \_ \_Метки SFT**</dt> <dt>0x00000080</dt> </dl>                                                    | Отображать текстовые метки рядом со значками языковой панели.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**Tf \_ \_**</dt> <dt>0x00000100ы</dt> SFT </dl>                                              | Скрыть текстовые метки значков языковой панели.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ екстраиконсонминимизед**</dt> <dt>0x00000200</dt> </dl>       | Отображение значков службы текста на панели задач, когда панель языка свернута.<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ ноекстраиконсонминимизед**</dt> <dt>0x00000400</dt> </dl> | Скрытие значков службы текста на панели задач при сворачивании языковой панели.<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**Tf \_ SFT \_ дескбанд**</dt> <dt>0x00000800</dt> </dl>                                              | Закрепите языковую панель на ригхсанд конец панели задач системы (непосредственно слева от области уведомлений или часов). Эту константу невозможно объединить с TF \_ SFT \_ ШОВНОРМАЛ, TF \_ SFT \_ Dock, TF \_ SFT \_ сворачивания или TF \_ SFT \_ Hidden константы. Доступно только в Windows XP.<br/> |



## <a name="remarks"></a>Комментарии

Метод [итфлангбармгр:: шовфлоатинг](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) задает результат логической операции **or** над одной или несколькими константами для указания атрибутов элемента языковой панели.

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

[Итфлангбармгр:: Шовфлоатинг](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





