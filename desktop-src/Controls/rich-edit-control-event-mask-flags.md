---
title: Флаги Маски событий элемента управления Rich Edit (RichEdit. h)
description: Маска событий определяет, какие коды уведомления отправляются элементом управления Rich Edit в его родительское окно. Маска события может иметь значение None или быть сочетанием этих значений.
ms.assetid: ae0d2cbe-5cbc-42bb-aeb1-7e6be846a4ba
topic_type:
- apiref
api_name:
- ENM_CHANGE
- ENM_CLIPFORMAT
- ENM_CORRECTTEXT
- ENM_DRAGDROPDONE
- ENM_DROPFILES
- ENM_IMECHANGE
- ENM_KEYEVENTS
- ENM_LINK
- ENM_LOWFIRTF
- ENM_MOUSEEVENTS
- ENM_OBJECTPOSITIONS
- ENM_PARAGRAPHEXPANDED
- ENM_PROTECTED
- ENM_REQUESTRESIZE
- ENM_SCROLL
- ENM_SCROLLEVENTS
- ENM_SELCHANGE
- ENM_UPDATE
api_location:
- RichEdit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006a6d82e7aa4958b03360d05d29a78564f99db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657259"
---
# <a name="rich-edit-control-event-mask-flags"></a>Флаги Маски событий элемента управления Rich Edit

Маска событий определяет, какие коды уведомления отправляются элементом управления Rich Edit в его родительское окно. Маска события может иметь значение None или быть сочетанием этих значений.



