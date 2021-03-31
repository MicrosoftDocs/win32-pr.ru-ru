---
title: Идентификаторы типов заметок (UIAutomationClient. h)
description: В этом разделе описываются именованные константы, используемые для обозначения типов заметок в документе.
ms.assetid: 46948B7C-EC9F-4B55-B769-62EE8BE11D33
topic_type:
- apiref
api_name:
- AnnotationType_AdvancedProofingIssue
- AnnotationType_Author
- AnnotationType_CircularReferenceError
- AnnotationType_Comment
- AnnotationType_ConflictingChange
- AnnotationType_DataValidationError
- AnnotationType_DeletionChange
- AnnotationType_EditingLockedChange
- AnnotationType_Endnote
- AnnotationType_ExternalChange
- AnnotationType_Footer
- AnnotationType_Footnote
- AnnotationType_FormatChange
- AnnotationType_FormulaError
- AnnotationType_GrammarError
- AnnotationType_Header
- AnnotationType_Highlighted
- AnnotationType_InsertionChange
- AnnotationType_Mathematics
- AnnotationType_MoveChange
- AnnotationType_SpellingError
- AnnotationType_TrackChanges
- AnnotationType_Unknown
- AnnotationType_UnsyncedChange
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb628c8e6ada93546291cd9afb87c3194798b9f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800934"
---
# <a name="annotation-type-identifiers"></a>Идентификаторы типов заметок

В этом разделе описываются именованные константы, используемые для обозначения типов заметок в документе.



