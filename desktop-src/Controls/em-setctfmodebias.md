---
title: Сообщение EM_SETCTFMODEBIAS (RichEdit. h)
description: Задает смещение режима в режиме платформы текстовых служб (TSF) для элемента управления расширенного редактирования.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- Элементы управления Windows для EM_SETCTFMODEBIAS сообщений
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535060"
---
# <a name="em_setctfmodebias-message"></a>\_Сообщение СЕТКТФМОДЕБИАС EM

Задает смещение режима в режиме платформы текстовых служб (TSF) для элемента управления расширенного редактирования.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение смещения режима. Это может быть одно из следующих значений.



| Значение                                                                                                                                                                                                                     | Значение                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**КТФМОДЕБИАС \_ по умолчанию**</dt> </dl>                                           | Смещение в режиме отсутствует.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**\_имя файла ктфмодебиас**</dt> </dl>                                        | Значение смещения — имя файла.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**\_имя ктфмодебиас**</dt> </dl>                                                    | Значение смещения — имя.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**\_Чтение ктфмодебиас**</dt> </dl>                                           | Смещение предназначено для чтения.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**КТФМОДЕБИАС \_ DateTime**</dt> </dl>                                        | Смещение — это дата или время.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**КТФМОДЕБИАС \_ беседа**</dt> </dl>                            | Смещение — это диалог.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**КТФМОДЕБИАС \_ числовой**</dt> </dl>                                           | Смещение — это число.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**КТФМОДЕБИАС \_ хирагана**</dt> </dl>                                        | Смещение — строки хирагана.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**КТФМОДЕБИАС \_ катакана**</dt> </dl>                                        | Значение смещения — строки катакана.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**\_ХАНГЫЛЬ ктфмодебиас**</dt> </dl>                                              | Смещение — символы хангыль.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**КТФМОДЕБИАС \_ халфвидскатакана**</dt> </dl>             | Смещение — строки катакана половинной ширины.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**КТФМОДЕБИАС \_ фуллвидсалфанумерик**</dt> </dl> | Смещение — это алфавитно-цифровые символы в полной ширине.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**КТФМОДЕБИАС \_ халфвидсалфанумерик**</dt> </dl> | Смещение — это алфавитно-цифровые символы половинной ширины.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвращаемое значение является новым значением смещения режима TSF. В случае неудачи возвращаемое значение является старым значением смещения режима TSF.

## <a name="remarks"></a>Комментарии

Если приложение Microsoft Rich Edit использует TSF, оно может выбрать смещение режима TSF. Это сообщение задает критерии, по которым в верхней части списка появляется альтернативный вариант выбора.

Чтобы установить сдвиг режима для редактора метода ввода (IME), используйте [**EM \_ сетимемодебиас**](em-setimemodebias.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ жетктфмодебиас**](em-getctfmodebias.md)
</dt> <dt>

[**EM \_ сетимемодебиас**](em-setimemodebias.md)
</dt> </dl>

 

 