| Константа                                                                                                                                                                              | Описание                                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENM_CHANGE"></span><span id="enm_change"></span><dl> <dt>**\_изменение енм**</dt> </dl>                                  | Отправляет уведомления о [ \_ смене на короткое](en-change--rich-edit-control-.md) .<br/>                                                                                                                                                                                                                                   |
| <span id="ENM_CLIPFORMAT"></span><span id="enm_clipformat"></span><dl> <dt>**ЕНМ \_ клипформат**</dt> </dl>                      | Отправляет [уведомления \_ клипформат](/windows/desktop/Controls/en-clipformat) .<br/>                                                                                                                                                                                                                                          |
| <span id="ENM_CORRECTTEXT"></span><span id="enm_correcttext"></span><dl> <dt>**ЕНМ \_ корректтекст**</dt> </dl>                   | Отправляет [уведомления \_ корректтекст](en-correcttext.md) .<br/>                                                                                                                                                                                                                                             |
| <span id="ENM_DRAGDROPDONE"></span><span id="enm_dragdropdone"></span><dl> <dt>**ЕНМ \_ драгдропдоне**</dt> </dl>                | Отправляет [уведомления \_ драгдропдоне](en-dragdropdone.md) .<br/>                                                                                                                                                                                                                                           |
| <span id="ENM_DROPFILES"></span><span id="enm_dropfiles"></span><dl> <dt>**ЕНМ \_ дропфилес**</dt> </dl>                         | Отправляет [уведомления \_ дропфилес](en-dropfiles.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_IMECHANGE"></span><span id="enm_imechange"></span><dl> <dt>**ЕНМ \_ имечанже**</dt> </dl>                         | Только Microsoft Rich Edit 1,0: отправляет [уведомления \_ имечанже](en-imechange.md) при изменении состояния преобразования IME. Только для азиатских языковых версий операционной системы.<br/>                                                                                                              |
| <span id="ENM_KEYEVENTS"></span><span id="enm_keyevents"></span><dl> <dt>**ЕНМ \_ кэйевентс**</dt> </dl>                         | Отправляет [уведомления \_ мсгфилтер](en-msgfilter.md) для событий клавиатуры.<br/>                                                                                                                                                                                                                             |
| <span id="ENM_LINK"></span><span id="enm_link"></span><dl> <dt>**Ссылка на ЕНМ \_**</dt> </dl>                                        | **Расширенное редактирование 2,0 и более поздних версий:** Отправляет уведомления о [ \_ ссылках на короткое](en-link.md) время, когда указатель мыши находится над текстом с \_ ссылкой CFE и выполняется одно из нескольких действий мыши.<br/>                                                                                                                     |
| <span id="ENM_LOWFIRTF"></span><span id="enm_lowfirtf"></span><dl> <dt>**ЕНМ \_ ловфиртф**</dt> </dl>                            | Отправляет [уведомления \_ ловфиртф](en-lowfirtf.md) .<br/>                                                                                                                                                                                                                                                   |
| <span id="ENM_MOUSEEVENTS"></span><span id="enm_mouseevents"></span><dl> <dt>**ЕНМ \_ маусивентс**</dt> </dl>                   | Отправляет [уведомления \_ мсгфилтер](en-msgfilter.md) для событий мыши.<br/>                                                                                                                                                                                                                                |
| <span id="ENM_OBJECTPOSITIONS"></span><span id="enm_objectpositions"></span><dl> <dt>**ЕНМ \_ обжектпоситионс**</dt> </dl>       | Отправляет [уведомления \_ обжектпоситионс](en-objectpositions.md) .<br/>                                                                                                                                                                                                                                     |
| <span id="ENM_PARAGRAPHEXPANDED"></span><span id="enm_paragraphexpanded"></span><dl> <dt>**ЕНМ \_ параграфекспандед**</dt> </dl> | Отправляет [уведомления \_ параграфекспандед](/windows/desktop/Controls/en-paragraphexpanded) .<br/>                                                                                                                                                                                                                            |
| <span id="ENM_PROTECTED"></span><span id="enm_protected"></span><dl> <dt>**ЕНМ с \_ защитой**</dt> </dl>                         | Отправляет уведомления с [ \_ защитой от короткого](en-protected.md) языка.<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_REQUESTRESIZE"></span><span id="enm_requestresize"></span><dl> <dt>**ЕНМ \_ рекуестресизе**</dt> </dl>             | Отправляет [уведомления \_ рекуестресизе](en-requestresize.md) .<br/>                                                                                                                                                                                                                                         |
| <span id="ENM_SCROLL"></span><span id="enm_scroll"></span><dl> <dt>**\_прокрутка енм**</dt> </dl>                                  | Отправляет [уведомления \_ HSCROLL](en-hscroll.md) и [en \_ VSCROLL](en-vscroll.md) .<br/>                                                                                                                                                                                                                   |
| <span id="ENM_SCROLLEVENTS"></span><span id="enm_scrollevents"></span><dl> <dt>**ЕНМ \_ скроллевентс**</dt> </dl>                | Отправляет [уведомления \_ мсгфилтер](en-msgfilter.md) для событий колесика мыши.<br/>                                                                                                                                                                                                                          |
| <span id="ENM_SELCHANGE"></span><span id="enm_selchange"></span><dl> <dt>**ЕНМ \_ селчанже**</dt> </dl>                         | Отправляет [уведомления \_ селчанже](en-selchange.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_UPDATE"></span><span id="enm_update"></span><dl> <dt>**\_Обновление енм**</dt> </dl>                                  | Отправляет уведомления о [ \_ обновлениях на короткое обновление](en-update.md) . <br/> **Расширенное изменение 2,0 и более поздних версий:** этот флаг игнорируется, и уведомления о [ \_ обновлениях на короткое обновление](en-update.md) всегда отправляются. Тем не менее, если Rich Edit 3,0 эмулирует Microsoft Rich Edit 1,0, этот флаг необходимо использовать для отправки \_ уведомлений о обновлении на короткое обновление.<br/> |



## <a name="remarks"></a>Комментарии

Маска событий по умолчанию — ЕНМ \_ None, в этом случае уведомления не отправляются в родительское окно. Можно получить и задать маску событий для элемента управления Rich Edit с помощью сообщений [**EM \_ GETEVENTMASK**](em-geteventmask.md) и [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>RichEdit. h</dt> </dl> |



 

