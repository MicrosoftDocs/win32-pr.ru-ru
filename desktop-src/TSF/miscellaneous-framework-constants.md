---
title: Различные константы платформы (Мсктф. h)
description: Различные константы платформы указывают параметры для клиентов, процессов или текста.
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492315"
---
# <a name="miscellaneous-framework-constants"></a>Различные константы платформы

Различные константы платформы указывают параметры для клиентов, процессов или текста.



| Константа/значение                                                                                                                                                                                                                                                      | Описание                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**Tf \_ CLIENTID \_ null**</dt> <dt>((тфклиентид) 0)</dt> </dl>                        | Указывает на службу текстового ввода, которую клиент деактивирует. См. [тфклиентид](tfclientid.md).<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**Tf \_ Недопустимый \_ гуидатом**</dt> <dt>((тфгуидатом) 0)</dt> </dl>               | Недопустимое значение [тфгуидатом](tfguidatom.md) для текущего процесса.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**Tf \_ \_Выбор по умолчанию**</dt> <dt>(Выбор служб терминалов \_ по умолчанию \_ )</dt> </dl> | Использовать выбор по умолчанию. Используется [ITfContext:: SELECT](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)и [итекстстореанчор:: SELECT](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**Tf \_ ГТП, \_ включая \_ текст**</dt> <dt>(0x1)</dt> </dl>                               | Указывает, что метод [итфедитрекорд:: жеттекстандпропертюпдатес](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) будет получать коллекцию объектов Range, охватывающую текст, измененный во время сеанса редактирования.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**Tf \_ \_Объект HF**</dt> <dt>(1)</dt> </dl>                                              | Если обнаружен внедренный объект, то при сдвиге диапазона останавливается. Используется в **dwFlags** члене структуры [tf \_ халтконд](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**Tf \_ \_Исправление IE**</dt> <dt>(1)</dt> </dl>                                  | Текст представляет собой преобразование (исправление) существующего содержимого, чтобы другие текстовые службы могли сохранять данные, связанные с исходным текстом. Используется в параметре *dwFlags* объекта [Итфранже:: инсертембеддед](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**Tf \_ Недопустимый \_ файл cookie**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                      | Не используется.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**Tf \_ НЕДОПУСТИМое \_ изменение \_ файла cookie**</dt> <dt>(0)</dt> </dl>               | Не используется.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**Tf \_ ПОПФ \_ все**</dt> <dt>(0x1)</dt> </dl>                                               | Все контексты удаляются из стека. Используется в параметре *dwFlags* параметра [ITfDocumentMgr::P Op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**Tf \_ ST- \_ исправление**</dt> <dt>(1)</dt> </dl>                                  | Текст представляет собой преобразование (исправление) существующего содержимого, чтобы другие текстовые службы могли сохранять данные, связанные с исходным текстом. Используется в параметре *dwFlags* объекта [Итфранже:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**Tf \_ \_Исправление Tu**</dt> <dt>(0x1)</dt> </dl>                                | Изменение текста является результатом преобразования (исправления) существующего содержимого. Это означает, что семантика текста не изменилась. Используется в параметре *dwFlags* объекта [Итфпропертисторе:: онтекступдатед](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**Tf \_ US \_ хидетипуи**</dt> <dt>0x00000001</dt> </dl>                                | Не используется.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                      |
| Header<br/>                   | <dl> <dt>Мсктф. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсктф. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ITextStoreACP:: выделять](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[Итекстстореанчор:: выделять](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITfContext:: выделять](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITfDocumentMgr::P Op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[Итфедитрекорд:: Жеттекстандпропертюпдатес](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[Итфпропертисторе:: Онтекступдатед](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[Итфранже:: Инсертембеддед](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[Итфранже:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[тфклиентид](tfclientid.md)
</dt> <dt>

[тфгуидатом](tfguidatom.md)
</dt> <dt>

[TF \_ халтконд](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