| Константа/значение                                                                                                                                                                                                                                                                                                                                           | Описание                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span id="AnnotationType_AdvancedProofingIssue"></span><span id="annotationtype_advancedproofingissue"></span><span id="ANNOTATIONTYPE_ADVANCEDPROOFINGISSUE"></span><dl> <dt>**Аннотатионтипе \_ Адванцедпруфингиссуе**</dt> <dt>60020</dt> </dl>     | Дополнительные проблемы с проверкой правописания.<br/>                                                             |
| <span id="AnnotationType_Author"></span><span id="annotationtype_author"></span><span id="ANNOTATIONTYPE_AUTHOR"></span><dl> <dt>**Аннотатионтипе \_ Автор**</dt> <dt>60019</dt> </dl>                                                                 | Автор документа.<br/>                                                             |
| <span id="AnnotationType_CircularReferenceError"></span><span id="annotationtype_circularreferenceerror"></span><span id="ANNOTATIONTYPE_CIRCULARREFERENCEERROR"></span><dl> <dt>**Аннотатионтипе \_ Циркуларреференцееррор**</dt> <dt>60022</dt> </dl> | Произошла ошибка циклической ссылки.<br/>                                               |
| <span id="AnnotationType_Comment"></span><span id="annotationtype_comment"></span><span id="ANNOTATIONTYPE_COMMENT"></span><dl> <dt>**Аннотатионтипе \_ Комментарий**</dt> <dt>60003</dt> </dl>                                                             | Примечание. Комментарии могут принимать различные формы в зависимости от приложения.<br/>              |
| <span id="AnnotationType_ConflictingChange"></span><span id="annotationtype_conflictingchange"></span><span id="ANNOTATIONTYPE_CONFLICTINGCHANGE"></span><dl> <dt>**Аннотатионтипе \_ Конфликтингчанже**</dt> <dt>60018</dt> </dl>                     | Конфликтующее изменение, внесенное в документ.<br/>                                     |
| <span id="AnnotationType_DataValidationError"></span><span id="annotationtype_datavalidationerror"></span><span id="ANNOTATIONTYPE_DATAVALIDATIONERROR"></span><dl> <dt>**Аннотатионтипе \_ Датавалидатионеррор**</dt> <dt>60021</dt> </dl>             | Произошла ошибка проверки данных.<br/>                                                  |
| <span id="AnnotationType_DeletionChange"></span><span id="annotationtype_deletionchange"></span><span id="ANNOTATIONTYPE_DELETIONCHANGE"></span><dl> <dt>**Аннотатионтипе \_ Делетиончанже**</dt> <dt>60012</dt> </dl>                                 | Изменение, внесенное в документ.<br/>                                        |
| <span id="AnnotationType_EditingLockedChange"></span><span id="annotationtype_editinglockedchange"></span><span id="ANNOTATIONTYPE_EDITINGLOCKEDCHANGE"></span><dl> <dt>**Аннотатионтипе \_ Едитинглоккедчанже**</dt> <dt>60016</dt> </dl>             | Изменение заблокированного изменения, внесенное в документ.<br/>                                 |
| <span id="AnnotationType_Endnote"></span><span id="annotationtype_endnote"></span><span id="ANNOTATIONTYPE_ENDNOTE"></span><dl> <dt>**Аннотатионтипе \_ Концевая сноска**</dt> <dt>60009</dt> </dl>                                                             | Концевая сноска для документа.<br/>                                                             |
| <span id="AnnotationType_ExternalChange"></span><span id="annotationtype_externalchange"></span><span id="ANNOTATIONTYPE_EXTERNALCHANGE"></span><dl> <dt>**Аннотатионтипе \_ Екстерналчанже**</dt> <dt>60017</dt> </dl>                                 | Внешнее изменение, внесенное в документ.<br/>                                       |
| <span id="AnnotationType_Footer"></span><span id="annotationtype_footer"></span><span id="ANNOTATIONTYPE_FOOTER"></span><dl> <dt>**Аннотатионтипе \_ Нижний колонтитул**</dt> <dt>60007</dt> </dl>                                                                 | Нижний колонтитул для страницы в документе.<br/>                                                    |
| <span id="AnnotationType_Footnote"></span><span id="annotationtype_footnote"></span><span id="ANNOTATIONTYPE_FOOTNOTE"></span><dl> <dt>**Аннотатионтипе \_ Сноска**</dt> <dt>60010</dt> </dl>                                                         | Сноска для страницы в документе.<br/>                                                  |
| <span id="AnnotationType_FormatChange"></span><span id="annotationtype_formatchange"></span><span id="ANNOTATIONTYPE_FORMATCHANGE"></span><dl> <dt>**Аннотатионтипе \_ Форматчанже**</dt> <dt>60014</dt> </dl>                                         | Внесенное изменение формата.<br/>                                                          |
| <span id="AnnotationType_FormulaError"></span><span id="annotationtype_formulaerror"></span><span id="ANNOTATIONTYPE_FORMULAERROR"></span><dl> <dt>**Аннотатионтипе \_ Формулаеррор**</dt> <dt>60004</dt> </dl>                                         | Ошибка в формуле. Ошибки формул обычно включают в себя красный текст и восклицательные знаки.<br/> |
| <span id="AnnotationType_GrammarError"></span><span id="annotationtype_grammarerror"></span><span id="ANNOTATIONTYPE_GRAMMARERROR"></span><dl> <dt>**Аннотатионтипе \_ Граммареррор**</dt> <dt>60002</dt> </dl>                                         | Грамматическая ошибка, часто обозначенная зеленой волнистой линией. <br/>                           |
| <span id="AnnotationType_Header"></span><span id="annotationtype_header"></span><span id="ANNOTATIONTYPE_HEADER"></span><dl> <dt>**Аннотатионтипе \_ Заголовок**</dt> <dt>60006</dt> </dl>                                                                 | Заголовок страницы в документе.<br/>                                                    |
| <span id="AnnotationType_Highlighted"></span><span id="annotationtype_highlighted"></span><span id="ANNOTATIONTYPE_HIGHLIGHTED"></span><dl> <dt>**Аннотатионтипе \_ Выделено**</dt> <dt>60008</dt> </dl>                                             | Выделенное содержимое, которое обычно обозначается контрастным цветом фона.<br/>               |
| <span id="AnnotationType_InsertionChange"></span><span id="annotationtype_insertionchange"></span><span id="ANNOTATIONTYPE_INSERTIONCHANGE"></span><dl> <dt>**Аннотатионтипе \_ Инсертиончанже**</dt> <dt>60011</dt> </dl>                             | Изменение вставки, внесенное в документ.<br/>                                      |
| <span id="AnnotationType_Mathematics"></span><span id="annotationtype_mathematics"></span><span id="ANNOTATIONTYPE_MATHEMATICS"></span><dl> <dt>**Аннотатионтипе \_ Математика**</dt> <dt>60023</dt> </dl>                                             | Текстовый диапазон, содержащий математику.<br/>                                                    |
| <span id="AnnotationType_MoveChange"></span><span id="annotationtype_movechange"></span><span id="ANNOTATIONTYPE_MOVECHANGE"></span><dl> <dt>**Аннотатионтипе \_ Мовечанже**</dt> <dt>60013</dt> </dl>                                                 | Изменение перемещения, внесенное в документ.<br/>                                            |
| <span id="AnnotationType_SpellingError"></span><span id="annotationtype_spellingerror"></span><span id="ANNOTATIONTYPE_SPELLINGERROR"></span><dl> <dt>**Аннотатионтипе \_ Спеллинжеррор**</dt> <dt>60001</dt> </dl>                                     | Орфографическая ошибка, которая часто обозначается красной волнистой линией. <br/>                                |
| <span id="AnnotationType_TrackChanges"></span><span id="annotationtype_trackchanges"></span><span id="ANNOTATIONTYPE_TRACKCHANGES"></span><dl> <dt>**Аннотатионтипе \_ Траккчанжес**</dt> <dt>60005</dt> </dl>                                         | Изменение, внесенное в документ.<br/>                                                 |
| <span id="AnnotationType_Unknown"></span><span id="annotationtype_unknown"></span><span id="ANNOTATIONTYPE_UNKNOWN"></span><dl> <dt>**Аннотатионтипе \_ Неизвестный**</dt> <dt>60000</dt> </dl>                                                             | Тип заметки неизвестен.<br/>                                                         |
| <span id="AnnotationType_UnsyncedChange"></span><span id="annotationtype_unsyncedchange"></span><span id="ANNOTATIONTYPE_UNSYNCEDCHANGE"></span><dl> <dt>**Аннотатионтипе \_ Унсинцедчанже**</dt> <dt>60015</dt> </dl>                                 | Несинхронизированное изменение, внесенное в документ.<br/>                                       |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                            |
| Header<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**Ианнотатионпровидер:: Аннотатионтипеид**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)
</dt> <dt>

[**Испреадшититемпровидер:: Жетаннотатионтипес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)
</dt> <dt>

[**Иуиаутоматионпаттерн:: Качеданнотатионтипеид**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_cachedannotationtypeid)
</dt> <dt>

[**Иуиаутоматионпаттерн:: Куррентаннотатионтипеид**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_currentannotationtypeid)
</dt> <dt>

[**Иуиаутоматионспреадшититемпаттерн:: Жеткачеданнотатионтипе**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationtypes)
</dt> <dt>

[**Иуиаутоматионспреадшититемпаттерн:: Жеткуррентаннотатионтипе**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationtypes)
</dt> <dt>

**Зрения**
</dt> <dt>

[Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>

 

